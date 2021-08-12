---
title: 管理访问控制Microsoft 365
description: 本文概述了管理访问控制和数据分类Microsoft 365。
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
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 06bdd239e2845d3495a40fc83bd33cbb0e43dbdb3d025bd8fa77b5d5451a680c
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "54289260"
---
# <a name="administrative-access-controls-in-microsoft-365"></a>管理访问控制Microsoft 365 

Microsoft 在系统和控制方面投入大量资源，使大多数Microsoft 365自动化，同时有意限制 Microsoft 访问客户内容。 人员管理服务，软件运行服务。 此结构使 Microsoft 能够Microsoft 365客户内容的内部威胁的风险。

默认情况下，Microsoft 工程师拥有零长期管理权限和零长期客户内容Microsoft 365。 Microsoft 工程师可以在有限时间内限制、审核和安全访问客户的内容。 只有在服务操作需要访问时，并且只有在 Microsoft 高层管理人员批准时才能访问。 对于客户密码箱许可客户，客户提供对托管在客户密码箱上的内容的访问Microsoft 365。

Microsoft 使用多种形式的云交付提供联机服务：

- **公共云：** 包括多租户版本的 Microsoft 365、Azure 以及北美、北美、欧洲、亚洲、澳大利亚等托管的其他服务。
- **国家云：** 包括美国 (以外的所有自主和第三方运营的云，但之前提到的云除外) Microsoft 365如由世纪) 运营的 (中国 (和由 Microsoft 运营的德国 (中的 Microsoft 365，但在德国数据受托人德国电信的模型中，控制并监视 Microsoft 对包含客户数据) 的客户数据和系统的访问。
- **政府云：** 包括Microsoft 365客户可用的 Azure 服务和 Azure 服务。

出于本文的目的，Microsoft 365服务包括：

- [Exchange Online](/Exchange/exchange-online)
- [Exchange Online Protection](/Office365/SecurityCompliance/eop/exchange-online-protection-overview)
- [SharePoint Online](/sharepoint/sharepoint-online)
- [OneDrive for Business](/OneDrive/onedrive)
- [Skype for Business](/SkypeForBusiness/skype-for-business-online)
- [Microsoft Teams](/MicrosoftTeams/Teams-overview)
- [Yammer](/yammer/yammer-landing-page)

## <a name="microsoft-365-access-controls"></a>Microsoft 365访问控制

出于访问控制目的，Microsoft 将Microsoft 365分类为客户数据或其他类型的数据。

### <a name="customer-data"></a>客户数据

客户数据是客户在使用此服务时或代表客户Microsoft 365数据。 此数据是由用户直接创建或上载的客户Microsoft 365，包括：

- 电子邮件
- SharePoint联机内容
- 即时消息
- 日历项目
- Documents
- 联系人
- EUII 最终用户可识别信息 (EUII)  (用户独有的数据，或链接到单个用户但不包括客户内容) 

### <a name="other-types-of-data"></a>其他类型的数据

其他类型的数据包括：

- **帐户数据：** 包括管理员 (或购买服务时提供的管理数据) ，以及付款 (支付工具的信息，如信用卡详细信息) 。
- **组织可识别信息：** 包括用于标识租户的数据、使用率数据，并且无法链接到单个用户或包含在客户内容中。
- **系统元数据：** 包括包含配置设置、系统状态、Microsoft IP 地址和有关订阅和租户的技术信息的服务日志。

Microsoft 建立了访问控制机制，以确保没有人未经批准能够访问客户数据或访问控制数据。 访问控制数据管理对环境中其他类型的数据或功能的访问，包括对客户内容或 EUII、Microsoft 密码、安全证书和其他身份验证相关数据的访问。 访问控制机制还防止未经批准的对生产环境的物理、逻辑或Microsoft 365访问。

Microsoft 使用三类访问控制来运行Microsoft 365：

- 隔离控制
- 人员控制
- 技术控制

组合后，这些控件有助于防止和检测恶意Microsoft 365。 除了 Microsoft 使用的隔离、人员和技术控制外，还有第四类控制措施：客户实施的控制措施。

Microsoft 365允许您以在本地环境中管理数据的方式管理数据。 注册组织供其使用Microsoft 365将自动成为全局管理员。 全局管理员有权访问管理门户中的所有功能，并且可以：

- 创建或编辑用户
- 将管理员角色分配给其他人
- 重置用户密码
- 管理用户许可证
- 管理域
- 批准客户密码箱请求

我们建议每个组织配置至少两个管理员帐户。 对于大型企业组织，我们建议使用服务于不同职能的专用管理员帐户。

有关分配管理员角色和权限的信息，请参阅分配 [管理员](/microsoft-365/admin/add-users/assign-admin-roles) 角色和关于 [管理员角色](/microsoft-365/admin/add-users/about-admin-roles)。

## <a name="related-links"></a>相关链接

- [隔离Microsoft 365](assurance-isolation-in-microsoft-365.md)
- [Microsoft 聘用前筛选](assurance-pre-employment-screening.md)
- [ Microsoft 云背景核查](assurance-cloud-background-check.md)
- [监视和审核访问控制](assurance-monitoring-and-auditing-access-controls.md)
- [Yammer Enterprise 访问控制](assurance-yammer-enterprise-access-controls.md)
