---
title: Microsoft 安全事件管理
description: 本文概述了 Microsoft 联机服务中的安全事件管理过程。
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
search.appverid:
- MET150
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: cb9d27f02ec53c98e2f00d3106f8e4be8798d78f
ms.sourcegitcommit: 9766d656d0e270f478437bd39c0546ad2e4d846f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/27/2021
ms.locfileid: "58678581"
---
# <a name="microsoft-security-incident-management"></a>Microsoft 安全事件管理

Microsoft 努力持续为 Microsoft 客户提供高度安全的企业级服务，但安全事件是一种必须全面且快速管理的真实现实。 本文档概述了 Microsoft 如何使用尝试和真实的方法和技术来处理安全事件，以最大限度地减少其潜在影响。 安全事件是指非法访问存储在 Microsoft 设备或 Microsoft 设施中的客户数据，或未经授权访问此类设备或设施，这些设备或设施可能会导致客户数据丢失、泄露或更改。 Microsoft 在响应安全事件时的目标就是保护客户数据和 Microsoft 的在线服务。

Microsoft 联机服务安全团队和各种服务团队共同协作，并采用相同方法处理安全事件：

- 准备
- 检测和分析
- 包含、抑制和恢复
- 事件后活动

## <a name="microsoft-approach-to-security-incident-management"></a>Microsoft 安全事件管理方法

Microsoft 管理安全事件的方法符合美国国家标准和技术协会 [ (NIST) ](https://www.nist.gov/) 特殊出版物 (SP) 800-61。 Microsoft 有几个专门的团队协同工作，以预防、监视、检测和响应安全事件。

|**团队/区域**|**说明**|
|:------------|:--------------|
| Microsoft 安全响应中心 | 识别、监视、解决和响应安全事件和 Microsoft 软件安全漏洞。 |
| 网络防御操作中心 | 网络防御操作中心是一个物理位置，将整个公司的安全响应团队和专家汇集在一起，以帮助实时保护、检测和响应威胁。 |
| 公司、外部和法律事务 | 为可疑的安全事件提供法律和监管建议。 |
| Microsoft 数据中心安全团队 | 专注于常见安全工程投资的各种服务的团队，用于保护、检测和响应服务体系结构风险和威胁。 |
| Microsoft 安全响应团队 | 独立的 Azure、Dynamics 365 和 Microsoft 365安全团队，与服务团队合作以构建适当的安全事件管理流程并推动任何安全事件响应。 |
| Microsoft 管理、风险和合规性 (GRC) 团队 | 提供有关法规要求、合规性和隐私的指南。 |
| 服务团队 | Azure、Dynamics 365 Microsoft 365团队，负责每项服务的安全相关策略和决策。 |
| Azure 运营经理 | 监督调查和解决与 Azure 相关的安全和隐私事件。 |
| Microsoft 威胁智能中心 (MSTIC)  | 提供针对 Microsoft 基础结构和资产的数字安全威胁的当前技术状态，帮助 Microsoft 内的合作伙伴团队确定缓解和防护工作行动计划的优先级，并采用近实时事件监视/检测来增强保护。 |
| 客户体验沟通团队 | 工程团队负责有关安全和服务事件的所有客户通信。 单独的团队专用于 Azure、Dynamics 365 和 Microsoft 365。 |

## <a name="response-management-process"></a>响应管理过程

Microsoft 联机服务安全团队和服务团队协同工作，并采用相同的方法处理安全事件，这基于 NIST 800-61 响应管理阶段：

- **准备**：是指能够响应的组织准备工作，包括工具、流程、能力和准备情况。
- **检测&** 分析：是指检测生产环境中的安全事件并分析所有事件以确认安全事件的真实性的活动。
- **包含、抑制、** 恢复：是指根据在上一阶段中完成的分析，为包含安全事件而采取的适当必需操作。 在此阶段，可能还需要进行更多分析，以从安全事件完全恢复。
- **事后活动**：是指在恢复安全事件后执行的事后分析。 将检查在过程中执行的操作，以确定是否需要在准备或检测和分析阶段进行任何更改。

![安全事件管理阶段。](../media/assurance-sim-phases.png)

## <a name="federated-security-response-model"></a>联合安全响应模型

Microsoft 在线服务由核心 Microsoft 产品组成，包括 Azure、Dynamics 365 和 Microsoft 365。 每个服务由具有其自己的安全运营流程的单独团队运营。 Microsoft 的其他团队（如 MSTIC）也参与 Microsoft 联机服务的各个安全方面。 由于许多团队致力于跨所有各种服务（包括 Microsoft 联机服务）进行安全操作管理，因此 Microsoft 实施了联合安全响应模型。

此表显示了各种 Microsoft 联机服务安全运营团队和 Microsoft 服务团队之间的操作边界：

|**活动**|**Microsoft 安全团队操作**|**Microsoft 服务团队操作**|
|:-----------|:-----------------------------------------|:----------------------------------------|
| 检测和分析 | - 检测要求 <br> - 安全监视和分析 <br> - IOC (扫描) 泄露指示器 <br> - 泄露搜寻 <br> - 24x7 呼叫和事件响应领导 | - 检测要求 <br> - 监视基础结构部署 <br> - 服务分析和见解 <br> - 事件和警报会审 <br> - 24x7 服务工程呼叫  |
| 包含、抑制、恢复 | - 事件响应主管 <br> - 取证调查 <br> - 安全专长和咨询 <br> - 恢复指南 | - 安全事件所有者 <br> - 服务见解和专业知识 <br> - 执行包含、消除和恢复 |
| 事件后活动 | - 事后分析主管 <br> - 数据收集和存档 <br> - 经验与错误请求 <br> - 事件报告 | - 服务器端事件分析 <br> - 确定后续活动优先级 <br> - 实施安全投资 <br> - 服务安全准备情况 |

## <a name="related-articles"></a>相关文章

- [Microsoft 安全事件管理：准备](assurance-sim-preparation.md)
- [Microsoft 安全事件管理：检测和分析](assurance-sim-detection-analysis.md)
- [Microsoft 安全事件管理：包含、隔离和恢复](assurance-sim-containment-eradication-recovery.md)
- [Microsoft 安全事件管理：事后活动](assurance-sim-post-incident-activity.md)
