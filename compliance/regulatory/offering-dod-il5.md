---
title: '美国国防部 (DOD) 影响级别 5 (IL5) '
description: 了解 Microsoft 如何满足美国国防部 (DOD) 5 级 (IL5) 标准。
keywords: Microsoft 365, 合规性, 产品/服务
localization_priority: None
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
ms.openlocfilehash: 9f92ed19a22b7eff8a7e9988e66c51aea90d42ab
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/12/2021
ms.locfileid: "53385699"
---
# <a name="department-of-defense-dod-impact-level-5-il5"></a><span data-ttu-id="60a54-104">美国国防部 (DOD) 影响级别 5 (IL5) </span><span class="sxs-lookup"><span data-stu-id="60a54-104">Department of Defense (DoD) Impact Level 5 (IL5)</span></span>

## <a name="dod-il5-overview"></a><span data-ttu-id="60a54-105">DoD IL5 概述</span><span class="sxs-lookup"><span data-stu-id="60a54-105">DoD IL5 overview</span></span>

<span data-ttu-id="60a54-106">美国国防部信息系统局 (DISA) 是美国国防部 (DoD) 的一个机构，负责开发和维护 DoD 云计算安全要求指南 [ (SRG) ](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html)。</span><span class="sxs-lookup"><span data-stu-id="60a54-106">The Defense Information Systems Agency (DISA) is an agency of the US Department of Defense (DoD) that is responsible for developing and maintaining the DoD Cloud Computing [Security Requirements Guide (SRG)](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html).</span></span> <span data-ttu-id="60a54-107">SRG 定义 DoD 用于评估云服务提供商 (CSP) 的安全状况的基准安全要求，以支持授权 DoD 临时授权 (PA) 的决定，该授权允许云解决方案提供商托管 DoD 任务。</span><span class="sxs-lookup"><span data-stu-id="60a54-107">The SRG defines the baseline security requirements used by DoD to assess the security posture of a cloud service provider (CSP), supporting the decision to grant a DoD Provisional Authorization (PA) that allows a CSP to host DoD missions.</span></span> <span data-ttu-id="60a54-108">它合并、取代并撤销以前发布的 DoD 云安全模型 (CSM) 并映射到 DoD 风险管理框架 (RMF) 。</span><span class="sxs-lookup"><span data-stu-id="60a54-108">It incorporates, supersedes, and rescinds the previously published DoD Cloud Security Model (CSM) and maps to the DoD Risk Management Framework (RMF).</span></span>

<span data-ttu-id="60a54-109">DISA 指导 DoD 机构和部门规划和授权 CSP 的使用。</span><span class="sxs-lookup"><span data-stu-id="60a54-109">DISA guides DoD agencies and departments in planning and authorizing the use of a CSP.</span></span> <span data-ttu-id="60a54-110">它还评估 CSP 产品/服务是否符合 SRG，SRG 是一个授权过程，CSP 可在其中提供概述其是否符合 DoD 标准的文档。</span><span class="sxs-lookup"><span data-stu-id="60a54-110">It also evaluates CSP offerings for compliance with the SRG, an authorization process whereby CSPs can furnish documentation outlining their compliance with DoD standards.</span></span> <span data-ttu-id="60a54-111">它在适当的时候 (DoD 临时授权) PA，因此 DoD 机构和支持组织可以使用云服务，而无需自行完成完全审批过程，从而节省时间和精力。</span><span class="sxs-lookup"><span data-stu-id="60a54-111">It issues DoD Provisional Authorizations (PAs) when appropriate, so DoD agencies and supporting organizations can use cloud services without having to go through a full approval process on their own, saving time and effort.</span></span>

<span data-ttu-id="60a54-112">根据 [SRG 3.2](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#3.2InformationImpactLevels) *信息影响级别，IL5* 信息涵盖：</span><span class="sxs-lookup"><span data-stu-id="60a54-112">According to [SRG Section 3.2](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#3.2InformationImpactLevels) *Information Impact Levels*, IL5 information covers:</span></span>

- <span data-ttu-id="60a54-113">受控未分类 (CUI) 要求比 IL4 提供的保护级别更高</span><span class="sxs-lookup"><span data-stu-id="60a54-113">Controlled Unclassified Information (CUI) that requires higher level of protection than that afforded by IL4</span></span>
    - <span data-ttu-id="60a54-114">[CUI 注册表](https://www.archives.gov/cui)提供由执行部门保护的特定类别的信息，例如，CUI 类别列表中包括 20[多个类别分组](https://www.archives.gov/cui/registry/category-list)。</span><span class="sxs-lookup"><span data-stu-id="60a54-114">The [CUI Registry](https://www.archives.gov/cui) provides specific categories of information that is under protection by the Executive branch, for example, more than 20 category groupings are included in the [CUI category list](https://www.archives.gov/cui/registry/category-list).</span></span>
    - <span data-ttu-id="60a54-115">[NIST SP 800-171](https://csrc.nist.gov/publications/detail/sp/800-171/rev-2/final)保护非联盟系统和组织中的受控未分类信息旨在由联邦机构在与非联邦组织签订的合同或其他协议中使用。</span><span class="sxs-lookup"><span data-stu-id="60a54-115">[NIST SP 800-171](https://csrc.nist.gov/publications/detail/sp/800-171/rev-2/final) *Protecting Controlled Unclassified Information in Nonfederal Systems and Organizations* is intended for use by federal agencies in contracts or other agreements established with non-federal organizations.</span></span>

- <span data-ttu-id="60a54-116">国家安全系统 (NSS) </span><span class="sxs-lookup"><span data-stu-id="60a54-116">National Security Systems (NSS)</span></span>
    - <span data-ttu-id="60a54-117">[NIST SP 800-59](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-59.pdf)用于将信息系统标识为 *国家* /系统的指南提供了 NSS 的定义。</span><span class="sxs-lookup"><span data-stu-id="60a54-117">[NIST SP 800-59](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-59.pdf) *Guideline for Identifying an Information System as a National Security System* provides definitions of NSS.</span></span>
    - <span data-ttu-id="60a54-118">[CNSSI 1253](https://www.dcsa.mil/portals/91/documents/ctp/nao/CNSSI_No1253.pdf)针对国家安全系统的安全分类和控制选择提供有关联邦机构应应用于对国家安全信息进行分类的安全标准的指南。</span><span class="sxs-lookup"><span data-stu-id="60a54-118">[CNSSI 1253](https://www.dcsa.mil/portals/91/documents/ctp/nao/CNSSI_No1253.pdf) *Security Categorization and Control Selection for National Security Systems* provides guidance on the security standards that federal agencies should apply to categorize national security information.</span></span>

<span data-ttu-id="60a54-119">有关购买和使用商业云计算服务的更新指南的[2014 年 12 月 15 日 DoD CIO](https://www.esi.mil/contentview.aspx?id=585)备忘录指出，"FedRAMP 将充当所有 DoD 云服务的最低安全基线"。</span><span class="sxs-lookup"><span data-stu-id="60a54-119">The [15 December 2014 DoD CIO memo](https://www.esi.mil/contentview.aspx?id=585) regarding *Updated Guidance on the Acquisition and Use of Commercial Cloud Computing Services* states that 'FedRAMP will serve as the minimum security baseline for all DoD cloud services'.</span></span> <span data-ttu-id="60a54-120">SRG 在所有信息影响级别使用 FedRAMP 中等基线 (IL) ，并考虑某些高基线。</span><span class="sxs-lookup"><span data-stu-id="60a54-120">The SRG uses the FedRAMP Moderate baseline at all information impact levels (IL) and considers the High Baseline at some.</span></span>

<span data-ttu-id="60a54-121">[SRG Section 5.1.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5SECURITYREQUIREMENTS) *DoD use of FedRAMP Security Controls* 指出，FedRAMP High PA， with DoD FedRAMP+ controls and control enhancements (C/CEs) and requirements in the SRG， are used to assess CSPs to awarding a DoD PA at IL5.</span><span class="sxs-lookup"><span data-stu-id="60a54-121">[SRG Section 5.1.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5SECURITYREQUIREMENTS) *DoD use of FedRAMP Security Controls* states that a FedRAMP High PA, supplemented with DoD FedRAMP+ controls and control enhancements (C/CEs) and requirements in the SRG, are used to assess CSPs toward awarding a DoD PA at IL5.</span></span> <span data-ttu-id="60a54-122">无论使用什么 C/CE 基线作为 FedRAMP High PA 的基础，都需要评估和批准其他注意事项和/或要求，然后才能在 IL5 上授予 DoD PA。</span><span class="sxs-lookup"><span data-stu-id="60a54-122">No matter what C/CE baseline is used as the basis for a FedRAMP High PA, additional considerations and/or requirements will need to be assessed and approved before a DoD PA can be awarded at IL5.</span></span> <span data-ttu-id="60a54-123">具体而言， [表 2 中的 SRG 第 5.1.2](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5SECURITYREQUIREMENTS)节 *DoD FedRAMP+* 安全控制/增强功能指出，DoD IL5 PA 需要超过 FedRAMP 高基线的 10 个其他 C/CES。</span><span class="sxs-lookup"><span data-stu-id="60a54-123">Specifically, [SRG Section 5.1.2](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5SECURITYREQUIREMENTS) *DoD FedRAMP+ Security Controls/Enhancements* states in Table 2 that 10 additional C/CEs beyond the FedRAMP High baseline are required for a DoD IL5 PA.</span></span>

<span data-ttu-id="60a54-124">此外，根据 [SRG 5.2.2.3](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5.2LegalConsiderations) *IL5* 位置和分离要求，5 级 PA (必须满足以下要求) 其他要求：</span><span class="sxs-lookup"><span data-stu-id="60a54-124">Moreover, according to [SRG Section 5.2.2.3](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5.2LegalConsiderations) *IL5 Location and Separation Requirements*, the following requirements (among others) must be in place for a Level 5 PA:</span></span>

- <span data-ttu-id="60a54-125">DoD 与联邦政府租户/任务之间的虚拟/逻辑分离已足够。</span><span class="sxs-lookup"><span data-stu-id="60a54-125">Virtual/logical separation between DoD and Federal Government tenants / missions is sufficient.</span></span> <span data-ttu-id="60a54-126">需要租户/任务系统之间的虚拟/逻辑分离。</span><span class="sxs-lookup"><span data-stu-id="60a54-126">Virtual/logical separation between tenant/mission systems is required.</span></span>
- <span data-ttu-id="60a54-127">需要与非 DoD/非联邦 (（即公共、本地/州/州政府租户）) 分离。</span><span class="sxs-lookup"><span data-stu-id="60a54-127">Physical separation from non-DoD/non-Federal Government tenants (that is, public, local/state government tenants) is required.</span></span>
- <span data-ttu-id="60a54-128">CSP 将潜在 DoD 和社区信息的访问权限限制为美国公民的云解决方案提供商员工。</span><span class="sxs-lookup"><span data-stu-id="60a54-128">The CSP restricts potential access to DoD's and the community's information to CSP employees that are U.S. Citizens.</span></span>

## <a name="microsoft-in-scope-cloud-platforms--services"></a><span data-ttu-id="60a54-129">Microsoft 范围内云平台&服务</span><span class="sxs-lookup"><span data-stu-id="60a54-129">Microsoft in-scope cloud platforms & services</span></span>

- <span data-ttu-id="60a54-130">Azure</span><span class="sxs-lookup"><span data-stu-id="60a54-130">Azure</span></span>
- <span data-ttu-id="60a54-131">Dynamics 365 客户服务</span><span class="sxs-lookup"><span data-stu-id="60a54-131">Dynamics 365 Customer Service</span></span>
- <span data-ttu-id="60a54-132">Microsoft Defender for Endpoint (以前是 Microsoft Defender 高级威胁防护) </span><span class="sxs-lookup"><span data-stu-id="60a54-132">Microsoft Defender for Endpoint (formerly Microsoft Defender Advanced Threat Protection)</span></span>
- <span data-ttu-id="60a54-133">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="60a54-133">Microsoft Graph</span></span>
- <span data-ttu-id="60a54-134">Microsoft Stream</span><span class="sxs-lookup"><span data-stu-id="60a54-134">Microsoft Stream</span></span>
- <span data-ttu-id="60a54-135">Office 365 美国政府防御版</span><span class="sxs-lookup"><span data-stu-id="60a54-135">Office 365 U.S. Government Defense</span></span>
- <span data-ttu-id="60a54-136">Power Automate（以前称为 Microsoft Flow）</span><span class="sxs-lookup"><span data-stu-id="60a54-136">Power Automate (formerly Microsoft Flow)</span></span>
- <span data-ttu-id="60a54-137">Power BI</span><span class="sxs-lookup"><span data-stu-id="60a54-137">Power BI</span></span>

## <a name="azure-dynamics-365-and-dod-il5"></a><span data-ttu-id="60a54-138">Azure、Dynamics 365 和 DoD IL5</span><span class="sxs-lookup"><span data-stu-id="60a54-138">Azure, Dynamics 365, and DoD IL5</span></span>

<span data-ttu-id="60a54-139">有关 Azure、Dynamics 365 和其他在线服务合规性的信息，请参阅 Azure [DoD IL5 产品](/azure/compliance/offerings/offering-dod-il5)/</span><span class="sxs-lookup"><span data-stu-id="60a54-139">For more information about Azure, Dynamics 365, and other online services compliance, see the [Azure DoD IL5 offering](/azure/compliance/offerings/offering-dod-il5).</span></span>

## <a name="office-365-and-dod-il5"></a><span data-ttu-id="60a54-140">Office 365 和 DoD IL5</span><span class="sxs-lookup"><span data-stu-id="60a54-140">Office 365 and DoD IL5</span></span>

### <a name="office-365-cloud-environments"></a><span data-ttu-id="60a54-141">Office 365云环境</span><span class="sxs-lookup"><span data-stu-id="60a54-141">Office 365 cloud environments</span></span>

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a><span data-ttu-id="60a54-142">Office 365适用性和范围内服务</span><span class="sxs-lookup"><span data-stu-id="60a54-142">Office 365 applicability and in-scope services</span></span>

<span data-ttu-id="60a54-143">使用下表确定您的 Office 365 服务和订阅的适用性：</span><span class="sxs-lookup"><span data-stu-id="60a54-143">Use the following table to determine applicability for your Office 365 services and subscription:</span></span>

| <span data-ttu-id="60a54-144">**适用性**</span><span class="sxs-lookup"><span data-stu-id="60a54-144">**Applicability**</span></span> | <span data-ttu-id="60a54-145">**范围内服务**</span><span class="sxs-lookup"><span data-stu-id="60a54-145">**In-scope services**</span></span> |
|:------------------|:----------------------|
| <span data-ttu-id="60a54-146">**DoD**</span><span class="sxs-lookup"><span data-stu-id="60a54-146">**DoD**</span></span> | <span data-ttu-id="60a54-147">活动源服务、必应 服务、Exchange Online、Exchange Online Protection、智能服务、Microsoft Teams、Office 365 客户门户、Office Online、Office 服务基础结构、Office 使用情况报告、OneDrive for Business、人员卡片、SharePoint Online、Skype for Business、Windows Ink</span><span class="sxs-lookup"><span data-stu-id="60a54-147">Activity Feed Service, Bing Services, Exchange Online, Exchange Online Protection, Intelligent Services, Microsoft Teams, Office 365 Customer Portal, Office Online, Office Service Infrastructure, Office Usage Reports, OneDrive for Business, People Card, SharePoint Online, Skype for Business, Windows Ink</span></span> |

### <a name="attestation-documents"></a><span data-ttu-id="60a54-148">证明文档</span><span class="sxs-lookup"><span data-stu-id="60a54-148">Attestation documents</span></span>

<span data-ttu-id="60a54-149">美国政府客户可以通过Office 365包访问请求表单，直接从[FedRAMP 市场](https://marketplace.fedramp.gov/#!/products?sort=productName&productNameSearch=azure)请求获取美国政府防御 FedRAMP 文档。</span><span class="sxs-lookup"><span data-stu-id="60a54-149">US government customers can request Office 365 U.S. Government Defense FedRAMP documentation directly from the [FedRAMP Marketplace](https://marketplace.fedramp.gov/#!/products?sort=productName&productNameSearch=azure) by submitting a package access request form.</span></span> <span data-ttu-id="60a54-150">您必须具有 .gov 或 .更新电子邮件地址，以直接从 FedRAMP 访问 FedRAMP 安全包。</span><span class="sxs-lookup"><span data-stu-id="60a54-150">You must have a .gov or .mil email address to access a FedRAMP security package directly from FedRAMP.</span></span>

<span data-ttu-id="60a54-151">选择 FedRAMP 和 DoD 文档，包括系统安全计划 (SSP) 、连续监控报告、行动计划和里程碑 (POA M) 等，这些文档可供 NDA 下的客户使用，并可从服务信任门户审核报告 \& [- FedRAMP](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3) 报告部分获取待访问授权。</span><span class="sxs-lookup"><span data-stu-id="60a54-151">Select FedRAMP and DoD documentation, including System Security Plan (SSP), continuous monitoring reports, Plan of Action and Milestones (POA\&M), etc., is available to customers under NDA and pending access authorization from the Service Trust Portal [Audit Reports - FedRAMP Reports](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3) section.</span></span> <span data-ttu-id="60a54-152">请联系你的 Microsoft 帐户代表寻求帮助。</span><span class="sxs-lookup"><span data-stu-id="60a54-152">Contact your Microsoft account representative for assistance.</span></span>

### <a name="resources"></a><span data-ttu-id="60a54-153">资源</span><span class="sxs-lookup"><span data-stu-id="60a54-153">Resources</span></span>

- [<span data-ttu-id="60a54-154">Microsoft 政府解决方案</span><span class="sxs-lookup"><span data-stu-id="60a54-154">Microsoft government solutions</span></span>](https://www.microsoft.com/enterprise/government)
- [<span data-ttu-id="60a54-155">DoD 云计算安全要求指南</span><span class="sxs-lookup"><span data-stu-id="60a54-155">DoD Cloud Computing Security Requirements Guide</span></span>](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html)
- [<span data-ttu-id="60a54-156">FedRAMP 文档</span><span class="sxs-lookup"><span data-stu-id="60a54-156">FedRAMP documents</span></span>](https://www.fedramp.gov/documents/)
- <span data-ttu-id="60a54-157">[DoD Instruction 8510.01](https://www.esd.whs.mil/Portals/54/Documents/DD/issuances/dodi/851001p.pdf) *DoD Risk Management Framework (RMF) for DoD Information Technology (IT)*</span><span class="sxs-lookup"><span data-stu-id="60a54-157">[DoD Instruction 8510.01](https://www.esd.whs.mil/Portals/54/Documents/DD/issuances/dodi/851001p.pdf) *DoD Risk Management Framework (RMF) for DoD Information Technology (IT)*</span></span>
- <span data-ttu-id="60a54-158">[适用于信息系统和组织的 NIST SP 800-37](https://csrc.nist.gov/publications/detail/sp/800-37/rev-2/final) *风险管理框架：Life-Cycle和隐私的系统管理方法*</span><span class="sxs-lookup"><span data-stu-id="60a54-158">[NIST SP 800-37](https://csrc.nist.gov/publications/detail/sp/800-37/rev-2/final) *Risk Management Framework for Information Systems and Organizations: A System Life-Cycle Approach for Security and Privacy*</span></span>
- <span data-ttu-id="60a54-159">适用于信息系统和组织的安全和隐私 *控制* [NIST SP 800-53](https://csrc.nist.gov/Projects/risk-management/sp800-53-controls/release-search#!/800-53)</span><span class="sxs-lookup"><span data-stu-id="60a54-159">[NIST SP 800-53](https://csrc.nist.gov/Projects/risk-management/sp800-53-controls/release-search#!/800-53) *Security and Privacy Controls for Information Systems and Organizations*</span></span>
- <span data-ttu-id="60a54-160">[NIST SP 800-59](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-59.pdf)关于将信息系统 *识别为国家/系统的指南*</span><span class="sxs-lookup"><span data-stu-id="60a54-160">[NIST SP 800-59](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-59.pdf) *Guideline for Identifying an Information System as a National Security System*</span></span>
- <span data-ttu-id="60a54-161">[CNSSI 1253](https://www.dcsa.mil/portals/91/documents/ctp/nao/CNSSI_No1253.pdf) *针对国家* 安全系统的安全分类和控制选择</span><span class="sxs-lookup"><span data-stu-id="60a54-161">[CNSSI 1253](https://www.dcsa.mil/portals/91/documents/ctp/nao/CNSSI_No1253.pdf) *Security Categorization and Control Selection for National Security Systems*</span></span>
- <span data-ttu-id="60a54-162">[NIST SP 800-171](https://csrc.nist.gov/publications/detail/sp/800-171/rev-2/final)保护非系统和组织中的受控未分类 *信息*</span><span class="sxs-lookup"><span data-stu-id="60a54-162">[NIST SP 800-171](https://csrc.nist.gov/publications/detail/sp/800-171/rev-2/final) *Protecting Controlled Unclassified Information in Nonfederal Systems and Organizations*</span></span>
- <span data-ttu-id="60a54-163">受控的未分类 (CUI) [和](https://www.archives.gov/cui) CUI [类别列表](https://www.archives.gov/cui/registry/category-list)。</span><span class="sxs-lookup"><span data-stu-id="60a54-163">Controlled Unclassified Information (CUI) [Registry](https://www.archives.gov/cui) and CUI [category list](https://www.archives.gov/cui/registry/category-list).</span></span>
