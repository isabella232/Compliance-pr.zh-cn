---
title: '美国国防部 (DOD) 影响级别 2 (IL2) '
description: 了解 Microsoft 如何满足美国国防部 (DoD) 2 级 (IL2) 标准。
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
ms.openlocfilehash: 77e8cb50f815c167e50293d495b4a548a73d022e
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/12/2021
ms.locfileid: "53385698"
---
# <a name="department-of-defense-dod-impact-level-2-il2"></a><span data-ttu-id="b315c-104">美国国防部 (DOD) 影响级别 2 (IL2) </span><span class="sxs-lookup"><span data-stu-id="b315c-104">Department of Defense (DoD) Impact Level 2 (IL2)</span></span>

## <a name="dod-il2-overview"></a><span data-ttu-id="b315c-105">DoD IL2 概述</span><span class="sxs-lookup"><span data-stu-id="b315c-105">DoD IL2 overview</span></span>

<span data-ttu-id="b315c-106">美国国防部信息系统局 (DISA) 是美国国防部 (DoD) 的一个机构，负责开发和维护 DoD 云计算安全要求指南 [ (SRG) ](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html)。</span><span class="sxs-lookup"><span data-stu-id="b315c-106">The Defense Information Systems Agency (DISA) is an agency of the US Department of Defense (DoD) that is responsible for developing and maintaining the DoD Cloud Computing [Security Requirements Guide (SRG)](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html).</span></span> <span data-ttu-id="b315c-107">SRG 定义 DoD 用于评估云服务提供商 (CSP) 的安全状况的基准安全要求，以支持授权 DoD 临时授权 (PA) 的决定，该授权允许云解决方案提供商托管 DoD 任务。</span><span class="sxs-lookup"><span data-stu-id="b315c-107">The SRG defines the baseline security requirements used by DoD to assess the security posture of a cloud service provider (CSP), supporting the decision to grant a DoD Provisional Authorization (PA) that allows a CSP to host DoD missions.</span></span> <span data-ttu-id="b315c-108">它合并、取代并撤销以前发布的 DoD 云安全模型 (CSM) 并映射到 DoD 风险管理框架 (RMF) 。</span><span class="sxs-lookup"><span data-stu-id="b315c-108">It incorporates, supersedes, and rescinds the previously published DoD Cloud Security Model (CSM) and maps to the DoD Risk Management Framework (RMF).</span></span>

<span data-ttu-id="b315c-109">DISA 指导 DoD 机构和部门规划和授权 CSP 的使用。</span><span class="sxs-lookup"><span data-stu-id="b315c-109">DISA guides DoD agencies and departments in planning and authorizing the use of a CSP.</span></span> <span data-ttu-id="b315c-110">它还评估 CSP 产品/服务是否符合 SRG，SRG 是一个授权过程，CSP 可在其中提供概述其是否符合 DoD 标准的文档。</span><span class="sxs-lookup"><span data-stu-id="b315c-110">It also evaluates CSP offerings for compliance with the SRG, an authorization process whereby CSPs can furnish documentation outlining their compliance with DoD standards.</span></span> <span data-ttu-id="b315c-111">它在适当的时候 (DoD 临时授权) PA，因此 DoD 机构和支持组织可以使用云服务，而无需自行完成完全审批过程，从而节省时间和精力。</span><span class="sxs-lookup"><span data-stu-id="b315c-111">It issues DoD Provisional Authorizations (PAs) when appropriate, so DoD agencies and supporting organizations can use cloud services without having to go through a full approval process on their own, saving time and effort.</span></span>

<span data-ttu-id="b315c-112">有关购买和使用商业云计算服务的更新指南的[2014 年 12 月 15 日 DoD CIO](https://www.esi.mil/contentview.aspx?id=585)备忘录指出，"FedRAMP 将充当所有 DoD 云服务的最低安全基线"。</span><span class="sxs-lookup"><span data-stu-id="b315c-112">The [15 December 2014 DoD CIO memo](https://www.esi.mil/contentview.aspx?id=585) regarding *Updated Guidance on the Acquisition and Use of Commercial Cloud Computing Services* states that 'FedRAMP will serve as the minimum security baseline for all DoD cloud services'.</span></span> <span data-ttu-id="b315c-113">SRG 在所有信息影响级别使用 FedRAMP 中等基线 (IL) ，并考虑某些高基线。</span><span class="sxs-lookup"><span data-stu-id="b315c-113">The SRG uses the FedRAMP Moderate baseline at all information impact levels (IL) and considers the High Baseline at some.</span></span>

<span data-ttu-id="b315c-114">[SRG Section 5.1.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5SECURITYREQUIREMENTS) *DoD use of FedRAMP Security Controls* 指出，IL2 信息可能托管在一个 CSP 中，其中最少具有 FedRAMP 中等 PA 和 DoD 级别 2 PA，但需遵守第 5.6.2 节中列出的人员安全要求。</span><span class="sxs-lookup"><span data-stu-id="b315c-114">[SRG Section 5.1.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5SECURITYREQUIREMENTS) *DoD use of FedRAMP Security Controls* states that IL2 information may be hosted in a CSP that minimally holds a FedRAMP Moderate PA and a DoD Level 2 PA, subject to compliance with the personnel security requirements outlined in Section 5.6.2.</span></span> <span data-ttu-id="b315c-115">但是，此方法不会减少云解决方案提供商满足任务所有者要求的其他安全和集成要求。</span><span class="sxs-lookup"><span data-stu-id="b315c-115">However, this approach does not alleviate the CSP from meeting other security and integration requirements as required by the Mission Owner.</span></span> <span data-ttu-id="b315c-116">根据 [SRG 5.2.2.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5.2LegalConsiderations) *IL2* 位置和分离要求，FedRAMP 中等 PA 充分涵盖了 DoD IL2 PA，因此不会为 IL2 PA 额外评估这些要求。</span><span class="sxs-lookup"><span data-stu-id="b315c-116">According to [SRG Section 5.2.2.1](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html#5.2LegalConsiderations) *IL2 Location and Separation Requirements*, DoD IL2 PA is adequately covered by a FedRAMP Moderate PA such that the requirements will not be additionally assessed for an IL2 PA.</span></span>

## <a name="microsoft-in-scope-cloud-platforms--services"></a><span data-ttu-id="b315c-117">Microsoft 范围内云平台&服务</span><span class="sxs-lookup"><span data-stu-id="b315c-117">Microsoft in-scope cloud platforms & services</span></span>

- <span data-ttu-id="b315c-118">Azure</span><span class="sxs-lookup"><span data-stu-id="b315c-118">Azure</span></span>
- <span data-ttu-id="b315c-119">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="b315c-119">Dynamics 365</span></span>
- <span data-ttu-id="b315c-120">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="b315c-120">Microsoft Cloud App Security</span></span>
- <span data-ttu-id="b315c-121">Microsoft Defender for Endpoint</span><span class="sxs-lookup"><span data-stu-id="b315c-121">Microsoft Defender for Endpoint</span></span>
- <span data-ttu-id="b315c-122">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="b315c-122">Microsoft Graph</span></span>
- <span data-ttu-id="b315c-123">Microsoft Intune</span><span class="sxs-lookup"><span data-stu-id="b315c-123">Microsoft Intune</span></span>
- <span data-ttu-id="b315c-124">Microsoft Stream</span><span class="sxs-lookup"><span data-stu-id="b315c-124">Microsoft Stream</span></span>
- <span data-ttu-id="b315c-125">Office 365美国政府，Office 365美国政府 - 高</span><span class="sxs-lookup"><span data-stu-id="b315c-125">Office 365 U.S. Government, Office 365 U.S. Government - High</span></span>
- <span data-ttu-id="b315c-126">Power Apps</span><span class="sxs-lookup"><span data-stu-id="b315c-126">Power Apps</span></span>
- <span data-ttu-id="b315c-127">Power Automate</span><span class="sxs-lookup"><span data-stu-id="b315c-127">Power Automate</span></span>
- <span data-ttu-id="b315c-128">Power BI</span><span class="sxs-lookup"><span data-stu-id="b315c-128">Power BI</span></span>

## <a name="azure-dynamics-365-and-dod-il2"></a><span data-ttu-id="b315c-129">Azure、Dynamics 365 和 DoD IL2</span><span class="sxs-lookup"><span data-stu-id="b315c-129">Azure, Dynamics 365, and DoD IL2</span></span>

<span data-ttu-id="b315c-130">有关 Azure、Dynamics 365 和其他联机服务合规性的信息，请参阅 [Azure DoD IL2 产品](/azure/compliance/offerings/offering-dod-il2)/</span><span class="sxs-lookup"><span data-stu-id="b315c-130">For more information about Azure, Dynamics 365, and other online services compliance, see the [Azure DoD IL2 offering](/azure/compliance/offerings/offering-dod-il2).</span></span>

## <a name="office-365-and-dod-il2"></a><span data-ttu-id="b315c-131">Office 365 和 DoD IL2</span><span class="sxs-lookup"><span data-stu-id="b315c-131">Office 365 and DoD IL2</span></span>

### <a name="office-365-cloud-environments"></a><span data-ttu-id="b315c-132">Office 365云环境</span><span class="sxs-lookup"><span data-stu-id="b315c-132">Office 365 cloud environments</span></span>

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a><span data-ttu-id="b315c-133">Office 365适用性和范围内服务</span><span class="sxs-lookup"><span data-stu-id="b315c-133">Office 365 applicability and in-scope services</span></span>

<span data-ttu-id="b315c-134">使用下表确定您的 Office 365 服务和订阅的适用性：</span><span class="sxs-lookup"><span data-stu-id="b315c-134">Use the following table to determine applicability for your Office 365 services and subscription:</span></span>

| <span data-ttu-id="b315c-135">**适用性**</span><span class="sxs-lookup"><span data-stu-id="b315c-135">**Applicability**</span></span> | <span data-ttu-id="b315c-136">**范围内服务**</span><span class="sxs-lookup"><span data-stu-id="b315c-136">**In-scope services**</span></span> |
|:------------------|:----------------------|
| <span data-ttu-id="b315c-137">**GCC**</span><span class="sxs-lookup"><span data-stu-id="b315c-137">**GCC**</span></span> | <span data-ttu-id="b315c-138">活动源服务、必应 服务、Delve、Exchange Online Protection、Exchange Online、智能服务、Microsoft Teams、Office 365 客户门户、Office Online、Office 服务基础结构、Office 使用情况报告、OneDrive for Business、人员卡片、SharePoint Online、Skype for Business、Windows Ink</span><span class="sxs-lookup"><span data-stu-id="b315c-138">Activity Feed Service, Bing Services, Delve, Exchange Online Protection, Exchange Online, Intelligent Services, Microsoft Teams, Office 365 Customer Portal, Office Online, Office Service Infrastructure, Office Usage Reports, OneDrive for Business, People Card, SharePoint Online, Skype for Business, Windows Ink</span></span> |
| <span data-ttu-id="b315c-139">**GCC 高**</span><span class="sxs-lookup"><span data-stu-id="b315c-139">**GCC High**</span></span> | <span data-ttu-id="b315c-140">活动源服务、必应 服务、Delve、Exchange Online Protection、Exchange Online、智能服务、Microsoft Teams、Office 365 客户门户、Office Online、Office 服务基础结构、Office 使用情况报告、OneDrive for Business、人员卡片、SharePoint Online、Skype for Business、Windows Ink</span><span class="sxs-lookup"><span data-stu-id="b315c-140">Activity Feed Service, Bing Services, Delve, Exchange Online Protection, Exchange Online, Intelligent Services, Microsoft Teams, Office 365 Customer Portal, Office Online, Office Service Infrastructure, Office Usage Reports, OneDrive for Business, People Card, SharePoint Online, Skype for Business, Windows Ink</span></span> |

### <a name="resources"></a><span data-ttu-id="b315c-141">资源</span><span class="sxs-lookup"><span data-stu-id="b315c-141">Resources</span></span>

- [<span data-ttu-id="b315c-142">Microsoft 政府解决方案</span><span class="sxs-lookup"><span data-stu-id="b315c-142">Microsoft government solutions</span></span>](https://www.microsoft.com/enterprise/government)
- [<span data-ttu-id="b315c-143">DoD 云计算安全要求指南</span><span class="sxs-lookup"><span data-stu-id="b315c-143">DoD Cloud Computing Security Requirements Guide</span></span>](https://dl.dod.cyber.mil/wp-content/uploads/cloud/SRG/index.html)
- [<span data-ttu-id="b315c-144">FedRAMP 文档</span><span class="sxs-lookup"><span data-stu-id="b315c-144">FedRAMP documents</span></span>](https://www.fedramp.gov/documents/)
- <span data-ttu-id="b315c-145">[适用于信息系统和组织的 NIST SP 800-37](https://csrc.nist.gov/publications/detail/sp/800-37/rev-2/final) *风险管理框架：Life-Cycle和隐私的系统管理方法*</span><span class="sxs-lookup"><span data-stu-id="b315c-145">[NIST SP 800-37](https://csrc.nist.gov/publications/detail/sp/800-37/rev-2/final) *Risk Management Framework for Information Systems and Organizations: A System Life-Cycle Approach for Security and Privacy*</span></span>
- <span data-ttu-id="b315c-146">适用于信息系统和组织的安全和隐私 *控制* [NIST SP 800-53](https://csrc.nist.gov/Projects/risk-management/sp800-53-controls/release-search#!/800-53)</span><span class="sxs-lookup"><span data-stu-id="b315c-146">[NIST SP 800-53](https://csrc.nist.gov/Projects/risk-management/sp800-53-controls/release-search#!/800-53) *Security and Privacy Controls for Information Systems and Organizations*</span></span>
- <span data-ttu-id="b315c-147">[DoD Instruction 8510.01](https://www.esd.whs.mil/Portals/54/Documents/DD/issuances/dodi/851001p.pdf) *DoD Risk Management Framework (RMF) for DoD Information Technology (IT)*</span><span class="sxs-lookup"><span data-stu-id="b315c-147">[DoD Instruction 8510.01](https://www.esd.whs.mil/Portals/54/Documents/DD/issuances/dodi/851001p.pdf) *DoD Risk Management Framework (RMF) for DoD Information Technology (IT)*</span></span>
