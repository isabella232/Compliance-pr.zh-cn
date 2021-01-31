---
title: Microsoft 365 安全事件管理：准备
description: 本文概述了 Microsoft 365 中安全事件管理的准备过程。
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
ms.openlocfilehash: b14a9fa236cd71cff7dd02baf04a30c249bc4346
ms.sourcegitcommit: 2973d25e9e0185b84d281f963553a332eac1c1a3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/28/2021
ms.locfileid: "50040335"
---
# <a name="microsoft-365-security-incident-management-preparation"></a>Microsoft 365 安全事件管理：准备

## <a name="training-and-background-checks"></a>培训和背景调查

每一位在 Microsoft 365 工作的员工都接受了适合其职责的安全事件和响应程序方面的培训。 每一位 Microsoft 365 员工都在加入时接受了培训，并且此后每年都接受年度进修培训。 培训旨在使员工对 Microsoft 的安全措施形成基本了解，培训结束时，所有员工可以掌握：

- 安全事件的定义
- 所有员工报告安全事件的责任
- 如何向 Microsoft 365 安全事件响应团队上报潜在安全事件
- Microsoft 365 安全事件响应团队如何响应安全事件
- 有关隐私尤其是客户隐私方面的特别问题
- 查找有关安全性和隐私性的其他信息的位置，以及上报联系人。
- 任何其他相关安全领域（根据需要）

每年，适当的员工会接受安全方面的进修培训。 年度进修培训的重点是：

- 任何针对上一年度标准操作程序的更改
- 所有员工报告安全事件的责任，以及操作方式
- 查找有关安全性和隐私性的其他信息的位置，以及上报联系人。
- 每年可能相关的任何其它安全重点领域

在 Microsoft 365 中工作的每名员工还要接受适当且完整的背景调查，其中包括候选者教育、雇佣状况、犯罪记录以及其他符合美国法规要求的特定信息，如《健康保险流通与责任法案》(HIPPA)、《国际武器贸易条例》(ITAR)、《联邦风险和授权管理计划》(FedRAMP) 等。

在 Microsoft 365 工程部门工作的所有员工均必须接受背景调查。 某些 Microsoft 365 环境和操作人员角色可能还需要接受完整的指纹识别、公民身份要求、政府许可要求和其他更加严格的控制。 此外，一些服务团队和角色可能会根据需要通过专门的安全培训。 最后，安全团队成员本身需要接受直接与安全相关的专门培训，并参与安全直接相关的会议。 此培训因团队和员工需要而异，但包含行业会议、内部 Microsoft 安全会议，以及行业内知名安全培训供应商的外部培训课程等内容。 我们在全年中针对跨 Microsoft 和 Microsoft 365 专门安全社区定期发布专门的安全培训文章。

## <a name="penetration-testing--assessment"></a>渗透测试和评估

Microsoft 与各个行业部门和安全专家合作以了解新的威胁和不断发展的趋势。 Microsoft 会不断评估自己的系统以查找漏洞，并与执行相同工作的各种独立外部专家签署合同。

测试以强化 Microsoft 365 产品服务为目的，可以分为四个常规类别：

1. **自动安全测试：** 根据 Microsoft SDL 实践、开放 Web 应用程序安全项目 (OWASP) 的 10 大风险以及不同行业机构报告的新兴威胁，内部和外部人员定期扫描 Microsoft 365 环境。
2. **漏洞评估：** 与独立第三方测试人员正式合作，定期验证关键逻辑控制是否有效运行，以履行各种监管人员的服务职责。 评估由注册道德安全测试员委员会 (CREST) 认证人员执行，以 OWASP 10 大风险和其他服务适用的威胁为基础。 发现的所有威胁都跟踪至其结束。
3. **持续系统漏洞测试：** Microsoft 执行定期测试，其中，团队尝试使用新兴威胁、混合威胁和/或高级持久威胁来破坏系统，而其他团队则尝试阻止此类攻击尝试。
4. **Microsoft Online Services 联机服务漏洞赏金计划**：此计划实施的策略允许由客户发起有限的针对 Microsoft 365 的漏洞评估。 有关详细信息，请参阅 [Microsoft 联机服务漏洞赏金条款](https://www.microsoft.com/msrc/bounty-terms)。

Microsoft 365 工程团队定期发布各种合规性文档。 其中几个文档可在遵守保密协议的前提下，从 [Microsoft 云服务信任门户](https://aka.ms/STP) 或 [Microsoft 365 合规中心](https://compliance.office.com) 的服务保证区域获取。

>[!NOTE]
>若要详细了解如何访问服务信任门户，请参阅 Office 365 商业版、Azure 和 Dynamics CRM Online 订阅的服务信任门户入门。 需要 Microsoft 365 订阅才能访问 Microsoft 365 合规中心。

## <a name="attack-simulation"></a>攻击模拟

Microsoft 参与持续的攻击模拟练习和我们的安全和响应计划的实时网站渗透测试，目的是改进检测和响应功能。 Microsoft 定期模拟真实攻击、执行持续安全监视，并实施安全事件响应，以验证 Microsoft 365 和 Azure 的安全性。

Microsoft 通过两个核心团队执行假设破坏安全策略：

### <a name="red-teams"></a>红队

Microsoft 365 安全红队是 Microsoft 中的一组全职员工，他们专注于破坏 Microsoft 的基础结构、平台和 Microsoft 自己的租户和应用程序。 他们是专门的黑客（一组道德黑客），对联机服务（但并非客户应用程序或数据）执行定向和持久攻击。 他们为服务事件响应功能提供持续“全谱”验证（如技术控制、纸张策略、人工响应等）。

### <a name="blue-teams"></a>蓝队

Microsoft 365 安全蓝队由一组专门的安全响应人员组成，其成员来自各个安全事件响应、工程和操作团队。 蓝队为独立团队，且与红队分开运营。 蓝队遵循已建立的安全流程，并使用最新工具和技术来检测并响应攻击和渗透尝试。 和真实攻击一样，蓝队不知道红队攻击的时间或方式，也不知道红队会使用哪些方法。 无论是红队攻击还是实际攻击，蓝队的职责都是检测并响应所有安全事件。 因此，蓝队会持续接到电话呼叫，必须和针对任何其他对手一样对红队的攻击做出反应。

Microsoft 员工在 Microsoft 各部门中分别全职加入红队和蓝队，并且跨服务及在其内部展开操作。 所谓 *红队测试*，其方法是针对实时生产基础结构，使用与真实对手相同的技巧、技术和程序在 Microsoft 服务系统和运营中进行测试，而无需预先了解基础结构和平台工程或运营团队。 此方法测试安全检测和响应能力，并帮助以可控方式识别生产漏洞、配置错误、无效假设或其他安全问题。 每次红队攻击之后均在包括服务团队在内的红队和蓝队之间进行完整披露，以识别缺陷、解决发现问题并显著改进攻击响应。

>[!NOTE]
>在红队测试或实时网站渗透练习期间，不会以任何客户数据为目标。 此测试针对 Microsoft 365、Azure 基础结构和平台，以及 Microsoft 自己的租户、应用程序和数据。 Microsoft 365 或 Azure 中托管的客户租户、应用程序和数据按照约定参与规则从未成为测试目标。

### <a name="joint-exercises"></a>共同练习

有时，Microsoft 365 安全蓝队和红队将执行联合操作，其中操作期间每队选定员工的关系更类似于合作伙伴而非对手。 这些练习在团队之间配合良好，通过道德黑客和响应者之间的实时协作来推动产生目标更为明确的结果。 这些“紫队”练习专门针对每个操作高度定制，以最大程度的把握机遇，但是每项操作都基于高带宽信息共享和合作关系来实现目标。

## <a name="related-articles"></a>相关文章

- [Microsoft 365 安全事件管理](assurance-security-incident-management.md)
- [Microsoft 365 安全事件管理检测和分析](assurance-sim-detection-analysis.md)
- [Microsoft 365 安全事件管理抑制、消除和恢复](assurance-sim-containment-eradication-recovery.md)
- [Microsoft 365 安全事件管理事后活动](assurance-sim-post-incident-activity.md)
