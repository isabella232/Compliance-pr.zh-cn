---
title: NEN 7510
description: 荷兰组织必须证明对患者健康状况数据的控制符合 NEN 7510 标准。
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
ms.openlocfilehash: 79dc7fc209b85048189016a9bed8f5ca45b99bdb
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/12/2021
ms.locfileid: "53384452"
---
# <a name="nen-7510"></a><span data-ttu-id="8b1b9-104">NEN 7510</span><span class="sxs-lookup"><span data-stu-id="8b1b9-104">NEN 7510</span></span>

## <a name="nen-7510-overview"></a><span data-ttu-id="8b1b9-105">NEN 7510 概述</span><span class="sxs-lookup"><span data-stu-id="8b1b9-105">NEN 7510 overview</span></span>

<span data-ttu-id="8b1b9-106">荷兰处理患者健康状况信息的组织必须证明对此类数据的控制及组织自身都符合 NEN 7510 标准规定的要求。</span><span class="sxs-lookup"><span data-stu-id="8b1b9-106">Organizations in the Netherlands that process patient health information must demonstrate control over that data and their organization consistent with the requirements set out in the NEN 7510 standard.</span></span> <span data-ttu-id="8b1b9-107">Microsoft 本身不受 NEN 7510 约束，但医疗保健部门的云客户需要确定其有关基于 Microsoft 云构建的解决方案符合 NEN 7510。</span><span class="sxs-lookup"><span data-stu-id="8b1b9-107">Microsoft is not itself subject to NEN 7510, but its cloud customers in the healthcare sector need to establish that they comply with NEN 7510 regarding solutions built on the Microsoft Cloud.</span></span> <span data-ttu-id="8b1b9-108">Microsoft 云服务会进行各种定期认证和审核，其中一些包括与 NEN 7510 中所规定要求密切相关的元素。</span><span class="sxs-lookup"><span data-stu-id="8b1b9-108">Microsoft cloud services undergo various periodic certifications and audits, some of which include elements closely related to requirements specified in NEN 7510.</span></span>

## <a name="microsoft-and-nen-75102011"></a><span data-ttu-id="8b1b9-109">Microsoft 和 NEN 7510:2011</span><span class="sxs-lookup"><span data-stu-id="8b1b9-109">Microsoft and NEN 7510:2011</span></span>

<span data-ttu-id="8b1b9-110">Microsoft 已分析我们当前的认证和保证声明，并且已创建 [NEN 7510 覆盖报告](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=3285c45c-921c-49ad-b881-be43e0b70490&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_Compliance_Guides)（可在服务信任平台上获得），该报告将这些认证和保证声明与 NEN 7510 控制措施（微软作为云服务提供商对此负责）进行了对应。</span><span class="sxs-lookup"><span data-stu-id="8b1b9-110">Microsoft has analyzed our current certifications and assurance statements and created a [NEN 7510 coverage report](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=3285c45c-921c-49ad-b881-be43e0b70490&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_Compliance_Guides) (available on the Service Trust Platform), which maps those certifications and assurance statements against the NEN 7510 controls for which Microsoft is responsible as a cloud service provider.</span></span> <span data-ttu-id="8b1b9-111">本文档可帮助客户确定他们必须实施哪些其他控制措施，以确保用于存储或处理患者健康状况信息的 Microsoft 云服务符合 NEN 7510 标准。</span><span class="sxs-lookup"><span data-stu-id="8b1b9-111">This document can help customers determine which other controls they must implement to ensure that their use of Microsoft cloud services for the storage or processing of patient health information complies with NEN 7510.</span></span>

<span data-ttu-id="8b1b9-112">了解如何借助 Azure 安全性和合规性蓝图加快 NEN 7510 部署：[下载 Microsoft 云：Azure 和 Office 365 NEN7510-2011 标准覆盖用户指南](https://aka.ms/Azure-NEN7510-2011)</span><span class="sxs-lookup"><span data-stu-id="8b1b9-112">Learn how to accelerate your NEN 7510 deployment with our Azure Security and Compliance Blueprints: [Download the Microsoft Cloud: Azure and Office 365 NEN7510-2011 Standard Coverage User Guide](https://aka.ms/Azure-NEN7510-2011)</span></span>

## <a name="microsoft-in-scope-cloud-platforms--services"></a><span data-ttu-id="8b1b9-113">Microsoft 范围内的云平台和云服务</span><span class="sxs-lookup"><span data-stu-id="8b1b9-113">Microsoft in-scope cloud platforms & services</span></span>

- <span data-ttu-id="8b1b9-114">Azure 与 Azure 政府</span><span class="sxs-lookup"><span data-stu-id="8b1b9-114">Azure and Azure Government</span></span>
- <span data-ttu-id="8b1b9-115">Intune</span><span class="sxs-lookup"><span data-stu-id="8b1b9-115">Intune</span></span>
- <span data-ttu-id="8b1b9-116">Office 365</span><span class="sxs-lookup"><span data-stu-id="8b1b9-116">Office 365</span></span>

## <a name="office-365-and-iso-27001"></a><span data-ttu-id="8b1b9-117">Office 365 和 ISO 27001</span><span class="sxs-lookup"><span data-stu-id="8b1b9-117">Office 365 and ISO 27001</span></span>

### <a name="office-365-cloud-environments"></a><span data-ttu-id="8b1b9-118">Office 365 云环境</span><span class="sxs-lookup"><span data-stu-id="8b1b9-118">Office 365 cloud environments</span></span>

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a><span data-ttu-id="8b1b9-119">Office 365 适用性和范围内的服务</span><span class="sxs-lookup"><span data-stu-id="8b1b9-119">Office 365 applicability and in-scope services</span></span>

<span data-ttu-id="8b1b9-120">使用下表确定 Office 365 服务和订阅的适用性：</span><span class="sxs-lookup"><span data-stu-id="8b1b9-120">Use the following table to determine applicability for your Office 365 services and subscription:</span></span>

| <span data-ttu-id="8b1b9-121">**适用性**</span><span class="sxs-lookup"><span data-stu-id="8b1b9-121">**Applicability**</span></span> | <span data-ttu-id="8b1b9-122">**范围内服务**</span><span class="sxs-lookup"><span data-stu-id="8b1b9-122">**In-scope services**</span></span> |
|:------------------|:----------------------|
| <span data-ttu-id="8b1b9-123">**Office 365**</span><span class="sxs-lookup"><span data-stu-id="8b1b9-123">**Office 365**</span></span> | <span data-ttu-id="8b1b9-124">Azure 信息保护， Bookings， Delve， Exchange Online， Exchange Online Protection， Kaizala， Microsoft Analytics， Microsoft Booking， Microsoft Graph， Microsoft Teams， Microsoft 待办事项网页版， MyAnalytics， Office 365 云应用安全， Office 365 组， Office 365 视频， OneDrive for Business， Planner， Power Apps， Power Automate， Power BI for Office 365， PowerApps， SharePoint Online， Skype for Business， StaffHub，Stream，Sway，Yammer Enterprise</span><span class="sxs-lookup"><span data-stu-id="8b1b9-124">Azure Information Protection, Bookings, Delve, Exchange Online, Exchange Online Protection, Kaizala, Microsoft Analytics, Microsoft Booking, Microsoft Graph, Microsoft Teams, Microsoft To- Do for Web, MyAnalytics, Office 365 Cloud App Security, Office 365 Groups, Office 365 Video, OneDrive for Business,Planner, Power Apps, Power Automate, Power BI for Office 365, PowerApps, SharePoint Online, Skype for Business, StaffHub, Stream, Sway, Yammer Enterprise</span></span> |

## <a name="audits-reports-and-certificates"></a><span data-ttu-id="8b1b9-125">审核、报告和证书</span><span class="sxs-lookup"><span data-stu-id="8b1b9-125">Audits, reports, and certificates</span></span>

- [<span data-ttu-id="8b1b9-126">Azure 和 Office 365 NEN 7510:2011 标准覆盖</span><span class="sxs-lookup"><span data-stu-id="8b1b9-126">Azure and Office 365 NEN 7510:2011 Standard Coverage</span></span>](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=15d5a5fa-fbb6-4ea6-8126-2a2c684ae789&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_GRC_Assessment_Reports)

## <a name="frequently-asked-questions"></a><span data-ttu-id="8b1b9-127">常见问题</span><span class="sxs-lookup"><span data-stu-id="8b1b9-127">Frequently asked questions</span></span>

<span data-ttu-id="8b1b9-128">**使用 Microsoft 云服务的客户符合 NEN 7510 吗？**</span><span class="sxs-lookup"><span data-stu-id="8b1b9-128">**Is a customer that uses Microsoft cloud services compliant with NEN 7510?**</span></span>

<span data-ttu-id="8b1b9-129">证明 NEN 合规性是医疗保健组织（即“客户”）的责任。</span><span class="sxs-lookup"><span data-stu-id="8b1b9-129">Demonstrating NEN compliance is the responsibility of the healthcare organization (the 'customer').</span></span> <span data-ttu-id="8b1b9-130">使用云服务供应商时，客户通常要求供应商提供保证，并添加他们自己的（其他）技术和组织决策、选择和流程。</span><span class="sxs-lookup"><span data-stu-id="8b1b9-130">When using a cloud services vendor, customers typically demand assurances from the vendor, and add their own (other) technology and organizational decisions, choices, and processes.</span></span> <span data-ttu-id="8b1b9-131">这将使得客户对 NEN 7510 合规性进行全面评估，并可将其提交到第三方审核员进行审核或获得认证。</span><span class="sxs-lookup"><span data-stu-id="8b1b9-131">This effort results in an overall assessment by the customer on its NEN 7510 compliance, which can be submitted for review or certification to a third-party auditor.</span></span> <span data-ttu-id="8b1b9-132">NEN 7510 覆盖报告提供了关于 Microsoft 云服务覆盖哪些 NEN 7510 控制措施的深入分析，但这不包括端到端合规性。</span><span class="sxs-lookup"><span data-stu-id="8b1b9-132">The NEN 7510 coverage report provides insight into which NEN 7510 controls are covered by Microsoft cloud services, but, as such, does not cover end-to-end compliance.</span></span>

<span data-ttu-id="8b1b9-133">**Microsoft 是否符合 NEN 7510？**</span><span class="sxs-lookup"><span data-stu-id="8b1b9-133">**Is Microsoft compliant with NEN 7510?**</span></span>

<span data-ttu-id="8b1b9-134">NEN 7510 合规性的责任适用于荷兰医疗保健组织。</span><span class="sxs-lookup"><span data-stu-id="8b1b9-134">The responsibility for NEN 7510 compliance is applicable to Dutch Healthcare organizations.</span></span> <span data-ttu-id="8b1b9-135">它要求组织实施信息安全管理系统，并借助适当的技术和组织措施来应对风险。</span><span class="sxs-lookup"><span data-stu-id="8b1b9-135">It requires the organization to implement an information security management system and to address risk with appropriate technical and organizational measures.</span></span> <span data-ttu-id="8b1b9-136">对于作为云服务提供商角色的 Microsoft，NEN 7510 合规性不是目标，在技术上也不可行。</span><span class="sxs-lookup"><span data-stu-id="8b1b9-136">For Microsoft in its role as cloud service provider, NEN 7510 compliance is not the objective, nor is it technically feasible.</span></span> <span data-ttu-id="8b1b9-137">客户实施或使用 Microsoft 云服务时，这些服务可能在 NEN 7510 评估范围内。</span><span class="sxs-lookup"><span data-stu-id="8b1b9-137">When a customer implements or uses Microsoft cloud services, those services may be in scope of a NEN 7510 evaluation.</span></span> <span data-ttu-id="8b1b9-138">但是，组织必须添加自己的（其他）控制措施、选择和流程，它们是 NEN 7510 总体评估的一部分。</span><span class="sxs-lookup"><span data-stu-id="8b1b9-138">However, the organization must add its own (other) controls, choices, and processes that are part of the overall NEN 7510 evaluation.</span></span> <span data-ttu-id="8b1b9-139">该报告的目的是证明医疗保健实体可以采用符合 NEN 7510 的 Microsoft 云服务。</span><span class="sxs-lookup"><span data-stu-id="8b1b9-139">The objective of the report is to demonstrate that a Healthcare entity can adopt the Microsoft cloud services in a manner that is compliant with NEN 7510.</span></span>

<span data-ttu-id="8b1b9-140">**此报告不显示 100% 的覆盖。NEN 7510 合规性不可行？**</span><span class="sxs-lookup"><span data-stu-id="8b1b9-140">**The report does not show 100% coverage. Is NEN 7510 compliance not feasible?**</span></span>

<span data-ttu-id="8b1b9-141">Microsoft 云服务提供了很多控制措施，可帮助荷兰医疗保健组织满足其 NEN 7510 合规性需求。</span><span class="sxs-lookup"><span data-stu-id="8b1b9-141">Microsoft cloud services provide many controls that help organizations within Dutch Healthcare with their NEN 7510 compliance needs.</span></span> <span data-ttu-id="8b1b9-142">但是，组织需要通过其自己的实施选择、其他技术控件和管理流程来补充这些供应商的保证。</span><span class="sxs-lookup"><span data-stu-id="8b1b9-142">However, an organization needs to complement those vendor assurances with their own implementation choices, other technology controls, and administrative processes.</span></span> <span data-ttu-id="8b1b9-143">该报告显示了适用控制措施的完整列表中超过 94% 的直接覆盖。</span><span class="sxs-lookup"><span data-stu-id="8b1b9-143">The report shows already over 94% direct coverage of the full list of applicable controls.</span></span> <span data-ttu-id="8b1b9-144">对于其他控制措施，Microsoft 在报告中提供了有关这些控制措施如何证明合规性的指南。</span><span class="sxs-lookup"><span data-stu-id="8b1b9-144">For the remaining controls, Microsoft provides guidance in the report on how compliance with those controls can be demonstrated.</span></span>

> [!NOTE]
> <span data-ttu-id="8b1b9-145">实施控制措施的完整列表不是 NEN 7510 的主要目的（虽然 Microsoft Online Services 广泛覆盖确实有所帮助）。</span><span class="sxs-lookup"><span data-stu-id="8b1b9-145">Implementing the full list of controls is not the primary purpose of NEN 7510 (although the large coverage of Microsoft Online Services does help).</span></span> <span data-ttu-id="8b1b9-146">NEN 7510 强制实施基于风险的信息安全系统，供组织用于确定适用于他们的控制措施。</span><span class="sxs-lookup"><span data-stu-id="8b1b9-146">NEN 7510 mandates the implementation of a risk-based information security system that can be used by an organization to determine which controls are applicable to them.</span></span>

<span data-ttu-id="8b1b9-147">**NEN 7510 覆盖报告是否是具有法律约束力的文档？**</span><span class="sxs-lookup"><span data-stu-id="8b1b9-147">**Is the NEN 7510 coverage report a legal binding document?**</span></span>

<span data-ttu-id="8b1b9-148">否。</span><span class="sxs-lookup"><span data-stu-id="8b1b9-148">No.</span></span> <span data-ttu-id="8b1b9-149">它是客户内部 NEN 7510 保证流程的支持工具，有助于建立 NEN 7510 合规性是可行的信心和信任。</span><span class="sxs-lookup"><span data-stu-id="8b1b9-149">It is a supporting tool for the customer's internal NEN 7510 assurance process and helps to establish confidence and trust that NEN 7510 compliance is feasible.</span></span> <span data-ttu-id="8b1b9-150">该报告（由 KPMG 的独立审核员创建）属于说明性文档，并且包含法律免责声明。</span><span class="sxs-lookup"><span data-stu-id="8b1b9-150">The report (created by independent auditor, KPMG) has a descriptive status and includes a legal disclaimer.</span></span>

<span data-ttu-id="8b1b9-151">**Microsoft 是否已为报告付费？**</span><span class="sxs-lookup"><span data-stu-id="8b1b9-151">**Did Microsoft pay for the report?**</span></span>

<span data-ttu-id="8b1b9-152">Microsoft 已在其全球保证与 NEN 7510 标准中的控制措施之间创建了对应关系。</span><span class="sxs-lookup"><span data-stu-id="8b1b9-152">Microsoft created a mapping between its global assurances to the controls in the NEN 7510 standard.</span></span> <span data-ttu-id="8b1b9-153">然后，Microsoft 聘用 KPMG 的一位独立审核员对与 NEN 7510 对应的控制措施进行独立审核，最终生成这份报告。</span><span class="sxs-lookup"><span data-stu-id="8b1b9-153">Microsoft then hired KPMG (an independent auditor) to perform an independent review on the control mapping to NEN 7510, which resulted in the report.</span></span>

<span data-ttu-id="8b1b9-154">**我们是否可以共享此报告？**</span><span class="sxs-lookup"><span data-stu-id="8b1b9-154">**Can we share this report?**</span></span>

<span data-ttu-id="8b1b9-155">该报告是根据保密协议 (NDA) 提供给你的，基于该协议，该报告仅供客户参考，并且不会通过 Microsoft 服务信任门户以外的其他渠道进行复制或披露。</span><span class="sxs-lookup"><span data-stu-id="8b1b9-155">The report is provided with you under a non-disclosure agreement (NDA), on the basis that it is for customer information only and that it will not be copied or disclosed via other channels than the Microsoft Service Trust Portal.</span></span>

<span data-ttu-id="8b1b9-156">客户可以在其合规性或保证流程中与自己的内部或外部审核员共享该报告。</span><span class="sxs-lookup"><span data-stu-id="8b1b9-156">Customers can share the report with their own internal or external auditor as part of their compliance or assurance processes.</span></span>

## <a name="resources"></a><span data-ttu-id="8b1b9-157">资源</span><span class="sxs-lookup"><span data-stu-id="8b1b9-157">Resources</span></span>

- [<span data-ttu-id="8b1b9-158">关于 NEN</span><span class="sxs-lookup"><span data-stu-id="8b1b9-158">About NEN</span></span>](https://www.nen.nl/About-NEN.htm)
- [<span data-ttu-id="8b1b9-159">NEN 7510:2011 标准</span><span class="sxs-lookup"><span data-stu-id="8b1b9-159">NEN 7510:2011 standard</span></span>](https://www.nen.nl/NEN-Shop-2/Standard/NEN-75102011-nl.htm)
- [<span data-ttu-id="8b1b9-160">Microsoft 信任中心内的合规性</span><span class="sxs-lookup"><span data-stu-id="8b1b9-160">Compliance on the Microsoft Trust Center</span></span>](https://www.microsoft.com/trust-center/compliance/compliance-overview)
