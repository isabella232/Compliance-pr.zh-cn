---
title: ISO/IEC 27017:2015 信息安全控制措施行为守则
description: Microsoft 云服务已实施此信息安全控制措施行为守则。
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
ms.openlocfilehash: 6c431d856fc03f328148722c14dfc558082aacb5
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/12/2021
ms.locfileid: "53384722"
---
# <a name="isoiec-270172015-code-of-practice-for-information-security-controls"></a><span data-ttu-id="b3382-104">ISO/IEC 27017:2015 信息安全控制措施行为守则</span><span class="sxs-lookup"><span data-stu-id="b3382-104">ISO/IEC 27017:2015 Code of Practice for Information Security Controls</span></span>

## <a name="iso-iec-27017-overview"></a><span data-ttu-id="b3382-105">ISO-IEC 27017 概述</span><span class="sxs-lookup"><span data-stu-id="b3382-105">ISO-IEC 27017 Overview</span></span>

<span data-ttu-id="b3382-106">ISO/IEC 27017:2015 行为守则专为组织设计，用作在根据 ISO/IEC 27002:2013 实施云计算信息安全管理系统时选择云服务信息安全控制措施的参考。</span><span class="sxs-lookup"><span data-stu-id="b3382-106">The ISO/IEC 27017:2015 code of practice is designed for organizations to use as a reference for selecting cloud services information security controls when implementing a cloud computing information security management system based on ISO/IEC 27002:2013.</span></span> <span data-ttu-id="b3382-107">此外，云服务提供商还可将其用作实施公认的保护控制措施的指南文档。</span><span class="sxs-lookup"><span data-stu-id="b3382-107">It can also be used by cloud service providers as a guidance document for implementing commonly accepted protection controls.</span></span>

<span data-ttu-id="b3382-108">此国际标准基于 ISO/IEC 27002 提供了特定于云的附加实施指南，并针对 ISO/IEC 27002:2013 第 5-18 条中特定于云的信息安全威胁和风险提供了附加控制措施、实施指南和其他信息。</span><span class="sxs-lookup"><span data-stu-id="b3382-108">This international standard provides additional cloud-specific implementation guidance based on ISO/IEC 27002, and provides additional controls to address cloud-specific information security threats and risks referring to clauses 5-18 in ISO/IEC 27002: 2013 for controls, implementation guidance, and other information.</span></span> <span data-ttu-id="b3382-109">具体来说，此标准提供了 ISO/IEC 27002 中有关 37 个控制措施的指南，以及在 ISO/IEC 27002 中未重复的 7 个新控制措施。</span><span class="sxs-lookup"><span data-stu-id="b3382-109">Specifically, this standard provides guidance on 37 controls in ISO/IEC 27002, and it also features seven new controls that are not duplicated in ISO/IEC 27002.</span></span> <span data-ttu-id="b3382-110">这些新控制措施可解决以下重要方面：</span><span class="sxs-lookup"><span data-stu-id="b3382-110">These new controls address the following important areas:</span></span>

- <span data-ttu-id="b3382-111">云计算环境中的共享角色和职责</span><span class="sxs-lookup"><span data-stu-id="b3382-111">Shared roles and responsibilities within a cloud computing environment</span></span>
- <span data-ttu-id="b3382-112">合同终止时删除和退回云服务客户资产</span><span class="sxs-lookup"><span data-stu-id="b3382-112">Removal and return of cloud service customer assets upon contract termination</span></span>
- <span data-ttu-id="b3382-113">保护客户的虚拟环境并将其与其他客户的虚拟环境分离</span><span class="sxs-lookup"><span data-stu-id="b3382-113">Protection and separation of a customer's virtual environment from environments of other customers</span></span>
- <span data-ttu-id="b3382-114">强化要求以满足业务需求的虚拟机</span><span class="sxs-lookup"><span data-stu-id="b3382-114">Virtual machine hardening requirements to meet business needs</span></span>
- <span data-ttu-id="b3382-115">云计算环境的管理操作程序</span><span class="sxs-lookup"><span data-stu-id="b3382-115">Procedures for administrative operations of a cloud computing environment</span></span>
- <span data-ttu-id="b3382-116">使客户能够监视云计算环境中的相关活动</span><span class="sxs-lookup"><span data-stu-id="b3382-116">Enabling customers to monitor relevant activities within a cloud computing environment</span></span>
- <span data-ttu-id="b3382-117">协调虚拟和物理网络的安全管理</span><span class="sxs-lookup"><span data-stu-id="b3382-117">Alignment of security management for virtual and physical networks</span></span>

## <a name="microsoft-and-isoiec-27017"></a><span data-ttu-id="b3382-118">Microsoft 和 ISO/IEC 27017</span><span class="sxs-lookup"><span data-stu-id="b3382-118">Microsoft and ISO/IEC 27017</span></span>

<span data-ttu-id="b3382-119">ISO/IEC 27017 在为云服务提供商和云服务客户提供指南方面是独一无二的。</span><span class="sxs-lookup"><span data-stu-id="b3382-119">ISO/IEC 27017 is unique in providing guidance for both cloud service providers and cloud service customers.</span></span> <span data-ttu-id="b3382-120">此外，它还为云服务客户提供有关预期从云服务提供商获得内容的实用信息。</span><span class="sxs-lookup"><span data-stu-id="b3382-120">It also provides cloud service customers with practical information on what they should expect from cloud service providers.</span></span> <span data-ttu-id="b3382-121">通过确保客户了解云中的共同职责，他们可以直接从 ISO/IEC 27017 中受益。</span><span class="sxs-lookup"><span data-stu-id="b3382-121">Customers can benefit directly from ISO/IEC 27017 by ensuring they understand the shared responsibilities in the cloud.</span></span>

## <a name="microsoft-in-scope-cloud-platforms--services"></a><span data-ttu-id="b3382-122">Microsoft 范围内的云平台和云服务</span><span class="sxs-lookup"><span data-stu-id="b3382-122">Microsoft in-scope cloud platforms & services</span></span>

- [<span data-ttu-id="b3382-123">Azure、Azure 政府和 Azure 德国</span><span class="sxs-lookup"><span data-stu-id="b3382-123">Azure, Azure Government, and Azure Germany</span></span>](https://aka.ms/AzureCompliance)
- <span data-ttu-id="b3382-124">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="b3382-124">Microsoft Cloud App Security</span></span>
- [<span data-ttu-id="b3382-125">Dynamics 365、Dynamics 365 和 Dynamics 365 德国</span><span class="sxs-lookup"><span data-stu-id="b3382-125">Dynamics 365, Dynamics 365, and Dynamics 365 Germany</span></span>](https://aka.ms/d365-compliance-list)
- <span data-ttu-id="b3382-126">Intune</span><span class="sxs-lookup"><span data-stu-id="b3382-126">Intune</span></span>
- <span data-ttu-id="b3382-127">Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="b3382-127">Microsoft Defender for Endpoint</span></span>
- <span data-ttu-id="b3382-128">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="b3382-128">Microsoft Graph</span></span>
- <span data-ttu-id="b3382-129">Microsoft 医疗保健机器人</span><span class="sxs-lookup"><span data-stu-id="b3382-129">Microsoft Healthcare Bot</span></span>
- [<span data-ttu-id="b3382-130">Microsoft 托管桌面</span><span class="sxs-lookup"><span data-stu-id="b3382-130">Microsoft Managed Desktop</span></span>](/microsoft-365/managed-desktop/intro/compliance)
- <span data-ttu-id="b3382-131">Office 365、Office 365 美国政府版、Office 365 美国政府国防部版和 Office 365 德国版</span><span class="sxs-lookup"><span data-stu-id="b3382-131">Office 365, Office 365 U.S. Government, Office 365 U.S. Government Defense, and Office 365 Germany</span></span>
- <span data-ttu-id="b3382-132">Power Automate (以前称为 Microsoft Flow) 云服务，作为独立服务提供，或者随 Office 365 或 Dynamics 365 品牌计划或套件一并提供</span><span class="sxs-lookup"><span data-stu-id="b3382-132">Power Automate (formerly Microsoft Flow) cloud service either as a standalone service or as included in an Office 365 or Dynamics 365 branded plan or suite</span></span>
- <span data-ttu-id="b3382-133">PowerApps 云服务，作为独立服务提供，后者随 Office 365 或 Dynamics 365 品牌计划或套件一并提供</span><span class="sxs-lookup"><span data-stu-id="b3382-133">PowerApps cloud service either as a standalone service or as included in an Office 365 or Dynamics 365 branded plan or suite</span></span>
- <span data-ttu-id="b3382-134">Power BI 云服务，作为独立服务提供，或者随 Office 365 品牌计划或套件一并提供</span><span class="sxs-lookup"><span data-stu-id="b3382-134">Power BI cloud service either as a standalone service or as included in an Office 365 branded plan or suite</span></span>
- <span data-ttu-id="b3382-135">Power BI Embedded</span><span class="sxs-lookup"><span data-stu-id="b3382-135">Power BI Embedded</span></span>

## <a name="azure-dynamics-365-and-iso-270172015"></a><span data-ttu-id="b3382-136">Azure、Dynamics 365 和 ISO 27017:2015</span><span class="sxs-lookup"><span data-stu-id="b3382-136">Azure, Dynamics 365, and ISO 27017:2015</span></span>

<span data-ttu-id="b3382-137">有关 Azure、Dynamics 365 和其他联机服务合规性的详细信息，请参阅 [Azure ISO 27017 产品/服务](/azure/compliance/offerings/offering-iso-27017)。</span><span class="sxs-lookup"><span data-stu-id="b3382-137">For more information about Azure, Dynamics 365, and other online services compliance, see the [Azure ISO 27017 offering](/azure/compliance/offerings/offering-iso-27017).</span></span>

## <a name="office-365-and-iso-270172015"></a><span data-ttu-id="b3382-138">Office 365 和 ISO 27017:2015</span><span class="sxs-lookup"><span data-stu-id="b3382-138">Office 365 and ISO 27017:2015</span></span>

### <a name="office-365-cloud-environments"></a><span data-ttu-id="b3382-139">Office 365 云环境</span><span class="sxs-lookup"><span data-stu-id="b3382-139">Office 365 cloud environments</span></span>

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a><span data-ttu-id="b3382-140">Office 365 适用性和范围内的服务</span><span class="sxs-lookup"><span data-stu-id="b3382-140">Office 365 applicability and in-scope services</span></span>

<span data-ttu-id="b3382-141">使用下表确定 Office 365 服务和订阅的适用性：</span><span class="sxs-lookup"><span data-stu-id="b3382-141">Use the following table to determine applicability for your Office 365 services and subscription:</span></span>

| <span data-ttu-id="b3382-142">**适用性**</span><span class="sxs-lookup"><span data-stu-id="b3382-142">**Applicability**</span></span> | <span data-ttu-id="b3382-143">**范围内服务**</span><span class="sxs-lookup"><span data-stu-id="b3382-143">**In-scope services**</span></span> |
|:------------------|:----------------------|
| <span data-ttu-id="b3382-144">**Office 365**</span><span class="sxs-lookup"><span data-stu-id="b3382-144">**Office 365**</span></span> | <span data-ttu-id="b3382-145">Access Online、Azure Active Directory、Azure 通信服务、合规性管理器、客户密码箱、Delve、Exchange Online、Exchange Online Protection、Forms、Griffin、身份管理器、密码箱 (Torus)、Microsoft Defender for Office 365、Microsoft Teams、MyAnalytics、Office 365 高级合规版附加产品、Office 365 客户门户、Office 365 微服务（包括但不限于 Kaizala、ObjectStore、Sway、PowerPoint Online 文档服务、查询批注服务、学校数据同步、Siphon、语音、StaffHub、可扩展应用程序计划）、Office 365 安全与合规中心、Office Online、Office Pro Plus、Office 服务基础结构、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、Project Online、使用客户密钥进行服务加密、SharePoint Online、Skype for Business、Stream</span><span class="sxs-lookup"><span data-stu-id="b3382-145">Access Online, Azure Active Directory, Azure Communications Service, Compliance Manager, Customer Lockbox, Delve, Exchange Online, Exchange Online Protection, Forms, Griffin, Identity Manager, Lockbox (Torus), Microsoft Defender for Office 365, Microsoft Teams, MyAnalytics, Office 365 Advanced Compliance add-on, Office 365 Customer Portal, Office 365 Microservices (including but not limited to Kaizala, ObjectStore, Sway, PowerPoint Online Document Service, Query Annotation Service, School Data Sync, Siphon, Speech, StaffHub, eXtensible Application Program), Office 365 Security & Compliance Center, Office Online, Office Pro Plus, Office Services Infrastructure, OneDrive for Business, Planner, PowerApps, Power Automate, Power BI, Project Online, Service Encryption with Customer Key, SharePoint Online, Skype for Business, Stream</span></span> |
| <span data-ttu-id="b3382-146">**GCC**</span><span class="sxs-lookup"><span data-stu-id="b3382-146">**GCC**</span></span> | <span data-ttu-id="b3382-147">Azure Active Directory、Azure 通信服务、合规性管理器、Delve、Exchange Online、Forms、Microsoft Defender for Office 365、Microsoft Teams、MyAnalytics、Office 365 高级合规版附加产品、Office 365 安全与合规中心、Office Online、Office Pro Plus、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、SharePoint Online、Skype for Business、Stream</span><span class="sxs-lookup"><span data-stu-id="b3382-147">Azure Active Directory, Azure Communications Service, Compliance Manager, Delve, Exchange Online, Forms, Microsoft Defender for Office 365, Microsoft Teams, MyAnalytics, Office 365 Advanced Compliance add-on, Office 365 Security & Compliance Center, Office Online, Office Pro Plus, OneDrive for Business, Planner, PowerApps, Power Automate, Power BI, SharePoint Online, Skype for Business, Stream</span></span> |
| <span data-ttu-id="b3382-148">**GCC 高级**</span><span class="sxs-lookup"><span data-stu-id="b3382-148">**GCC High**</span></span> | <span data-ttu-id="b3382-149">Azure Active Directory、Azure 通信服务、Exchange Online、Forms、Microsoft Defender for Office 365、Microsoft Teams、Office 365 高级合规版附加产品、Office 365 安全与合规中心、Office Online、Office Pro Plus、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、SharePoint Online、Skype for Business</span><span class="sxs-lookup"><span data-stu-id="b3382-149">Azure Active Directory, Azure Communications Service, Exchange Online, Forms, Microsoft Defender for Office 365, Microsoft Teams, Office 365 Advanced Compliance add-on, Office 365 Security & Compliance Center, Office Online, Office Pro Plus, OneDrive for Business, Planner, PowerApps, Power Automate, Power BI, SharePoint Online, Skype for Business</span></span> |
| <span data-ttu-id="b3382-150">**DoD**</span><span class="sxs-lookup"><span data-stu-id="b3382-150">**DoD**</span></span> | <span data-ttu-id="b3382-151">Azure Active Directory、Azure 通信服务、Exchange Online、Forms、Microsoft Defender for Office 365、Microsoft Teams、Office 365 高级合规版附加产品、Office 365 安全与合规中心、Office Online、Office Pro Plus、OneDrive for Business、Planner、Power BI、SharePoint Online、Skype for Business</span><span class="sxs-lookup"><span data-stu-id="b3382-151">Azure Active Directory, Azure Communications Service, Exchange Online, Forms, Microsoft Defender for Office 365, Microsoft Teams, Office 365 Advanced Compliance add-on, Office 365 Security & Compliance Center, Office Online, Office Pro Plus, OneDrive for Business, Planner, Power BI, SharePoint Online, Skype for Business</span></span> |

### <a name="office-365-audits-reports-and-certificates"></a><span data-ttu-id="b3382-152">Office 365 审核、报告和证书</span><span class="sxs-lookup"><span data-stu-id="b3382-152">Office 365 audits, reports, and certificates</span></span>

<span data-ttu-id="b3382-153">作为 ISO/IEC 27001:2013 认证过程的一部分，每年都会对 Microsoft 云服务进行 ISO/IEC 27017:2015 行为守则审核。</span><span class="sxs-lookup"><span data-stu-id="b3382-153">Microsoft cloud services are audited once a year for the ISO/IEC 27017:2015 code of practice as part of the certification process for ISO/IEC 27001:2013.</span></span>

- [<span data-ttu-id="b3382-154">Office 365: ISO 27001、27018 和 27017 审核评估报告</span><span class="sxs-lookup"><span data-stu-id="b3382-154">Office 365: ISO 27001, 27018, and 27017 Audit Assessment Report</span></span>](https://aka.ms/o365isoreport)

### <a name="frequently-asked-questions"></a><span data-ttu-id="b3382-155">常见问题解答</span><span class="sxs-lookup"><span data-stu-id="b3382-155">Frequently asked questions</span></span>

<span data-ttu-id="b3382-156">**此标准适用于哪些人员？**</span><span class="sxs-lookup"><span data-stu-id="b3382-156">**To whom does the standard apply?**</span></span>

<span data-ttu-id="b3382-157">此行为守则为云服务提供商和云服务客户提供控制措施和实施指南。</span><span class="sxs-lookup"><span data-stu-id="b3382-157">This code of practice provides controls and implementation guidance for both cloud service providers and cloud service customers.</span></span> <span data-ttu-id="b3382-158">其格式结构类似于 ISO/IEC 27002:2013。</span><span class="sxs-lookup"><span data-stu-id="b3382-158">It is structured in a format similar to ISO/IEC 27002:2013.</span></span>

<span data-ttu-id="b3382-159">**在哪里可以查看 Microsoft 的 ISO/IEC 27017:2015 合规性信息？**</span><span class="sxs-lookup"><span data-stu-id="b3382-159">**Where can I view Microsoft's compliance information for ISO/IEC 27017:2015?**</span></span>

<span data-ttu-id="b3382-160">你可以下载适用于 Azure、Intune 和 Power BI 的 [ISO/IEC 27017:2015 证书](https://aka.ms/azureiso27017)。</span><span class="sxs-lookup"><span data-stu-id="b3382-160">You can download the [ISO/IEC 27017:2015 certificate](https://aka.ms/azureiso27017) for Azure, Intune, and Power BI.</span></span>

<span data-ttu-id="b3382-161">**能否在我所在组织的认证过程中使用 Microsoft 服务的 ISO/IEC 27017 合规性认证？**</span><span class="sxs-lookup"><span data-stu-id="b3382-161">**Can I use the ISO/IEC 27017 compliance of Microsoft services in my organization's certification process?**</span></span>

<span data-ttu-id="b3382-162">正确。</span><span class="sxs-lookup"><span data-stu-id="b3382-162">Yes.</span></span> <span data-ttu-id="b3382-163">如果你的企业正在寻求对任何 Microsoft 范围内企业云服务中部署的实施流程进行认证，则可以在你的合规性评估中利用 Microsoft 的相关认证。</span><span class="sxs-lookup"><span data-stu-id="b3382-163">If your business is seeking certification for implementations deployed on any Microsoft in-scope enterprise cloud services, you can use Microsoft's relevant certifications in your compliance assessment.</span></span> <span data-ttu-id="b3382-164">但是，你需要负责聘请评估方来评估合规性政策的实施情况，以及所在组织中的控制措施和流程。</span><span class="sxs-lookup"><span data-stu-id="b3382-164">However, you are responsible for engaging an assessor to evaluate your implementation for compliance, and for the controls and processes within your own organization.</span></span>

<span data-ttu-id="b3382-165">**如何获得适用审核报告的副本？**</span><span class="sxs-lookup"><span data-stu-id="b3382-165">**How can I get copies of the applicable audit reports?**</span></span>

<span data-ttu-id="b3382-166">[服务信任门户](https://aka.ms/stphelp)提供独立第三方审核报告和其他相关文档。</span><span class="sxs-lookup"><span data-stu-id="b3382-166">The [Service Trust Portal](https://aka.ms/stphelp) provides independent, third-party audit reports and other related documentation.</span></span> <span data-ttu-id="b3382-167">你可以使用门户下载和查看本文档以就自己的法规要求获得帮助。</span><span class="sxs-lookup"><span data-stu-id="b3382-167">You can use the portal to download and review this documentation for assistance with your own regulatory requirements.</span></span>

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a><span data-ttu-id="b3382-168">使用 Microsoft 合规性管理器评估风险</span><span class="sxs-lookup"><span data-stu-id="b3382-168">Use Microsoft Compliance Manager to assess your risk</span></span>

<span data-ttu-id="b3382-169">[Microsoft 合规性管理器](/microsoft-365/compliance/compliance-manager)是 [Microsoft 365 合规中心](/microsoft-365/compliance/microsoft-365-compliance-center)中的一项预览功能，旨在帮助你了解组织的合规情况并采取措施帮助降低风险。</span><span class="sxs-lookup"><span data-stu-id="b3382-169">[Microsoft Compliance Manager](/microsoft-365/compliance/compliance-manager) is a feature in the [Microsoft 365 compliance center](/microsoft-365/compliance/microsoft-365-compliance-center) to help you understand your organization's compliance posture and take actions to help reduce risks.</span></span> <span data-ttu-id="b3382-170">合规性管理器提供了一个高级模板，用于对此法规建立评估。</span><span class="sxs-lookup"><span data-stu-id="b3382-170">Compliance Manager offers a premium template for building an assessment for this regulation.</span></span> <span data-ttu-id="b3382-171">在合规性管理器的“**评估模板**”页面中找到模板。</span><span class="sxs-lookup"><span data-stu-id="b3382-171">Find the template in the **assessment templates** page in Compliance Manager.</span></span> <span data-ttu-id="b3382-172">了解如何[在合规性管理器中建立评估](/microsoft-365/compliance/compliance-manager-assessments)。</span><span class="sxs-lookup"><span data-stu-id="b3382-172">Learn how to [build assessments in Compliance Manager](/microsoft-365/compliance/compliance-manager-assessments).</span></span>

### <a name="resources"></a><span data-ttu-id="b3382-173">资源</span><span class="sxs-lookup"><span data-stu-id="b3382-173">Resources</span></span>

- [<span data-ttu-id="b3382-174">ISO/IEC 27017:2015 行为守则</span><span class="sxs-lookup"><span data-stu-id="b3382-174">ISO/IEC 27017:2015 code of practice</span></span>](https://www.iso.org/iso/iso_catalogue/catalogue_tc/catalogue_detail.htm?csnumber=43757)
- [<span data-ttu-id="b3382-175">Microsoft 在线服务条款</span><span class="sxs-lookup"><span data-stu-id="b3382-175">Microsoft Online Services Terms</span></span>](https://aka.ms/Online-Services-Terms)
- [<span data-ttu-id="b3382-176">Microsoft 信任中心内的合规性</span><span class="sxs-lookup"><span data-stu-id="b3382-176">Compliance on the Microsoft Trust Center</span></span>](https://www.microsoft.com/trust-center/compliance/compliance-overview)
