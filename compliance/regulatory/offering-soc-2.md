---
title: 系统和组织控制 (SOC) 2 类型 2
description: 了解 Microsoft 云服务如何遵守系统和组织控制 (SOC) 2 类型 2 的操作安全标准。
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
ms.openlocfilehash: c20ad27b244825e017d7545e669262ca61202b60
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/12/2021
ms.locfileid: "53385712"
---
# <a name="system-and-organization-controls-soc-2-type-2"></a><span data-ttu-id="5da44-104">系统和组织控制 (SOC) 2 类型 2</span><span class="sxs-lookup"><span data-stu-id="5da44-104">System and Organization Controls (SOC) 2 Type 2</span></span>

## <a name="soc-2-type-2-overview"></a><span data-ttu-id="5da44-105">SOC 2 类型 2 概述</span><span class="sxs-lookup"><span data-stu-id="5da44-105">SOC 2 Type 2 overview</span></span>

<span data-ttu-id="5da44-106">服务组织的系统和组织控制 (SOC) 是由美国注册会计师协会 (AICPA) 创建的内部控制报告。</span><span class="sxs-lookup"><span data-stu-id="5da44-106">System and Organization Controls (SOC) for Service Organizations are internal control reports created by the American Institute of Certified Public Accountants (AICPA).</span></span> <span data-ttu-id="5da44-107">它们旨在检查服务组织提供的服务，以便最终用户可以评估和解决与外包服务相关的风险。</span><span class="sxs-lookup"><span data-stu-id="5da44-107">They are intended to examine services provided by a service organization so that end users can assess and address the risk associated with an outsourced service.</span></span>

<span data-ttu-id="5da44-108">SOC 2 类型 2 证明将根据以下标准执行：</span><span class="sxs-lookup"><span data-stu-id="5da44-108">A SOC 2 Type 2 attestation is performed under:</span></span>

- <span data-ttu-id="5da44-109">SSAE 第 </span><span class="sxs-lookup"><span data-stu-id="5da44-109">SSAE No.</span></span> <span data-ttu-id="5da44-110">18 号证明标准：阐述和准则修订，其中包括 AT-C 第 105 节“*所有证明业务通用的概念*”，以及 AT-C 第 205 节“*检验业务*”（AICPA，专业标准）。</span><span class="sxs-lookup"><span data-stu-id="5da44-110">18, Attestation Standards: Clarification and Recodification, which includes AT-C section 105, *Concepts Common to All Attestation Engagements*, and AT-C section 205, *Examination Engagements* (AICPA, Professional Standards).</span></span>
- <span data-ttu-id="5da44-111">SOC 2 报告：对服务组织中安全性、可用性、处理完整性、机密性或隐私相关的控制进行的检验（AICPA 指南）。</span><span class="sxs-lookup"><span data-stu-id="5da44-111">SOC 2 Reporting on an Examination of Controls at a Service Organization Relevant to Security, Availability, Processing Integrity, Confidentiality, or Privacy (AICPA Guide).</span></span>
- <span data-ttu-id="5da44-112">TSP 第 100 节，2017 年，有关安全性、可用性、处理完整性、机密性和隐私的信任服务标准（AICPA，2017 信任服务条件）。</span><span class="sxs-lookup"><span data-stu-id="5da44-112">TSP section 100, 2017 Trust Services Criteria for Security, Availability, Processing Integrity, Confidentiality, and Privacy (AICPA, 2017 Trust Services Criteria).</span></span>

<span data-ttu-id="5da44-113">此外，Office 365 SOC 2 类型 2 证明报告解决了云安全联盟 (CSA) 云控制矩阵 (CCM) 和德国联邦信息安全办公室 (BSI) 创建的云计算合规性标准目录 (C5:2020) 中所述的要求。</span><span class="sxs-lookup"><span data-stu-id="5da44-113">In addition, the Office 365 SOC 2 Type 2 attestation report addresses the requirements set forth in the Cloud Security Alliance (CSA) Cloud Controls Matrix (CCM), and the Cloud Computing Compliance Criteria Catalogue (C5:2020) created by the German Federal Office for Information Security (BSI).</span></span>

<span data-ttu-id="5da44-114">Office 365 SOC 2 证明基于可信誉良好的 CPA 公司进行的严格独立的第三方审核。</span><span class="sxs-lookup"><span data-stu-id="5da44-114">Office 365 SOC 2 attestations are based on rigorous independent third-party audits conducted by a reputable CPA firm.</span></span> <span data-ttu-id="5da44-115">在 SOC 2 审核结尾部分，审核员会在 SOC 2 类型 2 报告中提供评价意见，以描述云服务提供商 (CSP) 的系统并评估 CSP 对其所进行的控制的描述是否公平合理。</span><span class="sxs-lookup"><span data-stu-id="5da44-115">At the conclusion of a SOC 2 audit, the auditor renders an opinion in a SOC 2 Type 2 report, which describes the cloud service provider's (CSP) system and assesses the fairness of the CSP's description of its controls.</span></span> <span data-ttu-id="5da44-116">该结论还会评估 CSP 控制措施是否设计得当、在指定日期是否正常运行，以及在指定时间段内是否有效运行。</span><span class="sxs-lookup"><span data-stu-id="5da44-116">It also evaluates whether the CSP's controls are designed appropriately, were in operation on a specified date, and were operating effectively over a specified time period.</span></span> <span data-ttu-id="5da44-117">Office 365 SOC 2 类型 2 报告与系统安全性、可用性、处理完整性、机密性和隐私相关。</span><span class="sxs-lookup"><span data-stu-id="5da44-117">Office 365 SOC 2 Type 2 reports are relevant to system Security, Availability, Processing Integrity, Confidentiality, and Privacy.</span></span>

## <a name="microsoft-in-scope-cloud-platforms--services"></a><span data-ttu-id="5da44-118">Microsoft 范围内的云平台和云服务</span><span class="sxs-lookup"><span data-stu-id="5da44-118">Microsoft in-scope cloud platforms & services</span></span>

<span data-ttu-id="5da44-119">Azure SOC 2 类型 2 证明报告中显示了范围内的 Microsoft 联机服务：</span><span class="sxs-lookup"><span data-stu-id="5da44-119">Microsoft online services in scope are shown in the Azure SOC 2 Type 2 attestation report:</span></span>

- <span data-ttu-id="5da44-120">Azure（有关详细见解，请参阅 [Microsoft Azure 合规性产品/服务](https://azure.microsoft.com/resources/microsoft-azure-compliance-offerings/)或 Azure SOC 2 类型 2 证明报告）</span><span class="sxs-lookup"><span data-stu-id="5da44-120">Azure (for detailed insight, see [Microsoft Azure Compliance Offerings](https://azure.microsoft.com/resources/microsoft-azure-compliance-offerings/) or Azure SOC 2 Type 2 attestation report)</span></span>
- <span data-ttu-id="5da44-121">Azure DevOps（请另外参阅 Azure DevOps SOC 2 类型 2 证明报告）</span><span class="sxs-lookup"><span data-stu-id="5da44-121">Azure DevOps (see separate Azure DevOps SOC 2 Type 2 attestation report)</span></span>
- <span data-ttu-id="5da44-122">Dynamics 365（有关详细见解，请参阅 Azure SOC 2 类型 2 证明报告）</span><span class="sxs-lookup"><span data-stu-id="5da44-122">Dynamics 365 (for detailed insight, see Azure SOC 2 Type 2 attestation report)</span></span>
- <span data-ttu-id="5da44-123">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="5da44-123">Microsoft 365 Defender</span></span>
- <span data-ttu-id="5da44-124">Microsoft Cloud App Security (MCAS)</span><span class="sxs-lookup"><span data-stu-id="5da44-124">Microsoft Cloud App Security (MCAS)</span></span>
- <span data-ttu-id="5da44-125">Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="5da44-125">Microsoft Defender for Endpoint</span></span>
- <span data-ttu-id="5da44-126">Microsoft Defender for Identity</span><span class="sxs-lookup"><span data-stu-id="5da44-126">Microsoft Defender for Identity</span></span>
- <span data-ttu-id="5da44-127">Microsoft Forms Pro（不在 Azure 政府范围内）</span><span class="sxs-lookup"><span data-stu-id="5da44-127">Microsoft Forms Pro (not in scope for Azure Government)</span></span>
- <span data-ttu-id="5da44-128">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="5da44-128">Microsoft Graph</span></span>
- <span data-ttu-id="5da44-129">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="5da44-129">Microsoft Intune</span></span>
- <span data-ttu-id="5da44-130">Microsoft 托管桌面（不在 Azure 政府范围内）</span><span class="sxs-lookup"><span data-stu-id="5da44-130">Microsoft Managed Desktop (not in scope for Azure Government)</span></span>
- <span data-ttu-id="5da44-131">Microsoft Stream</span><span class="sxs-lookup"><span data-stu-id="5da44-131">Microsoft Stream</span></span>
- <span data-ttu-id="5da44-132">Microsoft 威胁专家（不在 Azure 政府范围内）</span><span class="sxs-lookup"><span data-stu-id="5da44-132">Microsoft Threat Experts (not in scope for Azure Government)</span></span>
- <span data-ttu-id="5da44-133">提名门户</span><span class="sxs-lookup"><span data-stu-id="5da44-133">Nomination Portal</span></span>
- <span data-ttu-id="5da44-134">Office 365、Office 365 美国政府版、Office 365 美国政府版 - 高级、Office 365 美国政府国防部版</span><span class="sxs-lookup"><span data-stu-id="5da44-134">Office 365, Office 365 U.S. Government, Office 365 U.S. Government - High, Office 365 U.S. Government Defense</span></span>
- <span data-ttu-id="5da44-135">Power Apps</span><span class="sxs-lookup"><span data-stu-id="5da44-135">Power Apps</span></span>
- <span data-ttu-id="5da44-136">Power Automate</span><span class="sxs-lookup"><span data-stu-id="5da44-136">Power Automate</span></span>
- <span data-ttu-id="5da44-137">Power BI</span><span class="sxs-lookup"><span data-stu-id="5da44-137">Power BI</span></span>
- <span data-ttu-id="5da44-138">Power Virtual Agents（不在 Azure 政府范围内）</span><span class="sxs-lookup"><span data-stu-id="5da44-138">Power Virtual Agents (not in scope for Azure Government)</span></span>
- <span data-ttu-id="5da44-139">更新合规性（不在 Azure 政府范围内）</span><span class="sxs-lookup"><span data-stu-id="5da44-139">Update Compliance (not in scope for Azure Government)</span></span>

## <a name="azure-dynamics-365-and-soc-2"></a><span data-ttu-id="5da44-140">Azure、Dynamics 365 和 SOC 2</span><span class="sxs-lookup"><span data-stu-id="5da44-140">Azure, Dynamics 365, and SOC 2</span></span>

<span data-ttu-id="5da44-141">有关 Azure、Dynamics 365 和其他联机服务合规性的详细信息，请参阅 [Azure SOC 2 产品/服务](/azure/compliance/offerings/offering-soc-2)。</span><span class="sxs-lookup"><span data-stu-id="5da44-141">For more information about Azure, Dynamics 365, and other online services compliance, see the [Azure SOC 2 offering](/azure/compliance/offerings/offering-soc-2).</span></span>

## <a name="office-365-and-soc-2"></a><span data-ttu-id="5da44-142">Office 365 和 SOC 2</span><span class="sxs-lookup"><span data-stu-id="5da44-142">Office 365 and SOC 2</span></span>

### <a name="office-365-cloud-environments"></a><span data-ttu-id="5da44-143">Office 365 云环境</span><span class="sxs-lookup"><span data-stu-id="5da44-143">Office 365 cloud environments</span></span>

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a><span data-ttu-id="5da44-144">Office 365 适用性和范围内的服务</span><span class="sxs-lookup"><span data-stu-id="5da44-144">Office 365 applicability and in-scope services</span></span>

<span data-ttu-id="5da44-145">使用下表确定 Office 365 服务和订阅的适用性：</span><span class="sxs-lookup"><span data-stu-id="5da44-145">Use the following table to determine applicability for your Office 365 services and subscription:</span></span>

| <span data-ttu-id="5da44-146">**适用性**</span><span class="sxs-lookup"><span data-stu-id="5da44-146">**Applicability**</span></span> | <span data-ttu-id="5da44-147">**范围内服务**</span><span class="sxs-lookup"><span data-stu-id="5da44-147">**In-scope services**</span></span> |
|:------------------|:----------------------|
| <span data-ttu-id="5da44-148">**Office 365**</span><span class="sxs-lookup"><span data-stu-id="5da44-148">**Office 365**</span></span> | <span data-ttu-id="5da44-149">合规性管理器、客户密码箱、Delve、Exchange Online Protection、Exchange Online、Forms、Griffin、身份管理器、密码箱 (Torus)、Microsoft Teams、MyAnalytics、Office 365 客户门户、Office 365 微服务（包括但不限于 Kaizala、ObjectStore、Sway、PowerPoint Online 文档服务、查询批注服务、学校数据同步、Siphon、语音、StaffHub、可扩展应用程序计划）、Office Online、Office 服务基础结构、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、Project Online、使用客户密钥进行服务加密、SharePoint Online、Skype for Business</span><span class="sxs-lookup"><span data-stu-id="5da44-149">Compliance Manager, Customer Lockbox, Delve, Exchange Online Protection, Exchange Online, Forms, Griffin, Identity Manager, Lockbox (Torus), Microsoft Teams, MyAnalytics, Office 365 Customer Portal, Office 365 Microservices (including but not limited to Kaizala, ObjectStore, Sway, PowerPoint Online Document Service, Query Annotation Service, School Data Sync, Siphon, Speech, StaffHub, eXtensible Application Program), Office Online, Office Services Infrastructure, OneDrive for Business, Planner, PowerApps, Power Automate, Power BI, Project Online, Service Encryption with Customer Key, SharePoint Online, Skype for Business</span></span> |
| <span data-ttu-id="5da44-150">**GCC**</span><span class="sxs-lookup"><span data-stu-id="5da44-150">**GCC**</span></span> | <span data-ttu-id="5da44-151">Azure Active Directory、合规性管理器、Delve、Exchange Online、Forms、Microsoft Defender for Office 365、Microsoft Teams、MyAnalytics、Office 365 高级合规版附加产品、Office 365 安全与合规中心、Office Online、Office Pro Plus、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、SharePoint Online、Skype for Business、Stream</span><span class="sxs-lookup"><span data-stu-id="5da44-151">Azure Active Directory, Compliance Manager, Delve, Exchange Online, Forms, Microsoft Defender for Office 365, Microsoft Teams, MyAnalytics, Office 365 Advanced Compliance add-on, Office 365 Security & Compliance Center, Office Online, Office Pro Plus, OneDrive for Business, Planner, PowerApps, Power Automate, Power BI, SharePoint Online, Skype for Business, Stream</span></span> |
| <span data-ttu-id="5da44-152">**GCC 高级**</span><span class="sxs-lookup"><span data-stu-id="5da44-152">**GCC High**</span></span> | <span data-ttu-id="5da44-153">Azure Active Directory、Exchange Online、Forms、Microsoft Defender for Office 365、Microsoft Teams、Office 365 高级合规版附加产品、Office 365 安全与合规中心、Office Online、Office Pro Plus、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、SharePoint Online、Skype for Business</span><span class="sxs-lookup"><span data-stu-id="5da44-153">Azure Active Directory, Exchange Online, Forms, Microsoft Defender for Office 365, Microsoft Teams, Office 365 Advanced Compliance add-on, Office 365 Security & Compliance Center, Office Online, Office Pro Plus, OneDrive for Business, Planner, PowerApps, Power Automate, Power BI, SharePoint Online, Skype for Business</span></span> |
| <span data-ttu-id="5da44-154">**DoD**</span><span class="sxs-lookup"><span data-stu-id="5da44-154">**DoD**</span></span> | <span data-ttu-id="5da44-155">Azure Active Directory、Exchange Online、Forms、Microsoft Defender for Office 365、Microsoft Teams、Office 365 高级合规版附加产品、Office 365 安全与合规中心、Office Online、Office Pro Plus、OneDrive for Business、Planner、Power BI、SharePoint Online、Skype for Business</span><span class="sxs-lookup"><span data-stu-id="5da44-155">Azure Active Directory, Exchange Online, Forms, Microsoft Defender for Office 365, Microsoft Teams, Office 365 Advanced Compliance add-on, Office 365 Security & Compliance Center, Office Online, Office Pro Plus, OneDrive for Business, Planner, Power BI, SharePoint Online, Skype for Business</span></span> |

### <a name="office-365-audit-reports"></a><span data-ttu-id="5da44-156">Office 365 审核报告</span><span class="sxs-lookup"><span data-stu-id="5da44-156">Office 365 audit reports</span></span>

- [<span data-ttu-id="5da44-157">Office 365 Core - SSAE 18 SOC 2 报告</span><span class="sxs-lookup"><span data-stu-id="5da44-157">Office 365 Core - SSAE 18 SOC 2 Report</span></span>](https://aka.ms/o365SOC-2)
- [<span data-ttu-id="5da44-158">Office 365 微服务 T1-SSAE 18 SOC2 类型 I 报告</span><span class="sxs-lookup"><span data-stu-id="5da44-158">Office 365 Microservices T1-SSAE 18 SOC2 Type I Report</span></span>](https://aka.ms/o365-MS-SOC-2-type1)
- [<span data-ttu-id="5da44-159">请参阅过渡函和其他审核报告</span><span class="sxs-lookup"><span data-stu-id="5da44-159">See bridge letters and additional audit reports</span></span>](https://aka.ms/auditreports)

<span data-ttu-id="5da44-160">必须要有 Office 365 或 [Office](https://azure.microsoft.com/global-infrastructure/government/request/) 365 美国政府版的现有订阅或免费试用帐户，才能根据需要下载 SOC 1 和 SOC 2 证明报告和任何过渡函。</span><span class="sxs-lookup"><span data-stu-id="5da44-160">You must have an existing subscription or free trial account in Office 365 or [Office](https://azure.microsoft.com/global-infrastructure/government/request/) 365 U.S. Government to download SOC 1 and SOC 2 attestation reports and any bridge letters as needed.</span></span>

### <a name="frequently-asked-questions"></a><span data-ttu-id="5da44-161">常见问题解答</span><span class="sxs-lookup"><span data-stu-id="5da44-161">Frequently asked questions</span></span>

<span data-ttu-id="5da44-162">**Office 365 SOC 报告多久发布一次？**</span><span class="sxs-lookup"><span data-stu-id="5da44-162">**How often are Office 365 SOC reports issued?**</span></span>

<span data-ttu-id="5da44-163">Office 365 和其他联机服务的 SOC 报告基于 12 个月的滚动时段（审核期），新报告每半年发布一次（期限为 3 月 31 日和 9 月 30 日）。</span><span class="sxs-lookup"><span data-stu-id="5da44-163">SOC reports for Office 365 and other online services are based on a rolling 12-month run window (audit period) with new reports issued semi-annually (period ends are March 31 and September 30).</span></span> <span data-ttu-id="5da44-164">*过渡函* 每季度发布一次，以涵盖前面的 3 个月。</span><span class="sxs-lookup"><span data-stu-id="5da44-164">*Bridge letters* are issued each quarter to cover the prior three-month period.</span></span> <span data-ttu-id="5da44-165">例如，1 月的过渡函涵盖 10 月 1 日到 12 月 31 日，4 月的过渡函涵盖 1 月 1 日到 3 月 31 日，7 月的过渡函涵盖 4 月 1 日到 6 月 30 日，10 月的过渡函涵盖 7 月 1 日到 9 月 30 日。</span><span class="sxs-lookup"><span data-stu-id="5da44-165">For example, the January letter covers 1-Oct through 31-Dec, the April letter covers 1-Jan through 31-Mar, the July letter covers 1-Apr through 30-Jun, and the October letter covers 1-Jul through 30-Sep.</span></span>

<span data-ttu-id="5da44-166">**在哪里可以获取 Office 365 SOC 审核文档（包括过渡函）？**</span><span class="sxs-lookup"><span data-stu-id="5da44-166">**Where can I get the Office 365 SOC audit documentation including bridge letters?**</span></span>

<span data-ttu-id="5da44-167">有关审核文档的链接，请参阅审核报告部分。</span><span class="sxs-lookup"><span data-stu-id="5da44-167">For links to audit documentation, see the audit report section.</span></span> <span data-ttu-id="5da44-168">必须要有 Office 365 或 [Office](https://azure.microsoft.com/global-infrastructure/government/request/) 365 美国政府版的现有订阅或免费试用帐户才能登录。</span><span class="sxs-lookup"><span data-stu-id="5da44-168">You must have an existing subscription or free trial account in Office 365or [Office](https://azure.microsoft.com/global-infrastructure/government/request/) 365 U.S. Government to log in.</span></span> <span data-ttu-id="5da44-169">然后，可以下载审核证书、评估报告和其他适用文档，以帮助你满足自己的法规要求。</span><span class="sxs-lookup"><span data-stu-id="5da44-169">You can then download audit certificates, assessment reports, and other applicable documents to help you with your own regulatory requirements.</span></span>

<span data-ttu-id="5da44-170">**在哪里可以找到对云安全联盟 CCM 控制实施的评估？**</span><span class="sxs-lookup"><span data-stu-id="5da44-170">**Where can I find an assessment of the Cloud Security Alliance CCM controls implementation?**</span></span>

<span data-ttu-id="5da44-171">Office 365 SOC 2 类型 2 审核基于美国注册会计师学会 (AICPA) 的信任服务原则和标准（包括安全性、可用性、机密性、隐私和处理完整性）以及云安全联盟 (CSA) 云控制矩阵 (CCM) 中的标准。</span><span class="sxs-lookup"><span data-stu-id="5da44-171">The Office 365 SOC 2 Type 2 audit is based on the American Institute of Certified Public Accountants (AICPA) Trust Services Principles and Criteria, including security, availability, confidentiality, privacy, and processing integrity, and the criteria in the Cloud Security Alliance (CSA) Cloud Controls Matrix (CCM).</span></span> <span data-ttu-id="5da44-172">目标是满足 AICPA 标准和 CCM 中规定的要求。</span><span class="sxs-lookup"><span data-stu-id="5da44-172">The objective is to meet both the AICPA criteria and requirements set forth in the CCM.</span></span> <span data-ttu-id="5da44-173">根据 CSA STAR 证明的要求，Office 365 SOC 2 类型 2 审核纳入了 CCM 控制评估。</span><span class="sxs-lookup"><span data-stu-id="5da44-173">The Office 365 SOC 2 Type 2 audit incorporates the CCM controls assessment as required by the CSA STAR Attestation.</span></span> <span data-ttu-id="5da44-174">有关详细信息，请参阅 Office 365 SOC 2 类型 2 证明报告。</span><span class="sxs-lookup"><span data-stu-id="5da44-174">For more information, see the Office 365 SOC 2 Type 2 attestation report.</span></span>

<span data-ttu-id="5da44-175">**在哪里可以查看针对已记录的异常的管理响应？**</span><span class="sxs-lookup"><span data-stu-id="5da44-175">**Where can I see management responses to exceptions noted?**</span></span>

<span data-ttu-id="5da44-176">管理响应位于 SOC 证明报告的末尾。</span><span class="sxs-lookup"><span data-stu-id="5da44-176">Management responses are located towards the end of the SOC attestation report.</span></span> <span data-ttu-id="5da44-177">请在文档中搜索“管理响应”。</span><span class="sxs-lookup"><span data-stu-id="5da44-177">Search the document for 'Management Response'.</span></span>

<span data-ttu-id="5da44-178">**在哪里可以查看用户实体责任？**</span><span class="sxs-lookup"><span data-stu-id="5da44-178">**Where can I see user entity responsibilities?**</span></span>

<span data-ttu-id="5da44-179">用户实体责任位于 SOC 证明报告的末尾。</span><span class="sxs-lookup"><span data-stu-id="5da44-179">User entity responsibilities are located at the very end of the SOC attestation report.</span></span> <span data-ttu-id="5da44-180">请在文档中搜索“用户实体责任”。</span><span class="sxs-lookup"><span data-stu-id="5da44-180">Search the document for 'User Entity Responsibilities'.</span></span>

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a><span data-ttu-id="5da44-181">使用 Microsoft 合规性管理器评估风险</span><span class="sxs-lookup"><span data-stu-id="5da44-181">Use Microsoft Compliance Manager to assess your risk</span></span>

<span data-ttu-id="5da44-182">[Microsoft 合规性管理器](/microsoft-365/compliance/compliance-manager)是 [Microsoft 365 合规中心](/microsoft-365/compliance/microsoft-365-compliance-center)中的一项预览功能，旨在帮助你了解组织的合规情况并采取措施帮助降低风险。</span><span class="sxs-lookup"><span data-stu-id="5da44-182">[Microsoft Compliance Manager](/microsoft-365/compliance/compliance-manager) is a feature in the [Microsoft 365 compliance center](/microsoft-365/compliance/microsoft-365-compliance-center) to help you understand your organization's compliance posture and take actions to help reduce risks.</span></span> <span data-ttu-id="5da44-183">合规性管理器提供了一个高级模板，用于对此法规建立评估。</span><span class="sxs-lookup"><span data-stu-id="5da44-183">Compliance Manager offers a premium template for building an assessment for this regulation.</span></span> <span data-ttu-id="5da44-184">在合规性管理器的“**评估模板**”页面中找到模板。</span><span class="sxs-lookup"><span data-stu-id="5da44-184">Find the template in the **assessment templates** page in Compliance Manager.</span></span> <span data-ttu-id="5da44-185">了解如何[在合规性管理器中建立评估](/microsoft-365/compliance/compliance-manager-assessments)。</span><span class="sxs-lookup"><span data-stu-id="5da44-185">Learn how to [build assessments in Compliance Manager](/microsoft-365/compliance/compliance-manager-assessments).</span></span>

### <a name="resources"></a><span data-ttu-id="5da44-186">资源</span><span class="sxs-lookup"><span data-stu-id="5da44-186">Resources</span></span>

- [<span data-ttu-id="5da44-187">服务信任门户审核报告</span><span class="sxs-lookup"><span data-stu-id="5da44-187">Service Trust Portal audit reports</span></span>](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3)
- [<span data-ttu-id="5da44-188">适用于服务组织的 AICPA SOC</span><span class="sxs-lookup"><span data-stu-id="5da44-188">AICPA SOC for Service Organizations</span></span>](https://www.aicpa.org/interestareas/frc/assuranceadvisoryservices/socforserviceorganizations.html)
- [<span data-ttu-id="5da44-189">SSAE 第 18 号证明标准：阐明和准则修订（AICPA 专业标准）</span><span class="sxs-lookup"><span data-stu-id="5da44-189">SSAE No. 18, Attestation Standards: Clarification and Recodification (AICPA Professional Standards)</span></span>](https://www.aicpa.org/Research/Standards/AuditAttest/DownloadableDocuments/SSAE_No_18.pdf)
- <span data-ttu-id="5da44-190">[SOC 2 报告：对服务组织中安全性、可用性、处理完整性、机密性或隐私相关的控制进行的检验（AICPA 指南）](https://future.aicpa.org/cpe-learning/publication/soc-2-reporting-on-an-examination-of-controls-at-a-service-organization-relevant-to-security-availability-processing-integrity-confidentiality-or-privacy-OPL)（可供购买）</span><span class="sxs-lookup"><span data-stu-id="5da44-190">[SOC 2 Reporting on an Examination of Controls at a Service Organization Relevant to Security, Availability, Processing Integrity, Confidentiality, or Privacy (AICPA Guide)](https://future.aicpa.org/cpe-learning/publication/soc-2-reporting-on-an-examination-of-controls-at-a-service-organization-relevant-to-security-availability-processing-integrity-confidentiality-or-privacy-OPL) (available for purchase)</span></span>
- [<span data-ttu-id="5da44-191">TSP 第 100 节（AICPA，2017 年信任服务标准）</span><span class="sxs-lookup"><span data-stu-id="5da44-191">TSP section 100 (AICPA, 2017 Trust Services Criteria)</span></span>](https://www.aicpa.org/content/dam/aicpa/interestareas/frc/assuranceadvisoryservices/downloadabledocuments/trust-services-criteria.pdf)
