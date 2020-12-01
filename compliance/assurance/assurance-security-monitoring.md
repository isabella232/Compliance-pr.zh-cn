---
title: 安全监视概述
description: 了解 Microsoft 365 中的安全监视
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
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: f3eae0aa5ba79372a7ce0d9a34d4dd35fe83a36b
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/30/2020
ms.locfileid: "49506479"
---
# <a name="security-monitoring-overview"></a>安全监视概述

## <a name="what-is-microsofts-strategy-for-monitoring-security"></a>Microsoft 的监视安全策略是什么？

Microsoft 365 参与对其系统的连续安全监视，以检测和响应 Microsoft 365 服务的威胁。 我们的安全监视和警报的关键原则是：

- 健壮：检测各种攻击行为的信号和逻辑
- 准确性：避免打扰干扰的有意义的警报
- 速度：能够更快地捕获攻击者的能力以停止攻击者

自动化、扩展和基于云的解决方案是我们监控和响应策略的关键要点。 为了让我们能够以一些 Microsoft 365 core services 的规模有效地捕获和停止攻击，我们的监控系统需要在近实时时间内自动提高非常准确的警报。 同样，当检测到问题时，我们需要能够在规模范围缓解风险，我们不能依赖团队手动修复计算机的问题。 为了在规模范围内缓解风险，我们使用基于云的工具自动应用对策并向工程师提供工具，以便在整个环境中快速应用经批准的缓解措施。

## <a name="how-does-microsoft-365-perform-security-monitoring"></a>Microsoft 365 如何执行安全监控？

Microsoft 365 使用集中日志记录来收集和分析可能表示安全事件的活动的日志事件。 集中式日志记录工具聚合来自所有系统组件（包括事件日志、应用程序日志、访问控制日志和基于网络的入侵检测系统）的日志。 除了服务器日志记录和应用程序级数据之外，我们的服务中的核心基础结构还配备了自定义安全代理，这些代理生成详细遥测并提供基于主机的入侵检测。 我们使用此遥测进行监控和辩论。

我们收集的日志记录和遥测数据支持24/7 安全警报。 我们的警报系统在上载日志数据时对其进行分析，并在近实时生成警报。 这包括基于规则的警报和基于机器学习模型的更复杂的警报。 我们的监控逻辑超出了一般性的攻击方案，并并入了对服务体系结构和操作的深入认知。 我们使用安全监视数据来不断改进模型，以检测新类型的攻击并提高安全监控的准确性。

## <a name="how-does-microsoft-365-respond-to-security-monitoring-alerts"></a>Microsoft 365 如何响应安全监控警报？

当我们需要采取行动来响应警报或进一步调查整个服务中的法庭证据时，我们基于云的工具使我们能够在整个环境中快速做出响应。 这些工具包括完全自动化的智能代理，它们通过安全对策响应检测到的威胁。 在很多情况下，这些代理部署自动对策以在不进行人为干预的情况下缓解安全检测。 如果无法这样做，安全监视系统将自动警告相应的待命工程师，这些工程师配备了一组工具，使他们能够实时操作，以在规模范围内缓解检测到的威胁。 升级到 Microsoft 365 安全响应团队的潜在事件是使用安全事件响应过程解决的。

## <a name="how-does-microsoft-365-monitor-system-availability"></a>Microsoft 365 如何监控系统可用性？

Microsoft 365 主动监视其系统，了解资源利用率和异常使用情况的指标。 服务冗余对资源监控进行了求和，以帮助避免意外停机，并为客户提供对产品和服务的可靠访问。 通过服务运行状况仪表板 (SHD) 将服务运行状况问题及时传达给客户。

## <a name="related-external-regulations--certifications"></a>& 认证的相关外部法规

将定期审核 Microsoft 的在线服务，以遵守外部法规和认证。 请参阅下表以验证与安全监视相关的控件。

| **外部审核** | **Section** | **最新报告日期** |
|:--------|:--------|:------|
| [FedRAMP (Office 365) ](https://compliance.microsoft.com/compliancemanager) | AC-2：帐户管理 <br> AC-17：远程访问 <br> AU-7：审核缩减和报告生成 <br> SI-4：信息系统监控 <br> SI-7：软件、固件和信息完整性 <br> | 2020年9月24日 |
| [ISO 27001/27002 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> <br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 12.1.3：可用性监控和容量规划 | 2020 年 2 月 22 日 |
| [ISO 27017 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 12.1.3：可用性监控和容量规划 <br> 16.1：信息安全事件管理和改进 | 2020 年 2 月 22 日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-19：更改监控 <br> CA-26：安全事件报告 <br> CA-29：待命工程师 <br> CA-48：数据中心日志记录 | 2019 年 9 月 30 日 |
| [SOC 2 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-19：更改监控 <br> CA-26：安全事件报告 <br> CA-29：待命工程师 <br> CA-30：可用性监控 <br> CA-48：数据中心日志记录 | 2019 年 9 月 30 日 |
| [SOC 3 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=9df8b99b-96ce-49a9-bff4-268031dcc9a6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CUEC-08：报告事件 <br> CUEC-10：服务约定 | 2019 年 9 月 30 日 |

## <a name="resources"></a>资源

- [幕后：保护 Microsoft 365 服务电源的基础结构](https://download.microsoft.com/download/c/4/5/c45b197e-f0d9-4f40-bd5f-ed8fc7d0cd8c/M365DCSecurityIntro_Whitepaper.pdf)
