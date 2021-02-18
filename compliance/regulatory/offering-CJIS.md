---
title: 刑事犯罪信息服务 (CJIS) 安全策略
description: Microsoft 政府云服务遵守美国刑事犯罪信息服务安全策略。
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
ms.openlocfilehash: 0a8cc37a24d3a51d79fb1ac34c92d96fc7e76fdd
ms.sourcegitcommit: 66a26facea6ec9a95e5e61f1b5b69402f03db481
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/17/2021
ms.locfileid: "50279839"
---
# <a name="criminal-justice-information-services-cjis-security-policy"></a><span data-ttu-id="2be50-104">刑事犯罪信息服务 (CJIS) 安全策略</span><span class="sxs-lookup"><span data-stu-id="2be50-104">Criminal Justice Information Services (CJIS) Security Policy</span></span>

## <a name="cjis-overview"></a><span data-ttu-id="2be50-105">CJIS 概述</span><span class="sxs-lookup"><span data-stu-id="2be50-105">CJIS overview</span></span>

<span data-ttu-id="2be50-106">美国联邦调查局 (联邦调查局) 的刑事犯罪信息服务 (CJIS) 部门使州、地方和联邦执法机构和刑事犯罪机构可以访问 CJI) 的刑事犯罪信息 (例如指纹记录和犯罪历史记录。</span><span class="sxs-lookup"><span data-stu-id="2be50-106">The Criminal Justice Information Services (CJIS) Division of the US Federal Bureau of Investigation (FBI) gives state, local, and federal law enforcement and criminal justice agencies access to criminal justice information (CJI) — for example, fingerprint records and criminal histories.</span></span> <span data-ttu-id="2be50-107">美国的执法机构和其他政府机构必须确保他们使用云服务传输、存储或处理 CJI 符合 [CJIS](https://aka.ms/cjis-security-policy)安全策略，该策略建立了最低安全要求和控制来保护 CJI。</span><span class="sxs-lookup"><span data-stu-id="2be50-107">Law enforcement and other government agencies in the United States must ensure that their use of cloud services for the transmission, storage, or processing of CJI complies with the [CJIS Security Policy](https://aka.ms/cjis-security-policy), which establishes minimum security requirements and controls to safeguard CJI.</span></span>

<span data-ttu-id="2be50-108">CJIS 安全策略集成了联邦和联邦指令、联邦法律以及刑事犯罪社区的建议策略委员会决策，以及国家标准和技术协会 NIST () 的指导。</span><span class="sxs-lookup"><span data-stu-id="2be50-108">The CJIS Security Policy integrates presidential and FBI directives, federal laws, and the criminal justice community's Advisory Policy Board decisions, along with guidance from the National Institute of Standards and Technology (NIST).</span></span> <span data-ttu-id="2be50-109">该策略会定期更新以反映不断变化的安全要求。</span><span class="sxs-lookup"><span data-stu-id="2be50-109">The Policy is periodically updated to reflect evolving security requirements.</span></span>

<span data-ttu-id="2be50-110">CJIS 安全策略定义了私人承包商（如云服务提供商）必须评估的 13 个方面，以确定其使用云服务是否与 CJIS 要求一致。</span><span class="sxs-lookup"><span data-stu-id="2be50-110">The CJIS Security Policy defines 13 areas that private contractors such as cloud service providers must evaluate to determine if their use of cloud services can be consistent with CJIS requirements.</span></span> <span data-ttu-id="2be50-111">这些区域与 NIST 800-53 紧密对应，NIST 800-53 也是联邦风险与授权管理计划 [ (FedRAMP) ](offering-FedRAMP.md)的基础，根据该计划，Microsoft 已通过政府云产品/服务认证。</span><span class="sxs-lookup"><span data-stu-id="2be50-111">These areas correspond closely to NIST 800-53, which is also the basis for the [Federal Risk and Authorization Management Program (FedRAMP)](offering-FedRAMP.md), a program under which Microsoft has been certified for its Government Cloud offerings.</span></span>

<span data-ttu-id="2be50-112">此外，处理 CJI 的所有私有承包商都必须签署 CJIS 安全附录，这是美国律师总长批准的统一协议，可帮助确保安全策略所需的 CJI 的安全性和机密性。</span><span class="sxs-lookup"><span data-stu-id="2be50-112">In addition, all private contractors who process CJI must sign the CJIS Security Addendum, a uniform agreement approved by the US Attorney General that helps ensure the security and confidentiality of CJI required by the Security Policy.</span></span> <span data-ttu-id="2be50-113">它还承诺承包商维护符合联邦和州法律、法规和标准的安全计划，并限制 CJI 的使用符合政府机构提供 CJI 的目的。</span><span class="sxs-lookup"><span data-stu-id="2be50-113">It also commits the contractor to maintaining a security program consistent with federal and state laws, regulations, and standards, and limits the use of CJI to the purposes for which a government agency provided it.</span></span>

## <a name="microsoft-and-cjis-security-policy"></a><span data-ttu-id="2be50-114">Microsoft 和 CJIS 安全策略</span><span class="sxs-lookup"><span data-stu-id="2be50-114">Microsoft and CJIS Security Policy</span></span>

<span data-ttu-id="2be50-115">Microsoft 使用 CJIS 信息协议在状态中签署 CJIS 安全附录。</span><span class="sxs-lookup"><span data-stu-id="2be50-115">Microsoft signs the CJIS Security Addendum in states with CJIS Information Agreements.</span></span> <span data-ttu-id="2be50-116">这些内容告知负责遵守 CJIS 安全策略的州执法机构，Microsoft 的云安全控制如何帮助保护数据的完整生命周期，并确保对有权访问 CJI 的操作人员进行适当的背景筛选。</span><span class="sxs-lookup"><span data-stu-id="2be50-116">These tell state law enforcement authorities responsible for compliance with CJIS Security Policy how Microsoft's cloud security controls help protect the full lifecycle of data and ensure appropriate background screening of operating personnel with access to CJI.</span></span> <span data-ttu-id="2be50-117">Microsoft 将继续与州政府合作，以签订 CJIS 信息协议。</span><span class="sxs-lookup"><span data-stu-id="2be50-117">Microsoft continues to work with state governments to enter into CJIS Information Agreements.</span></span>

<span data-ttu-id="2be50-118">Microsoft 已评估 Microsoft Azure 政府、Microsoft Office 365 美国政府版和 Microsoft Dynamics 365 美国政府版的操作策略和过程，并证明他们在适用的服务协议中满足使用范围内服务的 FBI 要求的能力。</span><span class="sxs-lookup"><span data-stu-id="2be50-118">Microsoft has assessed the operational policies and procedures of Microsoft Azure Government, Microsoft Office 365 U.S. Government, and Microsoft Dynamics 365 U.S. Government, and will attest to their ability in the applicable services agreements to meet FBI requirements for the use of in-scope services.</span></span>

<span data-ttu-id="2be50-119">了解 Microsoft 云上的 CJIS 安全策略的好处： [阅读了 How](https://customers.microsoft.com/story/genetec)</span><span class="sxs-lookup"><span data-stu-id="2be50-119">Learn about the benefits of CJIS Security policy on the Microsoft Cloud: [Read how Genetec cleared criminal investigations](https://customers.microsoft.com/story/genetec)</span></span>

## <a name="microsoft-in-scope-cloud-services"></a><span data-ttu-id="2be50-120">Microsoft 范围内的云服务</span><span class="sxs-lookup"><span data-stu-id="2be50-120">Microsoft in-scope cloud services</span></span>

- [<span data-ttu-id="2be50-121">Azure 政府</span><span class="sxs-lookup"><span data-stu-id="2be50-121">Azure Government</span></span>](/azure/azure-government/documentation-government-welcome)
- [<span data-ttu-id="2be50-122">Dynamics 365 美国政府版</span><span class="sxs-lookup"><span data-stu-id="2be50-122">Dynamics 365 U.S. Government</span></span>](/power-platform/admin/microsoft-dynamics-365-government#certifications-and-accreditations)
- [<span data-ttu-id="2be50-123">Office 365 美国政府版</span><span class="sxs-lookup"><span data-stu-id="2be50-123">Office 365 U.S. Government</span></span>](/office365/servicedescriptions/office-365-platform-service-description/office-365-us-government/gcc#us-government-community-compliance)
- <span data-ttu-id="2be50-124">Power BI 云服务，作为独立服务提供，或者随 Office 365 品牌计划或套件一并提供</span><span class="sxs-lookup"><span data-stu-id="2be50-124">Power BI cloud service either as a standalone service or as included in an Office 365 branded plan or suite</span></span>

## <a name="audits-reports-and-certificates"></a><span data-ttu-id="2be50-125">审核、报告和证书</span><span class="sxs-lookup"><span data-stu-id="2be50-125">Audits, reports, and certificates</span></span>

<span data-ttu-id="2be50-126">美国情报局不提供 Microsoft 遵守 CJIS 要求的认证。</span><span class="sxs-lookup"><span data-stu-id="2be50-126">The FBI does not offer certification of Microsoft compliance with CJIS requirements.</span></span> <span data-ttu-id="2be50-127">相反，Microsoft 证明包含在 Microsoft 与州 CJIS 颁发机构之间以及 Microsoft 与其客户之间的协议中。</span><span class="sxs-lookup"><span data-stu-id="2be50-127">Instead, a Microsoft attestation is included in agreements between Microsoft and a state's CJIS authority, and between Microsoft and its customers.</span></span>

[<span data-ttu-id="2be50-128">Microsoft CJIS 云要求</span><span class="sxs-lookup"><span data-stu-id="2be50-128">Microsoft CJIS Cloud Requirements</span></span>](https://aka.ms/MicrosoftCJISCloudRequirements)

## <a name="cjis-status-in-the-united-states-current-as-of-1152020"></a><span data-ttu-id="2be50-129">自 2020 年 5 月 11 (起，美国 CJIS 状态) </span><span class="sxs-lookup"><span data-stu-id="2be50-129">CJIS status in the United States (current as of 11/5/2020)</span></span>

<span data-ttu-id="2be50-130">44 个州以及具有管理协议的"哥伦比亚区"（在地图上以绿色突出显示）包括：</span><span class="sxs-lookup"><span data-stu-id="2be50-130">44 states and the District of Columbia with management agreements, highlighted on the map in green include:</span></span>

<span data-ttu-id="2be50-131">文莱巴马、加利福尼亚、加利福尼亚、加利福尼亚、Connect california、 华盛顿州、格鲁吉亚、夏威夷、Idaho、都尼西亚、剑桥、剑桥、卡塔基、Maine、Texats、波特兰、明尼西亚、密斯拉尼亚、密拉纳、尼伯拉萨、New Jersey、New Jersey、New York、New York、New Dakota、North Dakota、Oregonhoma、Oregon、一线、剑桥岛、南尼西亚、波特兰、德克萨斯州、Oregon、Ver mont、Washington、West Washington、以及剑桥地区。</span><span class="sxs-lookup"><span data-stu-id="2be50-131">Alabama, Alaska, Arizona, Arkansas, California, Colorado, Connecticut, Florida, Georgia, Hawaii, Idaho, Illinois, Indiana, Iowa, Kansas, Kentucky, Maine, Massachusetts, Michigan, Minnesota, Mississippi, Missouri, Montana, Nebraska, Nevada, New Hampshire, New Jersey, New York, North Carolina, North Dakota, Oklahoma, Oregon, Pennsylvania, Rhode Island, South Carolina, Tennessee, Texas, Utah, Vermont, Virginia, Washington, West Virginia, Wisconsin, and the District of Columbia.</span></span>

<span data-ttu-id="2be50-132">Microsoft 承诺遵守适用的 CJIS 法规控制，允许刑事犯罪组织实施基于云的解决方案，并符合 CJIS 安全策略 V5.8。</span><span class="sxs-lookup"><span data-stu-id="2be50-132">Microsoft's commitment to meeting the applicable CJIS regulatory controls allows Criminal Justice organizations to implement cloud-based solutions and be compliant with CJIS Security Policy V5.8.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="2be50-133">常见问题解答</span><span class="sxs-lookup"><span data-stu-id="2be50-133">Frequently asked questions</span></span>

<span data-ttu-id="2be50-134">**在哪里可以请求合规性信息？**</span><span class="sxs-lookup"><span data-stu-id="2be50-134">**Where can I request compliance information?**</span></span>

<span data-ttu-id="2be50-135">请联系你的 Microsoft 帐户代表，了解你感兴趣的管辖地的信息。</span><span class="sxs-lookup"><span data-stu-id="2be50-135">Contact your Microsoft account representative for information on the jurisdiction you are interested in.</span></span> <span data-ttu-id="2be50-136">有关 <cjis@microsoft.com> 当前哪些服务处于哪些状态的信息，请与联系人联系。</span><span class="sxs-lookup"><span data-stu-id="2be50-136">Contact <cjis@microsoft.com> for information on which services are currently available in which states.</span></span>

<span data-ttu-id="2be50-137">**Microsoft 如何证明其云服务符合我的状态要求？**</span><span class="sxs-lookup"><span data-stu-id="2be50-137">**How does Microsoft demonstrate that its cloud services enable compliance with my state's requirements?**</span></span>

<span data-ttu-id="2be50-138">Microsoft 与州 CJIS Systems Agency 与 CSA (签署信息) ;你可以从你州 CSA 请求副本。</span><span class="sxs-lookup"><span data-stu-id="2be50-138">Microsoft signs an Information Agreement with a state CJIS Systems Agency (CSA); you may request a copy from your state's CSA.</span></span> <span data-ttu-id="2be50-139">此外，Microsoft 为客户提供了深入的安全、隐私和合规性信息。</span><span class="sxs-lookup"><span data-stu-id="2be50-139">In addition, Microsoft provides customers with in-depth security, privacy, and compliance information.</span></span> <span data-ttu-id="2be50-140">客户还可以查看独立审核员准备的安全和合规性报告，以便他们可以验证 Microsoft 是否实施了安全控制措施 (如 ISO 27001) 适合相关审核范围。</span><span class="sxs-lookup"><span data-stu-id="2be50-140">Customers may also review security and compliance reports prepared by independent auditors so they can validate that Microsoft has implemented security controls (such as ISO 27001) appropriate to the relevant audit scope.</span></span>

<span data-ttu-id="2be50-141">**从何处着手执行我的代理的合规性工作？**</span><span class="sxs-lookup"><span data-stu-id="2be50-141">**Where do I start with my agency's compliance effort?**</span></span>

<span data-ttu-id="2be50-142">[CJIS 安全策略](https://aka.ms/cjis-security-policy) 涵盖机构保护 CJI 必须采取的预防措施。</span><span class="sxs-lookup"><span data-stu-id="2be50-142">[CJIS Security Policy](https://aka.ms/cjis-security-policy) covers the precautions that your agency must take to protect CJI.</span></span> <span data-ttu-id="2be50-143">此外，你的 Microsoft 客户代表可以联系熟悉你的管辖要求的人</span><span class="sxs-lookup"><span data-stu-id="2be50-143">In addition, your Microsoft account representative can put you in touch with those familiar with the requirements of your jurisdiction</span></span>

## <a name="use-microsoft-compliance-manager-to-assess-your-risk"></a><span data-ttu-id="2be50-144">使用 Microsoft 合规性管理器评估风险</span><span class="sxs-lookup"><span data-stu-id="2be50-144">Use Microsoft Compliance Manager to assess your risk</span></span>

<span data-ttu-id="2be50-145">[Microsoft 合规性管理器](/microsoft-365/compliance/compliance-manager)是 [Microsoft 365 合规中心](/microsoft-365/compliance/microsoft-365-compliance-center)中的一项预览功能，旨在帮助你了解组织的合规情况并采取措施帮助降低风险。</span><span class="sxs-lookup"><span data-stu-id="2be50-145">[Microsoft Compliance Manager](/microsoft-365/compliance/compliance-manager) is a feature in the [Microsoft 365 compliance center](/microsoft-365/compliance/microsoft-365-compliance-center) to help you understand your organization's compliance posture and take actions to help reduce risks.</span></span> <span data-ttu-id="2be50-146">合规性管理器提供了一个高级模板，用于对此法规建立评估。</span><span class="sxs-lookup"><span data-stu-id="2be50-146">Compliance Manager offers a premium template for building an assessment for this regulation.</span></span> <span data-ttu-id="2be50-147">在合规性管理器的“**评估模板**”页面中找到模板。</span><span class="sxs-lookup"><span data-stu-id="2be50-147">Find the template in the **assessment templates** page in Compliance Manager.</span></span> <span data-ttu-id="2be50-148">了解如何[在合规性管理器中建立评估](/microsoft-365/compliance/compliance-manager-assessments)。</span><span class="sxs-lookup"><span data-stu-id="2be50-148">Learn how to [build assessments in Compliance Manager](/microsoft-365/compliance/compliance-manager-assessments).</span></span>

## <a name="resources"></a><span data-ttu-id="2be50-149">资源</span><span class="sxs-lookup"><span data-stu-id="2be50-149">Resources</span></span>

- [<span data-ttu-id="2be50-150">刑事犯罪信息服务</span><span class="sxs-lookup"><span data-stu-id="2be50-150">Criminal Justice Information Services</span></span>](https://aka.ms/cjis)
- [<span data-ttu-id="2be50-151">CJIS 安全策略</span><span class="sxs-lookup"><span data-stu-id="2be50-151">CJIS Security Policy</span></span>](https://aka.ms/cjis-security-policy)
- [<span data-ttu-id="2be50-152">Azure 政府 CJIS 实施指南</span><span class="sxs-lookup"><span data-stu-id="2be50-152">CJIS implementation guidelines for Azure Government</span></span>](https://aka.ms/cjisimplementationguidelines)
- [<span data-ttu-id="2be50-153">Microsoft 公共控制中心合规性框架</span><span class="sxs-lookup"><span data-stu-id="2be50-153">Microsoft Common Controls Hub Compliance Framework</span></span>](https://www.microsoft.com/trustcenter/common-controls-hub)
- [<span data-ttu-id="2be50-154">Microsoft 政府云</span><span class="sxs-lookup"><span data-stu-id="2be50-154">Microsoft Government Cloud</span></span>](https://go.microsoft.com/fwlink/?linkid=2087246)
- [<span data-ttu-id="2be50-155">Microsoft 信任中心内的合规性</span><span class="sxs-lookup"><span data-stu-id="2be50-155">Compliance on the Microsoft Trust Center</span></span>](https://www.microsoft.com/trust-center/compliance/compliance-overview)
