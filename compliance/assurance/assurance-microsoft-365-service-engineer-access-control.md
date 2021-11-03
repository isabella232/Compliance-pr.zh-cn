---
title: Microsoft 365工程师访问控制
description: 高级服务工程师Microsoft 365体系结构概述。
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
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 2700c95feb5c32765e2dc3420c67800b154b1e9d
ms.sourcegitcommit: 85b36ce8c79fb111980cc6462f2addb44a924065
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/02/2021
ms.locfileid: "60678460"
---
# <a name="microsoft-365-service-engineer-access-control"></a>Microsoft 365工程师访问控制

零长期访问 (ZSA) 意味着 Microsoft 服务团队人员对 Microsoft 365 生产环境或客户数据没有任何长期特权访问。 当 Microsoft 服务团队成员出于任何原因想要更新服务或访问客户数据时，他们必须提交证明需要合理性的请求，并收到授权经理的批准。 大规模地手动提供和删除维护 Microsoft 365 服务所需的访问权限并不可行，因此 Microsoft 开发了一个自动化解决方案，以根据需要管理特权访问。

## <a name="lockbox"></a>密码箱

对 Microsoft 365 系统和客户数据的所有访问都由密码箱进行代理，锁箱是一个使用实时 (JIT) 和 Just-Enough-Access (JEA) 模型的访问控制系统，为服务工程师提供对指定的 Microsoft 365 服务和数据的临时特权访问。 此外，所有请求和操作都记录用于审核，并且可通过使用 Office 365[管理活动 API](/office/office-365-management-api/get-started-with-office-365-management-apis)和安全与合规中心[来访问](https://protection.office.com/)。

Microsoft 服务工程师必须先通过密码箱Microsoft 365访问客户数据，然后才能连接到任何系统或访问客户数据。 只有在满足特定条件时，才能批准此请求：

- 服务工程师符合 [服务团队帐户的资格要求](assurance-microsoft-365-account-management.md)。
- 它们属于与请求中的工作相关联的密码箱角色，
- 请求的访问时间不会超过允许的最大时间，
- 他们具有合法的业务理由，
- 他们希望访问的请求资源在其工作范围内，
- 他们收到经理批准

在密码箱满足并验证所有条件后，将授予临时访问权限以执行请求的特定操作。 请求时间过后，将撤消访问权限。

![密码箱访问过程。](../media/assurance-lockbox-process.png)

此外，如果客户许可证并启用客户密码箱[](/microsoft-365/compliance/customer-lockbox-requests)功能，Microsoft 服务工程师访问客户数据的任何尝试都必须获得客户租户管理员额外批准。 客户和 Microsoft 都需要访问客户数据。 例如，客户引发的事件可能需要访问其数据来解决此问题，或者 Microsoft 需要数据访问来应用特定更新。

![客户密码箱访问过程。](../media/assurance-customer-lockbox-process.png)

客户没有任何工具来启动客户密码箱请求;他们必须向 Microsoft 提交需要引发客户密码箱请求的票证。 Microsoft 服务工程师提出的客户密码箱请求必须由 Microsoft 经理和客户租户中的授权管理员批准。

### <a name="lockbox-roles"></a>密码箱角色

为了强制实施职责分离和最小特权原则，服务工程师必须属于与其在团队中的角色对应的密码箱角色。 密码箱角色在标识管理工具中进行管理，并定义服务团队成员可通过密码箱请求过程批准的特权和操作。 服务团队人员必须请求成为密码箱角色的成员并接收批准。 如果获得批准，员工的服务团队帐户将置于由 Active Directory 组织强制执行的安全组中 (AD) Azure Active Directory (AAD) 。

## <a name="constrained-management-interfaces"></a>受约束的管理接口

服务工程师使用两个管理界面来执行管理任务：通过安全终端服务网关 (TSG) 和远程 PowerShell 从安全访问工作站 (SAW) 远程桌面。 在这些管理界面中，基于批准的密码箱请求和软件策略的访问控制对执行哪些应用程序以及哪些命令和 cmdlet 可用施加了重大限制。

## <a name="remote-desktop"></a>远程桌面

使用远程桌面管理服务的服务团队成员必须从由 Microsoft 专门为此用例管理的由 SAW 专门设计和制造笔记本电脑进行连接。 Microsoft 与供应商合作构建 SAW，从而创建短而安全的供应链。 SAW 使用经过强化的操作系统，这些操作系统配置为限制除定义的管理任务所需的功能之外的所有功能。 这些限制包括禁用所有 USB 端口、严格的应用程序访问列表、删除电子邮件访问、限制 Internet 浏览以及强制执行非活动屏幕保护程序锁定。 Microsoft 访问控制系统定期检查 SAW 计算机，以确保它们符合最新的安全控件，如果确定计算机不合规，则自动禁用这些计算机。

服务工程师一次只允许连接到一个 TSG，不允许多个会话。 但是，TSG Microsoft 365服务团队管理员连接到多台服务器，每个服务器只有一个并发会话，以便管理员能够有效地执行自己的职责。 服务团队管理员本身对 TSG 没有任何权限。 TSG 仅用于强制执行多重身份验证 (MFA) 和加密要求。 服务团队管理员通过 TSG 连接到特定服务器后，特定服务器将强制实施每个管理员一个的会话限制。

Active Directory 组策略为Microsoft 365人员建立使用限制、连接和配置要求。 这些策略包括以下 TSG 特征：

- 仅使用 [FIPS 140-2](/compliance/regulatory/offering-FIPS-140-2) 验证的加密
- 会话在非活动状态 15 分钟后断开连接
- 会话在 24 小时后自动注销

连接到 TSG 还需要使用单独的物理智能卡进行 MFA。 为服务工程师颁发了适用于各种平台和密码管理平台的不同智能卡，以确保凭据的安全存储。 TSG 使用 Active Directory 组策略来控制哪些人可以登录远程服务器、允许的会话数和空闲超时设置。

## <a name="remote-powershell"></a>远程 PowerShell

除了使用专门配置的 TSG 进行远程访问之外，具有服务工程师操作密码箱角色的服务团队人员可以使用远程 PowerShell 访问生产服务器上特定的管理功能。 若要使用此访问权限，用户必须获得只读权限 (调试) 访问Microsoft 365环境。 特权提升的启用方式与使用密码箱进程为 TSG 启用的方式相同。

对于远程访问，每个数据中心都有一个充当单一访问点的负载平衡虚拟 IP。 可用的远程 PowerShell cmdlet 基于身份验证期间获取的访问声明中标识的特权级别。 这些 cmdlet 提供使用此方法进行连接的用户唯一可访问的管理工作。 远程 PowerShell 限制可供工程师使用的命令范围，并且基于通过密码箱进程授予的访问级别。 例如，在Exchange Online中，Get-Mailbox cmdlet 可能可用，但 Set-Mailbox cmdlet 不可用。

## <a name="resources"></a>资源

- [隔离Microsoft 365](assurance-isolation-in-microsoft-365.md)
- [Microsoft 雇佣前筛选](assurance-pre-employment-screening.md)[Microsoft 云背景调查](assurance-cloud-background-check.md)
