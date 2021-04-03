---
title: 用于 Office Server 的 GDPR
description: 了解如何解决 Office 本地服务器中的一般数据保护条例 (GDPR) 要求。
f1.keywords:
- NOCSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
titleSuffix: Microsoft GDPR
ms.collection: MS-Compliance
ms.custom: seo-marvel-apr2020
hideEdit: true
ms.openlocfilehash: 58f3d9108fe36175c2ce879054a35c2cc94d93c8
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496082"
---
# <a name="gdpr-for-office-on-premises-servers"></a><span data-ttu-id="d9f87-103">用于本地 Office 服务器的 GDPR</span><span class="sxs-lookup"><span data-stu-id="d9f87-103">GDPR for Office on-premises Servers</span></span>

<span data-ttu-id="d9f87-p101">一般数据保护条例 (GDPR) 为组织提供了保护个人数据和适当回应数据主体请求的要求。本系列文章为本地工作负载提供了推荐的方法：</span><span class="sxs-lookup"><span data-stu-id="d9f87-p101">The General Data Protection Regulation (GDPR) introduces requirements for organizations to protect personal data and respond appropriately to data subject requests. This series of articles provides recommended approaches for on-premises workloads:</span></span>

- [<span data-ttu-id="d9f87-106">SharePoint Server</span><span class="sxs-lookup"><span data-stu-id="d9f87-106">SharePoint Server</span></span>](gdpr-for-sharepoint-server.md)

- [<span data-ttu-id="d9f87-107">Exchange Server</span><span class="sxs-lookup"><span data-stu-id="d9f87-107">Exchange Server</span></span>](gdpr-for-exchange-server.md)

- [<span data-ttu-id="d9f87-108">Skype for Business Server</span><span class="sxs-lookup"><span data-stu-id="d9f87-108">Skype for Business Server</span></span>](gdpr-for-skype-for-business-server.md)

- [<span data-ttu-id="d9f87-109">Project Server</span><span class="sxs-lookup"><span data-stu-id="d9f87-109">Project Server</span></span>](gdpr-for-project-server.md)

- [<span data-ttu-id="d9f87-110">Office Web Apps Server 和 Office Online Server</span><span class="sxs-lookup"><span data-stu-id="d9f87-110">Office Web Apps Server and Office Online Server</span></span>](gdpr-for-office-online-server.md)

- [<span data-ttu-id="d9f87-111">本地文件共享</span><span class="sxs-lookup"><span data-stu-id="d9f87-111">On-premises file shares</span></span>](gdpr-for-on-premises-file-shares.md)

<span data-ttu-id="d9f87-112">有关 GDPR 以及 Microsoft 如何为你提供帮助的详细信息，请参阅 [Microsoft 信任中心](https://www.microsoft.com/trust-center/privacy/gdpr-overview
)。</span><span class="sxs-lookup"><span data-stu-id="d9f87-112">For more information about the GDPR and how Microsoft can help you, see the [Microsoft Trust Center](https://www.microsoft.com/trust-center/privacy/gdpr-overview
).</span></span>

<span data-ttu-id="d9f87-p102">在开展有关本地数据的任何工作之前，请咨询你的法律和合规性团队以寻求指导并了解现有分类架构和处理个人数据的方法。Microsoft 提供了有关在 Microsoft GDPR 数据发现工具包（位于 [https://aka.ms/gdprpartners](<https://aka.ms/gdprpartners>)）中开发和扩展分类架构的建议。此工具包还介绍了将本地数据移动到云的方法，可以使用更复杂的数据治理功能（如果需要）。该部分中的文章提供了有关保留在本地的数据的建议。</span><span class="sxs-lookup"><span data-stu-id="d9f87-p102">Before doing any work with on-premises data, consult with your legal and compliance teams to seek guidance and to learn about existing classification schemas and approaches to working with personal data. Microsoft provides recommendations for developing and extending classifications schemas in the Microsoft GDPR Data Discovery Toolkit at [https://aka.ms/gdprpartners](<https://aka.ms/gdprpartners>). This toolkit also describes approaches for moving on-premises data to the cloud where you can use more sophisticated data governance capabilities, if this is desired. The articles in this section provide recommendations for data that is intended to remain on premises.</span></span>

<span data-ttu-id="d9f87-p103">下图列出了在各个工作负载中使用的推荐功能，用于发现、保护和监视个人数据并对其进行分类。有关更多信息，请参阅该部分中的文章。</span><span class="sxs-lookup"><span data-stu-id="d9f87-p103">The following illustration lists recommended capabilities to use across each of these workloads to discover, classify, protect, and monitor personal data. See the articles in this section for more information.</span></span>

![描述跨工作负载发现、分类、保护和监视个人数据的功能图表](../media/gdpr-for-office-servers-image1.png)

## <a name="illustration-description"></a><span data-ttu-id="d9f87-120">图示说明</span><span class="sxs-lookup"><span data-stu-id="d9f87-120">Illustration description</span></span>

<span data-ttu-id="d9f87-121">为便于访问，下表提供了上图中的相同示例。</span><span class="sxs-lookup"><span data-stu-id="d9f87-121">For accessibility, the following table provides the same examples in the illustration.</span></span>

****

|<span data-ttu-id="d9f87-122">操作</span><span class="sxs-lookup"><span data-stu-id="d9f87-122">Action</span></span>|<span data-ttu-id="d9f87-123">Windows Server 文件共享</span><span class="sxs-lookup"><span data-stu-id="d9f87-123">Windows Server file shares</span></span>|<span data-ttu-id="d9f87-124">SharePoint Server</span><span class="sxs-lookup"><span data-stu-id="d9f87-124">SharePoint Server</span></span>|<span data-ttu-id="d9f87-125">Exchange Server</span><span class="sxs-lookup"><span data-stu-id="d9f87-125">Exchange Server</span></span>|<span data-ttu-id="d9f87-126">Skype for Business</span><span class="sxs-lookup"><span data-stu-id="d9f87-126">Skype for Business</span></span>|<span data-ttu-id="d9f87-127">Project Server</span><span class="sxs-lookup"><span data-stu-id="d9f87-127">Project Server</span></span>|
|---|---|---|---|---|---|
|<span data-ttu-id="d9f87-128">发现</span><span class="sxs-lookup"><span data-stu-id="d9f87-128">Discover</span></span>|<span data-ttu-id="d9f87-129">Azure 信息保护扫描程序<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="d9f87-129">Azure Information Protection scanner<sup>\*</sup></span></span>|<span data-ttu-id="d9f87-130">搜索中心或电子数据展示（对数据进行分类后）</span><span class="sxs-lookup"><span data-stu-id="d9f87-130">Search Center or eDiscovery (after data is classified)</span></span> <br/><br/> <span data-ttu-id="d9f87-131">Azure 信息保护扫描程序<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="d9f87-131">Azure Information Protection scanner<sup>\*</sup></span></span>|<span data-ttu-id="d9f87-132">Exchange 电子数据展示门户</span><span class="sxs-lookup"><span data-stu-id="d9f87-132">Exchange eDiscovery Portal</span></span>|<span data-ttu-id="d9f87-133">Exchange 电子数据展示门户</span><span class="sxs-lookup"><span data-stu-id="d9f87-133">Exchange eDiscovery portal</span></span>|<span data-ttu-id="d9f87-134">用于发现和导出的 SQL 脚本</span><span class="sxs-lookup"><span data-stu-id="d9f87-134">SQL scripts for discovery and exporting</span></span>|
|<span data-ttu-id="d9f87-135">分类</span><span class="sxs-lookup"><span data-stu-id="d9f87-135">Classify</span></span>|<span data-ttu-id="d9f87-136">Azure 信息保护扫描程序<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="d9f87-136">Azure Information Protection scanner<sup>\*</sup></span></span> <br/><br/> <span data-ttu-id="d9f87-137">Office 365 敏感信息类型</span><span class="sxs-lookup"><span data-stu-id="d9f87-137">Office 365 sensitive information types</span></span>|<span data-ttu-id="d9f87-138">Azure 信息保护扫描程序<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="d9f87-138">Azure Information Protection scanner<sup>\*</sup></span></span> <br/><br/> <span data-ttu-id="d9f87-139">Office 365 敏感信息类型</span><span class="sxs-lookup"><span data-stu-id="d9f87-139">Office 365 sensitive information types</span></span>|<span data-ttu-id="d9f87-140">Exchange 保留标记和保留策略</span><span class="sxs-lookup"><span data-stu-id="d9f87-140">Exchange retention tags and retention policies</span></span>|<span data-ttu-id="d9f87-141">Exchange 保留标记和保留策略</span><span class="sxs-lookup"><span data-stu-id="d9f87-141">Exchange retention tags and retention policies</span></span>||
|<span data-ttu-id="d9f87-142">保护</span><span class="sxs-lookup"><span data-stu-id="d9f87-142">Protect</span></span>||<span data-ttu-id="d9f87-143">Exchange Server 数据丢失防护规则</span><span class="sxs-lookup"><span data-stu-id="d9f87-143">Exchange Server data loss prevention rules</span></span> <br/><br/> <span data-ttu-id="d9f87-144">权限、库 IRM-保护</span><span class="sxs-lookup"><span data-stu-id="d9f87-144">Permissions, IRM-protection for libraries</span></span>|<span data-ttu-id="d9f87-145">Exchange Server 数据丢失防护规则</span><span class="sxs-lookup"><span data-stu-id="d9f87-145">Exchange Server data loss prevention rules</span></span> <br/><br/> <span data-ttu-id="d9f87-146">IRM 与 Exchange Server 的集成</span><span class="sxs-lookup"><span data-stu-id="d9f87-146">IRM integration with Exchange Server</span></span>|||
|<span data-ttu-id="d9f87-147">监视</span><span class="sxs-lookup"><span data-stu-id="d9f87-147">Monitor</span></span>|<span data-ttu-id="d9f87-148">将日志与 SIEM 工具集成</span><span class="sxs-lookup"><span data-stu-id="d9f87-148">Integrate logs with SIEM tools</span></span>|<span data-ttu-id="d9f87-149">将日志与 SIEM 工具集成</span><span class="sxs-lookup"><span data-stu-id="d9f87-149">Integrate logs with SIEM tools</span></span>|<span data-ttu-id="d9f87-150">将日志与 SIEM 工具集成</span><span class="sxs-lookup"><span data-stu-id="d9f87-150">Integrate logs with SIEM tools</span></span>|<span data-ttu-id="d9f87-151">将日志与 SIEM 工具集成</span><span class="sxs-lookup"><span data-stu-id="d9f87-151">Integrate logs with SIEM tools</span></span>|<span data-ttu-id="d9f87-152">将日志与 SIEM 工具集成</span><span class="sxs-lookup"><span data-stu-id="d9f87-152">Integrate logs with SIEM tools</span></span>|
|

<span data-ttu-id="d9f87-153"><sup>\*</sup>注意，保护功能会加密文件。</span><span class="sxs-lookup"><span data-stu-id="d9f87-153"><sup>\*</sup> Note that protection encrypts the file.</span></span> <span data-ttu-id="d9f87-154">因此，SharePoint Server 无法在受保护的文件中查找敏感信息类型。</span><span class="sxs-lookup"><span data-stu-id="d9f87-154">Consequently, SharePoint Server can't find the sensitive information types in protected files.</span></span>
