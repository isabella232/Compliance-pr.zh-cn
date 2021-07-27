---
title: 安全开发和操作概述
description: 了解安全开发和 Microsoft 365
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
ms.openlocfilehash: 7a706cda887c0c2675841648ef8541ffbb872884
ms.sourcegitcommit: 07578a8e03b931f47c49f4e34b78cf8ba0605e8f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/23/2021
ms.locfileid: "53573690"
---
# <a name="security-development-and-operations-overview"></a>安全开发和操作概述

## <a name="how-does-microsoft-implement-secure-development-practices"></a>Microsoft 如何实施安全开发实践？

Microsoft 安全开发生命周期 (SDL) 是一个侧重于开发和操作安全软件的质量保证过程。 SDL 为 Microsoft 的开发人员和工程师提供了详细的可衡量安全要求，以减少我们产品和服务中漏洞的数量和严重性。 所有 Microsoft 软件开发团队都必须遵循 SDL 要求，并持续更新 SDL 以反映不断变化的威胁环境、行业最佳做法和合规性法规标准。

## <a name="how-does-microsofts-sdl-improve-application-security"></a>Microsoft 的 SDL 如何提高应用程序安全性？

Microsoft 的 SDL 流程可考虑以下五个开发阶段：要求、设计、实现、验证和发布。 它首先定义软件要求时注意安全性。 为此，我们询问有关应用程序必须完成的任务的安全相关问题。 应用程序是否需要收集敏感数据？ 应用程序是否执行敏感任务或重要任务？ 应用程序是否需要接受来自不受信任的源的输入？

确定相关的安全要求后，我们将软件设计为包含满足这些要求的安全功能。 我们的开发人员在代码中实现 SDL 和设计要求，我们通过手动代码检查、自动化安全工具和渗透测试来验证这些要求。 最后，在发布代码之前，新功能和重大更改将经过最终安全和隐私审查，以确保满足所有要求。

## <a name="how-does-microsoft-test-source-code-for-common-vulnerabilities"></a>Microsoft 如何测试常见漏洞的源代码？

为了支持我们的开发人员在代码开发期间和发布后实现安全要求，Microsoft 提供了一套安全开发工具，可自动检查源代码中是否存在安全缺陷和漏洞。 Microsoft 定义并发布供开发人员使用的已批准工具列表，如编译器和开发环境，以及 Microsoft 生成管道中自动执行的内置安全检查。 我们的开发人员使用最新版本的已批准工具来利用新的安全功能。

在将代码签入发布分支之前，SDL 需要由单独的审阅者手动检查代码。 代码审查员会检查编码错误并验证代码更改是否满足 SDL 和设计要求、通过功能和安全测试并可靠地执行。 他们还会审查相关的文档、配置和依赖项，以确保正确记录代码更改并且不会导致意外的副作用。 如果审查者在代码审查期间发现问题，他们可以要求提交者在进行建议更改和额外测试后重新提交代码。 代码审查者也可能决定完全阻止不符合要求的代码签入。 在审阅者认为代码满意后，审阅者会提供审批，在代码可以继续执行下一个部署阶段之前需要此审批。

除了安全开发工具和手动代码检查之外，Microsoft 还使用自动化安全工具强制执行 SDL 要求。 其中许多工具内置在提交管道中，在签入和编译新的内部版本时自动分析代码的安全缺陷。 示例包括常见安全缺陷的静态代码分析和用于分析嵌入密码的代码的凭据扫描程序。 必须修复由自动安全工具发现的问题，然后新的内部版本才能通过安全审查并批准发布。

## <a name="how-does-microsoft-manage-open-source-software"></a>Microsoft 如何管理开放源代码软件？

Microsoft 已采用管理开放源代码安全性的高级别策略，该策略利用旨在：

- 了解在产品和服务中使用的开放源代码组件。
- 跟踪这些组件的使用位置和方式。
- 确定这些组件是否具有任何漏洞。
- 发现影响这些组件的漏洞时，请正确响应。

Microsoft 工程团队负责保护产品或服务中包含的所有开源软件的安全。 为大规模实现此目的，Microsoft 通过 CG 将基本功能内置到工程系统中，从而自动进行开放源代码检测、法律要求工作流和针对易受攻击的组件发出警报。 自动化 CG 工具扫描 Microsoft 内部版本，以发现开放源代码组件和相关安全漏洞或法律要求。 已发现的组件将注册并提交给相应的团队进行业务和安全审查。 这些审查旨在评估与开放源代码组件相关的任何法律义务或安全漏洞，并解决这些义务或漏洞，然后再批准组件进行部署。

## <a name="related-external-regulations--certifications"></a>认证的相关&法规

Microsoft 的在线服务会定期进行审核，以遵守外部法规和认证。 有关与安全开发和操作相关的控件的验证，请参阅下表。

| **外部审核** | **Section** | **最新报告日期** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365) ](https://compliance.microsoft.com/compliancemanager) | SA-3：系统开发生命周期 | 2020 年 9 月 24 日 |
| [ISO 27001/27002 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.2：更改管理控件 <br> A.14.2：开发和支持过程中的安全性 | 2021 年 4 月 20 日 |
| [ISO 27017 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.2：更改管理控件 <br> A.14.2：开发和支持过程中的安全性 | 2021 年 4 月 20 日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-03：风险管理 <br> CA-18：变更管理 <br> CA-19：更改监视 <br> CA-21：更改测试 <br> CA-38：基线配置 <br> CA-46：安全审查 | 2020 年 12 月 24 日 |
| [SOC 2 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-03：风险管理 <br> CA-18：变更管理 <br> CA-19：更改监视 <br> CA-21：更改测试 <br> CA-38：基线配置 <br> CA-46：安全审查 | 2020 年 12 月 24 日 |

## <a name="resources"></a>资源

- [Microsoft 的安全开发生命周期](https://www.microsoft.com/securityengineering/sdl)
