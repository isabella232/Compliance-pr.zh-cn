---
title: 弹性和连续性
description: 了解企业中的复原和Microsoft 365
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
ms.openlocfilehash: d05263c70b0e4210562b8a4ec7a8ec9c6600f9e5
ms.sourcegitcommit: 444a58b28f8611323e16d28b4c63a0f68eaaafa6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/04/2021
ms.locfileid: "60779988"
---
# <a name="resiliency-and-continuity-overview"></a>弹性和连续性概述

## <a name="how-does-microsoft-ensure-business-continuity-if-a-disaster-or-other-threat-to-service-availability-occurs"></a>如果发生灾难或其他服务可用性威胁，Microsoft 如何确保业务连续性？

Microsoft 的 Enterprise 业务连续性管理 (EBCM) 团队负责监管跨 Microsoft 服务 和云产品/服务的业务连续性管理和灾难恢复活动。 来自 Microsoft 业务部门的代表与 EBCM 团队合作，以制定业务连续性计划并验证是否符合业务连续性要求。

BCM (生命周期) 业务连续性管理是 BCM 方法的核心。 此三阶段过程旨在适应各种 Microsoft 业务模型实现。 它从评估 **阶段** 开始，以确定业务连续性计划应包括的关键流程和目标。 评估阶段还需要业务影响分析 (BIA) 。 规划 **阶段** 侧重于制定和实施复原和恢复策略，并记录在官方业务连续性计划中。 最后， **功能验证** 测试业务连续性计划及其实现，以验证有效性并确定潜在的改进。

Microsoft 在线服务业务连续性策略使用硬件、网络和数据中心冗余。 数据中心之间的数据复制在灾难性事件期间提供高可用性和可靠性。 它还提高了对意外事件的复原能力，如隔离硬件故障或数据损坏。

## <a name="how-does-microsoft-test-business-continuity-and-disaster-recovery-plans"></a>Microsoft 如何测试业务连续性和灾难恢复计划？

Microsoft 的 Enterprise 业务连续性管理 (EBCM) 策略规定必须每年测试、更新和审阅所有 Microsoft 业务连续性和灾难恢复计划。 Microsoft 在线服务至少每年根据 EBCM 策略测试其业务连续性计划。 创建并审阅操作报告以验证、测试结果并通知计划更新以响应在测试过程中发现的任何问题。

为了针对各种潜在事件验证复原能力和恢复策略，EBCM 计划定义了影响人员、位置和技术的多种类别的测试方案。 每个服务所需的验证级别取决于服务的关键程度，更关键的服务会受到更严格的验证。 每个 Microsoft 联机服务团队都根据 EBCM 准则测试其业务连续性计划，以衡量计划的有效性和服务团队执行计划的准备情况。

根据 EBCM 准则，业务连续性计划和功能验证的每年评审必须在上次审阅的 12 个月内进行。 功能验证必须包括对支持文档（如 BIA）的审阅，以确保其保持准确。 Microsoft 通过季度报告为客户提供精选 Microsoft 在线服务的功能验证结果。

## <a name="how-do-microsoft-online-services-ensure-system-capacity-meets-demand"></a>Microsoft 联机服务如何确保系统容量满足需求？

容量规划可帮助服务团队分配支持 Microsoft 联机服务可用性所需的资源。 作为 Microsoft EBCM 计划的一部分，需要定期进行容量规划。 服务团队在季度评审期间和紧急情况下查看容量数据，这要求进行更多容量评审。

容量规划的原始数据由每个服务团队维护，其中包括系统处理、内存和硬件容量等指标。 计划评审使用系统当前容量的模型，并根据紧急情况下的预计需求进行测试。 如果模型指示容量存在差距，则系统容量的建议更改将提交给服务团队领导进行评审。 在服务团队工程师实施之前，批准更改将合并到新模型中。

## <a name="how-do-microsoft-online-services-maintain-service-availability-during-routine-system-failures"></a>在常规系统故障期间，Microsoft 联机服务如何维护服务可用性？

Microsoft 在线服务通过冗余体系结构、数据复制和自动完整性检查实现服务恢复。 冗余体系结构涉及在地理位置和物理上独立的硬件上部署服务的多个实例，为 Microsoft 联机服务提供更高的容错能力。 数据复制可确保不同容错区域中始终存在客户数据的多个副本，从而允许在客户损坏、丢失甚至意外删除时恢复关键客户数据。 自动完整性检查通过自动还原受多种物理或逻辑损坏影响的数据来增加数据可用性。

## <a name="related-external-regulations--certifications"></a>认证相关的&法规

Microsoft 的在线服务会定期进行审核，以遵守外部法规和认证。 有关与复原和连续性相关的控件的验证，请参阅下表。

### <a name="azure-and-dynamics-365"></a>Azure 和 Dynamics 365

| **外部审核** | **Section** | **最新报告日期** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.17.1：信息安全连续性 <br> A.17.2：冗余 | 2020 年 12 月 2 日 |
| [ISO 22301](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=6d388547-fc88-46e3-8de2-6bc2edc08b06&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=ee4b611b-bb4d-4056-b189-00da36e88949&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 所有控件 | 2020 年 5 月 13 日 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | BC-1：业务连续性计划 <br> BC-3：业务连续性和灾难恢复过程 <br> BC-4：BCDR 测试 <br> BC-7：数据中心业务连续性计划 <br> BC-8：数据中心业务连续性测试 <br> BC-9：数据中心复原评估 <br> DS-5：备份关键服务组件 <br> DS-6：关键组件的冗余 <br> DS-7：自动复制客户数据 <br> DS-8：备份计划 <br> DS-9：备份还原过程 <br> DS-11：非现场备份 <br> DS-14：自动还原客户服务 | 2021 年 3 月 31 日 |

### <a name="office-365"></a>Office 365

| **外部审核** | **Section** | **最新报告日期** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | CP-2：应变计划 <br> CP-3：应变培训 <br> CP-4：应变计划测试 <br> CP-6：备用存储站点 <br> CP-7：备用处理站点 <br> CP-9：信息系统备份 <br> CP-10：信息系统恢复和重新建立 | 2020 年 9 月 24 日 |
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=08ce227f-d1d9-4c4c-b255-4f2e4ec8f941&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.17.1：信息安全连续性 <br> A.17.2：冗余 | 2021 年 4 月 20 日 |
| [ISO 22301](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=08ce227f-d1d9-4c4c-b255-4f2e4ec8f941&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=2bb29cc0-53e7-4a53-a9de-871316e1b80c&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 所有控件 | 2019 年 3 月 18 日 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-49：备份策略 <br> CA-50：业务连续性 <br> CA-51：数据复制 | 2020 年 12 月 24 日 |
| [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-09：EXO 电子邮件还原 | 2020 年 12 月 24 日 |

## <a name="resources"></a>资源

- [Microsoft Enterprise 业务连续性管理计划白皮书](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=64f922a6-d624-40dd-a8ae-6f996b5186f3&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f)
- [Microsoft 云 EBCM 和灾难恢复计划验证报告：FY22 Q1](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=f47df93a-f6a0-4013-96e6-35b91af90a78&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)

## <a name="legal-disclaimer"></a>法律免责声明

- [企业业务连续性法律免责声明](assurance-ebcm-legal-disclaimer.md)