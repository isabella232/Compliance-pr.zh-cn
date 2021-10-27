---
title: 安全监视概述
description: 了解安全监视Microsoft 365
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
ms.openlocfilehash: 37213f9c9ccab59bbd956cb64c1b2f16a8d72821
ms.sourcegitcommit: 1f30616328d7deb04e41dcbd44a330ea937fe94f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/26/2021
ms.locfileid: "60582475"
---
# <a name="security-monitoring-overview"></a>安全监视概述

## <a name="what-is-microsofts-strategy-for-monitoring-security"></a>Microsoft 的监视安全策略是什么？

Microsoft 持续监视其系统，以检测和响应对 Microsoft 联机服务的威胁。 安全监视和警报的关键原则是：

- 稳定性：检测各种攻击行为的信号和逻辑
- 准确性：有意义的警报，以避免干扰噪音
- 速度：足够快地捕获攻击者以阻止攻击者的能力

自动化、规模化和基于云的解决方案是我们监视和响应策略的关键支柱。 为了有效阻止某些 Microsoft 在线服务规模的攻击，我们的监控系统需要几乎实时自动引发高度准确的警报。 同样，当检测到问题时，我们需要能够大规模缓解风险，我们无法依赖团队手动解决计算机的问题。 为了大规模缓解风险，我们使用基于云的工具自动应用对策，并为工程师提供工具以在整个环境中快速应用批准的缓解措施。

## <a name="how-do-microsoft-online-services-perform-security-monitoring"></a>Microsoft 联机服务如何执行安全监视？

Microsoft 联机服务使用集中日志记录来收集和分析可能指示安全事件的活动的日志事件。 集中式日志记录工具可以聚合来自所有系统组件的日志，包括事件日志、应用程序日志、访问控制日志和基于网络的入侵检测系统。 除了服务器日志记录和应用程序级别数据之外，核心基础结构还配备了可生成详细遥测并提供基于主机的入侵检测的自定义安全代理。 我们使用此遥测数据进行监视和取证。

我们收集的日志记录和遥测数据可启用 24/7 安全警报。 警报系统会在上传日志数据时对其进行分析，并近乎实时地生成警报。 它包括基于规则的警报和基于机器学习模型的更复杂的警报。 我们的监视逻辑的涵盖范围远不止一般攻击方案，还融入了对服务体系结构和操作的深度感知。 我们分析安全监视数据以持续改进我们的模型，以检测新型攻击并提高安全监视的准确性。

## <a name="how-do-microsoft-online-services-respond-to-security-monitoring-alerts"></a>Microsoft 联机服务如何响应安全监视警报？

当触发警报的安全事件需要在整个服务中执行响应性操作或进一步调查取证证据时，我们的基于云的工具允许在整个环境中快速响应。 这些工具包括完全自动化的智能代理，后者可通过安全应对措施来响应检测到的威胁。 许多情况下，这些代理会部署自动应对措施来大规模缓解安全检测，而无需人工干预。 如果无法做出此响应，安全监视系统会自动向相应的呼叫工程师发出警报，这些工程师配备了一组工具，使他们能够实时采取行动，大规模缓解检测到的威胁。 潜在事件会上报给相应的 Microsoft 安全响应团队，然后使用安全事件响应流程进行解决。

## <a name="how-do-microsoft-online-services-monitor-system-availability"></a>Microsoft 联机服务如何监视系统可用性？

Microsoft 主动监视其系统，以指示资源过度使用和异常使用。 资源监控由服务冗余进行补充，以帮助避免意外停机，并为客户提供对产品和服务的可靠访问。 Microsoft 联机服务运行状况问题通过服务运行状况仪表板 (SHD) 。

Azure 和 Dynamics 365 联机服务利用多个基础结构服务来监视其安全性和运行状况可用性。 实施综合事务 (STX) 测试使 Azure 和 Dynamics 服务能够检查其服务的可用性。 STX 框架旨在支持在运行服务时自动测试组件，并针对实时站点故障警报进行测试。 此外，Azure 安全 (ASM) 服务已实施集中综合测试过程，以验证安全警报在新建和正在运行的服务中是否正常工作。

## <a name="related-external-regulations--certifications"></a>认证的相关&法规

Microsoft 的在线服务会定期进行审核，以遵守外部法规和认证。 有关与安全监视相关的控制措施的验证，请参阅下表。

### <a name="azure-and-dynamics-365"></a>Azure 和 Dynamics 365

| **外部审核** | **Section** | **最新报告日期** |
|:--------|:--------|:------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> <br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.3：可用性监视和容量规划 | 2020 年 12 月 2 日 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.3：可用性监视和容量规划 <br> A.16.1：信息安全事件管理和改进 | 2020 年 12 月 2 日 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | IM-1：事件管理框架 <br> IM-2：事件检测配置 <br> IM-3：事件管理过程 <br> IM-4：事后分析 <br> VM-1：安全事件日志记录和集合 <br> VM-12：Azure 服务可用性监视 <br> VM-4：恶意事件调查 <br> VM-6：安全漏洞监视 | 2021 年 3 月 31 日 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | IM-1：事件管理框架 <br> IM-2：事件检测配置 <br> IM-3：事件管理过程 <br> IM-4：事后分析 <br> PI-2：Azure 门户 SLA 性能评审 <br> VM-1：安全事件日志记录和集合 <br> VM-12：Azure 服务可用性监视 <br> VM-4：恶意事件调查 <br> VM-6：安全漏洞监视 | 2021 年 3 月 31 日 |

### <a name="office-365"></a>Office 365

| **外部审核** | **Section** | **最新报告日期** |
|:--------|:--------|:------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | AC-2：帐户管理 <br> AC-17：远程访问 <br> AU-7：减少审核并生成报告 <br> SI-4：信息系统监控 <br> SI-7：软件、固件和信息完整性 <br> | 2020 年 9 月 24 日 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> <br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.3：可用性监视和容量规划 | 2021 年 4 月 20 日 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-19：更改监视 <br> CA-26：安全事件报告 <br> CA-29：呼叫工程师 <br> CA-48：数据中心日志记录 | 2020 年 12 月 24 日 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-19：更改监视 <br> CA-26：安全事件报告 <br> CA-29：呼叫工程师 <br> CA-30：可用性监视 <br> CA-48：数据中心日志记录 | 2020 年 12 月 24 日 |
| [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-08：报告事件 <br> CUEC-10：服务合同 | 2020 年 12 月 24 日 |

## <a name="resources"></a>资源

- [幕后：保护支持 Microsoft 365 服务的基础结构](https://download.microsoft.com/download/c/4/5/c45b197e-f0d9-4f40-bd5f-ed8fc7d0cd8c/M365DCSecurityIntro_Whitepaper.pdf)
