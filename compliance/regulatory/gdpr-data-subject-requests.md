---
title: 针对 GDPR 和 CCPA 的数据主体请求
keywords: Microsoft 365, Microsoft 365 教育版, Microsoft 365 文档, GDPR, CCPA
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
- GDPR
- M365-security-compliance
- MS-Compliance
titleSuffix: Microsoft GDPR
description: 了解如何使用 Microsoft 产品和服务，在一般数据保护条例 (GPDR) 和加州消费者隐私法案 (CCPA) 下完成 DSR。
ms.custom: seo-marvel-mar2020
hideEdit: true
ms.openlocfilehash: 8e6b862de3e52b171d886613af8529c082bad56d
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496264"
---
# <a name="data-subject-requests-and-the-gdpr-and-ccpa"></a><span data-ttu-id="89ca0-104">针对 GDPR 和 CCPA 的数据主体请求</span><span class="sxs-lookup"><span data-stu-id="89ca0-104">Data Subject Requests and the GDPR and CCPA</span></span>

<span data-ttu-id="89ca0-105">一般数据保护条例 (GDPR) 引入了新规定，适用于向欧盟 (EU) 民众提供商品和服务的组织，或收集并分析欧盟居民相关数据的组织。无论你或你的企业位于何处，都要遵守这些新规定。</span><span class="sxs-lookup"><span data-stu-id="89ca0-105">The General Data Protection Regulation (GDPR) introduces new rules for organizations that offer goods and services to people in the European Union (EU), or that collect and analyze data for EU residents no matter where you or your enterprise are located.</span></span> <span data-ttu-id="89ca0-106">有关其他详细信息，请参阅 [GDPR 摘要主题](gdpr.md)。</span><span class="sxs-lookup"><span data-stu-id="89ca0-106">Additional details can be found in the [GDPR Summary topic](gdpr.md).</span></span>

<span data-ttu-id="89ca0-107">同样，加州消费者隐私法案 (CCPA) 规定了加州消费者的隐私权和义务，包括与 GDPR 的数据主体权利类似的权利，例如删除、访问和接收（可移植性）其个人信息的权利。</span><span class="sxs-lookup"><span data-stu-id="89ca0-107">Similarly, the California Consumer Privacy Act (CCPA), provides privacy rights and obligations to California consumers, including rights similar to GDPR's Data Subject Rights, such as the right to delete, access, and receive (portability) their personal information.</span></span>  <span data-ttu-id="89ca0-108">CCPA 还就某些披露规定了在选择行使权限时防止歧视的保障措施，并就分类为“销售”的特定数据传输提出了“选择退出/选择加入”要求。</span><span class="sxs-lookup"><span data-stu-id="89ca0-108">The CCPA also provides for certain disclosures, protections against discrimination when electing exercise rights, and "opt-out/ opt-in" requirements for certain data transfers classified as "sales".</span></span> <span data-ttu-id="89ca0-109">本文档介绍了如何根据 GDPR 和 CCPA 使用 Microsoft 产品和服务来完成数据主体请求 (DSR)。</span><span class="sxs-lookup"><span data-stu-id="89ca0-109">This document guides you to information on the completion of Data Subject Requests (DSRs) under the GDPR and CCPA using Microsoft products and services.</span></span>

- [<span data-ttu-id="89ca0-110">Office 365</span><span class="sxs-lookup"><span data-stu-id="89ca0-110">Office 365</span></span>](gdpr-dsr-Office365.md)
- [<span data-ttu-id="89ca0-111">Azure</span><span class="sxs-lookup"><span data-stu-id="89ca0-111">Azure</span></span>](gdpr-dsr-Azure.md)
- [<span data-ttu-id="89ca0-112">Intune</span><span class="sxs-lookup"><span data-stu-id="89ca0-112">Intune</span></span>](gdpr-dsr-Intune.md)
- [<span data-ttu-id="89ca0-113">Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="89ca0-113">Dynamics 365</span></span>](gdpr-dsr-Dynamics365.md)
- [<span data-ttu-id="89ca0-114">Visual Studio 系列产品</span><span class="sxs-lookup"><span data-stu-id="89ca0-114">Visual Studio Family</span></span>](gdpr-dsr-visual-studio-family.md)
- [<span data-ttu-id="89ca0-115">Azure DevOps Services</span><span class="sxs-lookup"><span data-stu-id="89ca0-115">Azure DevOps Services</span></span>](gdpr-dsr-vsts.md)
- [<span data-ttu-id="89ca0-116">Microsoft 支持和专业服务</span><span class="sxs-lookup"><span data-stu-id="89ca0-116">Microsoft Support and Professional Services</span></span>](gdpr-dsr-prof-services.md)

## <a name="terminology"></a><span data-ttu-id="89ca0-117">术语</span><span class="sxs-lookup"><span data-stu-id="89ca0-117">Terminology</span></span>

<span data-ttu-id="89ca0-118">本文档中使用的 GDPR 术语的有用定义：</span><span class="sxs-lookup"><span data-stu-id="89ca0-118">Helpful definitions for GDPR terms used in this document:</span></span>

- <span data-ttu-id="89ca0-119">*数据控制者（控制者）*：单独或与他人共同确定个人数据处理目的和方法的法人、公共机关、机构或其他团体。</span><span class="sxs-lookup"><span data-stu-id="89ca0-119">*Data Controller (Controller)*: A legal person, public authority, agency or other body which, alone or jointly with others, determines the purposes and means of the processing of personal data.</span></span>  
- <span data-ttu-id="89ca0-120">*个人数据* 和 *数据主体*：与已识别或可识别的自然人（数据主体）相关的任何信息；可识别的自然人是可以直接或间接识别的自然人。</span><span class="sxs-lookup"><span data-stu-id="89ca0-120">*Personal data* and *data subject*: Any information relating to an identified or identifiable natural person (data subject); an identifiable natural person is one who can be identified, directly or indirectly.</span></span>  
- <span data-ttu-id="89ca0-121">*处理者*：代表控制者处理个人数据的自然人或法人、公共机关、机构或其他团队。</span><span class="sxs-lookup"><span data-stu-id="89ca0-121">*Processor*: A natural or legal person, public authority, agency, or other body, which processes personal data on behalf of the controller.</span></span>  
- <span data-ttu-id="89ca0-122">*客户数据*：在企业日常运营中生成和存储的数据。</span><span class="sxs-lookup"><span data-stu-id="89ca0-122">*Customer Data*: Data produced and stored in the day-to-day operations of running your business.</span></span>

## <a name="what-is-a-dsr"></a><span data-ttu-id="89ca0-123">什么是 DSR？</span><span class="sxs-lookup"><span data-stu-id="89ca0-123">What is a DSR?</span></span>

<span data-ttu-id="89ca0-124">一般数据保护条例 (GDPR) 赋予民众（在条例中称为“数据主体”）权利，即管理已由雇主或其他类型机构或组织（称为“数据控制者”或简称为“控制者”）收集的个人数据。</span><span class="sxs-lookup"><span data-stu-id="89ca0-124">The General Data Protection Regulation (GDPR) gives rights to people (known in the regulation as data subjects) to manage the personal data that has been collected by an employer or other type of agency or organization (known as the data controller or just controller).</span></span> <span data-ttu-id="89ca0-125">GDPR 赋予数据主体对其个人数据的特定权利；这些权利包括，获取个人数据副本、请求更改个人数据、限制个人数据处理、删除个人数据，或接收能转移给另一个控制者的电子格式个人数据。</span><span class="sxs-lookup"><span data-stu-id="89ca0-125">The GDPR gives data subjects specific rights to their personal data; these rights include obtaining copies of it, requesting changes to it, restricting the processing of it, deleting it, or receiving it in an electronic format so it can be moved to another controller.</span></span>

<span data-ttu-id="89ca0-126">加州消费者隐私法案 (CCPA) 规定了加州消费者的隐私权和义务，包括与 GDPR 的数据主体权利类似的权利，例如删除、访问和接收（可移植性）其个人信息的权利。</span><span class="sxs-lookup"><span data-stu-id="89ca0-126">California Consumer Privacy Act (CCPA) provides privacy rights and obligations to California consumers, including rights similar to GDPR's Data Subject Rights, such as the right to delete, access, and receive (portability) their personal information.</span></span>  

<span data-ttu-id="89ca0-127">作为控制者，你有义务迅速考虑每个 DSR，并通过执行所请求的操作或解释控制者为什么无法接受 DSR 来提供实质性响应。</span><span class="sxs-lookup"><span data-stu-id="89ca0-127">As a controller, you are obligated to promptly consider each DSR and provide a substantive response either by taking the requested action or by providing an explanation for why the DSR cannot be accommodated by the controller.</span></span> <span data-ttu-id="89ca0-128">控制者应咨询自己的法律顾问或合规顾问，以决定如何妥善处置任何给定 DSR。</span><span class="sxs-lookup"><span data-stu-id="89ca0-128">A controller should consult with its own legal or compliance advisers regarding the proper disposition of any given DSR.</span></span>

<span data-ttu-id="89ca0-129">根据组织的 GDPR 合规性规定，完成 DSR 可能涉及多个过程。</span><span class="sxs-lookup"><span data-stu-id="89ca0-129">Several processes may be involved completing a DSR, subject to your organization's GDPR-compliance rules.</span></span>
  
- <span data-ttu-id="89ca0-130">**发现**。</span><span class="sxs-lookup"><span data-stu-id="89ca0-130">**Discovery**.</span></span> <span data-ttu-id="89ca0-131">确定完成 DSR 所需的数据的过程。</span><span class="sxs-lookup"><span data-stu-id="89ca0-131">The process of determining what data is needed to complete a DSR.</span></span>
- <span data-ttu-id="89ca0-132">**访问**。</span><span class="sxs-lookup"><span data-stu-id="89ca0-132">**Access**.</span></span> <span data-ttu-id="89ca0-133">检索数据，并可能将已发现的信息传输给数据主体。</span><span class="sxs-lookup"><span data-stu-id="89ca0-133">Retrieval and potential transmission to the data subject of discovered information.</span></span>
- <span data-ttu-id="89ca0-134">**校正**。</span><span class="sxs-lookup"><span data-stu-id="89ca0-134">**Rectify**.</span></span> <span data-ttu-id="89ca0-135">实现更改或其他请求的个人数据更改。</span><span class="sxs-lookup"><span data-stu-id="89ca0-135">Implement changes or other requested personal data changes.</span></span>
- <span data-ttu-id="89ca0-136">**限制**。</span><span class="sxs-lookup"><span data-stu-id="89ca0-136">**Restrict**.</span></span> <span data-ttu-id="89ca0-137">通过限制访问或从 Microsoft 云中删除数据，更改对个人数据的访问或处理。</span><span class="sxs-lookup"><span data-stu-id="89ca0-137">Changing the access or processing of persona data by restricting access, or removing data from the Microsoft cloud.</span></span>
- <span data-ttu-id="89ca0-138">**导出**。</span><span class="sxs-lookup"><span data-stu-id="89ca0-138">**Export**.</span></span> <span data-ttu-id="89ca0-139">根据 GDPR 的“数据可移植性权利”，向数据主体提供“结构化的计算机可读常用格式”个人数据。</span><span class="sxs-lookup"><span data-stu-id="89ca0-139">Providing a "structured, commonly used, machine-readable format" of personal data to the data subject, as provided by the GDPR's "right of data portability."</span></span>
- <span data-ttu-id="89ca0-140">**删除**。</span><span class="sxs-lookup"><span data-stu-id="89ca0-140">**Delete**.</span></span> <span data-ttu-id="89ca0-141">从 Microsoft 云中永久删除个人数据。</span><span class="sxs-lookup"><span data-stu-id="89ca0-141">Permanent removal of personal data from the Microsoft cloud.</span></span>

## <a name="specific-dsr-considerations"></a><span data-ttu-id="89ca0-142">具体 DSR 注意事项</span><span class="sxs-lookup"><span data-stu-id="89ca0-142">Specific DSR Considerations</span></span>

### <a name="insights-generated-by-microsoft-products-or-services"></a><span data-ttu-id="89ca0-143">Microsoft 产品或服务生成的见解</span><span class="sxs-lookup"><span data-stu-id="89ca0-143">Insights generated by Microsoft Products or Services</span></span>

<span data-ttu-id="89ca0-144">MyAnalytics 等服务可能会生成[见解](/microsoft-365/compliance/gdpr-dsr-office365#part-2-responding-to-dsrs-with-respect-to-insights-generated-by-office-365)。Office 365 包括，向使用它们的用户和组织提供见解的联机服务。</span><span class="sxs-lookup"><span data-stu-id="89ca0-144">[Insights](/microsoft-365/compliance/gdpr-dsr-office365#part-2-responding-to-dsrs-with-respect-to-insights-generated-by-office-365) may be generated by services (MyAnalytics, etc.) Office 365 includes online services that provide insights to users and organizations that use them.</span></span> <span data-ttu-id="89ca0-145">这些服务生成的数据可能会产生与 DSR 相关的个人数据。</span><span class="sxs-lookup"><span data-stu-id="89ca0-145">Data generated by these services may produce personal data relevant to a DSR.</span></span> <span data-ttu-id="89ca0-146">请单击下面列表中的链接，详细了解服务专属 DSR 过程。</span><span class="sxs-lookup"><span data-stu-id="89ca0-146">Follow the link in the list below for details regarding service-specific DSR processes.</span></span>  

### <a name="dsrs-for-system-generated-logs"></a><span data-ttu-id="89ca0-147">针对系统生成日志发出的 DSR</span><span class="sxs-lookup"><span data-stu-id="89ca0-147">DSRs for system-generated logs</span></span>

<span data-ttu-id="89ca0-148">Microsoft 生成的日志和相关数据可能包含，根据 GDPR 的“个人数据”定义被视为个人数据的数据。</span><span class="sxs-lookup"><span data-stu-id="89ca0-148">Logs and related data generated by Microsoft may contain data deemed personal under GDPR's definition of "personal data."</span></span> <span data-ttu-id="89ca0-149">不支持限制或校正系统生成日志中的数据。</span><span class="sxs-lookup"><span data-stu-id="89ca0-149">Restricting or rectifying data in system-generated logs is not supported.</span></span> <span data-ttu-id="89ca0-150">系统生成日志中的数据由 Microsoft 云内执行的实际操作和诊断数据构成；修改会泄漏操作历史记录，并增加欺诈和安全风险。</span><span class="sxs-lookup"><span data-stu-id="89ca0-150">Data in system-generated logs constitutes factual actions conducted within the Microsoft cloud and diagnostic data; modifications would compromise the historical record of actions and increase fraud and security risks.</span></span> <span data-ttu-id="89ca0-151">Microsoft 支持访问、导出和删除完成 DSR 所必需的系统生成日志。</span><span class="sxs-lookup"><span data-stu-id="89ca0-151">Microsoft provides the ability to access, export, and delete system-generated logs that may be necessary to complete a DSR.</span></span> <span data-ttu-id="89ca0-152">此类数据的示例可能包括：</span><span class="sxs-lookup"><span data-stu-id="89ca0-152">Examples of such data may include:</span></span>  

- <span data-ttu-id="89ca0-153">产品和服务使用情况数据，例如用户活动日志</span><span class="sxs-lookup"><span data-stu-id="89ca0-153">Product and service usage data such as user activity logs</span></span>
- <span data-ttu-id="89ca0-154">用户搜索请求和查询数据</span><span class="sxs-lookup"><span data-stu-id="89ca0-154">User search requests and query data</span></span>
- <span data-ttu-id="89ca0-155">由系统功能以及用户或其他系统的交互产生的产品和服务生成数据。</span><span class="sxs-lookup"><span data-stu-id="89ca0-155">Data generated by product and services resulting from system functionality and interaction by users or other systems.</span></span>  

### <a name="yammer-and-kaizala"></a><span data-ttu-id="89ca0-156">Yammer 和 Kaizala</span><span class="sxs-lookup"><span data-stu-id="89ca0-156">Yammer and Kaizala</span></span>

<span data-ttu-id="89ca0-157">删除用户的帐户不会删除 Yammer 和 Kaizala 的系统生成日志。</span><span class="sxs-lookup"><span data-stu-id="89ca0-157">Deleting a user's account will not remove system-generated logs for Yammer and Kaizala.</span></span> <span data-ttu-id="89ca0-158">若要从这些应用程序中删除数据，请参阅以下资源之一：</span><span class="sxs-lookup"><span data-stu-id="89ca0-158">To remove the data from these applications, see one of the following resources:</span></span>

- [<span data-ttu-id="89ca0-159">管理 Yammer Enterprise 中的 GDPR 数据主体请求</span><span class="sxs-lookup"><span data-stu-id="89ca0-159">Manage GDPR data subject requests in Yammer Enterprise</span></span>](/yammer/manage-security-and-compliance/gdpr-requests-in-yammer-enterprise)
- [<span data-ttu-id="89ca0-160">导出或删除用户在 Kaizala 中的组织数据</span><span class="sxs-lookup"><span data-stu-id="89ca0-160">Export or delete a user's organizational data in Kaizala</span></span>](/office365/kaizala/export-or-delete-a-user-s-data)

### <a name="national-clouds"></a><span data-ttu-id="89ca0-161">国家云</span><span class="sxs-lookup"><span data-stu-id="89ca0-161">National Clouds</span></span>

<span data-ttu-id="89ca0-162">在一些国家云中，全局 IT 管理员需要删除系统生成日志。</span><span class="sxs-lookup"><span data-stu-id="89ca0-162">In some national clouds, a global IT Administrator needs to delete system-generated logs.</span></span>

### <a name="microsoft-services"></a><span data-ttu-id="89ca0-163">Microsoft 服务</span><span class="sxs-lookup"><span data-stu-id="89ca0-163">Microsoft Services</span></span>

<span data-ttu-id="89ca0-164">如果组织或用户与 Microsoft 交互以获取与 Microsoft 产品和服务相关的支持，部分此类数据可能包含个人数据。</span><span class="sxs-lookup"><span data-stu-id="89ca0-164">If your organization or users engage with Microsoft to receive,  support related to Microsoft products and services some of this data may contain personal data.</span></span> <span data-ttu-id="89ca0-165">有关详细信息，请参阅[符合 GDPR 的 Microsoft 支持和专业服务数据主体请求](gdpr-dsr-prof-services.md)。</span><span class="sxs-lookup"><span data-stu-id="89ca0-165">For more information, see [Microsoft Support and Professional Services Data Subject Requests for the GDPR](gdpr-dsr-prof-services.md).</span></span>

### <a name="microsoft-controller-products"></a><span data-ttu-id="89ca0-166">Microsoft 控制者产品</span><span class="sxs-lookup"><span data-stu-id="89ca0-166">Microsoft Controller Products</span></span>

<span data-ttu-id="89ca0-167">在某些情况下，组织用户可能会访问 Microsoft 作为数据控制者的 Microsoft 产品或服务。</span><span class="sxs-lookup"><span data-stu-id="89ca0-167">In some circumstances, your organization's users may access Microsoft products or services for which Microsoft is the data controller.</span></span> <span data-ttu-id="89ca0-168">在这种情况下，用户需要直接向 Microsoft 发出自己的 DSR，并且 Microsoft 会直接向用户完成请求。</span><span class="sxs-lookup"><span data-stu-id="89ca0-168">In those cases, your users need to initiate their own DSRs directly to Microsoft, and Microsoft fulfills the requests directly to the user.</span></span>

### <a name="third-party-products"></a><span data-ttu-id="89ca0-169">第三方产品</span><span class="sxs-lookup"><span data-stu-id="89ca0-169">Third-party Products</span></span>

<span data-ttu-id="89ca0-170">对于通过 Microsoft 帐户身份验证访问的第三方产品和服务，应将任何数据主体请求定向到相应的第三方。</span><span class="sxs-lookup"><span data-stu-id="89ca0-170">For third-party products and services accessed through Microsoft account authentication, any data subject requests should be directed to the applicable third party.</span></span>

## <a name="data-subject-request-admin-tools"></a><span data-ttu-id="89ca0-171">数据主体请求管理工具</span><span class="sxs-lookup"><span data-stu-id="89ca0-171">Data Subject Request admin tools</span></span>

- <span data-ttu-id="89ca0-172">**安全与合规中心**：使用 [安全与合规性中心](https://aka.ms/stpsecurityandcompliance)或应用程序内部功能导出用户生成的数据。</span><span class="sxs-lookup"><span data-stu-id="89ca0-172">**Security & Compliance Center**: User-generated data is exported by the [Security & Compliance Center](https://aka.ms/stpsecurityandcompliance) or in-application features.</span></span>
- <span data-ttu-id="89ca0-173">**Azure AD 管理中心**：使用 [Azure AD 管理中心](https://ms.portal.azure.com/#blade/Microsoft_AAD_IAM/UserManagementMenuBlade/Allusers/menuId/)从 Azure Active Directory 和相关服务中删除数据主体。</span><span class="sxs-lookup"><span data-stu-id="89ca0-173">**Azure AD Admin Center**: Delete a data subject from Azure Active Directory and related services using [Azure AD Admin Center](https://ms.portal.azure.com/#blade/Microsoft_AAD_IAM/UserManagementMenuBlade/Allusers/menuId/).</span></span>
- <span data-ttu-id="89ca0-174">**Microsoft 数据日志导出**：租户管理员可使用 [Microsoft 数据记录导出](https://aka.ms/MicrosoftGDPR)功能导出系统生成的日志。</span><span class="sxs-lookup"><span data-stu-id="89ca0-174">**Microsoft Data Log Export**: System-generated logs can be exported by tenant administrators using the [Microsoft Data Log Export](https://aka.ms/MicrosoftGDPR).</span></span>

## <a name="learn-more"></a><span data-ttu-id="89ca0-175">了解更多</span><span class="sxs-lookup"><span data-stu-id="89ca0-175">Learn more</span></span>

- [<span data-ttu-id="89ca0-176">Microsoft 信任中心</span><span class="sxs-lookup"><span data-stu-id="89ca0-176">Microsoft Trust Center</span></span>](https://www.microsoft.com/trust-center/privacy/gdpr-overview)
