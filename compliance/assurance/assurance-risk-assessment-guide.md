---
title: Microsoft 云风险评估指南
description: 了解 Microsoft 云风险评估指南
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
ms.openlocfilehash: a7b6e345afa49d82f96d9eb9e5c804fc7cbf5ffe
ms.sourcegitcommit: 1f30616328d7deb04e41dcbd44a330ea937fe94f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/26/2021
ms.locfileid: "60584843"
---
# <a name="risk-assessment-guide-for-microsoft-cloud"></a>Microsoft 云风险评估指南

云风险评估的目标是确保迁移到云时考虑的系统和数据不会给组织带来任何新的或无法识别的风险。 重点是确保信息处理的机密性、完整性、可用性和隐私性，并且将识别的风险保持在接受的内部风险阈值以下。

在共同责任模型中，云服务提供商 (CSP) 负责管理云作为 *提供商的安全性和* 合规性。 客户仍负责根据自己的需求和风险承受能力管理和配置云中的安全性和合规性。

![共享责任模型。](../media/assurance-shared-responsibility-model.png)

在本指南中，共享了如何有效评估供应商风险以及如何使用 Microsoft 提供的资源和工具的最佳实践。

## <a name="understand-shared-responsibility-in-the-cloud"></a>了解云中的共同责任

云部署可以分类为基础结构即服务 (IaaS) 、平台即服务 (PaaS) 或软件即服务 (SaaS) 。 根据适用的云服务模型，解决方案的安全控制的责任级别在云解决方案提供商和客户之间转移。 在传统的本地模型中，客户负责整个堆栈。 迁移到云时，所有物理安全职责将转移到云解决方案提供商。 根据组织的云服务模型，其他责任将转移到云解决方案提供商。 但是，在大多数服务模型中，你的组织仍负责用于访问云的设备、网络连接、帐户和标识以及你的数据。 Microsoft 在创建允许客户在整个生命周期内控制其数据的服务方面投入大量资金。

Microsoft 云在超大规模运行，依靠 DevSecOps 和自动化的组合来标准化操作模型。 与传统的内部部署操作模型相比，Microsoft 运营模型改变了处理风险的方式，导致实施不同的（有时不熟悉）控制措施来管理风险。 在执行云风险评估时，请记住，Microsoft 的目标是确保解决所有风险，但不一定实现组织所实施的控制。 Microsoft 可能会通过一组不同的控制措施应对相同的风险，这些风险应反映在云风险评估中。 设计和实施强大的预防性控制措施可以减少检测型和纠正型控制措施所需的大部分工作。

## <a name="adopt-a-framework"></a>采用框架

Microsoft 建议客户将内部风险和控制框架映射到以标准化方式解决云风险的独立框架。 如果你的现有内部风险评估模型无法应对云计算带来的特定挑战，你将从这些广泛采用和标准化的框架中获益。 第二个好处是 Microsoft 在文档和工具中提供针对这些框架的映射，从而加快风险评估。 这些框架的示例包括 ISO [27001 信息安全标准、CIS](/compliance/regulatory/offering-iso-27001)基准和[NIST SP 800-53。](https://csrc.nist.gov/Projects/risk-management/sp800-53-controls/release-search#!/800-53) [](/compliance/regulatory/offering-cis-benchmark) Microsoft 提供任意云解决方案提供商最全面的合规性产品/服务。 有关详细信息，请参阅 [Microsoft 合规性产品/服务](/compliance/regulatory/offering-home)。

使用 [Microsoft 合规性管理器](/microsoft-365/compliance/compliance-manager) 创建您自己的评估，评估对适用于组织的行业和区域法规的合规性。 评估基于评估模板的框架构建，该框架包含必要的控制措施、改进措施以及完成评估的 Microsoft 行动（如果适用）。 对于 Microsoft 操作，提供了详细的实施计划和最近审核结果。 这样，就可以在事实查找、映射和研究 Microsoft 实现特定控件的方式上节省时间。 有关详细信息，请参阅 Microsoft 合规性管理器文章。

## <a name="understand-how-microsoft-operates-to-safeguard-your-data"></a>了解 Microsoft 如何操作来保护你的数据

客户负责管理和配置云中的安全性和合规性，而云解决方案提供商负责管理云的安全性 *和合规性*。 验证 CSP 是否有效履行责任并兑现承诺的一种方式是查看其外部审核报告，如 ISO 和 SOC。 Microsoft 在服务信任门户上向经过身份验证的受众 [提供外部审核报告](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3)。

除了外部审核报告之外，Microsoft 还强烈建议客户利用以下资源来帮助了解 Microsoft 的深入运营方式：

- [按需Learning路径](/learn/roles/auditor)：Microsoft 的学习平台提供数以百计的不同主题的学习路径和模块。 其中， [请了解 Microsoft 如何保护客户数据](/learn/paths/audit-safeguard-customer-data/) ，以了解 Microsoft 的基本安全和隐私做法。

- [Microsoft 合规性服务保证](/compliance/#service-assurance)：有关 Microsoft 实践的文章分为 16 个域，以便于审阅。 每个域包含概述，可捕获 Microsoft 如何管理与每个区域关联的风险。 提供审核表，其中包含指向存储在服务信任门户上的最新报告的链接、相关部分以及 Microsoft 联机服务的审核报告执行日期。 如果可用，则提供演示控制实现的项目的链接，例如第三方漏洞评估和业务连续性计划验证报告。 与审核报告一样，这些项目托管在 STP 上，并且需要进行身份验证来访问。

| **域** |**说明** |
|:---------- |:-------------- |
| [**体系结构**](assurance-architecture.md) | Microsoft 在线服务的设计以及充当其基础的安全原则。 |
| [**Audit logging**](assurance-audit-logging.md) | Microsoft 如何捕获、处理、存储和保护使安全和性能监视成为可能的日志。 |
| [**数据中心安全**](assurance-datacenter-security.md) | Microsoft 如何安全地运营数据中心，提供在全球运营 Microsoft 联机服务的方式。 |
| [**加密和密钥管理**](assurance-encryption.md) | 客户通信以及云中存储和处理的数据的加密保护。 |
| [**治理**](assurance-governance.md) | Microsoft 如何在整个企业内创建、分发、更新和实施安全策略，以满足客户的承诺和合规性要求。 |
| [**人力资源**](assurance-human-resources.md) | 在 Microsoft 中，人员在整个时间进行筛选过程和安全管理。 |
| [**标识和访问管理**](assurance-identity-and-access-management.md) | 保护 Microsoft 在线服务和客户数据，防止未经授权的或恶意访问。 |
| [**事件管理**](assurance-incident-management.md) | Microsoft 用于准备、检测、响应和传达所有安全和隐私事件的过程。 |
| [**网络安全性**](assurance-network-security.md) | Microsoft 如何保护其网络边界免受外部攻击并管理其内部网络以限制其传播。 |
| [**隐私**](assurance-privacy.md) | Microsoft 如何处理和保护客户数据以保留其数据权限。 |
| [**弹性和连续性**](assurance-resiliency-and-continuity.md) | 用于维护服务可用性并确保业务连续性和恢复的过程和技术。 |
| [**风险管理**](assurance-risk-management.md) | 确定、评估和采取的操作，以最大限度地降低整个企业的风险。 |
| [**安全开发和运营**](assurance-security-development-and-operation.md) | Microsoft 如何确保其服务在其整个生命周期内安全设计、运行和管理。 |
| [**安全监视**](assurance-security-monitoring.md) | 日志的中央分析，以检测任何未经授权的或恶意活动并提醒人员。 |
| [**供应商管理**](assurance-supplier-management.md) | Microsoft 如何筛选和管理协助 Microsoft 在线服务的第三方公司。 |
| [**漏洞管理**](assurance-vulnerability-management.md) | Microsoft 用于扫描、检测和解决漏洞和恶意软件的过程。 |

## <a name="resources"></a>资源

- [Microsoft 云中金融机构的风险评估和合规性指南](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=edee9b14-3661-4a16-ba83-c35caf672bd7&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)
- [集中风险：Microsoft 的角度](https://azure.microsoft.com/mediahandler/files/resourcefiles/concentration-risk-perspectives-from-microsoft-/Concentration_Risk_Perspectives_092020.pdf)
- [服务信任门户](https://servicetrust.microsoft.com/)
