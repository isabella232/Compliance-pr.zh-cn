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
hideEdit: true
ms.openlocfilehash: 7a38d4c16de5ee489dab76165b952140af6a4656
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497424"
---
# <a name="security-monitoring-overview"></a>安全监视概述

## <a name="what-is-microsofts-strategy-for-monitoring-security"></a>Microsoft 的监视安全策略是什么？

Microsoft 365 持续监视其系统，以检测和响应对 Microsoft 365 服务的威胁。 安全监视和警报的关键原则是：

- 稳定性：用于检测各种攻击行为的信号和逻辑
- 准确性：有意义的警报，以避免干扰噪音
- 速度：足够快地捕获攻击者以阻止攻击者的能力

自动化、扩展和基于云的解决方案是我们监控和响应策略的关键支柱。 为了有效捕获和停止某些 Microsoft 365 核心服务规模的攻击，我们的监控系统需要几乎实时地自动发出警报。 同样，当检测到问题时，我们需要能够大规模缓解风险，我们无法依赖团队手动解决计算机的问题。 为了大规模缓解风险，我们使用基于云的工具自动应用对策，并为工程师提供工具以在整个环境中快速应用批准的缓解措施。

## <a name="how-does-microsoft-365-perform-security-monitoring"></a>Microsoft 365 如何执行安全监视？

Microsoft 365 使用集中日志记录来收集和分析可能指示安全事件的活动的日志事件。 集中日志记录工具聚合来自所有系统组件的日志，包括事件日志、应用程序日志、访问控制日志和基于网络的入侵检测系统。 除了服务器日志记录和应用程序级别数据之外，服务中的核心基础结构还配备了可生成详细遥测并提供基于主机的入侵检测的自定义安全代理。 我们使用此遥测进行监视和取证。

我们收集的日志记录和遥测数据可启用 24/7 安全警报。 我们的警报系统在日志数据上载时对其进行分析，从而几乎实时生成警报。 这包括基于规则的警报和基于机器学习模型的更复杂的警报。 我们的监视逻辑超越常规攻击方案，并融入了对服务体系结构和操作的深入感知。 我们使用安全监视数据持续改进模型，以检测新型攻击并提高安全监视的准确性。

## <a name="how-does-microsoft-365-respond-to-security-monitoring-alerts"></a>Microsoft 365 如何响应安全监视警报？

当我们需要采取措施响应警报或进一步调查整个服务中的取证证据时，我们的基于云的工具使我们能够在整个环境中快速响应。 这些工具包括使用安全对策响应检测到的威胁的完全自动化的智能代理。 在许多情况下，这些代理部署自动对策，以在无需人为干预的情况下大规模缓解安全检测。 如果不可能，安全监视系统会自动向相应的呼叫工程师发出警报，这些工程师配备了一组工具，使他们能够实时采取行动，大规模缓解检测到的威胁。 使用安全事件响应流程解决上报给 Microsoft 365 安全响应团队的潜在事件。

## <a name="how-does-microsoft-365-monitor-system-availability"></a>Microsoft 365 如何监视系统可用性？

Microsoft 365 主动监视其系统，以指示资源过度使用和异常使用。 资源监控由服务冗余进行补充，以帮助避免意外停机，并为客户提供对产品和服务的可靠访问。 服务运行状况问题通过服务运行状况仪表板 (SHD) 。

## <a name="related-external-regulations--certifications"></a>认证的相关&法规

Microsoft 的在线服务会定期进行审核，以遵守外部法规和认证。 有关与安全监视相关的控制措施的验证，请参阅下表。

| **外部审核** | **Section** | **最新报告日期** |
|:--------|:--------|:------|
| [FedRAMP (Office 365) ](https://compliance.microsoft.com/compliancemanager) | AC-2：帐户管理 <br> AC-17：远程访问 <br> AU-7：减少审核并生成报告 <br> SI-4：信息系统监控 <br> SI-7：软件、固件和信息完整性 <br> | 2020 年 9 月 24 日 |
| [OFFICE 365 (ISO 27001/27002) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> <br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.3：可用性监视和容量规划 | 2020 年 2 月 22 日 |
| [OFFICE 365 (ISO 27017) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.3：可用性监视和容量规划 <br> A.16.1：信息安全事件管理和改进 | 2020 年 2 月 22 日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-19：更改监视 <br> CA-26：安全事件报告 <br> CA-29：呼叫工程师 <br> CA-48：数据中心日志记录 | 2020 年 12 月 24 日 |
| [SOC 2 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-19：更改监视 <br> CA-26：安全事件报告 <br> CA-29：呼叫工程师 <br> CA-30：可用性监视 <br> CA-48：数据中心日志记录 | 2020 年 12 月 24 日 |
| [OFFICE 365 (SOC 3) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-08：报告事件 <br> CUEC-10：服务合同 | 2020 年 12 月 24 日 |

## <a name="resources"></a>资源

- [后台：保护支持 Microsoft 365 服务的基础结构](https://download.microsoft.com/download/c/4/5/c45b197e-f0d9-4f40-bd5f-ed8fc7d0cd8c/M365DCSecurityIntro_Whitepaper.pdf)
