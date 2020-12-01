---
title: 事件管理概述
description: 了解 Microsoft 365 中的事件管理
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
ms.openlocfilehash: 6b5c77a2a81f8231ad620fbc40205457c6ba1a49
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/30/2020
ms.locfileid: "49505928"
---
# <a name="incident-management-overview"></a>事件管理概述

## <a name="what-is-a-security-incident"></a>什么是安全事件？

Microsoft 将安全事件定义在其在线服务中，作为已确认的安全漏洞，在 Microsoft 处理过程中导致意外或非法销毁、丢失、篡改、未经授权泄露或访问客户数据或个人数据。 例如，在未经授权的情况下访问 Microsoft 365 基础结构和 exfiltration 客户数据将构成安全事件，而不影响服务或客户数据的机密性、完整性或可用性的合规性事件不被视为安全事件。

## <a name="how-does-microsoft-respond-to-security-incidents"></a>Microsoft 如何响应安全事件？

每当出现安全事件时，Microsoft 都将尽力快速有效地进行响应，以保护 Microsoft 服务和客户数据。 Microsoft 采用了一个事件响应策略，旨在快速高效地调查、包含和删除安全威胁。

系统会持续监视 Microsoft 云服务的泄露迹象。 除了自动安全监视和警报之外，所有员工都会收到年度培训以识别并报告潜在安全事件的标志。 员工、客户或安全监控工具检测到的任何可疑活动都将升级到特定于服务的安全响应团队以供调查。 所有服务操作团队（包括特定于服务的安全响应团队）都维护一个深度的待命轮换，以确保资源可全天候适用于事件响应。 我们的呼叫循环使 Microsoft 能够在任何时间或规模（包括广泛的或并发的事件）上安装有效的事件响应。

当检测到可疑活动并进行升级时，特定于服务的安全响应团队将启动 **分析、控制、eradication 和恢复** 的过程。 这些团队将对潜在事件的分析进行协调以确定其范围，包括对客户或客户数据的任何影响。 根据此分析，特定于服务的安全响应团队可与受影响的服务团队合作，以制定包含威胁的计划，并最大限度地降低事件的影响，消除环境中的威胁，并完全恢复到已知的安全状态。 相关服务团队实施包含特定服务安全响应团队支持的计划，以确保成功消除了威胁，并将受影响的服务进行完全恢复。

在解决事件之后，服务团队将实现从事件中获得的任何经验教训，以便更好地防止、检测和响应未来的类似事件。 选择安全事件（尤其是客户影响或导致数据泄露的事件）会在事后后进行完整的事件。 事后旨在确定技术故障、过程故障、手动错误和其他可能对事件有贡献的过程缺陷，以及在事件响应过程中确定的其他过程缺陷。 在后期事后中确定的改进是通过与服务特定的安全响应团队进行协调实现的，以帮助防止将来发生的事件并改进检测和响应功能。

## <a name="how-and-when-are-customers-notified-of-security-or-privacy-incidents"></a>客户如何以及何时通知安全或隐私事件？

只要 Microsoft 意识到违反了授权丢失、泄露或修改客户数据的安全，Microsoft 就会在72小时内通知受影响的客户， (DPA) 的在线服务条款 (OST) 中所述。 在正式安全事件声明发生时，将开始通知时间线承诺。 在声明安全事件时，通知过程会尽可能 expeditiously，而不会出现不需要的延迟。

通知包括对泄露性质的描述、对用户的影响，以及在适用)  (的缓解步骤。 如果在初始通知时未完成 Microsoft 调查，则通知还将指示后续通信的后续步骤和时间线。

如果客户意识到可能会对 Microsoft 造成影响的事件（包括但不限于数据泄露），客户应负责根据 DPA 中定义的事件及时通知 Microsoft。

## <a name="related-external-regulations--certifications"></a>& 认证的相关外部法规

将定期审核 Microsoft 的在线服务，以遵守外部法规和认证。 请参阅下表，验证与事件管理相关的控制措施。

| **外部审核** | **Section** | **最新报告日期** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365) ](https://compliance.microsoft.com/compliancemanager) | IR-4：事件处理 <br> IR-6：事件报告 <br> IR-8：事件响应计划 | 2020年9月24日 |
| [ISO 27001/27002 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 16.1：信息安全事件管理和改进 | 2020 年 2 月 22 日 |
| [ISO 27017 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 16.1：信息安全事件管理和改进 | 2020 年 2 月 22 日 |
| [ISO 27018 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 10.1：涉及 PII 的数据泄露通知  | 2020 年 2 月 22 日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-26：安全事件报告 <br> CA-47：事件响应 | 2019 年 9 月 30 日 |
| [SOC 2 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-12：服务级别协议 (Sla)  <br> CA-13：事件响应指南 <br> CA-15：服务运行状况通知  <br>  <br> CA-26：安全事件报告 <br> CA-29：待命工程师 <br> CA-47：事件响应 | 2019 年 9 月 30 日 |
| [SOC 3 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=9df8b99b-96ce-49a9-bff4-268031dcc9a6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CUEC-08：报告事件  | 2019 年 9 月 30 日  |

## <a name="resources"></a>资源

- [ (OST) 的联机服务条款 ](https://www.microsoft.com/licensing/product-licensing/products)
- [ (DPA) 的数据保护附录 ](https://www.microsoft.com/licensing/product-licensing/products)
- [适用于 Azure 和 Office 365 的 Microsoft 云事件管理实施指南](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a8a7cb87-9710-4d09-8748-0835b6754e95&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)
- [Office 365-Office 365 的第三方漏洞评估-2019](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=e85e478f-2491-435d-9c1b-2f0ad7ca8e56&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_Pen_Test_and_Security_Assessments)
