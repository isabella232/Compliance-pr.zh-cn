---
title: 恢复能力和连续性
description: 了解 Microsoft 365 中的恢复能力和连续性
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
ms.openlocfilehash: 6763e363938c422ac419fe9e76f9170912627dd5
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/30/2020
ms.locfileid: "49505904"
---
# <a name="resiliency-and-continuity-overview"></a>恢复能力和连续性概述

## <a name="how-does-microsoft-ensure-business-continuity-in-the-case-of-a-disaster-or-other-threat-to-service-availability"></a>Microsoft 如何在灾难或其他威胁的情况下确保业务连续性，以实现服务可用性？

Microsoft 的企业业务连续性管理 (EBCM) 团队监督跨 Microsoft 服务和云产品的业务连续性管理和灾难恢复活动。 Microsoft 业务部门的代表（如 Microsoft 365）与 EBCM 团队合作以制定业务连续性计划，并验证是否符合业务连续性要求。

在我们的业务连续性管理 (BCM) 方法的核心是 BCM 生命周期。 这三个阶段的过程旨在适应可适应性性，以便可以在 Microsoft 之间通过多种业务模型实施。 它从 **评估** 阶段开始，以确定应包括在业务连续性计划中的关键流程和目标。 评估阶段还需要 (BIA) 的业务影响分析。 **规划** 阶段侧重于开发和实施恢复策略，并将其记录在正式的业务连续性计划中。 最后， **功能验证** 测试业务连续性计划及其实现以验证有效性并确定可能的改进。

Microsoft 365 的业务连续性策略利用硬件、网络和数据中心冗余。 数据中心之间的数据复制在发生灾难性事件时提供高可用性和可靠性。 它还可提高对常见事件（如独立硬件故障或数据损坏）的恢复能力。

## <a name="how-does-microsoft-test-business-continuity-and-disaster-recovery-plans"></a>Microsoft 如何测试业务连续性和灾难恢复计划？

Microsoft 的企业业务连续性管理 (EBCM) policy stipulates，必须在每年的基础上测试、更新和审查所有 Microsoft 业务连续性和灾难恢复计划。 Microsoft 365 服务每个 EBCM 策略至少每年测试一次其业务连续性计划。 在创建操作报告并进行检查以验证、测试结果并通知计划更新，以响应在测试过程中发现的任何问题。

为了针对多种潜在事件验证复原和恢复策略，EBCM 计划定义了影响人员、位置和技术的多个测试方案类别。 每个服务所需的验证级别都基于服务的关键程度，并且更关键的服务会收到更严格的验证。 每个 Microsoft 365 服务团队根据 EBCM 准则测试其业务连续性计划，以衡量计划的有效性和服务团队执行计划的准备工作。

根据 EBCM 准则，业务连续性计划和功能验证的年度审查必须在最后一次评审的12个月内进行。 功能验证必须包括对支持文档（如 BIA）的审查，以确保它保持准确。 Microsoft 通过季度报告为我们的客户提供了选择 Microsoft 365 服务的功能验证结果。

## <a name="how-does-microsoft-365-ensure-system-capacity-meets-demand"></a>Microsoft 365 如何确保系统容量满足需求？

容量规划有助于服务小组分配支持 Microsoft 365 服务可用性所需的资源。 在 Microsoft 的 EBCM 计划中，需要进行常规容量规划。 服务团队在季度检查期间以及在紧急情况下查看容量数据，以保证额外的容量。

容量规划的原始数据由每个服务团队维护，包括系统处理、内存和硬件容量等指标。 计划的审阅使用系统当前容量的模型，并针对紧急情况下的预计需求对其进行测试。 如果模型指示空间不足，则会将对系统容量所做的更改提交到服务团队领导，以供审查。 在服务团队工程师实施之前，已批准的更改合并到新的模型中。

## <a name="how-does-microsoft-365-maintain-service-availability-during-routine-system-failures"></a>在例行系统发生故障期间，Microsoft 365 如何维护服务可用性？

Microsoft 365 通过冗余体系结构、数据复制和自动完整性检查来实现服务恢复能力。 冗余体系结构涉及在地理上和物理上单独的硬件上部署服务的多个实例，从而为 Microsoft 365 服务提供了更高的容错能力。 数据复制可确保不同的故障区域中始终存在客户数据的多个副本，从而允许在损坏、丢失甚至意外删除客户的情况下恢复关键客户数据。 通过自动还原受多种物理或逻辑损坏影响的数据，自动完整性检查可提高数据可用性。

## <a name="related-external-regulations--certifications"></a>& 认证的相关外部法规

将定期审核 Microsoft 的在线服务，以遵守外部法规和认证。 请参阅下表，以验证与恢复能力和连续性相关的控制措施。

| **外部审核** | **Section** | **最新报告日期** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365) ](https://compliance.microsoft.com/compliancemanager) | CP-2：应变计划 <br> CP-3：应急培训 <br> CP-4：应变计划测试 <br> CP-6：备用存储站点 <br> CP-7：备用处理网站 <br> CP-9：信息系统备份 <br> CP-10：信息系统恢复和 reconstitution | 2020年9月24日 |
| [ISO 27001/27002 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 17.1：信息安全连续性 <br> 17.2：冗余 | 2020 年 2 月 22 日 |
| [ISO 22301 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=13951eb3-6339-4629-b80d-dd0d43812fe7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=2bb29cc0-53e7-4a53-a9de-871316e1b80c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 所有控件 | 2019 年 3 月 18 日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-49：备份策略 <br> CA-50：业务连续性 <br> CA-51：数据复制 | 2019 年 9 月 30 日 |
| [SOC 2 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-49：备份策略 <br> CA-50：业务连续性 <br> CA-51：数据复制 | 2019 年 9 月 30 日 |
| [SOC 3 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=9df8b99b-96ce-49a9-bff4-268031dcc9a6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CUEC-09： EXO 电子邮件还原 | 2019 年 9 月 30 日 |

## <a name="resources"></a>资源

- [Microsoft 企业业务连续性管理计划白皮书](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=64f922a6-d624-40dd-a8ae-6f996b5186f3&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f) 
- [Microsoft 云 EBCM 和灾难恢复计划验证报告： FY20 第4季度](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=5437a1d9-5883-468b-aee0-8c8a8e4ef56a&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)

## <a name="legal-disclaimer"></a>法律免责声明

- [企业业务连续性法律免责声明](assurance-ebcm-legal-disclaimer.md)