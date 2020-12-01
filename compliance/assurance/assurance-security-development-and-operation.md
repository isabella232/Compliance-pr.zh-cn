---
title: 安全开发和操作概述
description: 了解 Microsoft 365 中的安全性开发和操作
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
ms.openlocfilehash: 7c6752b84470eebbdb6ad78c212361156dea957b
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/30/2020
ms.locfileid: "49506244"
---
# <a name="security-development-and-operations-overview"></a>安全开发和操作概述

## <a name="how-does-microsoft-implement-secure-development-practices"></a>Microsoft 如何实现安全开发做法？

Microsoft 的安全开发生命周期 (SDL) 是一个侧重于开发和运营安全软件的安全保证过程。 SDL 为 Microsoft 的开发人员和工程师提供了详细、可衡量的安全要求，以减少产品和服务中漏洞的数量和严重性。 所有 Microsoft 软件开发团队必须遵守 SDL 要求，并且我们不断更新 SDL，以反映出变化的威胁前景、行业最佳做法和法规遵从性标准。

## <a name="how-does-microsofts-sdl-improve-application-security"></a>Microsoft 的 SDL 如何提高应用程序安全性？

Microsoft 的 SDL 过程可在开发的五个阶段进行思考：要求、设计、实现、验证和发布。 它首先定义具有安全的软件要求。 为此，我们会询问有关应用程序必须完成的操作的安全相关问题。 应用程序是否需要收集敏感数据？ 应用程序是否将执行敏感或重要的任务？ 应用程序是否需要接受来自不受信任的源的输入？

确定了相关的安全要求后，我们将设计软件，以包含符合这些要求的安全功能。 我们的开发人员在代码中实施 SDL 和设计要求，我们通过手动代码评审、自动化安全工具和渗透测试来进行验证。 最后，在发布代码之前，新的功能和内容更改会进行最终安全和隐私检查以确保满足所有要求。

## <a name="how-does-microsoft-test-source-code-for-common-vulnerabilities"></a>Microsoft 如何测试常见漏洞的源代码？

为了支持我们的开发人员在代码开发过程中和发布后实现安全要求，Microsoft 提供了一套安全开发工具，以自动检查源代码中的安全缺陷和漏洞。 Microsoft 定义并发布供开发人员使用的已批准工具的列表，如编译器和开发环境，以及在 Microsoft 生成管道中自动执行的内置安全检查。 我们的开发人员使用已批准工具的最新版本来充分利用新的安全功能。

在将代码签入发布分支之前，SDL 需要由单独的审阅者手动进行代码审阅。 代码审阅者会检查编码错误，并验证代码更改是否符合 SDL 和设计要求，通过功能和安全测试，以及是否可靠地执行。 它们还检查关联的文档、预加载和依赖项，以确保代码更改正确记录，并且不会导致意外的副作用。 如果审阅者发现代码评审过程中出现问题，他们可以请求提交者使用建议的更改和其他测试重新提交代码。 代码审阅者还可能决定完全阻止未满足要求的代码签入。 一旦认为该代码符合审阅者的要求，审阅者就会提供批准，这是代码可继续下一个部署阶段之前所必需的。

除了安全开发工具和手动代码审查之外，Microsoft 还使用自动安全工具强制实施 SDL 的要求。 其中许多工具都内置于提交管道中，并在将其签入和编译新版本时自动分析代码中的安全漏洞。 示例包括针对常见安全漏洞的静态代码分析和分析嵌入的机密代码的凭据扫描程序。 必须先修复自动安全工具发现的问题，然后新的生成才能通过安全评审并批准发布。

## <a name="how-does-microsoft-manage-open-source-software"></a>Microsoft 如何管理开放源代码软件？

Microsoft 采用了用于管理开放源代码安全性的高级别策略，它利用了旨在实现以下目的的工具和工作流：

- 了解产品和服务中使用的开放源代码组件。
- 跟踪使用这些组件的位置和方式。
- 确定这些组件是否有任何漏洞。
- 在发现影响这些组件的漏洞时进行正确的响应。

Microsoft 工程团队负责维护产品或服务中包含的所有开放源代码软件的安全性。 为实现这一规模，Microsoft 已通过 CG 为工程系统构建了基本功能，这将自动执行开放源代码检测、法律要求工作流和针对易受攻击组件的警报。 自动 CG 工具扫描 Microsoft for open source 组件和相关的安全漏洞或法律义务的版本。 已发现的组件已注册并提交到相应的团队进行商业和安全审查。 这些审查旨在评估与开放源代码组件相关的任何法律义务或安全漏洞，并在批准部署组件前解决这些问题。

## <a name="related-external-regulations--certifications"></a>& 认证的相关外部法规

将定期审核 Microsoft 的在线服务，以遵守外部法规和认证。 请参阅下表，以验证与安全开发和操作相关的控件。

| **外部审核** | **Section** | **最新报告日期** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365) ](https://compliance.microsoft.com/compliancemanager) | SA-3：系统开发生命周期 | 2020年9月24日 |
| [ISO 27001/27002 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 12.1.2：更改管理控件 <br> 14.2：开发和支持过程中的安全性 | 2020 年 2 月 22 日 |
| [ISO 27017 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 12.1.2：更改管理控件 <br> 14.2：开发和支持过程中的安全性 | 2020 年 2 月 22 日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-03：风险管理 <br> CA-18：更改管理 <br> CA-19：更改监控 <br> CA-21：更改测试 <br> CA-38：基准配置 <br> CA-46：安全审核 | 2019 年 9 月 30 日 |
| [SOC 2 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-03：风险管理 <br> CA-18：更改管理 <br> CA-19：更改监控 <br> CA-21：更改测试 <br> CA-38：基准配置 <br> CA-46：安全审核 | 2019 年 9 月 30 日 |

## <a name="resources"></a>资源

- [Microsoft 安全开发生命周期](https://www.microsoft.com/securityengineering/sdl)
