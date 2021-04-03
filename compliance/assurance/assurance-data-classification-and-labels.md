---
title: 数据分类&敏感度标签分类
description: 本文概述了如何对 Microsoft 365 &数据分类和敏感度标签分类。
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: fcfe98116f4d0629f322383f2992605d2dcf19de
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497789"
---
# <a name="data-classification--sensitivity-label-taxonomy"></a><span data-ttu-id="4ee96-103">数据分类&敏感度标签分类</span><span class="sxs-lookup"><span data-stu-id="4ee96-103">Data classification & sensitivity label taxonomy</span></span>

<span data-ttu-id="4ee96-104">如果敏感数据被盗、无意共享或因泄露而泄露，则给公司带来重大风险。</span><span class="sxs-lookup"><span data-stu-id="4ee96-104">Sensitive data presents significant risk to a company if it is stolen, inadvertently shared, or exposed through a breach.</span></span> <span data-ttu-id="4ee96-105">风险因素包括信誉受损、财务影响和失去竞争优势。</span><span class="sxs-lookup"><span data-stu-id="4ee96-105">Risk factors include reputational damage, financial impact, and loss of competitive advantage.</span></span> <span data-ttu-id="4ee96-106">保护企业管理的数据和信息是组织的一项首要任务，但您可能会发现，鉴于企业包含的内容量，您可能很难知道您的工作是否真正有效。</span><span class="sxs-lookup"><span data-stu-id="4ee96-106">Protecting the data and information your business manages is a top priority for your organization, but you may find it difficult to know if your efforts are truly effective, given the amount of content held by your enterprise.</span></span>

<span data-ttu-id="4ee96-107">除了音量之外，内容的重要性可能从高度敏感和影响范围到简单和短暂。</span><span class="sxs-lookup"><span data-stu-id="4ee96-107">In addition to volume, your content may range in importance from highly sensitive and impactful to trivial and transient.</span></span> <span data-ttu-id="4ee96-108">它还可能符合各种法规合规性要求。</span><span class="sxs-lookup"><span data-stu-id="4ee96-108">It can also be under the purview of various regulatory compliance requirements.</span></span> <span data-ttu-id="4ee96-109">了解要设置优先级和在何处应用控件可能是一个挑战。</span><span class="sxs-lookup"><span data-stu-id="4ee96-109">Knowing what to prioritize and where to apply controls can be a challenge.</span></span> <span data-ttu-id="4ee96-110">继续阅读， *了解数据分类*（一种用于防止内容被盗、破坏或无意破坏的重要工具）以及 Microsoft 365 如何帮助你实现信息安全目标。</span><span class="sxs-lookup"><span data-stu-id="4ee96-110">Read on to learn about *data classification*, an important tool for protecting your content from theft, sabotage, or inadvertent destruction, and how Microsoft 365 can help you meet your information security goals.</span></span>

## <a name="what-is-data-classification"></a><span data-ttu-id="4ee96-111">什么是数据分类？</span><span class="sxs-lookup"><span data-stu-id="4ee96-111">What is data classification?</span></span>

<span data-ttu-id="4ee96-112">[数据分类](/microsoft-365/compliance/data-classification-overview) 是网络安全和信息治理领域的一个专用术语，用于描述根据内容的敏感度或影响级别对内容进行标识、分类和保护的过程。</span><span class="sxs-lookup"><span data-stu-id="4ee96-112">[Data classification](/microsoft-365/compliance/data-classification-overview) is a specialized term used in the fields of cybersecurity and information governance to describe the process of identifying, categorizing, and protecting content according to its sensitivity or impact level.</span></span> <span data-ttu-id="4ee96-113">数据分类最基本的形式是，根据数据的敏感或影响，防止数据被未经授权泄露、更改或销毁。</span><span class="sxs-lookup"><span data-stu-id="4ee96-113">In its most basic form, data classification is a means of protecting your data from unauthorized disclosure, alteration, or destruction based on how sensitive or impactful it is.</span></span>

## <a name="what-is-a-data-classification-framework"></a><span data-ttu-id="4ee96-114">什么是数据分类框架？</span><span class="sxs-lookup"><span data-stu-id="4ee96-114">What is a data classification framework?</span></span>

<span data-ttu-id="4ee96-115">数据分类框架（有时称为 ("数据分类策略") 通常由 3-5 个分类级别组成，通常编成企业范围的正式策略。</span><span class="sxs-lookup"><span data-stu-id="4ee96-115">Often codified in a formal, enterprise-wide policy, a data classification framework (sometimes called a 'data classification policy') is typically comprised of 3-5 classification levels.</span></span> <span data-ttu-id="4ee96-116">这些元素通常包括三个元素：名称、说明和实际示例。</span><span class="sxs-lookup"><span data-stu-id="4ee96-116">These usually include three elements: a name, description, and real-world examples.</span></span> <span data-ttu-id="4ee96-117">Microsoft 建议不要超过五个顶级父标签，每个标签具有五个子标签 (25) ，以保持用户界面 (UI) 可管理。</span><span class="sxs-lookup"><span data-stu-id="4ee96-117">Microsoft recommends no more than five top-level parent labels, each with five sub-labels (25 total) to keep the user interface (UI) manageable.</span></span> <span data-ttu-id="4ee96-118">级别通常从最低到最敏感（如 *公共*、内部、*机密* 和 *高度* 
 *机密）排列*。</span><span class="sxs-lookup"><span data-stu-id="4ee96-118">Levels are typically arranged from least to most sensitive such as *Public*, *Internal*, *Confidential*, and *Highly*
*Confidential*.</span></span> <span data-ttu-id="4ee96-119">你可能会遇到的其他级别名称变体包括 *Restricted、Unrestricted* 和 *Consumer Protected*。</span><span class="sxs-lookup"><span data-stu-id="4ee96-119">Other level name variations you may encounter include *Restricted*, *Unrestricted*, and *Consumer Protected*.</span></span> <span data-ttu-id="4ee96-120">Microsoft 建议使用自我描述性标签名称，并明确突出显示其相对敏感度。</span><span class="sxs-lookup"><span data-stu-id="4ee96-120">Microsoft recommends label names that are self-descriptive and that highlight their relative sensitivity clearly.</span></span> <span data-ttu-id="4ee96-121">例如 *，"机密*"和"受限"可能会让用户猜出哪个标签合适，而"机密"和"高度机密"更清楚地解释哪个标签更敏感。 </span><span class="sxs-lookup"><span data-stu-id="4ee96-121">For example, *Confidential* and *Restricted* may leave users guessing which label is appropriate, while *Confidential* and *Highly Confidential* are clearer on which is more sensitive.</span></span> <span data-ttu-id="4ee96-122">下表显示了数据分类框架级别的示例。</span><span class="sxs-lookup"><span data-stu-id="4ee96-122">The following table shows examples of data classification framework levels.</span></span>

|<span data-ttu-id="4ee96-123">**分类级别**</span><span class="sxs-lookup"><span data-stu-id="4ee96-123">**Classification level**</span></span>|<span data-ttu-id="4ee96-124">**说明**</span><span class="sxs-lookup"><span data-stu-id="4ee96-124">**Description**</span></span>|<span data-ttu-id="4ee96-125">**示例**</span><span class="sxs-lookup"><span data-stu-id="4ee96-125">**Examples**</span></span>|
|:-----------------------|:--------------|:-----------|
| <span data-ttu-id="4ee96-126">高度机密</span><span class="sxs-lookup"><span data-stu-id="4ee96-126">Highly Confidential</span></span> | <span data-ttu-id="4ee96-127">高度机密数据是企业存储或管理的最敏感的数据类型，如果泄露或以其他方式披露，可能需要法律通知。</span><span class="sxs-lookup"><span data-stu-id="4ee96-127">Highly Confidential data is the most sensitive type of data stored or managed by the enterprise and may require legal notifications if breached or otherwise disclosed.</span></span> <br><br> <span data-ttu-id="4ee96-128">受限数据需要最高级别的控制和安全性，并且访问应限制为"需要知道"。</span><span class="sxs-lookup"><span data-stu-id="4ee96-128">Restricted Data requires the highest level of control and security, and access should be limited to "need-to- know."</span></span> | <span data-ttu-id="4ee96-129">敏感个人身份信息 (个人身份信息) </span><span class="sxs-lookup"><span data-stu-id="4ee96-129">Sensitive Personally Identifiable Information (Sensitive PII)</span></span> <br> <span data-ttu-id="4ee96-130">持卡人数据</span><span class="sxs-lookup"><span data-stu-id="4ee96-130">Cardholder Data</span></span> <br> <span data-ttu-id="4ee96-131">受保护的健康信息 (PHI) </span><span class="sxs-lookup"><span data-stu-id="4ee96-131">Protected Health Information (PHI)</span></span> <br> <span data-ttu-id="4ee96-132">银行帐户数据</span><span class="sxs-lookup"><span data-stu-id="4ee96-132">Bank Account Data</span></span> |

>[!TIP]
><span data-ttu-id="4ee96-133">Microsoft 的企业数据分类框架最初在试点阶段使用名为"Internal"的类别和标签，但发现出于合理原因，文档在外部共享并转移到使用"常规"。</span><span class="sxs-lookup"><span data-stu-id="4ee96-133">Microsoft's corporate data classification framework originally used a category and label named 'Internal' during pilot phase but found that there were legitimate reasons for a document to be shared externally and shifted to using 'General'.</span></span>

<span data-ttu-id="4ee96-134">数据分类框架的另一个重要组件是每个级别关联的控件。</span><span class="sxs-lookup"><span data-stu-id="4ee96-134">Another important component of a data classification framework is the controls associated with each level.</span></span> <span data-ttu-id="4ee96-135">数据分类级别本身只是标签 (或) 标签，用于指示内容的值或敏感度。</span><span class="sxs-lookup"><span data-stu-id="4ee96-135">Data classification levels by themselves are simply labels (or tags) that indicate the value or sensitivity of the content.</span></span> <span data-ttu-id="4ee96-136">为了保护 *该* 内容，数据分类框架定义了应针对每个数据分类级别实施的控制。</span><span class="sxs-lookup"><span data-stu-id="4ee96-136">To *protect* that content, data classification frameworks define the controls that should be in place for each of your data classification levels.</span></span> <span data-ttu-id="4ee96-137">这些控件可能包括与以下相关的要求：</span><span class="sxs-lookup"><span data-stu-id="4ee96-137">These controls may include requirements related to:</span></span>

- <span data-ttu-id="4ee96-138">存储类型和位置</span><span class="sxs-lookup"><span data-stu-id="4ee96-138">Storage type and location</span></span>
- <span data-ttu-id="4ee96-139">加密</span><span class="sxs-lookup"><span data-stu-id="4ee96-139">Encryption</span></span>
- <span data-ttu-id="4ee96-140">访问控制</span><span class="sxs-lookup"><span data-stu-id="4ee96-140">Access control</span></span>
- <span data-ttu-id="4ee96-141">数据销毁</span><span class="sxs-lookup"><span data-stu-id="4ee96-141">Data destruction</span></span>
- <span data-ttu-id="4ee96-142">数据丢失防护</span><span class="sxs-lookup"><span data-stu-id="4ee96-142">Data loss prevention</span></span>
- <span data-ttu-id="4ee96-143">公开披露</span><span class="sxs-lookup"><span data-stu-id="4ee96-143">Public disclosure</span></span>
- <span data-ttu-id="4ee96-144">日志记录和跟踪访问</span><span class="sxs-lookup"><span data-stu-id="4ee96-144">Logging and tracking access</span></span>
- <span data-ttu-id="4ee96-145">其他控制目标（根据需要）</span><span class="sxs-lookup"><span data-stu-id="4ee96-145">Other control objectives, as needed</span></span>

<span data-ttu-id="4ee96-146">安全控制措施因数据分类级别而异，因此，框架中定义的保护措施与内容的敏感度相一起提高。</span><span class="sxs-lookup"><span data-stu-id="4ee96-146">Your security controls will vary by data classification level, such that the protective measures defined in your framework increase commensurate with the sensitivity of your content.</span></span> <span data-ttu-id="4ee96-147">例如，数据存储控制要求因使用的媒体以及应用于给定内容的分类级别而异。</span><span class="sxs-lookup"><span data-stu-id="4ee96-147">For example, your data storage control requirements will vary depending upon the media that is being used as well as upon the classification level applied to a given piece of content.</span></span> <span data-ttu-id="4ee96-148">下表显示了特定存储类型的数据分类控件的示例：</span><span class="sxs-lookup"><span data-stu-id="4ee96-148">The following table shows an example of data classification controls for a specific storage type:</span></span>

|<span data-ttu-id="4ee96-149">**存储类型**</span><span class="sxs-lookup"><span data-stu-id="4ee96-149">**Storage type**</span></span>|<span data-ttu-id="4ee96-150">**机密**</span><span class="sxs-lookup"><span data-stu-id="4ee96-150">**Confidential**</span></span>|<span data-ttu-id="4ee96-151">**内部**</span><span class="sxs-lookup"><span data-stu-id="4ee96-151">**Internal**</span></span>|<span data-ttu-id="4ee96-152">**Unrestricted**</span><span class="sxs-lookup"><span data-stu-id="4ee96-152">**Unrestricted**</span></span>|
|:---------------|:---------------|:-----------|:---------------|
| <span data-ttu-id="4ee96-153">可移动存储</span><span class="sxs-lookup"><span data-stu-id="4ee96-153">Removable Storage</span></span> | <span data-ttu-id="4ee96-154">Prohibited</span><span class="sxs-lookup"><span data-stu-id="4ee96-154">Prohibited</span></span> | <span data-ttu-id="4ee96-155">除非已加密，否则禁止</span><span class="sxs-lookup"><span data-stu-id="4ee96-155">Prohibited unless encrypted</span></span> | <span data-ttu-id="4ee96-156">无需控制</span><span class="sxs-lookup"><span data-stu-id="4ee96-156">No control required</span></span> |

<span data-ttu-id="4ee96-157">正确应用正确级别的数据分类在真实情况下可能很复杂，有时可能会使最终用户不知所措。</span><span class="sxs-lookup"><span data-stu-id="4ee96-157">Correctly applying the right level of data classification can be complex in real-life situations and may sometimes overwhelm end users.</span></span> <span data-ttu-id="4ee96-158">创建定义所需数据分类级别的策略或标准后，必须指导最终用户如何在日常工作中实现此框架。</span><span class="sxs-lookup"><span data-stu-id="4ee96-158">Once a policy or standard has been created that defines the required levels of data classification, it is important to guide end users on how to bring this framework to life in their daily work.</span></span> <span data-ttu-id="4ee96-159">此区域是提供数据分类处理规则或指南的地方。</span><span class="sxs-lookup"><span data-stu-id="4ee96-159">This area is where data classification handling rules or guidelines come in.</span></span>

<span data-ttu-id="4ee96-160">数据分类处理指南将帮助最终用户获得有关如何在生命周期内为不同存储媒体适当处理每一级数据的特定指南。</span><span class="sxs-lookup"><span data-stu-id="4ee96-160">Data classification handling guidelines will help end users with specific guidance on how to handle each level of data appropriately, for different storage media throughout their lifecycle.</span></span> <span data-ttu-id="4ee96-161">这些指南可帮助最终用户在实际操作中正确应用规则，例如在共享文档、发送电子邮件或跨不同平台和组织进行协作时。</span><span class="sxs-lookup"><span data-stu-id="4ee96-161">These guidelines help end users to correctly apply rules in practice, for instance when sharing documents, sending emails, or collaborating across different platforms and organizations.</span></span>

<span data-ttu-id="4ee96-162">Microsoft 客户表示，大约 50% 的信息保护项目专注于业务而不是技术，因此最终用户培训和沟通对于成功至关重要。</span><span class="sxs-lookup"><span data-stu-id="4ee96-162">Microsoft customers indicate that approximately 50% of an Information Protection project is business focused rather than technical, so end-user training and communication is critical to success.</span></span>
