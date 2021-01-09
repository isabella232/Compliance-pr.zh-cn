---
title: 安全开发和操作概述
description: 了解 Microsoft 365 中的安全开发和操作
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
ms.openlocfilehash: 916303ff2a65777785c89c6ccae70bea9a0bfda9
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787301"
---
# <a name="security-development-and-operations-overview"></a>安全开发和操作概述

## <a name="how-does-microsoft-implement-secure-development-practices"></a>Microsoft 如何实施安全开发实践？

Microsoft 安全开发生命周期 (SDL) 是一个专注于开发和操作安全软件的安全保证流程。 SDL 为 Microsoft 的开发人员和工程师提供了详细的可衡量安全要求，以减少我们产品和服务中漏洞的数量和严重性。 所有 Microsoft 软件开发团队都必须遵循 SDL 要求，并持续更新 SDL 以反映不断变化的威胁环境、行业最佳做法和合规性法规标准。

## <a name="how-does-microsofts-sdl-improve-application-security"></a>Microsoft 的 SDL 如何提高应用程序安全性？

可以从五个开发阶段考虑 Microsoft 的 SDL 流程：要求、设计、实现、验证和发布。 它首先定义软件要求，并注意安全性。 为此，我们询问有关应用程序必须完成的任务的安全相关问题。 应用程序是否需要收集敏感数据？ 应用程序是否执行敏感任务或重要任务？ 应用程序是否需要接受来自不受信任的源的输入？

确定相关的安全要求后，我们设计软件以包含满足这些要求的安全功能。 我们的开发人员在代码中实现 SDL 和设计要求，我们通过手动代码评审、自动化安全工具和渗透测试来验证这些要求。 最后，在可以发布代码之前，新功能和材料更改将经过最终安全和隐私审查，以确保满足所有要求。

## <a name="how-does-microsoft-test-source-code-for-common-vulnerabilities"></a>Microsoft 如何测试常见漏洞的源代码？

为了支持我们的开发人员在代码开发期间和发布后实现安全要求，Microsoft 提供了一套安全开发工具，用于自动检查源代码的安全缺陷和漏洞。 Microsoft 定义并发布供开发人员使用的已批准工具（如编译器和开发环境）的列表，以及 Microsoft 生成管道中自动执行的内置安全检查。 我们的开发人员使用最新版本的已批准工具来利用新的安全功能。

在将代码签入发布分支之前，SDL 需要由单独的审阅者手动检查代码。 代码审阅者检查编码错误，并验证代码更改是否满足 SDL 和设计要求，通过功能和安全测试，并可靠地执行。 他们还会查看关联的文档、配置和依赖项，以确保正确记录代码更改，并且不会导致意外的副作用。 如果审阅者在代码审阅期间发现问题，他们可要求提交者重新提交包含建议更改和其他测试的代码。 代码审阅者还可以决定完全阻止不符合要求的代码签入。 一旦代码被审阅者视为满意，审阅者将提供审批，这是在代码可以继续下一个部署阶段之前所需的。

除了安全开发工具和手动代码检查之外，Microsoft 还使用自动化安全工具强制执行 SDL 要求。 其中许多工具内置于提交管道中，在签入代码和编译新的内部版本时自动分析代码的安全缺陷。 示例包括常见安全缺陷的静态代码分析，以及分析嵌入密码代码的凭据扫描程序。 必须修复自动安全工具发现的问题，然后新版本才能通过安全审查并获得批准发布。

## <a name="how-does-microsoft-manage-open-source-software"></a>Microsoft 如何管理开放源代码软件？

Microsoft 已采用用于管理开放源代码安全性的高级别策略，该策略利用旨在：

- 了解在产品和服务中使用的开放源代码组件。
- 跟踪这些组件的使用位置和方式。
- 确定这些组件是否具有任何漏洞。
- 发现影响这些组件的漏洞时正确响应。

Microsoft 工程团队负责保护产品或服务中包含的所有开源软件的安全性。 为大规模实现此目的，Microsoft 通过 CG 将基本功能内置到工程系统中，从而自动执行开放源代码检测、法律要求工作流和针对易受攻击的组件发出警报。 自动 CG 工具扫描 Microsoft 内部版本，以发现开放源代码组件以及相关的安全漏洞或法律要求。 已发现的组件将注册并提交给相应的团队进行业务和安全审查。 这些审查旨在评估与开放源代码组件相关的任何法律义务或安全漏洞，并解决这些义务或漏洞，然后再批准部署组件。

## <a name="related-external-regulations--certifications"></a>认证的相关&法规

Microsoft 的在线服务会定期进行审核，以遵守外部法规和认证。 有关与安全开发和操作相关的控制措施的验证，请参阅下表。

| **外部审核** | **Section** | **最新报告日期** |
|:--------------------|:------------|:-----------------------|
| [Office 365 (FedRAMP) ](https://compliance.microsoft.com/compliancemanager) | SA-3：系统开发生命周期 | 2020 年 9 月 24 日 |
| [ISO 27001/27002 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.2：更改管理控件 <br> A.14.2：开发和支持过程中的安全性 | 2020 年 2 月 22 日 |
| [Office 365 (ISO 27017) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.12.1.2：更改管理控件 <br> A.14.2：开发和支持过程中的安全性 | 2020 年 2 月 22 日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-03：风险管理 <br> CA-18：更改管理 <br> CA-19：更改监视 <br> CA-21：更改测试 <br> CA-38：基线配置 <br> CA-46：安全审查 | 2020 年 12 月 24 日 |
| [SOC 2 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-03：风险管理 <br> CA-18：更改管理 <br> CA-19：更改监视 <br> CA-21：更改测试 <br> CA-38：基线配置 <br> CA-46：安全审查 | 2020 年 12 月 24 日 |

## <a name="resources"></a>资源

- [Microsoft 的安全开发生命周期](https://www.microsoft.com/securityengineering/sdl)
