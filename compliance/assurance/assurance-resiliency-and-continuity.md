---
title: 弹性和连续性
description: 了解 Microsoft 365 中的复原和连续性
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
hideEdit: true
ms.openlocfilehash: 9f63630ac0e9c7a1b68d65c738e88b55f351a3ef
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496896"
---
# <a name="resiliency-and-continuity-overview"></a>弹性和连续性概述

## <a name="how-does-microsoft-ensure-business-continuity-in-the-case-of-a-disaster-or-other-threat-to-service-availability"></a>如果发生灾难或其他服务可用性威胁，Microsoft 如何确保业务连续性？

Microsoft 的企业业务连续性管理 (EBCM) 团队负责监视 Microsoft 服务和云产品/服务的业务连续性管理和灾难恢复活动。 来自 Microsoft 业务部门（如 Microsoft 365）的代表与 EBCM 团队进行协调，以制定业务连续性计划并验证是否符合业务连续性要求。

BCM (BCM) 是业务连续性管理的核心是 BCM 生命周期。 此三阶段过程旨在适应各种 Microsoft 业务模型实现。 它从评估 **阶段** 开始，以确定业务连续性计划应包括的关键流程和目标。 评估阶段还需要业务影响分析 (BIA) 。 规划 **阶段** 侧重于制定和实施复原和恢复策略，并记录在正式的业务连续性计划中。 最后， **功能验证** 测试业务连续性计划及其实现，以验证有效性并确定潜在改进。

Microsoft 365 的业务连续性策略利用硬件、网络和数据中心冗余。 数据中心之间的数据复制在出现灾难性事件时提供了高可用性和可靠性。 它还提高了对意外事件的复原能力，如隔离硬件故障或数据损坏。

## <a name="how-does-microsoft-test-business-continuity-and-disaster-recovery-plans"></a>Microsoft 如何测试业务连续性和灾难恢复计划？

Microsoft 的企业业务连续性管理 (EBCM) 策略规定，必须每年测试、更新和审阅所有 Microsoft 业务连续性和灾难恢复计划。 Microsoft 365 服务至少每年根据 EBCM 策略测试其业务连续性计划。 创建并审阅操作报告以验证、测试结果并通知计划更新以响应在测试过程中发现的任何问题。

为了针对各种潜在事件验证恢复和恢复策略，EBCM 计划定义了影响人员、位置和技术的多个类别的测试方案。 每个服务所需的验证级别都基于服务的关键程度，而更关键的服务获得更加严格的验证。 每个 Microsoft 365 服务团队都根据 EBCM 准则测试其业务连续性计划，以衡量计划的有效性和服务团队执行计划的准备情况。

根据 EBCM 准则，业务连续性计划和功能验证的每年评审必须在上一次审阅的 12 个月内进行。 功能验证必须包括对支持文档（如 BIA）的审阅，以确保其保持准确。 Microsoft 通过季度报告为客户提供精选 Microsoft 365 服务的功能验证结果。

## <a name="how-does-microsoft-365-ensure-system-capacity-meets-demand"></a>Microsoft 365 如何确保系统容量满足需求？

容量规划可帮助服务团队分配支持 Microsoft 365 服务可用性所需的资源。 作为 Microsoft EBCM 计划的一部分，需要定期进行容量规划。 服务团队在季度评审期间以及需要额外容量评审的紧急情况期间检查容量数据。

容量规划的原始数据由每个服务团队维护，其中包括系统处理、内存和硬件容量等指标。 计划审阅使用系统当前容量的模型，并针对紧急情况下的计划需求进行测试。 如果模型指示容量存在差异，则建议的系统容量更改将提交给服务团队领导进行审阅。 在服务团队工程师实施之前，批准的更改会合并到新模型中。

## <a name="how-does-microsoft-365-maintain-service-availability-during-routine-system-failures"></a>Microsoft 365 如何在常规系统故障期间维护服务可用性？

Microsoft 365 通过冗余体系结构、数据复制和自动完整性检查实现服务恢复。 冗余体系结构涉及在地理位置上和物理上独立的硬件上部署服务的多个实例，为 Microsoft 365 服务提供更高的容错能力。 数据复制可确保不同容错区域中始终存在客户数据的多个副本，从而允许在客户损坏、丢失甚至意外删除时恢复关键客户数据。 自动完整性检查通过自动还原受多种物理或逻辑损坏影响的数据来增加数据可用性。

## <a name="related-external-regulations--certifications"></a>认证的相关&法规

Microsoft 的在线服务会定期进行审核，以遵守外部法规和认证。 有关与复原和连续性相关的控件的验证，请参阅下表。

| **外部审核** | **Section** | **最新报告日期** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365) ](https://compliance.microsoft.com/compliancemanager) | CP-2：应变计划 <br> CP-3：应变培训 <br> CP-4：应变计划测试 <br> CP-6：备用存储站点 <br> CP-7：备用处理站点 <br> CP-9：信息系统备份 <br> CP-10：信息系统恢复和重新建立 | 2020 年 9 月 24 日 |
| [OFFICE 365 (ISO 27001/27002) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.17.1：信息安全连续性 <br> A.17.2：冗余 | 2020 年 2 月 22 日 |
| [OFFICE 365 (ISO 22301) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=13951eb3-6339-4629-b80d-dd0d43812fe7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=2bb29cc0-53e7-4a53-a9de-871316e1b80c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 所有控件 | 2019 年 3 月 18 日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-49：备份策略 <br> CA-50：业务连续性 <br> CA-51：数据复制 | 2020 年 12 月 24 日 |
| [SOC 2 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-49：备份策略 <br> CA-50：业务连续性 <br> CA-51：数据复制 | 2020 年 12 月 24 日 |
| [OFFICE 365 (SOC 3) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-09：EXO 电子邮件还原 | 2020 年 12 月 24 日 |

## <a name="resources"></a>资源

- [Microsoft 企业业务连续性管理计划白皮书](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=64f922a6-d624-40dd-a8ae-6f996b5186f3&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f) 
- [Microsoft Cloud EBCM and Disaster Recovery Plan Validation Report： FY21 Q1 and Q2](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=b4181ab3-b03d-4a62-b396-4bfd1c98ddb0&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)

## <a name="legal-disclaimer"></a>法律免责声明

- [企业业务连续性法律免责声明](assurance-ebcm-legal-disclaimer.md)