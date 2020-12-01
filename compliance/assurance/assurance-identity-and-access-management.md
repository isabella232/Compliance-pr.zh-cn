---
title: 标识和访问管理概述
description: 了解 Microsoft 365 中的标识和访问管理
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: b62219faa5bc55ef4bef9557d953caf1a2f95fc7
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/30/2020
ms.locfileid: "49505925"
---
# <a name="identity-and-access-management-overview"></a>标识和访问管理概述

## <a name="how-does-microsoft-365-protect-production-systems-from-unauthorized-or-malicious-access"></a>Microsoft 365 如何保护生产系统免遭未经授权或恶意访问？

Microsoft 365 旨在允许 Microsoft 工程师在不访问客户内容的情况下运行服务。 默认情况下，Microsoft 365 工程师拥有零的) ZSA 访问权限 (的客户内容，并且没有对生产环境的特权访问权限。 Microsoft 365 使用实时 (JIT) 、足够的访问 (JEA) 模型，以向服务团队工程师提供对生产环境的临时权限访问，以便支持 Microsoft 365 时需要此类访问权限。 JIT 访问模型将传统的永久性管理访问替换为工程师，以在需要时请求临时提升为特权角色。

分配给服务团队的工程师通过身份管理工具 (IDM) 来支持针对服务团队帐户的生产服务请求资格。 资格请求触发一系列人员检查以确保工程师已通过所有云屏蔽要求、完成必要的培训，并在创建帐户之前获得适当的管理审批。 仅在满足所有资格要求后，才可以为请求的环境创建服务团队帐户。

服务团队帐户不授予任何面向管理员的权限或对客户内容的访问权限。 如果工程师需要更多的访问权限来支持其 Microsoft 365 服务，则使用称为 "密码箱" 的访问管理工具，请求对所需资源的临时权限提升。 密码箱将提升的访问权限限制为完成分配的任务所需的最低权限、资源和时间。 如果授权的审阅者批准了 JIT 访问请求，则会向工程师授予一个临时帐户，其中仅包含完成所分配的工作所需的权限。 此临时帐户需要多重身份验证，并在批准的期限到期后自动删除。

## <a name="how-does-microsoft-365-handle-remote-access-to-production-systems"></a>Microsoft 365 如何处理对生产系统的远程访问？

Microsoft 365 系统组件驻留在与运营团队分开的数据中心。 数据中心人员不具有对 Microsoft 365 系统的逻辑访问权限。 因此，Microsoft 365 服务团队人员通过远程访问管理环境。 需要远程访问以支持 Microsoft 365 的服务团队人员仅在批准了授权管理器后才向其授予远程访问权限。 所有远程访问使用 FIPS 140-2 兼容的 TLS 进行安全的远程连接。

Microsoft 365 使用安全管理员工作站 (SAWs) 进行服务团队远程访问，以帮助防止 Microsoft 365 环境受到危害。 这些工作站专为防止无意或意外丢失生产数据而设计，包括锁定 USB 端口，并将所见即用的软件限制为支持环境所需的内容。 严密跟踪和监控 SAWs，以检测并阻止 Microsoft 工程师对客户数据的恶意或意外危害。

## <a name="how-does-customer-lockbox-add-additional-protection-for-customer-content"></a>客户密码箱如何为客户内容添加更多保护？

通过启用客户密码箱，客户可以向其内容添加其他级别的访问控制。 当密码箱提升请求涉及对客户内容的访问时，客户密码箱要求客户在审批工作流的最后步骤中进行审批。 这将为组织提供批准或拒绝这些请求的选项，并向客户提供直接访问控制。 如果客户拒绝客户密码箱请求，将拒绝对请求的内容的访问。 如果客户在特定时间段内未拒绝或批准请求，则请求将自动过期，而不会有 Microsoft 获取对客户内容的访问权限。 如果客户批准请求，则在分配用于完成故障排除操作的时间到期后，将自动记录、审核和吊销 Microsoft 对客户内容的临时访问权限。

## <a name="related-external-regulations--certifications"></a>& 认证的相关外部法规

将定期审核 Microsoft 的在线服务，以遵守外部法规和认证。 请参阅下表以验证与标识和访问控制相关的控件。

| **外部审核** | **Section** | **最新报告日期** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365) ](https://compliance.microsoft.com/compliancemanager) | AC-2：帐户管理 <br> AC-3：访问强制 <br> AC-5：职责分离 <br> AC-6：最小特权 <br> AC-17：远程访问 | 2020年9月24日 |
| [ISO 27001/27002 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | . 9.1：访问控制的业务要求 <br> 9.2：用户访问管理 <br> 9.3：用户职责 <br> 9.4：系统和应用程序访问控制 <br> 15.1：信息在供应商关系中的安全性 | 2020 年 2 月 22 日 |
| [ISO 27017 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 9.2：用户访问管理 <br> 9.4：系统和应用程序访问控制 <br> 15.1：信息在供应商关系中的安全性 | 2020 年 2 月 22 日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-33：帐户修改 <br> CA-34：用户身份验证 <br> CA-35：特权访问 <br> CA-36：远程访问 <br> CA-57：客户密码箱 Microsoft 管理审批 <br> CA-58：客户密码箱服务请求 <br> CA-59：客户密码箱通知 <br> CA-61： JIT 审阅和批准 | 2019 年 9 月 30 日 |
| [SOC 2 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-32：共享帐户策略 <br> CA-33：帐户修改 <br> CA-34：用户身份验证 <br> CA-35：特权访问 <br> CA-36：远程访问 <br> CA-53：第三方监视 <br> CA-56：客户的密码箱客户批准 <br> CA-57：客户密码箱 Microsoft 管理审批 <br> CA-58：客户密码箱服务请求 <br> CA-59：客户密码箱通知 <br> CA-61： JIT 审阅和批准 | 2019 年 9 月 30 日 |
| [SOC 3 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=9df8b99b-96ce-49a9-bff4-268031dcc9a6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CUEC-15：客户密码箱请求 | 2019 年 9 月 30 日 |