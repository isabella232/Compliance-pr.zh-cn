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
# <a name="system-and-organization-controls-soc-3"></a><span data-ttu-id="e60e3-104">系统和组织控制 (SOC) 3</span><span class="sxs-lookup"><span data-stu-id="e60e3-104">System and Organization Controls (SOC) 3</span></span>

## <a name="soc-3-overview"></a><span data-ttu-id="e60e3-105">SOC 3 概述</span><span class="sxs-lookup"><span data-stu-id="e60e3-105">SOC 3 overview</span></span>

<span data-ttu-id="e60e3-106">服务组织的系统和组织控制 (SOC) 是由美国注册会计师协会 (AICPA) 创建的内部控制报告。</span><span class="sxs-lookup"><span data-stu-id="e60e3-106">System and Organization Controls (SOC) for Service Organizations are internal control reports created by the American Institute of Certified Public Accountants (AICPA).</span></span> <span data-ttu-id="e60e3-107">它们旨在检查服务组织提供的服务，以便最终用户可以评估和解决与外包服务相关的风险。</span><span class="sxs-lookup"><span data-stu-id="e60e3-107">They are intended to examine services provided by a service organization so that end users can assess and address the risk associated with an outsourced service.</span></span>

<span data-ttu-id="e60e3-108">*SOC 3 适用于服务组织的 SOC：一般用途的信任服务标准报告* 是面向公众的简短 SOC 2 类型 2 证明报告版本，适用于需要有关安全性、可用性、处理完整性、机密性或隐私相关服务组织控制的保证，但又不需要完整 SOC 2 报告的用户。</span><span class="sxs-lookup"><span data-stu-id="e60e3-108">*SOC 3 SOC for Service Organizations: Trust Services Criteria for General Use Report* is a short, publicly facing version of the SOC 2 Type 2 attestation report for users who need assurances about service organization's controls relevant to Security, Availability, Processing Integrity, Confidentiality, or Privacy but do not need a full SOC 2 report.</span></span> <span data-ttu-id="e60e3-109">由于 SOC 3 报告是一般用途报告，因此可以自由分发。</span><span class="sxs-lookup"><span data-stu-id="e60e3-109">Because SOC 3 reports are general use reports, they can be freely distributed.</span></span>

<span data-ttu-id="e60e3-110">SOC 3 报告包含服务组织管理层关于控制在基于适用信任服务标准实现承诺方面的有效性的书面声明，以及服务审核员对管理层声明是否公平的意见。</span><span class="sxs-lookup"><span data-stu-id="e60e3-110">A SOC 3 report contains a written assertion by service organization management regarding control effectiveness to achieve commitments based on the applicable trust services criteria, as well as service auditor's opinion on whether management's assertion is stated fairly.</span></span>

## <a name="microsoft-in-scope-cloud-platforms--services"></a><span data-ttu-id="e60e3-111">Microsoft 范围内的云平台和云服务</span><span class="sxs-lookup"><span data-stu-id="e60e3-111">Microsoft in-scope cloud platforms & services</span></span>

<span data-ttu-id="e60e3-112">Microsoft 范围内的服务显示在 Azure [SOC 2 类型 2 证明](offering-soc-2.md)报告中。</span><span class="sxs-lookup"><span data-stu-id="e60e3-112">Microsoft in-scope services are shown in the Azure [SOC 2 Type 2 attestation](offering-soc-2.md) report.</span></span>

- <span data-ttu-id="e60e3-113">Azure（有关详细见解，请参阅 [Microsoft Azure 合规性产品/服务](https://azure.microsoft.com/resources/microsoft-azure-compliance-offerings/)或 Azure SOC 2 类型 2 证明报告）</span><span class="sxs-lookup"><span data-stu-id="e60e3-113">Azure (for detailed insight, see [Microsoft Azure Compliance Offerings](https://azure.microsoft.com/resources/microsoft-azure-compliance-offerings/) or Azure SOC 2 Type 2 attestation report)</span></span>
- <span data-ttu-id="e60e3-114">Dynamics 365（有关详细见解，请参阅 Azure SOC 2 类型 2 证明报告）</span><span class="sxs-lookup"><span data-stu-id="e60e3-114">Dynamics 365 (for detailed insight, see Azure SOC 2 Type 2 attestation report)</span></span>
- <span data-ttu-id="e60e3-115">Microsoft 365 Defender</span><span class="sxs-lookup"><span data-stu-id="e60e3-115">Microsoft 365 Defender</span></span>
- <span data-ttu-id="e60e3-116">Microsoft Cloud App Security (MCAS)</span><span class="sxs-lookup"><span data-stu-id="e60e3-116">Microsoft Cloud App Security (MCAS)</span></span>
- <span data-ttu-id="e60e3-117">Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="e60e3-117">Microsoft Defender for Endpoint</span></span>
- <span data-ttu-id="e60e3-118">Microsoft Defender for Identity</span><span class="sxs-lookup"><span data-stu-id="e60e3-118">Microsoft Defender for Identity</span></span>
- <span data-ttu-id="e60e3-119">Microsoft Forms Pro（不在 Azure 政府范围内）</span><span class="sxs-lookup"><span data-stu-id="e60e3-119">Microsoft Forms Pro (not in scope for Azure Government)</span></span>
- <span data-ttu-id="e60e3-120">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="e60e3-120">Microsoft Graph</span></span>
- <span data-ttu-id="e60e3-121">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="e60e3-121">Microsoft Intune</span></span>
- <span data-ttu-id="e60e3-122">Microsoft 托管桌面（不在 Azure 政府范围内）</span><span class="sxs-lookup"><span data-stu-id="e60e3-122">Microsoft Managed Desktop (not in scope for Azure Government)</span></span>
- <span data-ttu-id="e60e3-123">Microsoft Stream</span><span class="sxs-lookup"><span data-stu-id="e60e3-123">Microsoft Stream</span></span>
- <span data-ttu-id="e60e3-124">Microsoft 威胁专家（不在 Azure 政府范围内）</span><span class="sxs-lookup"><span data-stu-id="e60e3-124">Microsoft Threat Experts (not in scope for Azure Government)</span></span>
- <span data-ttu-id="e60e3-125">提名门户</span><span class="sxs-lookup"><span data-stu-id="e60e3-125">Nomination Portal</span></span>
- <span data-ttu-id="e60e3-126">Office 365、Office 365 美国政府版、Office 365 美国政府版 - 高级、Office 365 美国政府国防部版</span><span class="sxs-lookup"><span data-stu-id="e60e3-126">Office 365, Office 365 U.S. Government, Office 365 U.S. Government - High, Office 365 U.S. Government Defense</span></span>
- <span data-ttu-id="e60e3-127">Power Apps</span><span class="sxs-lookup"><span data-stu-id="e60e3-127">Power Apps</span></span>
- <span data-ttu-id="e60e3-128">Power Automate</span><span class="sxs-lookup"><span data-stu-id="e60e3-128">Power Automate</span></span>
- <span data-ttu-id="e60e3-129">Power BI</span><span class="sxs-lookup"><span data-stu-id="e60e3-129">Power BI</span></span>
- <span data-ttu-id="e60e3-130">Power Virtual Agents（不在 Azure 政府范围内）</span><span class="sxs-lookup"><span data-stu-id="e60e3-130">Power Virtual Agents (not in scope for Azure Government)</span></span>
- <span data-ttu-id="e60e3-131">更新合规性（不在 Azure 政府范围内）</span><span class="sxs-lookup"><span data-stu-id="e60e3-131">Update Compliance (not in scope for Azure Government)</span></span>

## <a name="azure-dynamics-365-and-soc-3"></a><span data-ttu-id="e60e3-132">Azure、Dynamics 365 和 SOC 3</span><span class="sxs-lookup"><span data-stu-id="e60e3-132">Azure, Dynamics 365, and SOC 3</span></span>

<span data-ttu-id="e60e3-133">有关 Azure、Dynamics 365 和其他联机服务合规性的详细信息，请参阅 [Azure SOC 3 产品/服务](/azure/compliance/offerings/offering-soc-3)。</span><span class="sxs-lookup"><span data-stu-id="e60e3-133">For more information about Azure, Dynamics 365, and other online services compliance, see the [Azure SOC 3 offering](/azure/compliance/offerings/offering-soc-3).</span></span>

## <a name="office-365-and-soc-3"></a><span data-ttu-id="e60e3-134">Office 365 和 SOC 3</span><span class="sxs-lookup"><span data-stu-id="e60e3-134">Office 365 and SOC 3</span></span>

### <a name="office-365-cloud-environments"></a><span data-ttu-id="e60e3-135">Office 365 云环境</span><span class="sxs-lookup"><span data-stu-id="e60e3-135">Office 365 cloud environments</span></span>

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a><span data-ttu-id="e60e3-136">Office 365 适用性和范围内的服务</span><span class="sxs-lookup"><span data-stu-id="e60e3-136">Office 365 applicability and in-scope services</span></span>

<span data-ttu-id="e60e3-137">使用下表确定 Office 365 服务和订阅的适用性：</span><span class="sxs-lookup"><span data-stu-id="e60e3-137">Use the following table to determine applicability for your Office 365 services and subscription:</span></span>

| <span data-ttu-id="e60e3-138">**适用性**</span><span class="sxs-lookup"><span data-stu-id="e60e3-138">**Applicability**</span></span> | <span data-ttu-id="e60e3-139">**范围内服务**</span><span class="sxs-lookup"><span data-stu-id="e60e3-139">**In-scope services**</span></span> |
|:------------------|:----------------------|
| <span data-ttu-id="e60e3-140">**Office 365**</span><span class="sxs-lookup"><span data-stu-id="e60e3-140">**Office 365**</span></span> | <span data-ttu-id="e60e3-141">合规性管理器、客户密码箱、Delve、Exchange Online Protection、Exchange Online、Forms、Griffin、身份管理器、密码箱 (Torus)、Microsoft Teams、MyAnalytics、Office 365 客户门户、Office 365 微服务（包括但不限于 Kaizala、ObjectStore、Sway、PowerPoint Online 文档服务、查询批注服务、学校数据同步、Siphon、语音、StaffHub、可扩展应用程序计划）、Office Online、Office 服务基础结构、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、Project Online、使用客户密钥进行服务加密、SharePoint Online、Skype for Business</span><span class="sxs-lookup"><span data-stu-id="e60e3-141">Compliance Manager, Customer Lockbox, Delve, Exchange Online Protection, Exchange Online, Forms, Griffin, Identity Manager, Lockbox (Torus), Microsoft Teams, MyAnalytics, Office 365 Customer Portal, Office 365 Microservices (including but not limited to Kaizala, ObjectStore, Sway, PowerPoint Online Document Service, Query Annotation Service, School Data Sync, Siphon, Speech, StaffHub, eXtensible Application Program), Office Online, Office Services Infrastructure, OneDrive for Business, Planner, PowerApps, Power Automate, Power BI, Project Online, Service Encryption with Customer Key, SharePoint Online, Skype for Business</span></span> |
| <span data-ttu-id="e60e3-142">**GCC**</span><span class="sxs-lookup"><span data-stu-id="e60e3-142">**GCC**</span></span> | <span data-ttu-id="e60e3-143">Azure Active Directory、合规性管理器、Delve、Exchange Online、</span><span class="sxs-lookup"><span data-stu-id="e60e3-143">Azure Active Directory, Compliance Manager, Delve, Exchange Online,</span></span> 
<span data-ttu-id="e60e3-144">、Microsoft Defender for Office 365、Microsoft Teams、MyAnalytics、Office 365 高级合规版附加产品、Office 365 安全与合规中心、Office Online、Office Pro Plus、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、SharePoint Online、Skype for Business、Stream</span><span class="sxs-lookup"><span data-stu-id="e60e3-144">, Microsoft Defender for Office 365, Microsoft Teams, MyAnalytics, Office 365 Advanced Compliance add-on, Office 365 Security & Compliance Center, Office Online, Office Pro Plus, OneDrive for Business, Planner, PowerApps, Power Automate, Power BI, SharePoint Online, Skype for Business, Stream</span></span> |
| <span data-ttu-id="e60e3-145">**GCC 高级**</span><span class="sxs-lookup"><span data-stu-id="e60e3-145">**GCC High**</span></span> | <span data-ttu-id="e60e3-146">Azure Active Directory、Exchange Online、Flow、Microsoft Defender for Office 365、Microsoft Teams、Office 365 高级合规版附加产品、Office 365 安全与合规中心、Office Online、Office Pro Plus、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、SharePoint Online、Skype for Business</span><span class="sxs-lookup"><span data-stu-id="e60e3-146">Azure Active Directory, Exchange Online, Flow, Microsoft Defender for Office 365, Microsoft Teams, Office 365 Advanced Compliance add-on, Office 365 Security & Compliance Center, Office Online, Office Pro Plus, OneDrive for Business, Planner, PowerApps, Power Automate, Power BI, SharePoint Online, Skype for Business</span></span> |
| <span data-ttu-id="e60e3-147">**DoD**</span><span class="sxs-lookup"><span data-stu-id="e60e3-147">**DoD**</span></span> | <span data-ttu-id="e60e3-148">Azure Active Directory、Exchange Online、Microsoft Defender for Office 365、Microsoft Teams、Office 365 高级合规版附加产品、Office 365 安全与合规中心、Office Online、Office Pro Plus、OneDrive for Business、Planner、Power Automate、Power BI、SharePoint Online、Skype for Business</span><span class="sxs-lookup"><span data-stu-id="e60e3-148">Azure Active Directory, Exchange Online, Microsoft Defender for Office 365, Microsoft Teams, Office 365 Advanced Compliance add-on, Office 365 Security & Compliance Center, Office Online, Office Pro Plus, OneDrive for Business, Planner, Power Automate, Power BI, SharePoint Online, Skype for Business</span></span> |

### <a name="office-365-audit-reports"></a><span data-ttu-id="e60e3-149">Office 365 审核报告</span><span class="sxs-lookup"><span data-stu-id="e60e3-149">Office 365 audit reports</span></span>

- [<span data-ttu-id="e60e3-150">Office 365 Core - SSAE 18 SOC 3 报告</span><span class="sxs-lookup"><span data-stu-id="e60e3-150">Office 365 Core - SSAE 18 SOC 3 Report</span></span>](https://aka.ms/o365SOC-3)
- [<span data-ttu-id="e60e3-151">请参阅过渡函和其他审核报告</span><span class="sxs-lookup"><span data-stu-id="e60e3-151">See bridge letters and additional audit reports</span></span>](https://aka.ms/auditreports)

<span data-ttu-id="e60e3-152">必须要有 Office 365 或 Office 365 美国政府版的现有订阅或免费试用帐户，才能根据需要下载 SOC 1 和 SOC 2 证明报告和任何过渡函。</span><span class="sxs-lookup"><span data-stu-id="e60e3-152">You must have an existing subscription or free trial account in Office 365 or Office 365 U.S. Government to download SOC 1 and SOC 2 attestation reports and any bridge letters as needed.</span></span>

### <a name="frequently-asked-questions"></a><span data-ttu-id="e60e3-153">常见问题解答</span><span class="sxs-lookup"><span data-stu-id="e60e3-153">Frequently asked questions</span></span>

<span data-ttu-id="e60e3-154">**Office 365 SOC 报告多久发布一次？**</span><span class="sxs-lookup"><span data-stu-id="e60e3-154">**How often are Office 365 SOC reports issued?**</span></span>

<span data-ttu-id="e60e3-155">Office 365 和其他联机服务的 SOC 报告基于 12 个月的滚动时段（审核期），新报告每半年发布一次（期限为 3 月 31 日和 9 月 30 日）。</span><span class="sxs-lookup"><span data-stu-id="e60e3-155">SOC reports for Office 365 and other online services are based on a rolling 12-month run window (audit period) with new reports issued semi-annually (period ends are March 31 and September 30).</span></span> <span data-ttu-id="e60e3-156">*过渡函* 每季度发布一次，以涵盖前面的 3 个月。</span><span class="sxs-lookup"><span data-stu-id="e60e3-156">*Bridge letters* are issued each quarter to cover the prior three-month period.</span></span> <span data-ttu-id="e60e3-157">例如，1 月的过渡函涵盖 10 月 1 日到 12 月 31 日，4 月的过渡函涵盖 1 月 1 日到 3 月 31 日，7 月的过渡函涵盖 4 月 1 日到 6 月 30 日，10 月的过渡函涵盖 7 月 1 日到 9 月 30 日。</span><span class="sxs-lookup"><span data-stu-id="e60e3-157">For example, the January letter covers 1-Oct through 31-Dec, the April letter covers 1-Jan through 31-Mar, the July letter covers 1-Apr through 30-Jun, and the October letter covers 1-Jul through 30-Sep.</span></span>

<span data-ttu-id="e60e3-158">**在哪里可以获取 Office 365 SOC 审核文档（包括过渡函）？**</span><span class="sxs-lookup"><span data-stu-id="e60e3-158">**Where can I get the Office 365 SOC audit documentation including bridge letters?**</span></span> <span data-ttu-id="e60e3-159">有关审核文档的链接，请参阅审核报告部分。</span><span class="sxs-lookup"><span data-stu-id="e60e3-159">For links to audit documentation, see the audit report section.</span></span> <span data-ttu-id="e60e3-160">必须要有 Office 365 或 [Office](https://azure.microsoft.com/global-infrastructure/government/request/) 365 美国政府版的现有订阅或免费试用帐户才能登录。</span><span class="sxs-lookup"><span data-stu-id="e60e3-160">You must have an existing subscription or free trial account in Office 365or [Office](https://azure.microsoft.com/global-infrastructure/government/request/) 365 U.S. Government to login.</span></span> <span data-ttu-id="e60e3-161">然后，可以下载审核证书、评估报告和其他适用文档，以帮助你满足自己的法规要求。</span><span class="sxs-lookup"><span data-stu-id="e60e3-161">You can then download audit certificates, assessment reports, and other applicable documents to help you with your own regulatory requirements.</span></span>

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a><span data-ttu-id="e60e3-162">使用 Microsoft 合规性管理器评估风险</span><span class="sxs-lookup"><span data-stu-id="e60e3-162">Use Microsoft Compliance Manager to assess your risk</span></span>

<span data-ttu-id="e60e3-163">[Microsoft 合规性管理器](/microsoft-365/compliance/compliance-manager)是 [Microsoft 365 合规中心](/microsoft-365/compliance/microsoft-365-compliance-center)中的一项预览功能，旨在帮助你了解组织的合规情况并采取措施帮助降低风险。</span><span class="sxs-lookup"><span data-stu-id="e60e3-163">[Microsoft Compliance Manager](/microsoft-365/compliance/compliance-manager) is a feature in the [Microsoft 365 compliance center](/microsoft-365/compliance/microsoft-365-compliance-center) to help you understand your organization's compliance posture and take actions to help reduce risks.</span></span> <span data-ttu-id="e60e3-164">合规性管理器提供了一个高级模板，用于对此法规建立评估。</span><span class="sxs-lookup"><span data-stu-id="e60e3-164">Compliance Manager offers a premium template for building an assessment for this regulation.</span></span> <span data-ttu-id="e60e3-165">在合规性管理器的“**评估模板**”页面中找到模板。</span><span class="sxs-lookup"><span data-stu-id="e60e3-165">Find the template in the **assessment templates** page in Compliance Manager.</span></span> <span data-ttu-id="e60e3-166">了解如何[在合规性管理器中建立评估](/microsoft-365/compliance/compliance-manager-assessments)。</span><span class="sxs-lookup"><span data-stu-id="e60e3-166">Learn how to [build assessments in Compliance Manager](/microsoft-365/compliance/compliance-manager-assessments).</span></span>

### <a name="resources"></a><span data-ttu-id="e60e3-167">资源</span><span class="sxs-lookup"><span data-stu-id="e60e3-167">Resources</span></span>

- [<span data-ttu-id="e60e3-168">服务信任门户审核报告</span><span class="sxs-lookup"><span data-stu-id="e60e3-168">Service Trust Portal audit reports</span></span>](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3)
- [<span data-ttu-id="e60e3-169">适用于服务组织的 AICPA SOC</span><span class="sxs-lookup"><span data-stu-id="e60e3-169">AICPA SOC for Service Organizations</span></span>](https://www.aicpa.org/interestareas/frc/assuranceadvisoryservices/socforserviceorganizations.html)
- [<span data-ttu-id="e60e3-170">SSAE 第 18 号证明标准：阐明和准则修订（AICPA 专业标准）</span><span class="sxs-lookup"><span data-stu-id="e60e3-170">SSAE No. 18, Attestation Standards: Clarification and Recodification (AICPA Professional Standards)</span></span>](https://www.aicpa.org/Research/Standards/AuditAttest/DownloadableDocuments/SSAE_No_18.pdf)
- <span data-ttu-id="e60e3-171">[SOC 2 报告：对服务组织中安全性、可用性、处理完整性、机密性或隐私相关的控制进行的检验（AICPA 指南）](https://future.aicpa.org/cpe-learning/publication/soc-2-reporting-on-an-examination-of-controls-at-a-service-organization-relevant-to-security-availability-processing-integrity-confidentiality-or-privacy-OPL)（可供购买）</span><span class="sxs-lookup"><span data-stu-id="e60e3-171">[SOC 2 Reporting on an Examination of Controls at a Service Organization Relevant to Security, Availability, Processing Integrity, Confidentiality, or Privacy (AICPA Guide)](https://future.aicpa.org/cpe-learning/publication/soc-2-reporting-on-an-examination-of-controls-at-a-service-organization-relevant-to-security-availability-processing-integrity-confidentiality-or-privacy-OPL) (available for purchase)</span></span>
- [<span data-ttu-id="e60e3-172">TSP 第 100 节（AICPA，2017 年信任服务标准）</span><span class="sxs-lookup"><span data-stu-id="e60e3-172">TSP section 100 (AICPA, 2017 Trust Services Criteria)</span></span>](https://www.aicpa.org/content/dam/aicpa/interestareas/frc/assuranceadvisoryservices/downloadabledocuments/trust-services-criteria.pdf)
