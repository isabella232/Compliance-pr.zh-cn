---
title: 技术控制Microsoft 365
description: 本文概述了 Microsoft 在企业技术控制中使用的Microsoft 365。
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom:
- seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 06d8f500a96c84bf961dc47f6b8d259e0fffe02d
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947020"
---
# <a name="technology-controls-in-microsoft-365"></a>技术控制Microsoft 365 

Microsoft 使用多种工具和技术来控制、管理和审核在其在线服务中访问客户数据。 它们适用于Exchange Online、SharePoint Online、密码箱和客户密码箱、多重身份验证等。 Yammer使用 Access Controls 中所述的Yammer Enterprise[控件](assurance-yammer-enterprise-access-controls.md)。

Microsoft 365工程师具有零长期访问Microsoft 365客户数据。 工程师必须先完成 Microsoft 审批流程，然后才能访问服务操作的客户数据。 如果客户为 Exchange Online 和 SharePoint 许可证客户密码箱功能，则访问客户数据需要经过客户批准。 获得批准后，将实时为服务请求所需的任务设置特定于服务的管理帐户的访问权限。

## <a name="lockbox-and-customer-lockbox"></a>密码箱和客户密码箱

虽然很少见，但客户可以请求 Microsoft 协助，向 Microsoft 工程师公开客户内容。 为了控制对Exchange Online的访问，Microsoft 使用一个称为"密码箱"的访问控制系统。 在 Microsoft 工程师访问任何 Exchange Online 或 SharePoint Online 系统或数据之前，他们必须使用密码箱提交访问请求。 密码箱系统Exchange Online SharePoint Online 的所有服务请求。 使用密码箱和客户密码箱，所有批准的访问均可跟踪到唯一用户，使工程师负责处理客户数据。

> [!NOTE]
> Exchange Online包括Skype for Business邮箱中存储的任何数据。 Skype for Business范围不包括Skype 会议上传到会议的广播录像或内容。 SharePoint联机包括OneDrive for Business。

密码箱处理授予工程师在服务中执行操作和管理功能的能力的权限请求。 工程师通过密码箱提交请求，Microsoft 经理必须批准请求，工程师才能访问客户数据。 经理批准后，工程师将具有对客户数据进行限时和范围限制的访问权限，以处理客户的问题。

客户密码箱Microsoft 365如果您需要明确的数据访问授权过程，则有助于你履行合规性义务。 这是某些合规性标准（如 FedRAMP 和 HIPAA）的要求。 客户密码箱将您插入密码箱审批流程，并让你能够控制 Microsoft 对服务操作对 Exchange Online 或 SharePoint Online 内容的访问授权。

在极少数情况下，当 Microsoft 服务工程师需要访问你的数据时，你仅授予对解决问题所需的数据的访问权限，并且仅在一定的时间内授予访问权限。 如果拒绝访问请求，Microsoft 工程师将无法访问你的内容，并且无法完成服务操作。 如果批准请求，Microsoft 工程师通过受监视和限制的管理界面具有对内容的有限即时访问权限。

支持工程师采取的操作记录用于审核目的，可通过 Office 365 管理活动[API](/office/office-365-management-api/get-started-with-office-365-management-apis)和安全与合规中心[访问](https://protection.office.com/)。

>[!NOTE]
> 客户密码箱[Microsoft 365 E5加载项购买](https://products.office.com/business/office-365-enterprise-e5-business-software)。 有关详细信息，请参阅客户[Microsoft 365密码箱请求](https://support.office.com/article/Office-365-Customer-Lockbox-Requests-36f9cdd1-e64c-421b-a7e4-4a54d16440a2)。

## <a name="just-in-time-access"></a>即时访问权限

Microsoft 使用 JIT (JIT) 访问原则Microsoft 365凭据篡改风险和横向攻击。 JIT 删除对服务的持久管理访问权限，并替换为按需提升为这些角色的能力。 删除管理员的永久访问权限可确保凭据仅在需要凭据时可用，并降低凭据盗窃风险。

JIT 访问模型要求工程师在有限时段内请求提升的权限，以执行管理职责。 此外，工程师使用使用计算机生成的复杂密码创建的临时帐户，并仅授予允许其执行必要任务的角色。 例如，密码箱授予的管理访问权限具有时间限制，并且授予的访问时间量取决于请求的角色。 工程师指定对密码箱系统的请求中所需的访问持续时间。 当请求的时间超过提升允许的最大时间时，密码箱系统将拒绝请求。 过期后，管理访问权限将被删除，临时帐户将过期。

获得授权和批准后，工程师将收到授权系统生成的一次使用管理密码。 每次批准提升的访问请求时，将生成新密码。 密码将复制到密码安全中，独立于 Microsoft 公司环境的工程师凭据，并且仅适用于批准的提升的访问会话。

## <a name="constrained-management-interfaces"></a>受约束的管理接口

工程师使用两个管理界面来执行管理任务：通过安全终端服务网关和 TSG (远程桌面) 远程 PowerShell。 在这些管理界面中，软件策略和访问控制对执行哪些应用程序以及哪些命令和 cmdlet 可用施加了重大限制。

Microsoft 365服务器将并发会话限制为每个服务器一个会话（每个服务团队管理员一个会话）。 TSG 仅允许用户使用单个并发会话，不允许多个会话。 通过每个服务器使用一个会话，TSG Microsoft 365服务团队管理员同时连接到多台服务器，以便管理员能够有效地执行自己的职责。 服务团队管理员本身对 TSG 没有任何权限。 TSG 仅用于强制执行多重身份验证 (MFA) 和加密要求。 服务团队管理员通过 TSG 连接到特定服务器后，特定服务器将强制实施每个管理员一个的会话限制。

Active Directory 组策略可Microsoft 365人员使用限制以及连接和配置要求。 这些策略包括以下特征：

- TSG 仅使用 [经过 FIPS](https://www.microsoft.com/TrustCenter/Compliance/FIPS) 140-2 验证的加密。
- TSG 会话在非活动状态 30 分钟后断开连接。
- TSG 会话将在 24 小时后自动注销。

连接到 TSG 还需要使用单独的物理智能卡和独立于工程师的 Microsoft 公司凭据的帐户进行 MFA。 为工程师颁发了适用于各种平台的不同智能卡，密钥管理平台可确保安全存储凭据。 TSG 使用 Active Directory 组策略来控制哪些人可以登录远程服务器、允许的会话数和空闲超时设置。 其他策略限制对允许的应用程序的访问，并限制 Internet 访问。

除了使用专门配置的 TSG 进行远程访问之外，Exchange Online还允许具有服务工程师操作角色的用户使用远程 PowerShell 访问生产服务器上特定的管理功能。 为此，必须授权用户进行只读 (调试) 访问Microsoft 365环境。 特权提升的启用方式与使用密码箱进程为 TSG 启用的方式相同。

对于远程访问，每个数据中心都有一个充当单一访问点的负载平衡虚拟 IP。 可用的远程 PowerShell cmdlet 基于身份验证期间获取的访问声明中标识的特权级别。 这些 cmdlet 提供使用此方法进行连接的用户唯一可访问的管理工作。 远程 PowerShell 限制可供工程师使用的命令范围，并且基于通过密码箱进程授予的访问级别。 例如，在Exchange Online中，Get-Mailbox可能可用，Set-Mailbox不可用。
