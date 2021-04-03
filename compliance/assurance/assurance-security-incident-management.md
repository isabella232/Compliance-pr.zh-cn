---
title: Microsoft 365 安全事件管理
description: 本文概述了 Microsoft 365 中的安全事件管理过程。
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance0
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: a61a4406c4951c4d4584831cf58030545955fd35
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496781"
---
# <a name="microsoft-365-security-incident-management"></a>Microsoft 365 安全事件管理

Microsoft 努力为 Microsoft 365 客户提供高度安全的企业级服务。 本文档介绍 Microsoft 如何处理 Microsoft 365 中的安全事件。 安全事件是指非法访问存储在 Microsoft 设备或 Microsoft 设施中的客户数据，或未经授权访问此类设备或设施，这些设备或设施可能会导致客户数据丢失、泄露或更改。 Microsoft 在响应安全事件时的目标就是保护客户数据和 Microsoft 365 服务。

Microsoft 365 安全团队和各种服务团队共同协作，采取相同的方法处理安全事件：

- 准备
- 检测和分析
- 包含
- 百年
- 恢复
- 事件后活动

## <a name="microsoft-approach-to-security-incident-management"></a>Microsoft 安全事件管理方法

Microsoft 管理安全事件的方法符合美国国家标准和技术协会 [NIST () ](https://www.nist.gov/) Special Publication (SP) 800-61。 Microsoft 有几个专门的团队协同工作，以预防、监视、检测和响应安全事件。

|**团队/区域**|**描述**|
|:------------|:--------------|
| Microsoft 安全响应中心 | 识别、监视、解决和响应安全事件和 Microsoft 软件安全漏洞。 |
| 网络防御操作中心 | 网络防御操作中心是一个物理位置，将整个公司的安全响应团队和专家汇集在一起，以帮助实时保护、检测和响应威胁。 |
| 公司、外部和法律事务 | 为可疑的安全事件提供法律和监管建议。 |
| Microsoft 365 安全响应团队 | 与 Microsoft 365 服务团队合作，以构建适当的安全事件管理流程并推动任何安全事件响应。 |
| Office 365 信任 | 提供有关法规要求、合规性和隐私的指南。 |
| Microsoft 365 数据中心安全团队 | 专注于常见安全工程投资的各种服务的团队，用于保护、检测和响应 Microsoft 365 服务体系结构风险和威胁。 |
| 服务团队 | 为 Microsoft 365 服务（如 Exchange、SharePoint 和 Microsoft Teams）工程团队，负责每项服务的安全相关策略和决策。 |
| Microsoft 威胁智能中心 (MSTIC)  | 提供针对 Microsoft 基础结构和资产的数字安全威胁的当前技术状态，帮助 Microsoft 内的合作伙伴团队确定缓解和防护工作行动计划的优先级，并采用近实时事件监视/检测来增强保护。 |
| 合作伙伴安全团队 | Microsoft 内提供关键服务或负责 Microsoft 365 中关键依赖项的其他合作伙伴安全团队，例如 Azure 安全响应团队、标识安全响应和 Microsoft 公司安全响应团队。 |
| Microsoft 365 客户体验通信 | 工程团队负责有关安全和服务事件的所有客户通信。 |

## <a name="response-management-process"></a>响应管理过程

Microsoft 365 安全团队和服务团队协同工作，并采用相同方法处理安全事件，这基于 NIST 800-61 响应管理阶段：

- **准备**：是指能够响应的组织准备工作，包括工具、流程、能力和准备情况。
- **检测&** 分析：是指检测生产环境中的安全事件并分析所有事件以确认安全事件的真实性的活动。
- **包含、抑制、** 恢复：是指根据上一阶段中完成的分析，为包含安全事件而采取的适当必需操作。 在此阶段，可能还需要进行更多分析，以从安全事件完全恢复。
- **事后活动**：是指在恢复安全事件后执行的事后分析。 将检查在过程中执行的操作，以确定是否需要在准备或检测和分析阶段进行任何更改。

## <a name="federated-security-response-model"></a>联合安全响应模型

Microsoft 365 服务包括核心 Microsoft online services (Exchange、SharePoint 和 Microsoft Teams 等 ) 以及其他 Microsoft 云服务，如 Azure Active Directory、Microsoft Commerce Platform 和 MSTIC。 这些服务由具有其自己的安全运营流程的单独团队运营。 Microsoft 的其他团队还参与 Microsoft 365 的各个安全方面。 由于许多团队致力于跨 Microsoft 365 的所有各种服务进行安全操作管理，因此 Microsoft 实施了联合安全响应模型。

此表显示了各种 Microsoft 365 安全运营团队和 Microsoft 365 服务团队之间的操作边界：

|**活动**|**Microsoft 365 安全团队操作**|**Microsoft 365 服务团队操作**|
|:-----------|:-----------------------------------------|:----------------------------------------|
| 检测和分析 | - 检测要求 <br> - 安全监视和分析 <br> - IOC 扫描 (泄露) 指示器 <br> - 泄露搜寻 <br> - 24x7 呼叫和事件响应领导 | - 检测要求 <br> - 监视基础结构部署 <br> - 服务分析和见解 <br> - 事件和警报会审 <br> - 24x7 服务工程呼叫  |
| 包含、抑制、恢复 | - 事件响应主管 <br> - 取证调查 <br> - 安全专长和咨询 <br> - 恢复指南 | - 安全事件所有者 <br> - 服务见解和专业知识 <br> - 执行包含、消除和恢复 |
| 事件后活动 | - 事后分析主管 <br> - 数据收集和存档 <br> - 经验与错误请求 <br> - 事件报告 | - 服务器端事件分析 <br> - 确定后续活动优先级 <br> - 实施安全投资 <br> - 服务安全准备情况 |

## <a name="related-articles"></a>相关文章

- [Microsoft 365 安全事件管理准备](assurance-sim-preparation.md)
- [Microsoft 365 安全事件管理检测和分析](assurance-sim-detection-analysis.md)
- [Microsoft 365 安全事件管理抑制、消除和恢复](assurance-sim-containment-eradication-recovery.md)
- [Microsoft 365 安全事件管理事后活动](assurance-sim-post-incident-activity.md)
