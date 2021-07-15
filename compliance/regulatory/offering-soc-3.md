---
title: 系统和组织控制 (SOC) 3
description: 了解 Microsoft 云服务如何遵守系统和组织控制 (SOC) 3 的操作安全标准。
keywords: Microsoft 365, 合规性, 产品/服务
localization_priority: Priority
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
ms.openlocfilehash: 1d6f6b0a4c9bd3ebbccb90331a8cf17df7ff8928
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/12/2021
ms.locfileid: "53385711"
---
# <a name="system-and-organization-controls-soc-3"></a>系统和组织控制 (SOC) 3

## <a name="soc-3-overview"></a>SOC 3 概述

服务组织的系统和组织控制 (SOC) 是由美国注册会计师协会 (AICPA) 创建的内部控制报告。 它们旨在检查服务组织提供的服务，以便最终用户可以评估和解决与外包服务相关的风险。

*SOC 3 适用于服务组织的 SOC：一般用途的信任服务标准报告* 是面向公众的简短 SOC 2 类型 2 证明报告版本，适用于需要有关安全性、可用性、处理完整性、机密性或隐私相关服务组织控制的保证，但又不需要完整 SOC 2 报告的用户。 由于 SOC 3 报告是一般用途报告，因此可以自由分发。

SOC 3 报告包含服务组织管理层关于控制在基于适用信任服务标准实现承诺方面的有效性的书面声明，以及服务审核员对管理层声明是否公平的意见。

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Microsoft 范围内的云平台和云服务

Microsoft 范围内的服务显示在 Azure [SOC 2 类型 2 证明](offering-soc-2.md)报告中。

- Azure（有关详细见解，请参阅 [Microsoft Azure 合规性产品/服务](https://azure.microsoft.com/resources/microsoft-azure-compliance-offerings/)或 Azure SOC 2 类型 2 证明报告）
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

## <a name="azure-dynamics-365-and-soc-3"></a>Azure、Dynamics 365 和 SOC 3

有关 Azure、Dynamics 365 和其他联机服务合规性的详细信息，请参阅 [Azure SOC 3 产品/服务](/azure/compliance/offerings/offering-soc-3)。

## <a name="office-365-and-soc-3"></a>Office 365 和 SOC 3

### <a name="office-365-cloud-environments"></a>Office 365 云环境

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 适用性和范围内的服务

使用下表确定 Office 365 服务和订阅的适用性：

| **适用性** | **范围内服务** |
|:------------------|:----------------------|
| **Office 365** | 合规性管理器、客户密码箱、Delve、Exchange Online Protection、Exchange Online、Forms、Griffin、身份管理器、密码箱 (Torus)、Microsoft Teams、MyAnalytics、Office 365 客户门户、Office 365 微服务（包括但不限于 Kaizala、ObjectStore、Sway、PowerPoint Online 文档服务、查询批注服务、学校数据同步、Siphon、语音、StaffHub、可扩展应用程序计划）、Office Online、Office 服务基础结构、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、Project Online、使用客户密钥进行服务加密、SharePoint Online、Skype for Business |
| **GCC** | Azure Active Directory、合规性管理器、Delve、Exchange Online、 
、Microsoft Defender for Office 365、Microsoft Teams、MyAnalytics、Office 365 高级合规版附加产品、Office 365 安全与合规中心、Office Online、Office Pro Plus、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、SharePoint Online、Skype for Business、Stream |
| **GCC 高级** | Azure Active Directory、Exchange Online、Flow、Microsoft Defender for Office 365、Microsoft Teams、Office 365 高级合规版附加产品、Office 365 安全与合规中心、Office Online、Office Pro Plus、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、SharePoint Online、Skype for Business |
| **DoD** | Azure Active Directory、Exchange Online、Microsoft Defender for Office 365、Microsoft Teams、Office 365 高级合规版附加产品、Office 365 安全与合规中心、Office Online、Office Pro Plus、OneDrive for Business、Planner、Power Automate、Power BI、SharePoint Online、Skype for Business |

### <a name="office-365-audit-reports"></a>Office 365 审核报告

- [Office 365 Core - SSAE 18 SOC 3 报告](https://aka.ms/o365SOC-3)
- [请参阅过渡函和其他审核报告](https://aka.ms/auditreports)

必须要有 Office 365 或 Office 365 美国政府版的现有订阅或免费试用帐户，才能根据需要下载 SOC 1 和 SOC 2 证明报告和任何过渡函。

### <a name="frequently-asked-questions"></a>常见问题解答

**Office 365 SOC 报告多久发布一次？**

Office 365 和其他联机服务的 SOC 报告基于 12 个月的滚动时段（审核期），新报告每半年发布一次（期限为 3 月 31 日和 9 月 30 日）。 *过渡函* 每季度发布一次，以涵盖前面的 3 个月。 例如，1 月的过渡函涵盖 10 月 1 日到 12 月 31 日，4 月的过渡函涵盖 1 月 1 日到 3 月 31 日，7 月的过渡函涵盖 4 月 1 日到 6 月 30 日，10 月的过渡函涵盖 7 月 1 日到 9 月 30 日。

**在哪里可以获取 Office 365 SOC 审核文档（包括过渡函）？** 有关审核文档的链接，请参阅审核报告部分。 必须要有 Office 365 或 [Office](https://azure.microsoft.com/global-infrastructure/government/request/) 365 美国政府版的现有订阅或免费试用帐户才能登录。 然后，可以下载审核证书、评估报告和其他适用文档，以帮助你满足自己的法规要求。

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>使用 Microsoft 合规性管理器评估风险

[Microsoft 合规性管理器](/microsoft-365/compliance/compliance-manager)是 [Microsoft 365 合规中心](/microsoft-365/compliance/microsoft-365-compliance-center)中的一项预览功能，旨在帮助你了解组织的合规情况并采取措施帮助降低风险。 合规性管理器提供了一个高级模板，用于对此法规建立评估。 在合规性管理器的“**评估模板**”页面中找到模板。 了解如何[在合规性管理器中建立评估](/microsoft-365/compliance/compliance-manager-assessments)。

### <a name="resources"></a>资源

- [服务信任门户审核报告](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3)
- [适用于服务组织的 AICPA SOC](https://www.aicpa.org/interestareas/frc/assuranceadvisoryservices/socforserviceorganizations.html)
- [SSAE 第 18 号证明标准：阐明和准则修订（AICPA 专业标准）](https://www.aicpa.org/Research/Standards/AuditAttest/DownloadableDocuments/SSAE_No_18.pdf)
- [SOC 2 报告：对服务组织中安全性、可用性、处理完整性、机密性或隐私相关的控制进行的检验（AICPA 指南）](https://future.aicpa.org/cpe-learning/publication/soc-2-reporting-on-an-examination-of-controls-at-a-service-organization-relevant-to-security-availability-processing-integrity-confidentiality-or-privacy-OPL)（可供购买）
- [TSP 第 100 节（AICPA，2017 年信任服务标准）](https://www.aicpa.org/content/dam/aicpa/interestareas/frc/assuranceadvisoryservices/downloadabledocuments/trust-services-criteria.pdf)
