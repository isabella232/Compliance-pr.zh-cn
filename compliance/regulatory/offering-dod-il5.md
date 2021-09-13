---
title: '美国国防部 (DOD) 影响级别 5 (IL5) '
description: 了解 Microsoft 如何满足美国国防部 (DOD) 5 级 (IL5) 标准。
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
ms.openlocfilehash: c0c987dc5fbe2bee60508f0fab7dbdb8dce97857
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/12/2021
ms.locfileid: "59158821"
---
# <a name="department-of-defense-dod-impact-level-5-il5"></a>美国国防部 (DOD) 影响级别 5 (IL5) 

## <a name="dod-il5-overview"></a>DoD IL5 概述

国防信息系统局 (DISA) 是美国国防部 (DoD) 的一个机构，负责开发和维护 DoD 云计算安全要求指南 [ (SRG) ](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html)。 SRG 定义 DoD 用于评估云服务提供商 (CSP) 的安全状况的基准安全要求，以支持授权 DoD 临时授权 (PA) 的决定，该授权允许云解决方案提供商托管 DoD 任务。 它合并、取代并撤销以前发布的 DoD 云安全模型 (CSM) 并映射到 DoD 风险管理框架 (RMF) 。

DISA 指导 DoD 机构和部门规划和授权 CSP 的使用。 它还评估 CSP 产品/服务是否符合 SRG，SRG 是一个授权流程，CSP 可在其中提供概述其是否符合 DoD 标准的文档。 它在适当的时候 (DoD 临时授权) PA，因此 DoD 机构和支持组织可以使用云服务，而无需自行完成完全审批过程，从而节省时间和精力。

根据 [SRG 3.2](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#3.2InformationImpactLevels) *信息影响级别，IL5* 信息涵盖：

- 受控未分类 (要求) 比 IL4 提供的保护级别更高的 CUI 服务
    - [CUI 注册表](https://www.archives.gov/cui)提供由行政部保护的特定类别的信息，例如，CUI 类别列表中包括 20[多个类别分组](https://www.archives.gov/cui/registry/category-list)。
    - [NIST SP 800-171](https://csrc.nist.gov/publications/detail/sp/800-171/rev-2/final)保护非联盟系统和组织中的受控未分类信息旨在由联邦机构在与非联邦组织签订的合同或其他协议中使用。

- 国家安全系统 (NSS) 
    - [NIST SP 800-59](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-59.pdf)用于将信息系统标识为 *国家* /系统的指南提供了 NSS 的定义。
    - [CNSSI 1253](https://www.dcsa.mil/portals/91/documents/ctp/nao/CNSSI_No1253.pdf)针对国家安全系统的安全分类和控制选择提供有关联邦机构应应用于对国家安全信息进行分类的安全标准的指南。

[2014 年 12](https://www.esi.mil/contentview.aspx?id=585)月 15日有关购买和使用商业云计算服务的更新指南的 DoD CIO 备忘录指出，"FedRAMP 将充当所有 DoD 云服务的最低安全基线"。 SRG 使用 FedRAMP 中等基线，在 IL (所有信息影响) 并考虑某些高基线。

[SRG Section 5.1.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5SECURITYREQUIREMENTS) *DoD use of FedRAMP Security Controls* 指出，FedRAMP High PA， with DoD FedRAMP+ controls and control enhancements (C/CEs) and requirements in the SRG， are used to assess CSPs to awarding a DoD PA at IL5. 无论使用什么 C/CE 基线作为 FedRAMP High PA 的基础，都需要评估和批准其他注意事项和/或要求，然后才能在 IL5 上授予 DoD PA。 具体而言， [表 2 中的 SRG 第 5.1.2](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5SECURITYREQUIREMENTS)节 *DoD FedRAMP+* 安全控制/增强功能指出，DoD IL5 PA 需要超过 FedRAMP 高基线的 10 个其他 C/CES。

此外，根据 [SRG 第 5.2.2.3](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5.2LegalConsiderations) *IL5* 节的"位置和分离要求"，5 级 PA (除其他要求) 必须满足以下要求：

- DoD 与联邦政府租户/任务之间的虚拟/逻辑分离已足够。 需要租户/任务系统之间的虚拟/逻辑分离。
- 需要与非 DoD/非联邦 (（即公共、本地/州/州政府租户) 分离。
- CSP 将潜在 DoD 和社区信息的访问权限限制为美国公民的云解决方案提供商员工。

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Microsoft 范围内的云平台和云服务

- Azure
- Dynamics 365 客户服务
- Microsoft Defender for Endpoint（曾用名：Microsoft Defender 高级威胁防护）
- Microsoft Graph
- Microsoft Stream
- Office 365 美国政府防御版
- Power Automate（以前称为 Microsoft Flow）
- Power BI

## <a name="azure-dynamics-365-and-dod-il5"></a>Azure、Dynamics 365 和 DoD IL5

有关 Azure、Dynamics 365 和其他在线服务合规性的信息，请参阅 Azure [DoD IL5 产品](/azure/compliance/offerings/offering-dod-il5)/

## <a name="office-365-and-dod-il5"></a>Office 365 和 DoD IL5

### <a name="office-365-cloud-environments"></a>Office 365 云环境

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 适用性和范围内的服务

使用下表确定 Office 365 服务和订阅的适用性：

| **适用性** | **范围内服务** |
|:------------------|:----------------------|
| **DoD** | 活动源服务、必应 服务、Exchange Online、Exchange Online Protection、智能服务、Microsoft Teams、Office 365 客户门户、Office Online、Office 服务基础结构、Office 使用情况报告、OneDrive for Business、人员卡片、SharePoint Online、Skype for Business、Windows Ink |

### <a name="attestation-documents"></a>证明文档

美国政府客户可以通过Office 365包访问请求表单，直接从[FedRAMP 市场](https://marketplace.fedramp.gov/#!/products?sort=productName&productNameSearch=azure)请求获取美国政府防御 FedRAMP 文档。 您必须具有 .gov 或 .更新电子邮件地址，以直接从 FedRAMP 访问 FedRAMP 安全包。

选择 FedRAMP 和 DoD 文档，包括系统安全计划 (SSP) 、连续监控报告、行动计划和里程碑 (POA M) 等，这些文档可供 NDA 下的客户使用，并可从服务信任门户审核报告 \& [- FedRAMP](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3) 报告部分获取待访问授权。 请联系你的 Microsoft 帐户代表寻求帮助。

### <a name="resources"></a>资源

- [Microsoft 政府解决方案](https://www.microsoft.com/enterprise/government)
- [DoD 云计算安全要求指南](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html)
- [FedRAMP 文档](https://www.fedramp.gov/documents/)
- [DoD Instruction 8510.01](https://www.esd.whs.mil/Portals/54/Documents/DD/issuances/dodi/851001p.pdf) *DoD Risk Management Framework (RMF) for DoD Information Technology (IT)*
- [适用于信息系统和组织的 NIST SP 800-37](https://csrc.nist.gov/publications/detail/sp/800-37/rev-2/final)风险管理框架 *：Life-Cycle和隐私的系统管理方法*
- 适用于信息系统和组织的安全和隐私 *控制* [NIST SP 800-53](https://csrc.nist.gov/Projects/risk-management/sp800-53-controls/release-search#!/800-53)
- [NIST SP 800-59](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-59.pdf)关于将信息系统 *识别为国家/系统的指南*
- [CNSSI 1253](https://www.dcsa.mil/portals/91/documents/ctp/nao/CNSSI_No1253.pdf) *安全分类和控制选择（针对国家安全系统）*
- [NIST SP 800-171](https://csrc.nist.gov/publications/detail/sp/800-171/rev-2/final)保护非系统和组织中的受控未分类 *信息*
- 受控的未分类 (CUI) [和](https://www.archives.gov/cui) CUI [类别列表](https://www.archives.gov/cui/registry/category-list)。
