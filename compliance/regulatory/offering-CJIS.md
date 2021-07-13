---
title: 犯罪犯罪信息服务 (CJIS) 安全策略
description: Microsoft 政府云服务遵守美国《刑事犯罪信息服务安全策略》
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
ms.openlocfilehash: 896202ea1f51d88d1871a2c7ff81f4ee1e620d17
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/12/2021
ms.locfileid: "53385362"
---
# <a name="criminal-justice-information-services-cjis-security-policy"></a><span data-ttu-id="601d2-104">犯罪犯罪信息服务 (CJIS) 安全策略</span><span class="sxs-lookup"><span data-stu-id="601d2-104">Criminal Justice Information Services (CJIS) Security Policy</span></span>

## <a name="cjis-overview"></a><span data-ttu-id="601d2-105">CJIS 概述</span><span class="sxs-lookup"><span data-stu-id="601d2-105">CJIS overview</span></span>

<span data-ttu-id="601d2-106">美国联邦调查局 () 的犯罪调查信息服务 (CJIS) 部门为州、当地和联邦执法机构和犯罪犯罪机构提供对犯罪情报 (CJI) （例如指纹记录和犯罪历史记录）的访问权限。</span><span class="sxs-lookup"><span data-stu-id="601d2-106">The Criminal Justice Information Services (CJIS) Division of the US Federal Bureau of Investigation (FBI) gives state, local, and federal law enforcement and criminal justice agencies access to criminal justice information (CJI) — for example, fingerprint records and criminal histories.</span></span> <span data-ttu-id="601d2-107">美国执法机构和其他政府机构必须确保他们使用云服务传输、存储或处理 CJI 符合 [CJIS](https://aka.ms/cjis-security-policy)安全策略，该安全策略建立了最低安全要求和控制来保护 CJI。</span><span class="sxs-lookup"><span data-stu-id="601d2-107">Law enforcement and other government agencies in the United States must ensure that their use of cloud services for the transmission, storage, or processing of CJI complies with the [CJIS Security Policy](https://aka.ms/cjis-security-policy), which establishes minimum security requirements and controls to safeguard CJI.</span></span>

<span data-ttu-id="601d2-108">CJIS 安全策略集成了国家标准和技术协会 NIST (的法规、联邦法律以及刑事犯罪社区的建议策略委员会) 决策。</span><span class="sxs-lookup"><span data-stu-id="601d2-108">The CJIS Security Policy integrates presidential and FBI directives, federal laws, and the criminal justice community's Advisory Policy Board decisions, along with guidance from the National Institute of Standards and Technology (NIST).</span></span> <span data-ttu-id="601d2-109">该策略会定期更新，以反映不断变化的安全要求。</span><span class="sxs-lookup"><span data-stu-id="601d2-109">The Policy is periodically updated to reflect evolving security requirements.</span></span>

<span data-ttu-id="601d2-110">CJIS 安全策略定义了 13 个私有承包商（如云服务提供商）必须评估的区域，以确定其对云服务的使用是否与 CJIS 要求一致。</span><span class="sxs-lookup"><span data-stu-id="601d2-110">The CJIS Security Policy defines 13 areas that private contractors such as cloud service providers must evaluate to determine if their use of cloud services can be consistent with CJIS requirements.</span></span> <span data-ttu-id="601d2-111">这些方面与 NIST 800-53 紧密对应，NIST 800-53 也是联邦风险和授权管理计划 [ (FedRAMP) ](offering-FedRAMP.md)的基础，该计划通过 Microsoft 政府云产品/服务认证。</span><span class="sxs-lookup"><span data-stu-id="601d2-111">These areas correspond closely to NIST 800-53, which is also the basis for the [Federal Risk and Authorization Management Program (FedRAMP)](offering-FedRAMP.md), a program under which Microsoft has been certified for its Government Cloud offerings.</span></span>

<span data-ttu-id="601d2-112">此外，处理 CJI 的所有私有承包商都必须签署 CJIS 安全附录，这是美国律师总署批准的统一协议，有助于确保安全策略要求的 CJI 的安全性和机密性。</span><span class="sxs-lookup"><span data-stu-id="601d2-112">In addition, all private contractors who process CJI must sign the CJIS Security Addendum, a uniform agreement approved by the US Attorney General that helps ensure the security and confidentiality of CJI required by the Security Policy.</span></span> <span data-ttu-id="601d2-113">它还承诺承包商维护与联邦和州法律、法规和标准一致的安全计划，并限制使用 CJI 的目的（政府机构提供 CJI 的目的）。</span><span class="sxs-lookup"><span data-stu-id="601d2-113">It also commits the contractor to maintaining a security program consistent with federal and state laws, regulations, and standards, and limits the use of CJI to the purposes for which a government agency provided it.</span></span>

## <a name="microsoft-and-cjis-security-policy"></a><span data-ttu-id="601d2-114">Microsoft 和 CJIS 安全策略</span><span class="sxs-lookup"><span data-stu-id="601d2-114">Microsoft and CJIS Security Policy</span></span>

<span data-ttu-id="601d2-115">Microsoft 使用 CJIS 信息协议签署 CJIS 安全附录。</span><span class="sxs-lookup"><span data-stu-id="601d2-115">Microsoft signs the CJIS Security Addendum in states with CJIS Information Agreements.</span></span> <span data-ttu-id="601d2-116">这些说明会告知负责遵守 CJIS 安全策略的州执法机构，Microsoft 的云安全控制如何帮助保护数据的整个生命周期，并确保对有权访问 CJI 的操作人员进行适当的背景调查。</span><span class="sxs-lookup"><span data-stu-id="601d2-116">These tell state law enforcement authorities responsible for compliance with CJIS Security Policy how Microsoft's cloud security controls help protect the full lifecycle of data and ensure appropriate background screening of operating personnel with access to CJI.</span></span> <span data-ttu-id="601d2-117">Microsoft 将继续与州政府合作，以签订 CJIS 信息协议。</span><span class="sxs-lookup"><span data-stu-id="601d2-117">Microsoft continues to work with state governments to enter into CJIS Information Agreements.</span></span>

<span data-ttu-id="601d2-118">Microsoft 已评估 Microsoft Azure Government、Microsoft Office 365 U.S. Government 和 Microsoft Dynamics 365 美国政府版的操作策略和过程，并证明他们在适用的服务协议中能够满足使用范围内服务的 FBI 要求的能力。</span><span class="sxs-lookup"><span data-stu-id="601d2-118">Microsoft has assessed the operational policies and procedures of Microsoft Azure Government, Microsoft Office 365 U.S. Government, and Microsoft Dynamics 365 U.S. Government, and will attest to their ability in the applicable services agreements to meet FBI requirements for the use of in-scope services.</span></span>

<span data-ttu-id="601d2-119">了解 Microsoft 云上 CJIS 安全策略的好处：[阅读使用 Clearedtec](https://customers.microsoft.com/story/genetec)清除犯罪调查</span><span class="sxs-lookup"><span data-stu-id="601d2-119">Learn about the benefits of CJIS Security policy on the Microsoft Cloud: [Read how Genetec cleared criminal investigations](https://customers.microsoft.com/story/genetec)</span></span>

## <a name="microsoft-in-scope-cloud-platforms--services"></a><span data-ttu-id="601d2-120">Microsoft 范围内云平台&服务</span><span class="sxs-lookup"><span data-stu-id="601d2-120">Microsoft in-scope cloud platforms & services</span></span>

- <span data-ttu-id="601d2-121">Azure 政府</span><span class="sxs-lookup"><span data-stu-id="601d2-121">Azure Government</span></span>
- <span data-ttu-id="601d2-122">Dynamics 365 美国政府版</span><span class="sxs-lookup"><span data-stu-id="601d2-122">Dynamics 365 U.S. Government</span></span>
- <span data-ttu-id="601d2-123">Office 365美国政府</span><span class="sxs-lookup"><span data-stu-id="601d2-123">Office 365 U.S. Government</span></span>
- <span data-ttu-id="601d2-124">Power BI 云服务，作为独立服务提供，后者随 Office 365 品牌计划或套件一并提供</span><span class="sxs-lookup"><span data-stu-id="601d2-124">Power BI cloud service either as a standalone service or as included in an Office 365 branded plan or suite</span></span>

## <a name="azure-dynamics-365-and-cjis"></a><span data-ttu-id="601d2-125">Azure、Dynamics 365 和 CJIS</span><span class="sxs-lookup"><span data-stu-id="601d2-125">Azure, Dynamics 365, and CJIS</span></span>

<span data-ttu-id="601d2-126">有关 Azure、Dynamics 365 和其他联机服务合规性的信息，请参阅 [Azure CJIS 产品](/azure/compliance/offerings/offering-cjis)。</span><span class="sxs-lookup"><span data-stu-id="601d2-126">For more information about Azure, Dynamics 365, and other online services compliance, see the [Azure CJIS offering](/azure/compliance/offerings/offering-cjis).</span></span>

## <a name="office-365-and-cjis"></a><span data-ttu-id="601d2-127">Office 365 和 CJIS</span><span class="sxs-lookup"><span data-stu-id="601d2-127">Office 365 and CJIS</span></span>

### <a name="office-365-cloud-environments"></a><span data-ttu-id="601d2-128">Office 365云环境</span><span class="sxs-lookup"><span data-stu-id="601d2-128">Office 365 cloud environments</span></span>

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a><span data-ttu-id="601d2-129">Office 365适用性和范围内服务</span><span class="sxs-lookup"><span data-stu-id="601d2-129">Office 365 applicability and in-scope services</span></span>

<span data-ttu-id="601d2-130">使用下表确定您的 Office 365 服务和订阅的适用性：</span><span class="sxs-lookup"><span data-stu-id="601d2-130">Use the following table to determine applicability for your Office 365 services and subscription:</span></span>

| <span data-ttu-id="601d2-131">**适用性**</span><span class="sxs-lookup"><span data-stu-id="601d2-131">**Applicability**</span></span> | <span data-ttu-id="601d2-132">**范围内服务**</span><span class="sxs-lookup"><span data-stu-id="601d2-132">**In-scope services**</span></span> |
|:------------------|:----------------------|
| <span data-ttu-id="601d2-133">**GCC**</span><span class="sxs-lookup"><span data-stu-id="601d2-133">**GCC**</span></span> | <span data-ttu-id="601d2-134">Azure Active Directory、合规性管理器、Delve、Exchange Online、Forms、Microsoft Defender for Office 365、Microsoft Teams、MyAnalytics、Office 365 高级合规版 加载项、Office 365 安全 & 合规性中心、Office Online、Office Pro Plus、OneDrive for Business、Planner、PowerApps、Power Automate、Power BI、SharePoint Online、Skype for Business、Stream</span><span class="sxs-lookup"><span data-stu-id="601d2-134">Azure Active Directory, Compliance Manager, Delve, Exchange Online, Forms, Microsoft Defender for Office 365, Microsoft Teams, MyAnalytics, Office 365 Advanced Compliance add-on, Office 365 Security & Compliance Center, Office Online, Office Pro Plus, OneDrive for Business, Planner, PowerApps, Power Automate, Power BI, SharePoint Online, Skype for Business, Stream</span></span> |

### <a name="office-365-audits-reports-and-certificates"></a><span data-ttu-id="601d2-135">Office 365审核、报告和证书</span><span class="sxs-lookup"><span data-stu-id="601d2-135">Office 365 audits, reports, and certificates</span></span>

<span data-ttu-id="601d2-136">MICROSOFT 不提供 Microsoft 遵守 CJIS 要求的认证。</span><span class="sxs-lookup"><span data-stu-id="601d2-136">The FBI does not offer certification of Microsoft compliance with CJIS requirements.</span></span> <span data-ttu-id="601d2-137">相反，Microsoft 证明包含在 Microsoft 与州 CJIS 颁发机构之间以及 Microsoft 与其客户之间的协议中。</span><span class="sxs-lookup"><span data-stu-id="601d2-137">Instead, a Microsoft attestation is included in agreements between Microsoft and a state's CJIS authority, and between Microsoft and its customers.</span></span>

[<span data-ttu-id="601d2-138">Microsoft CJIS 云要求</span><span class="sxs-lookup"><span data-stu-id="601d2-138">Microsoft CJIS Cloud Requirements</span></span>](https://aka.ms/MicrosoftCJISCloudRequirements)

### <a name="cjis-status-in-the-united-states-current-as-of-1152020"></a><span data-ttu-id="601d2-139">自 2020 年 11 月 5 (起，美国 CJIS 状态) </span><span class="sxs-lookup"><span data-stu-id="601d2-139">CJIS status in the United States (current as of 11/5/2020)</span></span>

<span data-ttu-id="601d2-140">45 个州以及具有管理协议（在地图上以绿色突出显示）的学区包括：</span><span class="sxs-lookup"><span data-stu-id="601d2-140">45 states and the District of Columbia with management agreements, highlighted on the map in green include:</span></span>

<span data-ttu-id="601d2-141">该州是，加利福尼亚、格鲁吉亚 哥伦比亚、爱达荷州、波利尼西亚、阿鲁巴岛、阿鲁巴基、马来尼西亚、剑桥、明尼西亚、圣文莱纳、内巴ska、剑桥、纽约、北尼西亚、北美、北达库塔、格林威斯、俄勒冈、密尔尼群岛、南尼西亚、格林纳西、底特律、华盛顿州、西尼西亚、华盛顿州和华盛顿州。</span><span class="sxs-lookup"><span data-stu-id="601d2-141">Alabama, Alaska, Arizona, Arkansas, California, Colorado, Connecticut, Florida, Georgia, Hawaii, Idaho, Illinois, Indiana, Iowa, Kansas, Kentucky, Maine, Massachusetts, Michigan, Minnesota, Mississippi, Missouri, Montana, Nebraska, Nevada, New Hampshire, New Jersey, New Mexico, New York, North Carolina, North Dakota, Oklahoma, Oregon, Pennsylvania, Rhode Island, South Carolina, Tennessee, Texas, Utah, Vermont, Virginia, Washington, West Virginia, Wisconsin, and the District of Columbia.</span></span>

<span data-ttu-id="601d2-142">Microsoft 承诺遵守适用的 CJIS 法规控制，允许犯罪犯罪组织实施基于云的解决方案，并符合 CJIS 安全策略 V5.9。</span><span class="sxs-lookup"><span data-stu-id="601d2-142">Microsoft's commitment to meeting the applicable CJIS regulatory controls allows Criminal Justice organizations to implement cloud-based solutions and be compliant with CJIS Security Policy V5.9.</span></span>

### <a name="frequently-asked-questions"></a><span data-ttu-id="601d2-143">常见问题解答</span><span class="sxs-lookup"><span data-stu-id="601d2-143">Frequently asked questions</span></span>

<span data-ttu-id="601d2-144">**在哪里可以请求合规性信息？**</span><span class="sxs-lookup"><span data-stu-id="601d2-144">**Where can I request compliance information?**</span></span>

<span data-ttu-id="601d2-145">有关你感兴趣的管辖地的信息，请与你的 Microsoft 帐户代表联系。</span><span class="sxs-lookup"><span data-stu-id="601d2-145">Contact your Microsoft account representative for information on the jurisdiction you are interested in.</span></span> <span data-ttu-id="601d2-146">有关 <cjis@microsoft.com> 当前哪些服务在哪些状态中可用的信息，请与联系人联系。</span><span class="sxs-lookup"><span data-stu-id="601d2-146">Contact <cjis@microsoft.com> for information on which services are currently available in which states.</span></span>

<span data-ttu-id="601d2-147">**Microsoft 如何证明其云服务支持符合我州的要求？**</span><span class="sxs-lookup"><span data-stu-id="601d2-147">**How does Microsoft demonstrate that its cloud services enable compliance with my state's requirements?**</span></span>

<span data-ttu-id="601d2-148">Microsoft 与州 CJIS Systems Agency 与 CSA (签署信息) ;你可以从你州 CSA 请求副本。</span><span class="sxs-lookup"><span data-stu-id="601d2-148">Microsoft signs an Information Agreement with a state CJIS Systems Agency (CSA); you may request a copy from your state's CSA.</span></span> <span data-ttu-id="601d2-149">此外，Microsoft 为客户提供了深入的安全、隐私和合规性信息。</span><span class="sxs-lookup"><span data-stu-id="601d2-149">In addition, Microsoft provides customers with in-depth security, privacy, and compliance information.</span></span> <span data-ttu-id="601d2-150">客户还可以查看独立审核员准备的安全和合规性报告，以便他们可以验证 Microsoft 是否实施了适用于相关审核 (如 ISO 27001) 安全控制措施。</span><span class="sxs-lookup"><span data-stu-id="601d2-150">Customers may also review security and compliance reports prepared by independent auditors so they can validate that Microsoft has implemented security controls (such as ISO 27001) appropriate to the relevant audit scope.</span></span>

<span data-ttu-id="601d2-151">**从何处着手执行我的机构合规性工作？**</span><span class="sxs-lookup"><span data-stu-id="601d2-151">**Where do I start with my agency's compliance effort?**</span></span>

<span data-ttu-id="601d2-152">[CJIS 安全策略](https://aka.ms/cjis-security-policy) 涵盖机构保护 CJI 必须采取的预防措施。</span><span class="sxs-lookup"><span data-stu-id="601d2-152">[CJIS Security Policy](https://aka.ms/cjis-security-policy) covers the precautions that your agency must take to protect CJI.</span></span> <span data-ttu-id="601d2-153">此外，你的 Microsoft 客户代表可以联系熟悉你的管辖地要求的人</span><span class="sxs-lookup"><span data-stu-id="601d2-153">In addition, your Microsoft account representative can put you in touch with those familiar with the requirements of your jurisdiction</span></span>

### <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a><span data-ttu-id="601d2-154">使用 Microsoft 合规性管理器评估风险</span><span class="sxs-lookup"><span data-stu-id="601d2-154">Use Microsoft Compliance Manager to assess your risk</span></span>

<span data-ttu-id="601d2-155">[Microsoft 合规性管理器](/microsoft-365/compliance/compliance-manager)是 [Microsoft 365 合规中心](/microsoft-365/compliance/microsoft-365-compliance-center)中的一项预览功能，旨在帮助你了解组织的合规情况并采取措施帮助降低风险。</span><span class="sxs-lookup"><span data-stu-id="601d2-155">[Microsoft Compliance Manager](/microsoft-365/compliance/compliance-manager) is a feature in the [Microsoft 365 compliance center](/microsoft-365/compliance/microsoft-365-compliance-center) to help you understand your organization's compliance posture and take actions to help reduce risks.</span></span> <span data-ttu-id="601d2-156">合规性管理器提供了一个高级模板，用于对此法规建立评估。</span><span class="sxs-lookup"><span data-stu-id="601d2-156">Compliance Manager offers a premium template for building an assessment for this regulation.</span></span> <span data-ttu-id="601d2-157">在合规性管理器的“**评估模板**”页面中找到模板。</span><span class="sxs-lookup"><span data-stu-id="601d2-157">Find the template in the **assessment templates** page in Compliance Manager.</span></span> <span data-ttu-id="601d2-158">了解如何[在合规性管理器中建立评估](/microsoft-365/compliance/compliance-manager-assessments)。</span><span class="sxs-lookup"><span data-stu-id="601d2-158">Learn how to [build assessments in Compliance Manager](/microsoft-365/compliance/compliance-manager-assessments).</span></span>

### <a name="resources"></a><span data-ttu-id="601d2-159">资源</span><span class="sxs-lookup"><span data-stu-id="601d2-159">Resources</span></span>

- [<span data-ttu-id="601d2-160">犯罪犯罪信息服务</span><span class="sxs-lookup"><span data-stu-id="601d2-160">Criminal Justice Information Services</span></span>](https://aka.ms/cjis)
- [<span data-ttu-id="601d2-161">CJIS 安全策略</span><span class="sxs-lookup"><span data-stu-id="601d2-161">CJIS Security Policy</span></span>](https://aka.ms/cjis-security-policy)
- [<span data-ttu-id="601d2-162">Microsoft 公共控制中心合规性框架</span><span class="sxs-lookup"><span data-stu-id="601d2-162">Microsoft Common Controls Hub Compliance Framework</span></span>](https://www.microsoft.com/trustcenter/common-controls-hub)
- [<span data-ttu-id="601d2-163">Microsoft 政府云</span><span class="sxs-lookup"><span data-stu-id="601d2-163">Microsoft Government Cloud</span></span>](https://go.microsoft.com/fwlink/?linkid=2087246)
- [<span data-ttu-id="601d2-164">Microsoft 信任中心内的合规性</span><span class="sxs-lookup"><span data-stu-id="601d2-164">Compliance on the Microsoft Trust Center</span></span>](https://www.microsoft.com/trust-center/compliance/compliance-overview)
