---
title: Microsoft 365 中的隔离和访问控制
description: 摘要：有关应用程序的各个应用程序中的隔离和访问控制Microsoft 365。
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- SPO_Content
- MS-Compliance
f1.keywords:
- NOCSH
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: ca0371d51bfe0b403805f259d87a8162e32bfd1e
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088581"
---
# <a name="isolation-and-access-control-in-microsoft-365"></a>隔离和访问控制Microsoft 365

Azure Active Directory (Azure AD) 和 Microsoft 365 使用高度复杂的数据模型，其中包括数十个服务、数百个实体、数千个关系和数万个属性。 在高级别上，Azure AD 和服务目录是租户和收件人的容器，使用基于状态复制协议保持同步。 除了 Azure AD 中存储的目录信息之外，每个服务工作负荷还具有其自己的目录服务基础结构。
 
![Microsoft 365租户数据同步](../media/office-365-isolation-tenant-data-sync.png)

在此模型中，没有单一的目录数据源。 特定系统拥有单个数据部分，但任何一个系统均不保存所有数据。 Microsoft 365数据模型中，服务与 Azure AD 合作。 Azure AD 是共享数据的"真实系统"，它通常是供每个服务使用的小数据和静态数据。 Microsoft 365 和 Azure AD 中使用的联合模型提供数据的共享视图。

Microsoft 365使用物理存储和 Azure 云存储。 Exchange Online (包括Exchange Online Protection) Skype for Business客户数据使用自己的存储。 SharePoint联机功能SQL Server存储和Azure 存储，因此需要在存储级别额外隔离客户数据。

## <a name="exchange-online"></a>Exchange Online

Exchange Online将客户数据存储在邮箱中。 邮箱托管在称为邮箱数据库存储 ESE (ESE) 中。 这包括用户邮箱、链接邮箱、共享邮箱和公用文件夹邮箱。 用户邮箱包括保存Skype for Business内容，如对话历史记录。

用户邮箱内容包括：

- 电子邮件和电子邮件附件
- 日历和忙/闲信息
- 联系人
- Tasks
- 注释
- 组
- 推断数据

每个邮箱数据库Exchange Online多个租户的邮箱。 授权代码保护每个邮箱，包括租赁内邮箱。 默认情况下，只有分配的用户有权访问邮箱。 用于保护邮箱 (ACL) 访问控制列表包含租户级别由 Azure AD 验证的标识。 每个租户的邮箱限制为针对租户的身份验证提供程序进行身份验证的标识，该提供程序仅包含来自该租户的用户。 租户 A 中的内容无法由租户 B 中的用户以任何方式获取，除非租户 A 明确批准。

## <a name="skype-for-business"></a>Skype for Business

Skype for Business数据存储在各种位置：

- 用户和帐户信息（包括连接终结点、租户 ID、拨号计划、漫游设置、状态、联系人列表等）存储在 Skype for Business Active Directory 服务器和各种 Skype for Business 数据库服务器中。 如果为用户启用了这两Exchange Online，联系人列表将存储在用户的邮箱中;如果用户未启用Skype for Business，则存储在用户邮箱中。 Skype for Business数据库服务器不按租户进行分区，但数据多租户隔离是通过基于角色的访问控制和 RBAC (强制执行) 。
- 会议内容和上载的数据存储在分布式文件系统 (DFS) 共享。 如果启用，此内容Exchange Online存档。 不按租户对 DFS 共享进行分区。 内容使用 ACL 进行保护，并通过 RBAC 强制执行多租户。
- 呼叫详细信息记录（即活动历史记录，如呼叫历史记录、IM 会话、应用程序共享、IM 历史记录等）也可以存储在 Exchange Online 中，但大多数呼叫详细信息记录临时存储在呼叫详细信息记录 (CDR) 服务器上。 内容不按租户分区，但通过 RBAC 强制执行多租户。

## <a name="sharepoint-online"></a>SharePoint Online

SharePointOnline 具有多个提供数据隔离的独立机制。 它将对象存储为应用程序数据库中的抽象代码。 例如，当用户将文件上载到 SharePoint Online 时，文件会进行反汇编，转换为应用程序代码，并存储在多个数据库中的多个表中。

如果用户可以直接访问包含数据的存储，则内容不能解释为用户或除 SharePoint Online 系统。 这些机制包括安全访问控制和属性。 所有 SharePoint Online 资源都受授权代码和 RBAC 策略（包括租赁内）保护。 用于保护资源的 (ACL) 包含在租户级别进行身份验证的标识。 SharePoint租户的联机数据仅限于由租户的身份验证提供程序进行身份验证的标识。

除了 ACL 之外，指定身份验证提供程序 (（租户特定的 Azure AD) ）的租户级别属性只写一次，一旦设置就无法更改。 为租户设置身份验证提供程序租户属性后，将无法使用向租户公开的任何 API 进行更改。

每个租户 *使用唯一的 SubscriptionId。* 所有客户网站归租户所有，并分配有租户唯一的 *SubscriptionId。* 站点上 *的 SubscriptionId* 属性编写一次，并且是永久性的。 分配给租户后，网站无法移动到其他租户。 *SubscriptionId* 是用于创建验证提供程序的安全作用域的密钥，并绑定到租户。

SharePointOnline 使用 SQL Server 和 Azure 存储 存储内容元数据。 内容存储的分区密钥是 *网站* SQL。 当运行SQL查询时，SharePoint Online 使用 *作为* 租户级 SubscriptionId 检查的一部分验证的 *SiteId。*

SharePoint联机将加密的文件内容存储在Microsoft Azure blob 中。 每个 SharePoint Online 场都有自己的Microsoft Azure帐户，并且保存在 Azure 中的所有 blob 都使用存储在内容存储中的密钥SQL加密。 在代码中受授权层保护且未直接向最终用户公开的加密密钥。 SharePointOnline 具有实时监视功能，用于检测 HTTP 请求何时读取或写入多个租户的数据。 根据已访问资源的 *SubscriptionId* 跟踪请求标识 *SubscriptionId。* 最终用户绝不应请求访问多个租户的资源。 多租户环境中的服务请求是唯一的例外。 例如，搜索爬网程序一次提取整个数据库的内容更改。 这通常涉及到在单个服务请求中查询多个租户的网站，这样做是出于效率原因。

## <a name="teams"></a>Teams

您的Teams数据的存储方式不同，具体取决于内容类型。 

查看有关[Microsoft Teams 体系结构的 Ignite](https://channel9.msdn.com/Events/Ignite/Microsoft-Ignite-Orlando-2017/BRK3071)研讨会，进行深入讨论。

### <a name="core-teams-customer-data"></a>核心Teams客户数据

如果你的租户在澳大利亚、加拿大、欧盟、法国、德国、印度、日本、南非、韩国、瑞士 (包括列支敦士登) 、阿拉伯联合酋长国、英国或美国进行预配，Microsoft 将仅将以下客户数据存储在此位置：

- Teams聊天、团队和频道对话、图像、语音邮件和联系人。
- SharePoint Online 网站内容和网站中存储的文件。
- 上传到工作OneDrive学校的文件。

#### <a name="chat-channel-messages-team-structure"></a>聊天、频道消息、团队结构

每个团队Teams由 Microsoft 365 组及其SharePoint网站和Exchange支持。 私人聊天 (包括群聊) 、作为频道对话的一部分发送的消息，以及团队和频道的结构都存储在 Azure 中运行的聊天服务中。 数据还存储在用户和组邮箱的隐藏文件夹中，以启用信息保护功能。

#### <a name="voicemail-and-contacts"></a>语音邮件和联系人

语音邮件存储在Exchange。 联系人存储在基于Exchange云数据存储中。 Exchange基于 Exchange 的云存储已在每个全球数据中心地理位置中提供数据驻留。 对于所有团队，语音邮件和联系人存储在澳大利亚、加拿大、法国、德国、印度、日本、阿拉伯联合酋长国、英国、南非、韩国、瑞士 (包括列支敦士登) 和美国的国家/地区。 对于所有其他国家/地区，文件将存储在美国、欧洲或Asia-Pacific租户相关性的地理位置。

#### <a name="images-and-media"></a>图像和媒体

聊天中使用的媒体 (除 Giphy GIF（未存储但为指向原始 Giphy 服务 URL 的引用链接）外，Giphy 是非 Microsoft 服务) 存储在部署到聊天服务的相同位置的基于 Azure 的媒体服务中。

#### <a name="files"></a>文件

文件 (包括OneNote和 Wiki) 在频道中共享的文件存储在团队的 SharePoint 网站中。 对于共享该文件的用户的工作或学校帐户，在会议或通话过程中在私人聊天或聊天中共享的文件将上载并存储在 OneDrive 中。 Exchange、SharePoint 和 OneDrive已在每个全球数据中心地理位置中提供数据驻留。 因此，对于现有客户，OneNote体验一部分的所有文件、OneNote Teams 笔记本、Teams Wiki 内容和邮箱已存储在位置中，这基于租户相关性。 文件存储在澳大利亚、加拿大、法国、德国、印度、日本、阿拉伯联合酋长国、英国、南非、韩国和瑞士 (包括列支敦士登) 。 对于所有其他国家/地区，文件根据租户相关性存储在美国、欧洲或亚太地区。
