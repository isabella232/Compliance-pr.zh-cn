---
title: Microsoft 安全事件管理：事后活动
description: 本文概述了 Microsoft 联机服务中的安全事件管理后期事件活动过程。
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
ms.openlocfilehash: 820c912dc55d5cc98cedc38676b5039591cf5baa
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/09/2021
ms.locfileid: "58946995"
---
# <a name="microsoft-security-incident-management-post-incident-activity"></a>Microsoft 安全事件管理：事后活动

## <a name="postmortem"></a>Postmortem

某些安全事件（尤其是影响客户或导致数据泄露的事件）会接受完整的事件事后分析。 安全响应团队与参与安全事件响应的各方一起执行详细的事后调查，以：

- 记录导致事件的事件序列。
- 创建事件的技术摘要，该证据支持该证据包括泄露事件所涉及的 (如果已知) 。 此摘要将包括响应的执行方式和其他关键要点。
- 确定安全事件响应过程中发现的技术缺陷、过程失败、手动错误、流程缺陷和通信故障和/或任何以前未知的攻击途径。

事后分析将在 Microsoft 在线服务工程开发周期中设置新的优先级，直接影响 Microsoft 在线服务改进、运营流程和文档。

## <a name="documentation"></a>文档

事后分析过程中的所有关键技术成果均以 Bug 或开发更改请求的形式捕获在报告和服务投资或修复中。 这些发现将跟进相应的工程团队。 对于进程失败和跨组织问题，问题记录在安全响应团队的数据库中，并跟进相应的组以解决这些问题。

## <a name="process-improvement"></a>流程改进

响应 Microsoft 联机服务中的安全事件涉及与分布在 Microsoft 内不同组织的多个组，甚至是可能适当的外部组织（如执法机构）进行协调。 我们知道，评估每个安全事件后的响应至关重要，既满足又完整。 对于任何已确定的改进或更改，安全响应团队会与相应的团队和利益干系人共同评估建议，并在适当的时候将它们纳入标准操作过程。 在安全事件响应或事后活动期间发现的所有必需更改、Bug 或服务改进都记录并跟踪在内部 Microsoft 工程数据库中。 所有潜在的 Bug 或功能都分配给相应的所有者。 Microsoft 安全响应团队会检查所有条目，直到问题得到解决。

## <a name="related-articles"></a>相关文章

- [Microsoft 安全事件管理](assurance-security-incident-management.md)
- [Microsoft 安全事件管理：准备](assurance-sim-preparation.md)
- [Microsoft 安全事件管理：检测和分析](assurance-sim-detection-analysis.md)
- [Microsoft 安全事件管理：包含、隔离和恢复](assurance-sim-containment-eradication-recovery.md)
- [如何记录安全事件支持票证](/azure/security/fundamentals/event-support-ticket)
- [GDPR 规定的 Azure 和 Dynamics 365 泄露通知](/compliance/regulatory/gdpr-breach-azure-dynamics)
