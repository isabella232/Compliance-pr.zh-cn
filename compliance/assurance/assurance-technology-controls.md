---
title: Microsoft 365 中的技术控件
description: 本文概述了 Microsoft 在 Microsoft 365 中用于技术控制的工具和技术。
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
f1.keywords:
- NOCSH
ms.custom:
- seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: c3b443505c78832af47719e6840c8b7011f9dfe1
ms.sourcegitcommit: 2b347c9b778ac9b6450daf20fdf8eb74ed14cbbd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/23/2021
ms.locfileid: "51002162"
---
# <a name="technology-controls-in-microsoft-365"></a>Microsoft 365 中的技术控件 

Microsoft 使用多种工具和技术来控制、管理和审核在其在线服务中访问客户数据。 这些适用于 Exchange Online、SharePoint Online、密码箱和客户密码箱、多重身份验证等。 Yammer 使用 Yammer Enterprise Access Controls 中所述 [的类似控件](assurance-yammer-enterprise-access-controls.md)。

Microsoft 365 工程师对 Microsoft 365 客户数据没有长期访问权限。 工程师必须先完成 Microsoft 审批流程，然后才能访问服务操作的客户数据。 如果客户对 Exchange Online 和 SharePoint Online 的客户密码箱功能进行许可，则访问客户数据需要客户批准。 获得批准后，将实时为服务请求所需的任务设置特定于服务的管理帐户的访问权限。

## <a name="lockbox-and-customer-lockbox"></a>密码箱和客户密码箱

虽然很少见，但客户可以请求 Microsoft 协助，向 Microsoft 工程师公开客户内容。 为了控制对 Exchange Online 的访问，Microsoft 使用名为"密码箱"的访问控制系统。 在任何 Microsoft 工程师访问任何 Exchange Online 或 SharePoint Online 系统或数据之前，他们必须使用密码箱提交访问请求。 Exchange Online 和 SharePoint Online 的所有服务请求都由密码箱系统处理。 使用密码箱和客户密码箱，所有批准的访问均可跟踪到唯一用户，使工程师负责处理客户数据。

> [!NOTE]
> Exchange Online 包括用户邮箱中存储的任何 Skype for Business 数据。 Skype for Business 覆盖不包括 Skype 会议直播录像或用户上传到会议的内容。 SharePoint Online 包括 OneDrive for Business。

密码箱处理授予工程师在服务中执行操作和管理功能的能力的权限请求。 工程师通过密码箱提交请求，Microsoft 经理必须批准请求，工程师才能访问客户数据。 经理批准后，工程师将具有对客户数据进行限时和范围限制的访问权限，以处理客户的问题。

如果需要执行明确的数据访问授权过程，Microsoft 365 客户密码箱可帮助你履行合规性义务。 这是某些合规性标准（如 FedRAMP 和 HIPAA）的要求。 客户密码箱将您插入密码箱审批流程，并让你能够控制 Microsoft 对 Exchange Online 或 SharePoint Online 内容的授权，以执行服务操作。

在极少数情况下，当 Microsoft 服务工程师需要访问你的数据时，你仅授予对解决问题所需的数据的访问权限，并且仅在一定的时间内授予访问权限。 如果拒绝访问请求，Microsoft 工程师将无法访问你的内容，并且无法完成服务操作。 如果批准请求，Microsoft 工程师将限制通过受监视和受限的管理界面实时访问内容。

支持工程师采取的操作记录用于审核，可通过 [Office 365](/office/office-365-management-api/get-started-with-office-365-management-apis) 管理活动 API 和安全与合规中心 [访问](https://protection.office.com/)。

>[!NOTE]
> 客户密码箱在 [Microsoft 365 E5 中](https://products.office.com/business/office-365-enterprise-e5-business-software) 作为加载项购买提供。 有关详细信息，请参阅 [Microsoft 365 客户密码箱请求](https://support.office.com/article/Office-365-Customer-Lockbox-Requests-36f9cdd1-e64c-421b-a7e4-4a54d16440a2)。

## <a name="just-in-time-access"></a>实时访问

Microsoft 使用 Microsoft 365 (JIT) 访问原则来缓解凭据篡改风险和横向攻击。 JIT 删除对服务的持久管理访问权限，并替换为按需提升为这些角色的能力。 删除管理员的永久访问权限可确保凭据仅在需要凭据时可用，并降低凭据盗窃风险。

JIT 访问模型要求工程师在有限时段内请求提升的权限，以执行管理职责。 此外，工程师使用使用计算机生成的复杂密码创建的临时帐户，并仅授予允许其执行必要任务的角色。 例如，密码箱授予的管理访问权限具有时间限制，授予的访问时间量取决于请求的角色。 工程师指定对密码箱系统的请求中所需的访问持续时间。 当请求的时间超过提升允许的最大时间时，密码箱系统将拒绝请求。 过期后，管理访问权限将被删除，临时帐户将过期。

获得授权和批准后，工程师将收到授权系统生成的一次使用管理密码。 每次批准提升的访问请求时，将生成新密码。 密码将复制到密码安全中，独立于 Microsoft 公司环境的工程师凭据，并且仅适用于批准的提升的访问会话。

## <a name="constrained-management-interfaces"></a>受约束的管理接口

工程师使用两个管理界面来执行管理任务：通过安全终端服务网关远程桌面 (TSG) 远程 PowerShell。 在这些管理界面中，软件策略和访问控制对执行哪些应用程序以及哪些命令和 cmdlet 可用施加了重大限制。

Microsoft 365 服务器将并发会话限制为每个服务器一个会话（每个服务团队管理员一个会话）。 TSG 仅允许用户使用单个并发会话，不允许多个会话。 借助每个服务器一个会话，TSG 允许 Microsoft 365 服务团队管理员同时连接到多台服务器，以便管理员能够有效地履行自己的职责。 服务团队管理员本身对 TSG 没有任何权限。 TSG 仅用于强制执行多重身份验证 (MFA) 和加密要求。 服务团队管理员通过 TSG 连接到特定服务器后，特定服务器将强制实施每个管理员一个的会话限制。

Microsoft 365 人员的使用限制、连接和配置要求由 Active Directory 组策略确定。 这些策略包括以下特征：

- TSG 仅使用 [经过 FIPS](https://www.microsoft.com/TrustCenter/Compliance/FIPS) 140-2 验证的加密。
- TSG 会话在非活动状态 30 分钟后断开连接。
- TSG 会话会在 24 小时后自动注销。

连接到 TSG 还需要使用单独的物理智能卡和独立于工程师的 Microsoft 公司凭据的帐户进行 MFA。 为工程师颁发了适用于各种平台的不同智能卡，密钥管理平台可确保安全存储凭据。 TSG 使用 Active Directory 组策略来控制哪些人可以登录远程服务器、允许的会话数和空闲超时设置。 其他策略限制对允许的应用程序的访问，并限制 Internet 访问。

除了使用专门配置的 TSG 进行远程访问之外，Exchange Online 还允许具有服务工程师操作角色的用户使用远程 PowerShell 访问生产服务器上特定的管理功能。 为此，用户必须有权使用只读 (调试) 访问 Microsoft 365 生产环境。 特权提升的启用方式与使用密码箱进程为 TSG 启用的方式相同。

对于远程访问，每个数据中心都有一个充当单一访问点的负载平衡虚拟 IP。 可用的远程 PowerShell cmdlet 基于身份验证期间获取的访问声明中标识的特权级别。 这些 cmdlet 提供使用此方法进行连接的用户可访问的唯一的管理工作。 远程 PowerShell 限制可供工程师使用的命令范围，并且基于通过密码箱进程授予的访问级别。 例如，在 Exchange Online 中，Get-Mailbox可用，Set-Mailbox不可用。
