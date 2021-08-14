---
title: 事件管理概述
description: 了解事件管理中的Microsoft 365
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
hideEdit: true
ms.openlocfilehash: 977f6fcb60dd57033cf2f3555d9d4bf2bf74066c
ms.sourcegitcommit: 01938022a292c07e98041dc6ae1312a1b8c617db
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/13/2021
ms.locfileid: "58260767"
---
# <a name="incident-management-overview"></a>事件管理概述

## <a name="what-is-a-security-incident"></a>什么是安全事件？

Microsoft 在其联机服务中将安全事件定义为已确认的安全漏洞，它们会导致在 Microsoft 处理时意外或非法销毁、丢失、更改、未经授权泄漏或访问客户数据或个人数据。 例如，未经授权访问 Microsoft 在线服务基础结构和泄露客户数据将构成安全事件，而不影响服务或客户数据的机密性、完整性或可用性的合规性事件不被视为安全事件。

## <a name="how-does-microsoft-respond-to-security-incidents"></a>Microsoft 如何响应安全事件？

每当发生安全事件时，Microsoft 都会努力快速响应，以保护Microsoft 服务客户数据。 Microsoft 采用旨在快速高效地调查、包含和删除安全威胁的事件响应策略。

Microsoft 云服务会持续受到监视，以发现泄露的迹象。 除了自动安全监视和警报之外，所有员工都每年接受一次培训，以识别和报告潜在安全事件的迹象。 员工、客户或安全监视工具检测到的任何可疑活动都升级为特定于服务的安全响应团队进行调查。 所有服务运营团队（包括特定于服务的安全响应团队）保持深层的呼叫轮换，以确保资源可用于 24x7x365 事件响应。 我们的呼叫轮换使 Microsoft 能够随时或大规模地装入有效的事件响应，包括大范围或并发事件。

当检测到可疑活动并上报时，特定于服务的安全响应团队将启动分析、抑制、 **消除和恢复过程**。 这些团队协调潜在事件的分析以确定其范围，包括对客户或客户数据的任何影响。 基于此分析，特定于服务的安全响应团队与受影响服务团队合作，共同制定包含威胁并最大限度地减少事件影响的计划，从环境中消除威胁，并完全恢复到已知安全状态。 相关服务团队在特定于服务的安全响应团队的支持下实施计划，以确保成功消除威胁，并且影响的服务将进行完整恢复。

在事件解决后，服务团队将实施从事件获得的任何经验，以更好地防止、检测和响应将来发生的类似事件。 选择安全事件，尤其是影响客户或导致数据泄露的事件，在事后进行完整事件。 事后剖析旨在识别技术失效、过程失败、手动错误以及可能导致事件发生的或在事件响应过程中识别的其他流程缺陷。 在事后分析期间确定的改进在特定于服务的安全响应团队的协作下实现，以帮助防止未来事件并改进检测和响应功能。

## <a name="how-and-when-are-customers-notified-of-security-or-privacy-incidents"></a>如何以及何时向客户通知安全或隐私事件？

只要 Microsoft 发现涉及未经授权丢失、泄露或修改客户数据的安全漏洞，Microsoft 就会在 72 小时内通知受影响的客户，如联机服务条款 (OST) 的数据保护附录 (DPA) 所述。 通知日程表承诺从正式安全事件声明发生时开始。 在声明发生安全事件后，通知流程将尽快进行，不要出现不当的延迟。

通知包括泄露性质、大致用户影响和缓解措施 (（如果适用) ）。 如果 Microsoft 的调查在初始通知时尚未完成，则通知还将指示后续步骤和后续通信日程表。

如果客户意识到会对 Microsoft 产生影响的事件，包括但不限于数据泄露，客户应负责根据 DPA 中的定义，立即通知 Microsoft 该事件。

## <a name="related-external-regulations--certifications"></a>认证的相关&法规

Microsoft 的在线服务会定期进行审核，以遵守外部法规和认证。 有关与事件管理相关的控制措施的验证，请参阅下表。

### <a name="azure-and-dynamics-365"></a>Azure 和 Dynamics 365

| **外部审核** | **Section** | **最新报告日期** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.16.1：信息安全事件管理和改进 | 2021 年 12 月 2 日 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.16.1：信息安全事件管理和改进 | 2021 年 12 月 2 日 |
| [ISO 27018](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=56904fc3-0942-4ff5-9eef-7cabc751a25c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.1：有关涉及 PII 的数据泄露的通知  | 2021 年 12 月 2 日 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | IM-1：事件管理框架 <br> IM-2：检测机制和警报 <br> IM-3：事件响应执行 <br> IM-4：事后分析 <br> IM-6：事件响应测试 <br> OA-7：呼叫工程师访问 | 2021 年 3 月 31 日 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CCM-9：取证过程 <br> CUEC：报告事件 <br> IM-1：事件管理框架 <br> IM-2：检测机制和警报 <br> IM-3：事件响应执行 <br> IM-4：事后分析 <br> IM-6：事件响应测试 <br> OA-7：呼叫工程师访问 <br> SOC2-6：客户支持网站 <br> SOC2-9：服务仪表板 | 2021 年 3 月 31 日 |

### <a name="office-365"></a>Office 365

| **外部审核** | **Section** | **最新报告日期** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | IR-4：事件处理 <br> IR-6：事件报告 <br> IR-8：事件响应计划 | 2020 年 9 月 24 日 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.16.1：信息安全事件管理和改进 | 2021 年 4 月 20 日 |
| [ISO 27018](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1：有关涉及 PII 的数据泄露的通知  | 2021 年 4 月 20 日 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-26：安全事件报告 <br> CA-47：事件响应 | 2020 年 12 月 24 日 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-12：SLA (服务级别)  <br> CA-13：事件响应指南 <br> CA-15：服务运行状况通知  <br>  <br> CA-26：安全事件报告 <br> CA-29：呼叫工程师 <br> CA-47：事件响应 | 2020 年 12 月 24 日 |
| [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-08：报告事件  | 2020 年 12 月 24 日  |

## <a name="resources"></a>资源

- [联机服务条款 (OST)](https://www.microsoft.com/licensing/product-licensing/products)
- [数据保护附录 (DPA) ](https://www.microsoft.com/licensing/product-licensing/products)
- [Azure 和 Microsoft 云事件管理实施Office 365](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a8a7cb87-9710-4d09-8748-0835b6754e95&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)
- [Office 365 - 第三方漏洞评估 -Office 365 - 2019](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=e85e478f-2491-435d-9c1b-2f0ad7ca8e56&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_Pen_Test_and_Security_Assessments)
