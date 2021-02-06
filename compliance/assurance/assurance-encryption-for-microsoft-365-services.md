---
title: Skype、OneDrive、SharePoint 和 Exchange 的加密
description: 摘要：Skype、OneDrive、SharePoint、Microsoft Teams 和 Exchange Online 加密的说明。
ms.author: krowley
author: kccross
manager: laurawi
ms.reviewer: sosstah
f1.keywords:
- NOCSH
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_Enterprise
- M365-security-compliance
- Strat_O365_Enterprise
- SPO_Content
- MS-Compliance
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 9317b112d1fa759b1f90e072203e7b8093a432fd
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120541"
---
# <a name="encryption-for-skype-for-business-onedrive-for-business-sharepoint-online-microsoft-teams-and-exchange-online"></a>Skype for Business、OneDrive for Business、SharePoint Online、Microsoft Teams 和 Exchange Online 的加密

Microsoft 365 是高度安全的环境，提供多层的广泛保护：物理数据中心安全、网络安全、访问安全、应用程序安全和数据安全。

## <a name="skype-for-business"></a>Skype for Business

Skype for Business 客户数据可以以会议参与者上载的文件或演示文稿的形式存储。 Web 会议服务器使用 AES 和 256 位密钥加密客户数据。 加密的客户数据存储在文件共享中。 每段客户数据都使用不同的随机生成的 256 位密钥进行加密。 在会议中共享一部分客户数据时，Web 会议服务器会指示会议客户端通过 HTTPS 下载加密的客户数据。 它将相应的密钥发送到客户端，以便可以解密客户数据。 Web 会议服务器还会在允许客户端访问会议客户数据之前对会议客户端进行身份验证。 加入 Web 会议时，每个会议客户端首先建立一个 SIP 对话框，其中会议焦点组件在前端服务器内部通过 TLS 运行。 会议焦点将 Web 会议服务器生成的身份验证 Cookie 传递给会议客户端。 然后，会议客户端连接到呈现要由服务器进行身份验证的身份验证 Cookie 的 Web 会议服务器。

## <a name="sharepoint-online-and-onedrive-for-business"></a>SharePoint Online 和 OneDrive for Business

SharePoint Online 中所有客户文件都受每个文件的唯一密钥（始终专用于单个租户）保护。 密钥由 SharePoint Online 服务创建和管理，或在客户使用、创建和管理客户密钥时创建和管理。 上载文件时，SharePoint Online 在上载请求上下文中执行加密，然后再发送到 Azure 存储。 下载文件时，SharePoint Online 将基于唯一文档标识符从 Azure 存储检索加密的客户数据，并在将客户数据发送到用户之前对其进行解密。 Azure 存储无法解密，甚至无法识别或了解客户数据。 所有加密和解密都发生在强制执行租户隔离的相同系统中，即 Azure Active Directory 和 SharePoint Online。

Microsoft 365 中的一些工作负载将数据存储在 SharePoint Online 中，包括 Microsoft Teams（将所有文件存储在 SharePoint Online 中）和 OneDrive for Business（使用 SharePoint Online 进行存储）。 SharePoint Online 中存储的所有客户数据都 (一个或多个 AES 256 位密钥进行加密) 分布在数据中心，如下所示。  (此加密过程的每一步都经过 FIPS 140-2 级别 2 验证。 有关 FIPS 140-2 合规性的其他信息，请参阅 [FIPS 140-2 合规性](/previous-versions/sql/sql-server-2008-r2/bb326611(v=sql.105)).) 

- 每个文件将拆分为一个或多个区块，具体取决于文件大小。 每个区块都使用自己的唯一 AES 256 位密钥进行加密。
- 更新文件时，将按相同方式处理更新：更改拆分为一个或多个区块，每个区块使用单独的唯一密钥进行加密。
- 这些区块（文件、文件片段和更新增量）作为 blob 存储在 Azure 存储中，随机分布在多个 Azure 存储帐户中。
- 这些客户数据块的加密密钥集本身已加密。

    - 用于加密 blob 的密钥存储在 SharePoint Online 内容数据库中。
    - 内容数据库受数据库访问控制和静态加密保护。 加密使用 Azure [ (](/sql/relational-databases/security/encryption/transparent-data-encryption-tde) 数据库中的透明数据) TDE [SQL执行](/azure/sql-database/sql-database-technical-overview)。  (Azure SQL 数据库是 Microsoft Azure 中通用的 关系数据库 服务，支持关系数据、JSON、空间和 XML 等结构。) 这些密码位于 SharePoint Online 的服务级别，而不是租户级别。 这些 (有时称为主密钥) 存储在称为密钥存储的单独安全存储库中。 TDE 可为活动数据库、数据库备份和事务日志提供处于非活动状态的安全性。
    - 当客户提供可选密钥时，客户密钥将存储在 Azure 密钥保管库中，服务使用该密钥来加密租户密钥，该密钥用于加密站点密钥，然后用于加密文件级别密钥。 实质上，当客户提供密钥时，将引入新的密钥层次结构。
- 用于重新组合文件的映射与解密密钥所需的主密钥分开存储在内容数据库中。
- 每个 Azure 存储帐户具有每个访问类型的唯一凭据 (读取、写入、枚举和删除) 。 每组凭据都存放在安全的密钥存储中，并定期刷新。 如上所述，有三种不同类型的存储，每种类型的存储具有不同的功能：
    - 客户数据存储为 Azure 存储中的加密 blob。 每个客户数据块的密钥都经过加密，并单独存储在内容数据库中。 客户数据本身没有关于如何对其进行解密的线索。
    - "内容数据库"是一个 SQL Server 数据库。 它保留查找和重新组合 Azure 存储中保留的客户数据 blob 所需的映射，以及加密这些 blob 所需的密钥。 但是，密钥集本身已加密 (如上文所述) 保存在单独的密钥存储中。
    - 密钥存储在物理上独立于内容数据库和 Azure 存储。 它保留每个 Azure 存储容器的凭据以及内容数据库中保留的一组加密密钥的主密钥。

这三个存储组件（Azure blob 存储、内容数据库和密钥存储）在物理上是分开的。 保留在其中任一个组件中的信息在其自身上都不可用。 如果不访问这三个区块，则不可能检索到区块的密钥、解密密钥使其可用、将密钥与相应的区块关联、解密每个区块或从构成块重新构造文档。

保护数据中心中计算机上物理磁盘卷的 BitLocker 证书存储在受场密钥保护的安全存储库 (SharePoint Online 密码存储) 中。

保护每个 blob 密钥的 TDE 密钥存储在两个位置：

- 存储 BitLocker 证书并受服务器场密钥保护的安全存储库;and
- 在由 Azure 数据库管理的安全SQL中。

用于访问 Azure 存储容器的凭据也保存在 SharePoint Online 密码存储中，并根据需要委派给每个 SharePoint Online 场。 这些凭据是 Azure 存储 SAS 签名，具有用于读取或写入数据的单独凭据，并应用了策略，以便每 60 天自动过期一次。 不同的凭据用于读取或写入数据 (，) 和 SharePoint Online 场都未授予枚举权限。

> [!NOTE]
> 对于 Office 365 美国政府版客户，数据 blob 存储在 Azure 美国政府存储中。 此外，Office 365 美国政府版中的 SharePoint Online 密钥的访问权限仅限于经过专门筛选的 Office 365 员工。 Azure 美国政府运营人员无法访问用于加密数据 blob 的 SharePoint Online 密钥存储。

有关 SharePoint Online 和 OneDrive for Business 中数据加密的信息，请参阅 [OneDrive for Business](https://technet.microsoft.com/library/dn905447.aspx)和 SharePoint Online 中的数据加密。

### <a name="list-items-in-sharepoint-online"></a>SharePoint Online 中的列表项

列表项是临时创建的客户数据的较小区块，或可以更动态地在网站中活动的客户数据块，例如用户创建的列表中的行、SharePoint Online 博客中的单个文章或 SharePoint Online Wiki 网页中的条目。 列表项存储在 Azure 数据库数据库 (Azure SQL 数据库) TDE 进行保护。

## <a name="encryption-of-data-in-transit"></a>中转数据的加密

在 OneDrive for Business 和 SharePoint Online 中，有两种数据进入和退出数据中心的方案。

- **客户端与服务器的通信** - 通过 Internet 与 SharePoint Online 和 OneDrive for Business 的通信使用 TLS 连接。
- **数据中心之间的数据移动** - 在数据中心之间移动数据的主要原因是进行异地复制以实现灾难恢复。 例如，SQL Server 事务日志和 blob 存储增量沿着此管道传输。 虽然已使用专用网络传输此数据，但还将进一步使用一流加密技术来保护此数据。

## <a name="exchange-online"></a>Exchange Online

Exchange Online 将 BitLocker 用于所有邮箱数据，BitLocker 配置在 [BitLocker for Encryption 中进行了介绍](/microsoft-365/compliance/office-365-bitlocker-and-distributed-key-manager-for-encryption)。 服务级别加密对邮箱级别的所有邮箱数据进行加密。 

除了服务加密之外，Microsoft 365 还支持基于服务加密构建的客户密钥。 客户密钥是 Microsoft 管理的 Exchange Online 服务加密密钥选项，也位于 Microsoft 路线图中。 这种加密方法提供 BitLocker 未提供的增强保护，因为它可分离服务器管理员和解密数据所需的加密密钥，并且将加密直接应用于数据 (与 BitLocker 相反，BitLocker 在逻辑磁盘卷应用加密) 从 Exchange 服务器复制的任何客户数据保持加密状态。

Exchange Online 服务加密的范围是存储在 Exchange Online 中的静态客户数据。  (Skype for Business 将几乎所有用户生成的内容存储在用户的 Exchange Online 邮箱中，因此继承了 Exchange Online.) 


## <a name="microsoft-teams"></a>Microsoft Teams

Teams 使用 TLS 和 MTLS 加密即时消息。 所有服务器到服务器流量都需要 MTLS，而不管通信是仅限于内部网络还是跨越内部网络外围。

此表总结了 Teams 使用的协议。

|**通信类型**|**加密者**|
|:-----|:-----|
|服务器到服务器|MTLS|
|例如，客户端到 (服务器 即时消息和状态) |TLS|
|媒体流 ( 媒体传输的音频和视频) |TLS|
|媒体的音频和视频共享|SRTP/TLS|
|信号|TLS|

#### <a name="media-encryption"></a>媒体加密

媒体通信是使用安全 RTP (SRTP) 进行加密的，SRTP 是为 RTP 通信提供保密性、身份验证和重播攻击保护的实时传输协议 (RTP) 的配置文件。 SRTP 使用使用安全随机数字生成器生成的会话密钥，并使用信号 TLS 通道进行交换。 客户端到客户端媒体流量通过客户端到服务器连接信号协商，但在直接进入客户端到客户端时使用 SRTP 进行加密。

Teams 使用基于凭据的令牌通过 TURN 安全访问媒体中继。 媒体中继通过 TLS 安全通道交换令牌。

#### <a name="fips"></a>FIPS

Teams 使用 FIPS (美国联邦信息处理标准) 加密密钥交换的兼容算法。 有关 FIPS 实现详细信息，请参阅联邦信息处理标准 ([FIPS) 出版物 140-2。](/microsoft-365/compliance/offering-fips-140-2)
