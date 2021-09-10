---
title: 系统和组织控制 (SOC) 2 类型 2
description: 了解 Microsoft 云服务如何遵守系统和组织控制 (SOC) 2 类型 2 的操作安全标准。
keywords: Microsoft 365, 合规性, 产品/服务
ms.localizationpriority: high
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
ms.openlocfilehash: 92fb47f98e60eb655ee68b38cb747a7d2eb9d2ff
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947732"
---
# <a name="system-and-organization-controls-soc-2-type-2"></a>系统和组织控制 (SOC) 2 类型 2

## <a name="soc-2-type-2-overview"></a>SOC 2 类型 2 概述

服务组织的系统和组织控制 (SOC) 是由美国注册会计师协会 (AICPA) 创建的内部控制报告。 它们旨在检查服务组织提供的服务，以便最终用户可以评估和解决与外包服务相关的风险。

SOC 2 类型 2 证明将根据以下标准执行：

- SSAE 第  18 号证明标准：阐述和准则修订，其中包括 AT-C 第 105 节“*所有证明业务通用的概念*”，以及 AT-C 第 205 节“*检验业务*”（AICPA，专业标准）。
- SOC 2 报告：对服务组织中安全性、可用性、处理完整性、机密性或隐私相关的控制进行的检验（AICPA 指南）。
- TSP 第 100 节，2017 年，有关安全性、可用性、处理完整性、机密性和隐私的信任服务标准（AICPA，2017 信任服务条件）。

此外，Office 365 SOC 2 类型 2 证明报告解决了云安全联盟 (CSA) 云控制矩阵 (CCM) 和德国联邦信息安全办公室 (BSI) 创建的云计算合规性标准目录 (C5:2020) 中所述的要求。

Office 365 SOC 2 证明基于可信誉良好的 CPA 公司进行的严格独立的第三方审核。 在 SOC 2 审核结尾部分，审核员会在 SOC 2 类型 2 报告中提供评价意见，以描述云服务提供商 (CSP) 的系统并评估 CSP 对其所进行的控制的描述是否公平合理。 该结论还会评估 CSP 控制措施是否设计得当、在指定日期是否正常运行，以及在指定时间段内是否有效运行。 Office 365 SOC 2 类型 2 报告与系统安全性、可用性、处理完整性、机密性和隐私相关。

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Microsoft 范围内的云平台和云服务

Azure SOC 2 类型 2 证明报告中显示了范围内的 Microsoft 联机服务：

- Azure（有关详细见解，请参阅 [Microsoft Azure 合规性产品/服务](https://azure.microsoft.com/resources/microsoft-azure-compliance-offerings/)或 Azure SOC 2 类型 2 证明报告）
- Azure DevOps（请另外参阅 Azure DevOps SOC 2 类型 2 证明报告）
- Dynamics 365（有关详细见解，请参阅 Azure SOC 2 类型 2 证明报告）
- Microsoft 365 Defender
- Microsoft Cloud App Security (MCAS)
- Microsoft Defender for Endpoint
- Microsoft Defender for Identity
- Microsoft Forms Pro（不在 Azure 政府范围内）
- Microsoft Graph
- Microsoft Intune
- Microsoft 托管桌面（不在 Azure 政府范围内）
- Microsoft Stream
- Microsoft 威胁专家（不在 Azure 政府范围内）
- 提名门户
- Office 365、Office 365 美国政府版、Office 365 美国政府版 - 高级、Office 365 美国政府国防部版
- Power Apps
- Power Automate
- Power BI
- Power Virtual Agents（不在 Azure 政府范围内）
- 更新合规性（不在 Azure 政府范围内）

## <a name="azure-dynamics-365-and-soc-2"></a>Azure、Dynamics 365 和 SOC 2

有关 Azure、Dynamics 365 和其他联机服务合规性的详细信息，请参阅 [Azure SOC 2 产品/服务](/azure/compliance/offerings/offering-soc-2)。

## <a name="office-365-and-soc-2"></a>Office 365 和 SOC 2

### <a name="office-365-cloud-environments"></a>Office 365 云环境

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 适用性和范围内的服务

使用下表确定 Office 365 服务和订阅的适用性：

| **适用性** | **范围内服务** |
|:------------------|:----------------------|
| **商业** | 合规性管理器、客户密码箱、Delve、Exchange Online Protection、Exchange Online、Forms、Griffin、身份管理器、密码箱 (Torus)、Microsoft Teams、MyAnalytics、Office 365 客户门户、Office 365 微服务（包括但不限于 Kaizala、ObjectStore、Sway、PowerPoint Online 文档服务、查询批注服务、学校数据同步、Siphon、语音、StaffHub、可扩展应用程序计划）、Office Online、Office 服务基础结构、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、Project Online、使用客户密钥进行服务加密、SharePoint Online、Skype for Business |
| **GCC** | Azure Active Directory、合规性管理器、Delve、Exchange Online、Forms、Microsoft Defender for Office 365、Microsoft Teams、MyAnalytics、Office 365 高级合规版附加产品、Office 365 安全与合规中心、Office Online、Office Pro Plus、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、SharePoint Online、Skype for Business、Stream |
| **GCC 高级** | Azure Active Directory、Exchange Online、Forms、Microsoft Defender for Office 365、Microsoft Teams、Office 365 高级合规版附加产品、Office 365 安全与合规中心、Office Online、Office Pro Plus、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、SharePoint Online、Skype for Business |
| **DoD** | Azure Active Directory、Exchange Online、Forms、Microsoft Defender for Office 365、Microsoft Teams、Office 365 高级合规版附加产品、Office 365 安全与合规中心、Office Online、Office Pro Plus、OneDrive for Business、Planner、Power BI、SharePoint Online、Skype for Business |

### <a name="office-365-audit-reports"></a>Office 365 审核报告

- [Office 365 Core - SSAE 18 SOC 2 报告](https://aka.ms/o365SOC-2)
- [Office 365 微服务 T1-SSAE 18 SOC2 类型 I 报告](https://aka.ms/o365-MS-SOC-2-type1)
- [请参阅过渡函和其他审核报告](https://aka.ms/auditreports)

必须要有 Office 365 或 [Office](https://azure.microsoft.com/global-infrastructure/government/request/) 365 美国政府版的现有订阅或免费试用帐户，才能根据需要下载 SOC 1 和 SOC 2 证明报告和任何过渡函。

### <a name="frequently-asked-questions"></a>常见问题解答

**Office 365 SOC 报告多久发布一次？**

Office 365 和其他联机服务的 SOC 报告基于 12 个月的滚动时段（审核期），新报告每半年发布一次（期限为 3 月 31 日和 9 月 30 日）。 *过渡函* 每季度发布一次，以涵盖前面的 3 个月。 例如，1 月的过渡函涵盖 10 月 1 日到 12 月 31 日，4 月的过渡函涵盖 1 月 1 日到 3 月 31 日，7 月的过渡函涵盖 4 月 1 日到 6 月 30 日，10 月的过渡函涵盖 7 月 1 日到 9 月 30 日。

**在哪里可以获取 Office 365 SOC 审核文档（包括过渡函）？**

有关审核文档的链接，请参阅审核报告部分。 必须要有 Office 365 或 [Office](https://azure.microsoft.com/global-infrastructure/government/request/) 365 美国政府版的现有订阅或免费试用帐户才能登录。 然后，可以下载审核证书、评估报告和其他适用文档，以帮助你满足自己的法规要求。

**在哪里可以找到对云安全联盟 CCM 控制实施的评估？**

Office 365 SOC 2 类型 2 审核基于美国注册会计师学会 (AICPA) 的信任服务原则和标准（包括安全性、可用性、机密性、隐私和处理完整性）以及云安全联盟 (CSA) 云控制矩阵 (CCM) 中的标准。 目标是满足 AICPA 标准和 CCM 中规定的要求。 根据 CSA STAR 证明的要求，Office 365 SOC 2 类型 2 审核纳入了 CCM 控制评估。 有关详细信息，请参阅 Office 365 SOC 2 类型 2 证明报告。

**在哪里可以查看针对已记录的异常的管理响应？**

管理响应位于 SOC 证明报告的末尾。 请在文档中搜索“管理响应”。

**在哪里可以查看用户实体责任？**

用户实体责任位于 SOC 证明报告的末尾。 请在文档中搜索“用户实体责任”。

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>使用 Microsoft 合规性管理器评估风险

[Microsoft 合规性管理器](/microsoft-365/compliance/compliance-manager)是 [Microsoft 365 合规中心](/microsoft-365/compliance/microsoft-365-compliance-center)中的一项预览功能，旨在帮助你了解组织的合规情况并采取措施帮助降低风险。 合规性管理器提供了一个高级模板，用于对此法规建立评估。 在合规性管理器的“**评估模板**”页面中找到模板。 了解如何[在合规性管理器中建立评估](/microsoft-365/compliance/compliance-manager-assessments)。

### <a name="resources"></a>资源

- [服务信任门户审核报告](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3)
- [适用于服务组织的 AICPA SOC](https://www.aicpa.org/interestareas/frc/assuranceadvisoryservices/socforserviceorganizations.html)
- [SSAE 第 18 号证明标准：阐明和准则修订（AICPA 专业标准）](https://www.aicpa.org/Research/Standards/AuditAttest/DownloadableDocuments/SSAE_No_18.pdf)
- [SOC 2 报告：对服务组织中安全性、可用性、处理完整性、机密性或隐私相关的控制进行的检验（AICPA 指南）](https://future.aicpa.org/cpe-learning/publication/soc-2-reporting-on-an-examination-of-controls-at-a-service-organization-relevant-to-security-availability-processing-integrity-confidentiality-or-privacy-OPL)（可供购买）
- [TSP 第 100 节（AICPA，2017 年信任服务标准）](https://www.aicpa.org/content/dam/aicpa/interestareas/frc/assuranceadvisoryservices/downloadabledocuments/trust-services-criteria.pdf)
