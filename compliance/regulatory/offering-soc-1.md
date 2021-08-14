---
title: 系统和组织控制 （SOC） 1 类型 2
description: 了解 Microsoft 云服务是如何遵守系统和组织控制 （SOC） 1 类型 2的操作安全标准。
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
ms.openlocfilehash: bfa130999fb2c527f4b3f233958d10b24cba76d4
ms.sourcegitcommit: 01938022a292c07e98041dc6ae1312a1b8c617db
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/13/2021
ms.locfileid: "58260956"
---
# <a name="system-and-organization-controls-soc-1-type-2"></a>系统和组织控制 （SOC） 1 类型 2

## <a name="soc-1-type-2-overview"></a>SOC 1 类型 2 概述

服务组织的系统和组织控制 （SOC） 是由美国注册会计师协会 （AICPA） 创建的内部控制报告。 它们旨在检查服务组织提供的服务，以便最终用户可以评估和解决与外包服务相关的风险。

SOC 1 类型 2 证明是根据以下标准执行：

- SSAE 编号。 18，证明标准：阐明和重新编纂，包括 AT-C 第 320 部分， *对与用户实体财务报告的内部控制相关的服务组织中的控制检查进行报告* （AICPA、专业标准）。
- SOC 1 对与用户实体财务报告的内部控制相关的服务组织中的控制检查进行报告（AICPA 指南）。

除了 AICPA 关于证明业务标准的声明 18（SSAE 18） 之外，Office 365 SOC 1 类型 2 审核是根据鉴证业务国际标准进行验证。 3402（ISAE 3402）。 SOC 1 证明已取代 SAS 70，适合对与用户实体财务报表内部控制相关的服务组织中的控制进行报告。 类型 2 报告包括审核员对控制有效性的意见，以便在指定的监视期间实现相关的控制目标。

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Microsoft 范围内的云平台和云服务

Azure SOC 1 类型 2 证明报告中显示了范围内的 Microsoft 联机服务：

- Azure（有关详细见解，请参阅 [Microsoft Azure 合规性产品/服务](https://azure.microsoft.com/resources/microsoft-azure-compliance-offerings/) 或 Azure SOC 1 类型 2 证明报告）
- Azure DevOps（请另外参阅 Azure DevOps SOC 1 类型 2 证明报告）
- Dynamics 365（有关详细见解，请参阅 Azure SOC 1 类型 2 证明报告）
- Microsoft 365 Defender
- Microsoft Cloud App Security (MCAS)
- Microsoft Defender for Endpoint（曾用名：Microsoft Defender 高级威胁防护）
- Microsoft Defender for Identity（曾用名： Azure 高级威胁防护）
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
- 更新合规性（不在 Microsoft Azure 政府范围内）

## <a name="azure-dynamics-365-and-soc-1"></a>Azure, Dynamics 365, 和 SOC 1

有关 Azure、Dynamics 365 和其他联机服务合规性的详细信息，请参阅 [Azure SOC 1 产品/服务](/azure/compliance/offerings/offering-soc-1)。

## <a name="office-365-and-soc-1"></a>Office 365 和 SOC 1

### <a name="office-365-cloud-environments"></a>Office 365 云环境

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365 适用性和范围内的服务

使用下表确定 Office 365 服务和订阅的适用性：

| **适用性** | **范围内服务** |
|:------------------|:----------------------|
| **商业** | 合规性管理器，客户密码箱，Delve，Exchange Online Protection， Exchange Online、Forms、Griffin、身份管理器、密码箱 （Torus）、Microsoft Teams、MyAnalytics、Office 365 客户门户、Office 365 微服务（包括但不限于 Kaizala、ObjectStore、Sway、PowerPoint Online 文档服务、查询批注服务、学校数据同步、Siphon、语音、StaffHub、可扩展应用程序计划）、Office Online、Office 服务基础结构、OneDrive for Business， Planner， PowerApps， Power BI， Project Online， Service Encryption with Customer Key， SharePoint Online， Skype for Business |
| **GCC** | Azure Active Directory、合规性管理器、Delve、Exchange Online、Forms、Microsoft Defender for Office 365、Microsoft Teams、MyAnalytics、Office 365 高级合规版附加产品、Office 365 安全与合规中心、Office Online、Office Pro Plus、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、SharePoint Online、Skype for Business、Stream |
| **GCC 高级** | Azure Active Directory、Exchange Online、Forms、Microsoft Defender for Office 365、Microsoft Teams、Office 365 高级合规版加载项、Office 365 安全与合规中心、Office Online、Office Pro Plus、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、SharePoint Online、Skype for Business |
| **DoD** | Azure Active Directory、Exchange Online、Forms、Microsoft Defender for Office 365、Microsoft Teams、Office 365 高级合规版附加产品、Office 365 安全与合规中心、Office Online、Office Pro Plus、OneDrive for Business、Planner、Power BI、SharePoint Online、Skype for Business |

### <a name="office-365-audit-reports"></a>Office 365 审核日志

- [Office 365 Core - SSAE 18 SOC 1 报告](https://aka.ms/o365SOC-1)
- 请参阅 bridge letter 和其他审核报告

必须拥有 Office 365 或 Office 365 美国政府版的现有订阅或免费试用帐户，才能根据需要下载 SOC 1 和 SOC 2 证明报告和任何bridge letter。

### <a name="frequently-asked-questions"></a>常见问题解答

**Office 365 SOC 报告多久发布一次？**

Office 365 和其他联机服务的 SOC 报告基于 12 个月的滚动时段（审核期），新报告每半年发布一次（期限为 3 月 31 日和 9 月 30 日）。 *过渡函* 每季度发布一次，以涵盖前面的 3 个月。 例如，1 月的 bridge letter 涵盖 10 月 1 日到 12 月 31 日，4 月的 bridge letter 涵盖 1 月 1 日到 3 月 31 日，7 月的 bridge letter 涵盖 4 月 1 日到 6 月 30 日，10 月的 bridge letter 涵盖 7 月 1 日到 9 月 30 日。

**客户如何从 Office 365 SOC 1 类型 2 证明中受益？**

客户在遵循自己的特定金融行业合规性要求，如 Sarbanes-Oxley （SOX）、联邦金融机构检查委员会 （FFIEC）、Gramm-Leach-Bliley Act （GLBA） 等时，可以使用 Office 365 SOC 1 类型 2 证明。

**在哪里可以获取 Office 365 SOC 审核文档（包括 bridge letter）？**

有关审核文档的链接，请参阅审核报告部分。 必须拥有 Office 365 或 Office 365 美国政府版中的现有订阅或免费试用帐户才能登录。 然后，可以下载审核证书、评估报告和其他适用文档，以帮助你满足自己的法规要求。

**在哪里可以查看针对已记录的异常的管理响应？**

管理响应位于 SOC 证明报告的末尾。 请在文档中搜索“管理响应”。

**在哪里可以查看用户实体责任？**

用户实体责任位于 SOC 证明报告的末尾。 请在文档中搜索“用户实体责任”。

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a>使用 Microsoft 合规性管理器评估风险

[Microsoft 合规性管理器](/microsoft-365/compliance/compliance-manager)是 [Microsoft 365 合规中心](/microsoft-365/compliance/microsoft-365-compliance-center)中的一项预览功能，旨在帮助你了解组织的合规情况并采取措施帮助降低风险。 合规性管理器提供了一个高级模板，用于对此法规建立评估。 在合规性管理器的“**评估模板**”页面中找到模板。 了解如何[在合规性管理器中建立评估](/microsoft-365/compliance/compliance-manager-assessments)。

### <a name="resources"></a>资源

- [服务信任门户审核报告](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3)
- [SSAE 第 18 号证明标准：阐明和重新编纂](https://www.aicpa.org/Research/Standards/AuditAttest/DownloadableDocuments/SSAE_No_18.pdf)
- [SOC 1 对与用户实体财务报告的内部控制相关的服务组织中的控制检查进行报告（AICPA 指南）](https://future.aicpa.org/cpe-learning/publication/reporting-on-an-examination-of-controls-at-a-service-organization-relevant-to-user-entities-internal-control-over-financial-reporting-soc-1-guide-OPL) （可供购买）
