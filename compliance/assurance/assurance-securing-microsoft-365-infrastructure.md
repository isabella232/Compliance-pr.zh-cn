---
title: 保护 Microsoft 365 基础结构
description: 了解 Microsoft 如何保护Microsoft 365基础结构。
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
ms.openlocfilehash: 6c20c62feb1ff3ab23eeb97d5ad11abb5ad85a07
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947007"
---
# <a name="securing-the-microsoft-365-infrastructure"></a>保护 Microsoft 365 基础结构

Microsoft 365是世界各地最大的企业和客户云服务之一，在客户群、产品和功能方面继续快速增长。 客户不仅Microsoft 365世界一流的生产力解决方案，还帮助保护他们的最敏感信息免受不断变化的网络威胁形势的影响。 确保客户数据安全并保持客户信任是 Microsoft 的首要任务。

如果安全性是一种后天安全，则不可能保护这种规模和复杂性的系统，只有在初始设计过程中集成了安全性时，它才有效。 它需要强大的威胁检测系统，同时提供来自自动化系统和技能熟练工程师的提示响应。 持续评估和验证这些系统对于确保安全配置保持不变以及识别以前未知的漏洞至关重要。

## <a name="core-security-principles"></a>核心安全原则

七个安全原则为保护 Microsoft 365 服务免受威胁、检测和响应任何威胁，以及根据这些评估的结果持续评估安全状况和改进服务的框架奠定了基础。 

- **数据隐私**：客户拥有自己的数据，而 Microsoft 是保管人。 Microsoft 365服务旨在无需工程师访问客户数据即可运行，除非客户明确请求和批准。
- **假设泄露**：将处理人员和服务，就好像存在泄露的可能性一样。
- **最小特权**：对资源的访问和权限仅限于执行所需任务所需的内容。
- **泄露边界**：一个边界中的标识和基础结构独立于其他边界中的资源。 泄露一个边界不应导致另一个边界的泄露。
- **服务结构集成安全性**：安全优先级和要求内置于新特性和功能设计中，确保强大的安全状况随每个服务而扩展。
- **自动和** 自动：Microsoft 侧重于开发可智能和自动强制执行服务安全的持久型产品和体系结构，同时使 Microsoft 工程师能够安全地大规模管理对安全威胁的响应。
- **自适应安全性**：Microsoft 的管理功能适应机器学习模型、日常渗透测试和自动评估，并增强了这些功能。

## <a name="protection"></a>Protection

### <a name="access-control"></a>访问控制

默认情况下，负责开发和维护服务Microsoft 365人员对服务基础结构 (ZSA) 零长期访问权。 虽然 Microsoft 努力只雇用最佳工程师，并且需要严格的背景调查，但 Microsoft 不会假定他们在运营服务中默认受信任。 此外，当批准工程师进行特权访问时，他们只能获得有限期限的访问权限，以仅执行服务基础结构的特定范围所需的操作。 Microsoft 将这些策略称为实时 (JIT) 和 Just-Enough-Access (JEA) 通过称为密码箱的系统实现。

为了获取提升的权限，Microsoft 工程师提交特定任务请求并指定执行该任务的时间框架。 一旦获得批准，密码箱将生成一个专用 JIT 帐户，该帐户只能执行请求的任务。 操作通常采用自动工作流的形式，可安全地执行所需的任何故障排除或恢复。 在极少数情况下，当需要直接访问基础结构时，需要严格监视 Privileged Access Workstations (PAW) 要求。

未授权用户和遭到入侵的帐户在任何组织中都有可能存在，我们的访问控制系统旨在防范这些威胁。

有关访问控制详细信息，请参阅标识 [和访问管理概述](assurance-identity-and-access-management.md)。

### <a name="encryption"></a>加密

访问控制在保护服务Microsoft 365至关重要，但加密在整个数据生命周期内用于进一步保护 Microsoft 客户的机密性和隐私。

客户端计算机、Microsoft 365服务器和非 Microsoft 365 之间传输的数据使用 TLS 1.2 进行加密。 我们定期查看使用中的密码和协议，添加改进的协议（如果可用）并根据需要删除较弱的协议。

Microsoft 服务器上处于其余状态的客户内容使用 BitLocker 在卷级别加密。 此外，还可使用由 Microsoft 或客户管理的密钥应用应用程序级加密。 只有在通过 JIT 和 JEA 过程获得授权和批准后，才能访问 Microsoft 管理的密钥。

有关加密中加密Microsoft 365，请参阅[加密和密钥管理概述](assurance-encryption.md)。

### <a name="network-isolation"></a>网络隔离

根据最小特权原则，Microsoft 365服务基础结构的不同部分之间的通信限制为仅操作所需的内容。 默认情况下，所有网络流量都被拒绝，只允许显式定义的通信。 此限制在整个基础结构中建立了泄露边界。 Teams添加新网络路径以将新功能添加到其服务中之前，必须对请求进行评估和批准，然后才能打开它。

有关网络隔离中网络隔离Microsoft 365，请参阅Microsoft 365[隔离控件](/microsoft-365/enterprise/microsoft-365-isolation-controls)。

## <a name="detection--response"></a>检测&响应

### <a name="security-monitoring"></a>安全监视

只有在使用基于云的自动化解决方案生成高度准确的警报后，Microsoft 才能大规模进行安全监视。 从整个核心基础结构中收集的每个服务和遥测数据的审核日志将发送到专用的集中式近实时处理和警报解决方案。

如果可能，使用自动触发的操作修正检测到的威胁。 当自动化解决方案失败或无法解决问题时，呼叫中的 Microsoft 工程师将立即采取措施来缓解威胁。

有关安全监视中安全监视Microsoft 365，请参阅[安全监视概述](assurance-security-monitoring.md)。

## <a name="assessment"></a>评估

### <a name="automated-assessments"></a>自动评估

无论系统是如何设计的，安全状况都会因有意和无意的配置随着时间的推移而降级。 自动化工具会不断Microsoft 365查找未修补和错误配置服务的系统。 此评估通常称为 PATCHINGC (修补、防病毒、漏洞和) 。

我们的体系结构也经常经过验证，识别未使用的开放端口和具有长期管理访问权限的帐户等实例。 与预定义的所需状态偏离的任何服务都会自动恢复对齐。

有关安全监视中安全监视Microsoft 365，请参阅[漏洞管理概述](assurance-vulnerability-management.md)。

### <a name="attack-simulation-and-penetration-testing"></a>攻击模拟和渗透测试

Microsoft 365头等要的是防止攻击。 Microsoft 365一个专门的安全专家团队，他们不断进行模拟攻击，以识别以前未知的漏洞，并提供丰富的持续数据流，以改进安全监视功能。 这些模拟攻击采用频繁自动小型攻击和专家驱动的深入探究的形式。 从这些活动中，Microsoft 评估检测、响应和收回攻击者的能力。

有关安全监视中安全监视Microsoft 365，请参阅攻击[模拟Microsoft 365。](assurance-monitoring-and-testing.md)

## <a name="resources"></a>资源

[幕后：保护支持 Microsoft 365 服务的基础结构](https://download.microsoft.com/download/c/4/5/c45b197e-f0d9-4f40-bd5f-ed8fc7d0cd8c/M365DCSecurityIntro_Whitepaper.pdf)
