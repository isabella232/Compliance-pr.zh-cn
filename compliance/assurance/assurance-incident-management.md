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
hideEdit: true
ms.openlocfilehash: 45636bbefc0bdd85ab2d8f21091060d49dbaa4c6
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497156"
---
# <a name="incident-management-overview"></a>事件管理概述

## <a name="what-is-a-security-incident"></a>什么是安全事件？

Microsoft 在其在线服务中将安全事件定义为经确认的安全泄露，导致 Microsoft 处理期间意外或非法破坏、丢失、更改、未经授权披露或访问客户数据或个人数据。 例如，未经授权访问 Microsoft 365 基础结构和泄露客户数据将构成安全事件，而不影响服务或客户数据的机密性、完整性或可用性的合规性事件不被视为安全事件。

## <a name="how-does-microsoft-respond-to-security-incidents"></a>Microsoft 如何响应安全事件？

每当发生安全事件时，Microsoft 都会努力快速响应并有效保护 Microsoft 服务和客户数据。 Microsoft 采用旨在快速高效地调查、包含和删除安全威胁的事件响应策略。

Microsoft 云服务会持续受到监视，以发现泄露的迹象。 除了自动安全监视和警报之外，所有员工都每年接受一次培训，以识别和报告潜在安全事件的迹象。 员工、客户或安全监视工具检测到的任何可疑活动都升级为特定于服务的安全响应团队进行调查。 所有服务运营团队（包括特定于服务的安全响应团队）保持深层的呼叫轮换，以确保资源可用于 24x7x365 事件响应。 我们的呼叫轮换使 Microsoft 能够随时或大规模地装入有效的事件响应，包括大范围或并发事件。

当检测到可疑活动并上报时，特定于服务的安全响应团队将启动分析、抑制、 **消除和恢复过程**。 这些团队协调潜在事件的分析以确定其范围，包括对客户或客户数据的任何影响。 基于此分析，特定于服务的安全响应团队与受影响服务团队合作，共同制定包含威胁并最大限度地减少事件影响的计划，从环境中消除威胁，并完全恢复到已知安全状态。 相关服务团队在特定于服务的安全响应团队的支持下实施计划，以确保成功消除威胁，并且影响的服务将进行完整恢复。

在事件解决后，服务团队将实施从事件获得的任何经验，以更好地在将来预防、检测和响应类似的事件。 选择安全事件，尤其是影响客户或导致数据泄露的事件，在事后进行完整事件。 事后分析旨在识别技术缺陷、过程失败、手动错误以及可能导致事件或在事件响应过程中识别的其他过程缺陷。 在事后分析期间确定的改进在特定于服务的安全响应团队的协作下实现，以帮助防止未来事件并改进检测和响应功能。

## <a name="how-and-when-are-customers-notified-of-security-or-privacy-incidents"></a>如何以及何时向客户通知安全或隐私事件？

只要 Microsoft 发现涉及未经授权丢失、泄露或修改客户数据的安全漏洞，Microsoft 就会在 72 小时内通知受影响的客户，如联机服务条款 (OST) 的数据保护附录 (DPA) 所述。 当发生官方安全事件声明时，通知时间线承诺将开始。 声明安全事件时，通知过程将尽可能快地发生，而不会过度延迟。

通知包括泄露性质、近似用户影响和缓解步骤 (适用) 。 如果 Microsoft 的调查在初始通知时尚未完成，则通知还将指示后续步骤和后续通信日程表。

如果客户意识到会对 Microsoft 产生影响的事件，包括但不限于数据泄露，客户应负责根据 DPA 中的定义，立即通知 Microsoft 该事件。

## <a name="related-external-regulations--certifications"></a>认证的相关&法规

Microsoft 的在线服务会定期进行审核，以遵守外部法规和认证。 有关与事件管理相关的控制措施的验证，请参阅下表。

| **外部审核** | **Section** | **最新报告日期** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365) ](https://compliance.microsoft.com/compliancemanager) | IR-4：事件处理 <br> IR-6：事件报告 <br> IR-8：事件响应计划 | 2020 年 9 月 24 日 |
| [OFFICE 365 (ISO 27001/27002) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.16.1：信息安全事件管理和改进 | 2020 年 2 月 22 日 |
| [OFFICE 365 (ISO 27017) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.16.1：信息安全事件管理和改进 | 2020 年 2 月 22 日 |
| [OFFICE 365 (ISO 27018) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.10.1：有关涉及 PII 的数据泄露的通知  | 2020 年 2 月 22 日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-26：安全事件报告 <br> CA-47：事件响应 | 2020 年 12 月 24 日 |
| [SOC 2 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-12：SLA (服务级别)  <br> CA-13：事件响应指南 <br> CA-15：服务运行状况通知  <br>  <br> CA-26：安全事件报告 <br> CA-29：呼叫工程师 <br> CA-47：事件响应 | 2020 年 12 月 24 日 |
| [OFFICE 365 (SOC 3) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-08：报告事件  | 2020 年 12 月 24 日  |

## <a name="resources"></a>资源

- [OST (联机服务) ](https://www.microsoft.com/licensing/product-licensing/products)
- [数据保护附录 (DPA) ](https://www.microsoft.com/licensing/product-licensing/products)
- [Azure 和 Office 365 的 Microsoft 云事件管理实施指南](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=a8a7cb87-9710-4d09-8748-0835b6754e95&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)
- [Office 365 - Office 365 的第三方漏洞评估 - 2019](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=e85e478f-2491-435d-9c1b-2f0ad7ca8e56&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_Pen_Test_and_Security_Assessments)
