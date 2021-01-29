---
title: Microsoft 365 安全事件管理：检测和分析
description: 本文概述了 Microsoft 365 中的安全事件管理检测和分析过程。
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
- MS-Compliance
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 1fbdca0c0b08c793732ba31414bedd943d4dc115
ms.sourcegitcommit: d67e4d4fdc664f1da450c8ef2f6732e19bdd403a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/28/2021
ms.locfileid: "50037577"
---
# <a name="microsoft-365-security-incident-management-detection-and-analysis"></a>Microsoft 365 安全事件管理：检测和分析

为了检测恶意活动，Microsoft 365 集中记录安全事件和其他数据，并执行各种分析技术以查找异常或可疑活动。 日志文件从 Microsoft 365 服务器和基础结构设备收集，并存储在中央合并数据库中。

Microsoft 采用基于风险的方法检测恶意活动。 我们使用事件数据和威胁智能来定义检测并设置其优先级。

在检测和分析阶段，使用一个拥有丰富经验、熟练且技能丰富的人员的团队是成功的关键支柱之一。 Microsoft 365 采用多个服务团队，这些团队包括具有堆栈中所有组件（包括网络、路由器、防火墙、负载平衡器、操作系统和应用程序）的能力的员工。

Microsoft 365 中的安全检测机制还包括由不同来源启动的通知和警报。 Microsoft 365 安全响应团队是安全事件升级过程的重要协调者。 此团队接收所有上报，并负责分析和确认安全事件的有效性。

检测的主要支柱之一是通知：

- 每个服务团队都负责根据 Microsoft 365 安全团队的要求记录服务内的任何操作或事件。 由不同服务团队创建的所有日志都由 SIEM (安全) 和检测规则处理。 这些规则根据 Microsoft 365 安全团队的建议，根据从以前的安全事件中获得的信息进行改进，以确定是否有可疑或恶意活动。
- 如果客户确定正在处理安全事件，他们可能会向 Microsoft 开启支持案例，该案例分配给 Microsoft 365 客户体验 (CxP) 通信团队，并转变为向所有相应团队上报。

Microsoft 365 服务团队还使用通过安全监视和日志记录在趋势分析中获得的信息来检测 Microsoft 365 信息系统中可能指示攻击或安全事件的异常。 Microsoft 365 服务器将生产环境中这些日志的输出聚合到集中日志记录服务器中。 通过此集中日志记录服务器，检查日志以发现整个生产环境的趋势。 集中服务器中聚合的数据安全地传输到日志记录服务中，以用于高级查询、仪表板生成和检测异常和恶意活动。 该服务还使用机器学习来检测日志输出的异常。

在升级阶段，根据安全事件的性质，Microsoft 365 安全响应团队可能会与来自 Microsoft 各团队的一个或多个主题专家联系：

- 联机服务安全与合规团队
- Microsoft 威胁智能中心 (MSTIC) 
- Microsoft 安全响应中心 (MSRC) 
- CELA (、外部和法律) 
- Azure 安全性
- Microsoft 365 工程和其他项目。

在向 Microsoft 365 安全响应团队进行任何上报之前，服务团队负责根据定义的条件确定和设置安全事件的严重性级别，例如：

- 隐私
- 影响
- 范围
- 受影响的租户数
- 地区
- 服务
- 事件的详细信息
- 特定客户行业或市场法规。

事件优先顺序是使用不同因素确定的，包括但不限于事件的功能影响、事件的信息影响以及事件的可恢复性。

在收到有关安全事件的上报后，Microsoft 365 安全团队将组织一个由 Microsoft 365 安全响应团队、服务团队和 Microsoft 365 事件通信团队的成员组成的虚拟团队 (v-team) 。 此 v 团队的活动更复杂的部分是确认安全事件并消除任何误报。 由准备阶段确定的指标提供的信息的准确性至关重要。 通过按矢量攻击类别分析此信息，v 团队可以确定安全事件是否合法。

在调查开始时，Office 安全事件响应团队根据我们的案例管理策略记录有关事件的所有信息。 随着案例的进展，我们将跟踪正在进行的操作，并遵循证据处理标准，以收集、保留和保护整个事件生命周期中的此数据。

这些操作的示例包括：

- 摘要，简要说明事件及其潜在影响
- 事件的严重性和优先级，通过评估潜在影响派生
- 标识了导致检测事件的所有指标的列表
- 任何相关事件的列表
- v-team 执行的所有操作的列表
- 收集的任何证据，还将保留这些证据，用于事后分析和将来的取证调查
- 建议的下一步和操作

在安全事件确认后，Microsoft 365 安全响应团队和相应服务团队的主要目标是控制攻击，保护服务 () 受到攻击，并避免更大的全球影响。 同时，相应的工程团队努力确定根本原因并准备第一个恢复计划。

下一阶段，Microsoft 365 安全响应团队将 (受) 事件影响的客户的标识（如果有）。 影响范围可能需要一些时间才能根据区域、数据中心、服务、服务器场、服务器等确定。 受影响的客户列表由服务团队和 Microsoft 365 CxP 通信团队编译，然后由他们处理合同和合规性义务中的客户通知流程。

## <a name="related-articles"></a>相关文章

- [Microsoft 365 安全事件管理](assurance-security-incident-management.md)
- [Microsoft 365 安全事件管理准备](assurance-sim-preparation.md)
- [Microsoft 365 安全事件管理包含、限制和恢复](assurance-sim-containment-eradication-recovery.md)
- [Microsoft 365 安全事件管理后期活动](assurance-sim-post-incident-activity.md)
