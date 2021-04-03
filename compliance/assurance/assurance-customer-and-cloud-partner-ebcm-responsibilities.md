---
title: 客户和云合作伙伴在企业业务连续性方面的责任
description: 了解 Microsoft 在服务事件期间采取了哪些措施来让你能够更好地准备业务连续性计划。
author: robmazz
ms.author: robmazz
manager: laurawi
ms.reviewer: sosstah
f1.keywords:
- NOCSH
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
- MS-Compliance
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 74bdf63fcf704aa285a2803e5b7af7455a0291c6
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497655"
---
# <a name="enterprise-business-continuity-management-customer-and-cloud-partner-responsibilities"></a><span data-ttu-id="79797-103">客户和云合作伙伴在企业业务连续性方面的责任</span><span class="sxs-lookup"><span data-stu-id="79797-103">Enterprise business continuity management customer and cloud partner responsibilities</span></span>

<span data-ttu-id="79797-104">你的组织与 Microsoft 之间建立了合作关系，让你能够向用户提供 Microsoft 365 云服务。</span><span class="sxs-lookup"><span data-stu-id="79797-104">Getting Microsoft 365 cloud services to your users is a partnership between your organization and Microsoft.</span></span> <span data-ttu-id="79797-105">由 Microsoft 提供服务，而你负责连接客户端终结点、管理标识和访问权限并管理这些服务的使用方式。</span><span class="sxs-lookup"><span data-stu-id="79797-105">Microsoft provides the services and you are responsible for connecting your client endpoints, managing identity and access and how those services are used.</span></span> <span data-ttu-id="79797-106">也有一些共同的责任，例如标识和目录基础结构。</span><span class="sxs-lookup"><span data-stu-id="79797-106">There are shared responsibilities, such as the identity and directory infrastructure as well.</span></span> <span data-ttu-id="79797-107">本文介绍了在出现服务事件的情况下要保证业务正常运转而需注意的一些关键事项，它可帮助你对发生服务事件时 Microsoft 要执行哪些操作设定预期。</span><span class="sxs-lookup"><span data-stu-id="79797-107">This article covers some of the critical items you need to be mindful of to keep your business functioning in the event of a service incident and it helps set expectations as to what Microsoft will do during a service incident.</span></span>

## <a name="transparency-during-service-incidents"></a><span data-ttu-id="79797-108">服务事件期间操作公开透明</span><span class="sxs-lookup"><span data-stu-id="79797-108">Transparency during service incidents</span></span>

<span data-ttu-id="79797-109">Microsoft 是值得信赖的合作伙伴，它构建了高弹性的云服务并按照结构化流程在服务事件发生时加以处理。</span><span class="sxs-lookup"><span data-stu-id="79797-109">As a trusted partner, Microsoft  builds highly resilient cloud services and follows structured procedures to resolve service incidents when they happen.</span></span> <span data-ttu-id="79797-110">当服务事件发生时，Microsoft 意识到 **及时**、**有针对性的** 和 **高度可触达的** 通信对客户而言非常重要。</span><span class="sxs-lookup"><span data-stu-id="79797-110">When a service incident occurs, Microsoft recognizes that **timely**, **targeted**, and **highly available** communications are critical for customers.</span></span>

## <a name="timely"></a><span data-ttu-id="79797-111">及时</span><span class="sxs-lookup"><span data-stu-id="79797-111">Timely</span></span>

<span data-ttu-id="79797-112">Microsoft 通过更新 Microsoft 365 管理门户上租户专用的服务运行状况仪表板 (SHD) 来通知 Microsoft 365 管理员。</span><span class="sxs-lookup"><span data-stu-id="79797-112">Microsoft notifies Microsoft 365 administrators by updating the tenant-specific Service Health Dashboard (SHD) in the Microsoft 365 Admin Portal.</span></span> <span data-ttu-id="79797-113">服务事件动态通常每小时提供一次。</span><span class="sxs-lookup"><span data-stu-id="79797-113">Service incident updates are normally provided on an hourly cadence.</span></span> <span data-ttu-id="79797-114">如果需调整频率，我们将在 SHD 通信公告中让你获知所做的更改。</span><span class="sxs-lookup"><span data-stu-id="79797-114">If a different cadence is needed we'll keep you informed of the change in the SHD communication postings.</span></span>

## <a name="targeted"></a><span data-ttu-id="79797-115">有针对性</span><span class="sxs-lookup"><span data-stu-id="79797-115">Targeted</span></span>

<span data-ttu-id="79797-116">在大多数情况下，当我们的监视系统检测到问题时，我们可确定受影响的客户群（范围从一名客户到区域或更大范围不等），并向这些客户发送必要的通知。</span><span class="sxs-lookup"><span data-stu-id="79797-116">In most cases, when our monitoring systems detect an issue, we can identify the affected customer base, from a single customer up to region or beyond and direct the necessary communications to those customers.</span></span> <span data-ttu-id="79797-117">这可帮助你了解业务须知信息，而不受对你没有影响的不必要通知的干扰。</span><span class="sxs-lookup"><span data-stu-id="79797-117">This helps you know what you need to know for your business and not be distracted by noise notifications that don't impact you.</span></span> <span data-ttu-id="79797-118">例如，如果特定邮箱数据库受到影响，我们能够准确确定哪些客户有用户位于受影响的基础结构中并向他们发送通知。</span><span class="sxs-lookup"><span data-stu-id="79797-118">For example, if a specific mailbox database is impacted, we're able to identify exactly which customers have users on the affected infrastructure and scope our communications to them.</span></span> <span data-ttu-id="79797-119">如果事件影响范围不明确，我们会向可能受到影响的范围最广的客户发送通知。</span><span class="sxs-lookup"><span data-stu-id="79797-119">If the scope of impact of the incident is unclear, we expand our communications out to the widest group of customers who are potentially impacted.</span></span>

## <a name="highly-available"></a><span data-ttu-id="79797-120">高可用性</span><span class="sxs-lookup"><span data-stu-id="79797-120">Highly available</span></span>

<span data-ttu-id="79797-121">Microsoft 维持了多个渠道可供客户用来获取服务状态通知。</span><span class="sxs-lookup"><span data-stu-id="79797-121">Microsoft maintains multiple channels for service status communications that customers can use.</span></span>

- <span data-ttu-id="79797-122">如果管理中心或其中的服务运行状况仪表板不可用，你可使用我们的[备份网站](https://status.office365.com/)监视服务状态。</span><span class="sxs-lookup"><span data-stu-id="79797-122">In the event the Admin center or the Service Health Dashboard within the Admin center are unavailable, you can monitor the service status using our [backup site](https://status.office365.com/).</span></span>
- <span data-ttu-id="79797-123">我们保留了 Twitter 帐户 [@MSFT365Status](https://twitter.com/msft365status?lang=en)，我们将在这里答复影响报告并发布 SHD 影响事件的最新动态。</span><span class="sxs-lookup"><span data-stu-id="79797-123">We maintain a Twitter account [@MSFT365Status](https://twitter.com/msft365status?lang=en) where we will respond to reports of impact and post updates on SHD impacting events.</span></span>
- <span data-ttu-id="79797-124">借助适用于 Microsoft 365 租户管理员的管理应用，可随时随地了解你所在组织的 Microsoft 365 服务状态。</span><span class="sxs-lookup"><span data-stu-id="79797-124">The Admin App for Microsoft 365 tenant administrators gives you the ability to connect with your organization's Microsoft 365 service status on the go.</span></span> <span data-ttu-id="79797-125">租户管理员可在其移动设备上查看服务运行状况信息和维护状态更新。</span><span class="sxs-lookup"><span data-stu-id="79797-125">Tenant administrators will have the ability to view service health information and maintenance status updates from their mobile devices.</span></span> <span data-ttu-id="79797-126">有关详细信息，请访问[管理应用常见问题解答](/office365/admin/admin-overview/admin-mobile-app)。</span><span class="sxs-lookup"><span data-stu-id="79797-126">For more information, visit the [Admin App FAQ](/office365/admin/admin-overview/admin-mobile-app).</span></span>
- <span data-ttu-id="79797-127">通过 [Microsoft 365 服务通信 API](/office365/servicedescriptions/office-365-platform-service-description/service-health-and-continuity#office-365-service-communications-api) 可访问服务通知，从而可更轻松地监视你的环境。</span><span class="sxs-lookup"><span data-stu-id="79797-127">The [Microsoft 365 Service Communications API](/office365/servicedescriptions/office-365-platform-service-description/service-health-and-continuity#office-365-service-communications-api) enables you to access service communications so you can more easily monitor your environment.</span></span> <span data-ttu-id="79797-128">可连接到 API、接收实时服务运行状况数据，还可在内部仪表板上发布消息，将事件告知给企业用户。</span><span class="sxs-lookup"><span data-stu-id="79797-128">You can connect to the API, receive real-time service health data, and publish the information on an internal dashboard to inform enterprise users of incidents.</span></span> <span data-ttu-id="79797-129">通过在内部分发信息，可降低服务中断期间支持人员的负担。</span><span class="sxs-lookup"><span data-stu-id="79797-129">Distributing the information internally can decrease your helpdesk traffic during an outage.</span></span>
- <span data-ttu-id="79797-130">对于主要事件，Microsoft 会在管理中心向 SHD 发布事后回顾 (PIR)。</span><span class="sxs-lookup"><span data-stu-id="79797-130">For major incidents, Microsoft publishes Post Incident Reviews (PIR) to the SHD within the Admin center.</span></span> <span data-ttu-id="79797-131">PIR 包含了关键事件信息，可帮助你了解服务中断的本质。</span><span class="sxs-lookup"><span data-stu-id="79797-131">PIRs contain key incident information to help you understand the nature of the outage.</span></span> <span data-ttu-id="79797-132">它通常包含以下部分：</span><span class="sxs-lookup"><span data-stu-id="79797-132">It generally contains the following sections:</span></span>
    - <span data-ttu-id="79797-133">对用户的影响</span><span class="sxs-lookup"><span data-stu-id="79797-133">user impact</span></span>
    - <span data-ttu-id="79797-134">影响范围</span><span class="sxs-lookup"><span data-stu-id="79797-134">scope of impact</span></span>
    - <span data-ttu-id="79797-135">事件开始/结束日期和时间</span><span class="sxs-lookup"><span data-stu-id="79797-135">incident start-end date and time</span></span>
    - <span data-ttu-id="79797-136">根本原因</span><span class="sxs-lookup"><span data-stu-id="79797-136">root cause</span></span>
    - <span data-ttu-id="79797-137">执行的操作</span><span class="sxs-lookup"><span data-stu-id="79797-137">actions taken</span></span>
    - <span data-ttu-id="79797-138">后续步骤</span><span class="sxs-lookup"><span data-stu-id="79797-138">next steps</span></span>
- <span data-ttu-id="79797-139">可在 Microsoft 365 消息中心查看辅助消息，例如有关即将进行的更改、新功能或计划内维护的通知。</span><span class="sxs-lookup"><span data-stu-id="79797-139">Ancillary communications are available in the Microsoft 365 Message Center, such as notices of upcoming changes, new features, or planned maintenance.</span></span>
- <span data-ttu-id="79797-140">有关详细信息，请参阅[服务运行状况和连续性指南](/office365/servicedescriptions/office-365-platform-service-description/service-health-and-continuity)，详细了解不同的通信渠道以及服务运行状况监视方式。</span><span class="sxs-lookup"><span data-stu-id="79797-140">For more information, see the [Service Health and Continuity guide](/office365/servicedescriptions/office-365-platform-service-description/service-health-and-continuity) to learn more about the different communication channels and how to monitor service health.</span></span>

<span data-ttu-id="79797-141">你的组织与 Microsoft 之间建立了合作关系，让你能够提供对 Microsoft 365 联机服务的访问权限。</span><span class="sxs-lookup"><span data-stu-id="79797-141">Providing access to Microsoft 365 online services is a partnership between your organization and Microsoft.</span></span> <span data-ttu-id="79797-142">下图总结了服务事件和定期操作期间 Microsoft 与客户之间责任的平衡。</span><span class="sxs-lookup"><span data-stu-id="79797-142">The following chart summarizes the balance of responsibility for both Microsoft and the customer during a service incident and during regular operations.</span></span>

![客户与 Microsoft 责任间的平衡](../media/responsibilities.png)

## <a name="your-environment---service-continuity"></a><span data-ttu-id="79797-144">你的环境 - 服务连续性</span><span class="sxs-lookup"><span data-stu-id="79797-144">Your environment - service continuity</span></span>

<span data-ttu-id="79797-145">考虑连续性计划时，请注意可能影响你的组织的事件以及其整体通知能力。</span><span class="sxs-lookup"><span data-stu-id="79797-145">When thinking about your continuity plan, be mindful of events which may impact your organization and it's overall ability to communicate.</span></span> <span data-ttu-id="79797-146">概括来讲，有三个因素可能会影响你的业务。</span><span class="sxs-lookup"><span data-stu-id="79797-146">At a high level there are three factors that could impact your business.</span></span>

### <a name="people"></a><span data-ttu-id="79797-147">人员</span><span class="sxs-lookup"><span data-stu-id="79797-147">People</span></span>

<span data-ttu-id="79797-148">考虑自然灾害或流行病等会影响员工的事件。</span><span class="sxs-lookup"><span data-stu-id="79797-148">Consider events that would cause impact to your workforce like a natural disaster or a pandemic.</span></span> <span data-ttu-id="79797-149">如果员工分布广泛，则由于本质上不太可能造成大规模的影响，因而此因素常会被忽略。</span><span class="sxs-lookup"><span data-stu-id="79797-149">This is often overlooked, due to the unlikely nature of a broad-scale impact if your workforce is widely distributed.</span></span> <span data-ttu-id="79797-150">但是，如果有很大比例的员工没法工作，你的企业才会继续运转吗？</span><span class="sxs-lookup"><span data-stu-id="79797-150">But, if a large percentage of the workforce were offline, would your business continue to operate?</span></span> <span data-ttu-id="79797-151">那么如何缓解这一影响呢？</span><span class="sxs-lookup"><span data-stu-id="79797-151">How do you mitigate that?</span></span>

### <a name="location"></a><span data-ttu-id="79797-152">位置</span><span class="sxs-lookup"><span data-stu-id="79797-152">Location</span></span>

<span data-ttu-id="79797-153">很多组织都要求员工在特定的物理位置或网络位置工作，以便连接到企业系统和云服务。</span><span class="sxs-lookup"><span data-stu-id="79797-153">Many organizations require employees to be in specific physical or network locations in order to connect to enterprise systems and cloud services.</span></span>  
<span data-ttu-id="79797-154">Microsoft 发布了[网络连接原则](/microsoft-365/enterprise/microsoft-365-network-connectivity-principles)，它可引导企业找到最佳做法来设置到云资源的网络连接。</span><span class="sxs-lookup"><span data-stu-id="79797-154">Microsoft publishes [network connectivity principles](/microsoft-365/enterprise/microsoft-365-network-connectivity-principles) that guide enterprises through best practices for setting up network connectivity to cloud resources.</span></span> <span data-ttu-id="79797-155">优化示例包括实施拆分的隧道 VPN，以便直接从用户的网络而不是通过 VPN 隧道进行连接。</span><span class="sxs-lookup"><span data-stu-id="79797-155">Examples of optimization include implementation of split tunnel VPNs to allow connections directly from a user’s network rather than over a VPN tunnel.</span></span>  <span data-ttu-id="79797-156">虽然这些连接原则对维持低延迟连接很重要，但要保证服务弹性，需要用替代方法连接到公司资源来进行常规协作。</span><span class="sxs-lookup"><span data-stu-id="79797-156">While these connectivity principles are important for maintaining low-latency connections, service resiliency requires alternative methods of connecting to corporate resources for general collaboration.</span></span>

### <a name="systems"></a><span data-ttu-id="79797-157">系统</span><span class="sxs-lookup"><span data-stu-id="79797-157">Systems</span></span>

<span data-ttu-id="79797-158">很多协作解决方案都依赖于系统，例如公司广域网 (WAN)。</span><span class="sxs-lookup"><span data-stu-id="79797-158">Many collaboration solutions are dependent on systems, such as the company wide area network (WAN).</span></span> <span data-ttu-id="79797-159">当这些系统不可用时，你的组织会如何应对？</span><span class="sxs-lookup"><span data-stu-id="79797-159">When those systems are not available, how would your organization respond?</span></span>
<span data-ttu-id="79797-160">下图展示了可能影响多个方面的问题。</span><span class="sxs-lookup"><span data-stu-id="79797-160">This graphic represents issues that may impact more than one area.</span></span> <span data-ttu-id="79797-161">随附的表格提供了要考虑的示例</span><span class="sxs-lookup"><span data-stu-id="79797-161">The accompanying table provides examples to consider</span></span>

![维恩系统图](../media/venn-diagram.png)

<span data-ttu-id="79797-163">你的连续性计划应将上述每个方面都考虑在内。</span><span class="sxs-lookup"><span data-stu-id="79797-163">Your continuity plans should consider each of these areas.</span></span> <span data-ttu-id="79797-164">例如，如果你需要用户访问公司网络，但当地下暴风雪了，那么这些用户如果能够访问关键资源呢？</span><span class="sxs-lookup"><span data-stu-id="79797-164">For example: If you require users to be on the corporate network and there is a snowstorm, how do those users gain access to key resources?</span></span> <span data-ttu-id="79797-165">如果大雪让用户没法抵达办公室，而服务工程师必须连接到公司网络，有没有策略批准他们在家中持有公司笔记本电脑呢？</span><span class="sxs-lookup"><span data-stu-id="79797-165">If the snow prevents travel into the office and service engineers are required to connect to the corporate network, is there a policy mandating they have their corporate laptops in their possession at home?</span></span>
