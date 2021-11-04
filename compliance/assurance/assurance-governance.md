---
title: 治理概述
description: 了解 Microsoft 联机服务中的合规性治理。
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
ms.openlocfilehash: 7b4e8bef0c5aca8749ed963c7fac2674d5cbf015
ms.sourcegitcommit: 444a58b28f8611323e16d28b4c63a0f68eaaafa6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/04/2021
ms.locfileid: "60780088"
---
# <a name="governance-overview"></a>治理概述

## <a name="how-does-microsoft-provide-effective-security-governance-across-the-enterprise"></a>Microsoft 如何在整个企业内提供有效的安全治理？

Microsoft 知道必须在企业内持续实施有效的安全策略，以保护 Microsoft 信息系统和客户。 安全策略还必须考虑到业务功能和信息系统中的变化才能做到普遍适用。 为满足这些要求，Microsoft 实施了全面的安全治理计划，作为 Microsoft 策略框架的一部分。 安全治理属于 Microsoft 安全策略 (MSP) 的一部分。

MSP 组织 Microsoft 的安全策略、标准和要求，以便可以在所有 Microsoft 工程组和业务部门中实现这些策略、标准和要求。 单个业务部门负责 Microsoft 安全策略的具体实现。 例如，Microsoft 365信息安全策略Microsoft 365相关的安全控制框架Microsoft 365实现。 Azure 和 Dynamics 365 在标准操作程序 (SOP) Azure Control Framework 中记录其安全实现。 这些安全实现与 MSP 的目标一致。

Microsoft 的安全治理计划由各种法规和合规性框架告知，并与这些框架保持一致。 安全要求在不断演变，以考虑新技术、法规和合规性要求以及安全威胁。 由于这些更改，Microsoft 会定期更新我们的安全策略和支持文档，以保护 Microsoft 系统和客户、履行我们的承诺并保持客户的信任。

## <a name="how-do-microsoft-online-services-implement-the-microsoft-security-policy-msp"></a>Microsoft 在线服务如何实施 Microsoft 安全策略 (MSP) ？

Microsoft 365将安全实现记录在Microsoft 365安全策略中。 此策略遵循 Microsoft 安全策略并治理 Microsoft 365 信息系统，包括收集、处理、维护、使用、共享、传播和处置数据过程中涉及的所有 Microsoft 365 环境和所有资源。 同样，Azure 和 Dynamics 365 使用 Microsoft 安全策略来管理其信息系统。

信息系统包括受 Microsoft 365 Information Security Policy (for Microsoft 365) 和 Microsoft Security Policy (for Azure 和 Dynamics 365) 控制的组件：

- 基础结构：Azure、Dynamics 365 和 Microsoft 365 系统的物理和硬件 (、设备和) 
- 软件：Azure、Dynamics 365 和 Microsoft 365 系统的程序和 (、应用程序和实用程序) 
- 人员：涉及 Azure、Dynamics 365 和 Microsoft 365 系统的运营和使用的人员 (开发人员、操作员、用户和经理) 
- 过程：Azure、Dynamics 365 和 Microsoft 365系统的操作所涉及的编程和手动过程
- 数据：Azure、Dynamics 365 和 Microsoft 365 系统生成、收集和处理的信息 (流、文件、数据库和表) 

Microsoft 365 信息安全策略由 Microsoft 365 控制框架补充。 此Microsoft 365控制框架详细介绍了所有 Microsoft 365 服务和信息系统组件的最低安全要求。 它还引用每个控件背后的法律和公司要求。 该框架包含控制活动名称、说明以及指南，以确保服务团队高效实施控制。 Microsoft 365控件框架跟踪内部和外部报告的控件实现。 同样，Azure 控件框架中的 Azure 和 Dynamics 365 记录控制实现。

## <a name="how-do-online-services-limit-and-track-exceptions-to-established-policies-and-procedures"></a>联机服务如何限制和跟踪已制定的策略和程序的例外？

控制框架的所有例外情况都必须具有合法的业务理由，并经每个联机服务团队中的相应治理实体批准。 根据异常的范围及其代表的潜在风险，可能需要获得公司副总裁或更高层对异常的批准。 在跟踪工具中对例外进行管理，并检查和批准它们是否具有持续的相关性。

## <a name="how-do-online-services-keep-security-and-compliance-requirements-updated"></a>联机服务如何保持安全性和合规性要求更新？

GRC 的每个在线服务团队的治理、风险和 (团队) 持续维护控制框架。 多个方案可能需要 GRC 团队更新控制框架，包括相关法规或法律的更改、新出现的威胁、渗透测试结果、安全事件、审核反馈和新合规性要求。 当需要更改框架时，信任团队将确定负责批准和实施更改的关键利益干系人，以确保更改可行且不会导致联机服务出现意外问题。 在 GRC 团队和相关利益干系人就更改要求达成一致后，负责实施更改集目标完成日期的工作负荷将努力在各自的服务中实施更改。 在达到实现目标后，信任团队会使用新的或更新的控件更新控制框架。

## <a name="related-external-regulations--certifications"></a>认证相关的&法规

Microsoft 的在线服务会定期进行审核，以遵守外部法规和认证。 有关与治理相关的控制措施的验证，请参阅下表。

### <a name="azure-and-dynamics-365"></a>Azure 和 Dynamics 365

| **外部审核** | **Section** | **最新报告日期** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.18.1：遵守法律和合同要求 <br> A.18.2：信息安全审查 | 2020 年 12 月 2 日 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.18.1：遵守法律和合同要求 <br> A.18.2：信息安全审查 | 2020 年 12 月 2 日 |
| [SOC 1](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fservicetrust.microsoft.com%2FViewPage%2FMSComplianceGuideV3%3Fcommand%3DDownload%26downloadType%3DDocument%26downloadId%3D66043614-5628-4e26-83be-057eb3bb026c%26tab%3D7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb%26docTab%3D7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%252F_SSAE_16_Reports&data=04%7C01%7Csostah%40microsoft.com%7Cb9591cf4bd214d42c4f408d93cd83520%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637607721602686385%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=B2xjy%2Bx70e8vI%2FKC2BCa4AyJt0OSMzAGuhwllHF4NGM%3D&reserved=0) | IS-1：Microsoft 安全策略 <br> IS-2：Microsoft 安全策略审查 <br> IS-3：安全角色和责任 | 2021 年 3 月 31 日 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | C5-1：标准操作过程 <br> IS-1：Microsoft 安全策略 <br> IS-2：Microsoft 安全策略审查 <br> IS-3：安全角色和责任 <br> SOC2-14：保密性和保密协议 <br> SOC2-18：法规、法规和合同要求 <br> SOC2-19：跨职能合规性计划 <br> SOC2-20：ISMS 程序 | 2021 年 3 月 31 日 |

### <a name="office-365"></a>Office 365

| **外部审核** | **Section** | **最新报告日期** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | CA-2：安全评估 <br> PL-2：系统安全计划 | 2020 年 9 月 24 日 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=08ce227f-d1d9-4c4c-b255-4f2e4ec8f941&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.18.1：遵守法律和合同要求 <br> A.18.2：信息安全审查 | 2021 年 4 月 20 日 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-11：策略框架更新 <br> CA-17：Microsoft 安全策略 <br> CA-25：控制框架更新 | 2020 年 12 月 24 日 |

## <a name="resources"></a>资源

- [Microsoft 安全策略](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=bc35aefb-ec41-4a0e-bfc7-10aa5169ca88&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)
- [Microsoft 安全计划策略](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=4b010ac5-2861-4d20-b8ff-db77875b43a9&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_FAQ_and_White_Papers)