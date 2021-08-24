---
title: '美国国防部 (DOD) 影响级别 2 (IL2) '
description: 了解 Microsoft 如何满足美国国防部 (DoD) 级别 2 (IL2) 标准。
keywords: Microsoft 365, 合规性, 产品/服务
ms.localizationpriority: medium
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection:
- M365-security-compliance
- MS-Compliance
hideEdit: true
titleSuffix: Microsoft Compliance
ms.openlocfilehash: c57183a53c563fffa2bb3eb1cedb2fca23db26f4
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2021
ms.locfileid: "58482445"
---
# <a name="department-of-defense-dod-impact-level-2-il2"></a>美国国防部 (DOD) 影响级别 2 (IL2) 

## <a name="dod-il2-overview"></a>DoD IL2 概述

国防信息系统局 (DISA) 是美国国防部 (DoD) 的一个机构，负责开发和维护 DoD 云计算安全要求指南 [ (SRG) ](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html)。 SRG 定义 DoD 用于评估云服务提供商 (CSP) 的安全状况的基准安全要求，以支持授权 DoD 临时授权 (PA) 的决定，该授权允许云解决方案提供商托管 DoD 任务。 它合并、取代并撤销之前发布的 DoD 云安全模型 (CSM) 并映射到 DoD 风险管理框架 (RMF) 。

DISA 指导 DoD 机构和部门规划和授权 CSP 的使用。 它还评估 CSP 产品/服务是否符合 SRG，SRG 是一个授权流程，CSP 可在其中提供概述其是否符合 DoD 标准的文档。 它在适当时 (DoD 临时授权) PA，因此 DoD 机构和支持组织可以使用云服务，而无需自行完成完全审批过程，从而节省时间和精力。

[2014 年 12](https://www.esi.mil/contentview.aspx?id=585)月 15日有关购买和使用商业云计算服务的更新指南的 DoD CIO 备忘录指出，"FedRAMP 将充当所有 DoD 云服务的最低安全基线"。 SRG 在所有信息影响级别使用 FedRAMP 中等基线 (IL) ，并在某些情况下考虑高基线。

[SRG Section 5.1.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5SECURITYREQUIREMENTS) *DoD use of FedRAMP Security Controls* 指出，IL2 信息可能托管在一个 CSP 中，该 CSP 中最少具有 FedRAMP 中等 PA 和 DoD 级别 2 PA，但需遵守第 5.6.2 节中列出的人员安全要求。 但是，此方法不会减少云解决方案提供商满足任务所有者要求的其他安全和集成要求。 根据 [SRG 5.2.2.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5.2LegalConsiderations) *IL2* 位置和分离要求，FedRAMP 中等 PA 充分涵盖了 DoD IL2 PA，因此不会为 IL2 PA 额外评估这些要求。

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Microsoft 范围内的云平台和云服务

- Azure
- Dynamics 365
- Microsoft Cloud App Security
- Microsoft Defender for Endpoint
- Microsoft Graph
- Microsoft Intune
- Microsoft Stream
- Office 365美国政府，Office 365美国政府 - 高
- Power Apps
- Power Automate
- Power BI

## <a name="azure-dynamics-365-and-dod-il2"></a>Azure、Dynamics 365 和 DoD IL2

有关 Azure、Dynamics 365 和其他联机服务合规性的信息，请参阅 [Azure DoD IL2 产品](/azure/compliance/offerings/offering-dod-il2)/

## <a name="office-365-and-dod-il2"></a>Office 365 和 DoD IL2

### <a name="office-365-cloud-environments"></a>Office 365 云环境

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 适用性和范围内的服务

使用下表确定 Office 365 服务和订阅的适用性：

| **适用性** | **范围内服务** |
|:------------------|:----------------------|
| **GCC** | 活动源服务、必应 服务、Delve、Exchange Online Protection、Exchange Online、智能服务、Microsoft Teams、Office 365 客户门户、Office Online、Office 服务基础结构、Office 使用情况报告、OneDrive for Business、人员卡片、SharePoint Online、Skype for Business、Windows Ink |
| **GCC 高级** | 活动源服务、必应 服务、Delve、Exchange Online Protection、Exchange Online、智能服务、Microsoft Teams、Office 365 客户门户、Office Online、Office 服务基础结构、Office 使用情况报告、OneDrive for Business、人员卡片、SharePoint Online、Skype for Business、Windows Ink |

### <a name="resources"></a>资源

- [Microsoft 政府解决方案](https://www.microsoft.com/enterprise/government)
- [DoD 云计算安全要求指南](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html)
- [FedRAMP 文档](https://www.fedramp.gov/documents/)
- [适用于信息系统和组织的 NIST SP 800-37](https://csrc.nist.gov/publications/detail/sp/800-37/rev-2/final) *风险管理框架：Life-Cycle和隐私的系统管理方法*
- 适用于信息系统和组织的安全和隐私 *控制* [NIST SP 800-53](https://csrc.nist.gov/Projects/risk-management/sp800-53-controls/release-search#!/800-53)
- [DoD Instruction 8510.01](https://www.esd.whs.mil/Portals/54/Documents/DD/issuances/dodi/851001p.pdf) *DoD Risk Management Framework (RMF) for DoD Information Technology (IT)*
