---
title: 标识和访问管理概述
description: 了解企业中的标识和访问Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
ms.localizationpriority: medium
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: d5983ce587aa515be68c462c49eee87d7709bb23
ms.sourcegitcommit: 444a58b28f8611323e16d28b4c63a0f68eaaafa6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/04/2021
ms.locfileid: "60780028"
---
# <a name="identity-and-access-management-overview"></a>标识和访问管理概述

## <a name="how-do-microsoft-online-services-protect-production-systems-from-unauthorized-or-malicious-access"></a>Microsoft 联机服务如何保护生产系统免受未经授权的或恶意的访问？

Microsoft 在线服务旨在允许 Microsoft 工程师在不访问客户内容的情况下操作服务。 默认情况下，Microsoft 工程师具有零长期访问 (ZSA) 访问客户内容，并且没有对生产环境的特权访问。 Microsoft 联机服务使用实时 (JIT) 、Just-Enough-Access (JEA) 模型，在需要服务团队工程师支持 Microsoft 联机服务时，提供对生产环境的临时特权访问。 JIT 访问模型将传统的长期管理访问权限替换为工程师在需要时请求临时提升为特权角色的过程。

工程师被分配到服务团队，通过标识和访问管理解决方案支持生产服务请求服务团队帐户的资格。 资格申请触发了一系列人员检查，以确保工程师已通过所有云筛选要求、完成必要的培训，并获得了帐户创建前的适当管理批准。 只有在满足所有资格要求后，才能为申请环境创建服务团队帐户。 若要维护服务团队帐户的资格，人员每年必须接受基于角色的培训，并每两年重新进行一次审查。 未能完成或通过这些检查会导致资格被自动吊销。

服务团队帐户不会授予任何长期管理员权限或客户内容的访问权限。 当工程师需要其他访问权限以支持 Microsoft 联机服务时，他们使用名为 Lockbox 的访问管理工具请求临时提升的资源访问权限。 密码箱将提升的访问权限限制为完成所分配任务需要的最低权限、资源和时间。 如果授权审阅者批准 JIT 访问请求，则只会向工程师授予一个临时帐户，该帐户仅具有完成其分配的工作所需的权限。 此临时帐户需要多重身份验证，在批准期限到期后自动删除。

JEA 由资格和密码箱角色在请求 JIT 访问时强制执行。 只接受对工程师资格范围内资产的访问请求，并传递给审批者。 密码箱会自动拒绝超出工程师资格和密码箱角色范围的 JIT 请求，包括超出允许阈值的请求。  

## <a name="how-do-microsoft-online-services-use-role-based-access-control-rbac-with-lockbox-to-enforce-least-privilege"></a>Microsoft 联机服务如何使用基于角色的访问控制 (RBAC) 密码箱强制实施最小特权？

服务团队帐户不会授予任何长期管理员权限或客户内容的访问权限。 受限管理员权限的 JIT 请求通过密码箱进行管理。 密码箱使用 RBAC 限制 JIT 提升请求工程师可以提出的类型，从而提供额外的保护层以强制实施最小特权。 RBAC 还通过将服务团队帐户限制到适当的角色来帮助强制实施职责分离。
支持服务的工程师将基于其角色被授予安全组的成员身份。 安全组的成员身份不会授予任何特权访问权限。 相反，安全组允许工程师使用密码箱请求 JIT 提升（如果需要支持系统）。 工程师可以提出的特定 JIT 请求受其安全组成员身份限制。

## <a name="how-do-microsoft-online-services-handle-remote-access-to-production-systems"></a>Microsoft 联机服务如何处理对生产系统的远程访问？

Microsoft 在线服务系统组件位于地理位置上与运营团队分开的数据中心中。 数据中心人员对 Microsoft 在线服务系统没有逻辑访问权限。 因此，Microsoft 服务团队人员通过远程访问管理环境。 需要远程访问以支持 Microsoft 联机服务的服务团队人员只有在获得授权经理批准后，才被授予远程访问。 所有远程访问都使用与 FIPS 140-2 兼容的 TLS 进行安全远程连接。

Microsoft 联机服务使用 SECURE Admin Workstations (SAW) for service team remote access，帮助保护 Microsoft 联机服务环境免遭入侵。 这些工作站旨在防止有意或无意丢失生产数据，包括锁定 USB 端口，以及将安全管理工作站上可用的软件限制到支持环境所需的功能。 安全管理工作站受到密切跟踪和监视，以检测和防止 Microsoft 工程师恶意或无意泄露客户数据。

## <a name="how-does-customer-lockbox-add-additional-protection-for-customer-content"></a>客户密码箱如何为客户内容添加其他保护？

客户可以通过启用客户密码箱来向其内容添加其他级别的访问控制。 当密码箱提升请求涉及访问客户内容时，客户密码箱需要客户批准，这是审批工作流的最后一步。 此过程使组织可以选择批准或拒绝这些请求，并为客户提供直接访问控制。 如果客户拒绝客户密码箱请求，则对所请求内容的访问将被拒绝。 如果客户在特定时间内未拒绝或批准请求，那么请求将自动过期，Microsoft 不会获得客户内容的访问权限。 如果客户批准请求，Microsoft 对客户内容的临时访问将在分配完成疑难解答操作的时间到期后自动记录、审核和撤消。

## <a name="related-external-regulations--certifications"></a>认证相关的&法规

Microsoft 的在线服务会定期进行审核，以遵守外部法规和认证。 有关与标识和访问控制相关的控件的验证，请参阅下表。

### <a name="azure-and-dynamics-365"></a>Azure 和 Dynamics 365

| **外部审核** | **Section** | **最新报告日期** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.1：访问控制的业务要求 <br> A.9.2：用户访问管理 <br> A.9.3：用户责任 <br> A.9.4：系统和应用程序访问控制 <br> A.15.1：供应商关系中的信息安全 | 2020 年 12 月 2 日 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.1：访问控制的业务要求 <br> A.9.2：用户访问管理 <br> A.9.3：用户责任 <br> A.9.4：系统和应用程序访问控制 <br> A.15.1：供应商关系中的信息安全 | 2020 年 12 月 2 日 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | OA-2：预配访问 <br> OA-7：JIT 访问 <br> OA-21：安全管理工作站和 MFA | 2021 年 3 月 31 日 |

### <a name="office-365"></a>Office 365

| **外部审核** | **Section** | **最新报告日期** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | AC-2：帐户管理 <br> AC-3：实施访问 <br> AC-5：职责分离 <br> AC-6：最小特权 <br> AC-17：远程访问 | 2020 年 9 月 24 日 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=08ce227f-d1d9-4c4c-b255-4f2e4ec8f941&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.1：访问控制的业务要求 <br> A.9.2：用户访问管理 <br> A.9.3：用户责任 <br> A.9.4：系统和应用程序访问控制 <br> A.15.1：供应商关系中的信息安全 | 2021 年 4 月 20 日 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-33：帐户修改 <br> CA-34：用户身份验证 <br> CA-35：特权访问 <br> CA-36：远程访问 <br> CA-57：客户密码箱 Microsoft 管理审批 <br> CA-58：客户密码箱服务请求 <br> CA-59：客户密码箱通知 <br> CA-61：JIT 审阅和审批 | 2020 年 12 月 24 日 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-32：共享帐户策略 <br> CA-33：帐户修改 <br> CA-34：用户身份验证 <br> CA-35：特权访问 <br> CA-36：远程访问 <br> CA-53：第三方监控 <br> CA-56：客户密码箱客户批准 <br> CA-57：客户密码箱 Microsoft 管理审批 <br> CA-58：客户密码箱服务请求 <br> CA-59：客户密码箱通知 <br> CA-61：JIT 审阅和审批 | 2020 年 12 月 24 日 |
| [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-15：客户密码箱请求 | 2020 年 12 月 24 日 |