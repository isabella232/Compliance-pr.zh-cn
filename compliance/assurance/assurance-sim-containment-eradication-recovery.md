---
title: Microsoft 365 安全事件管理：抑制、隔离和恢复
description: 本文概述了 Microsoft 365 中的安全事件管理控制、隔离和恢复过程。
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
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 702735ed2ba35a4f3b0a02123f0c58b5fb4d397e
ms.sourcegitcommit: d67e4d4fdc664f1da450c8ef2f6732e19bdd403a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/28/2021
ms.locfileid: "50037578"
---
# <a name="microsoft-365-security-incident-management-containment-eradication-and-recovery"></a><span data-ttu-id="bd916-103">Microsoft 365 安全事件管理：抑制、隔离和恢复</span><span class="sxs-lookup"><span data-stu-id="bd916-103">Microsoft 365 security incident management: Containment, eradication, and recovery</span></span>

<span data-ttu-id="bd916-104">根据 Microsoft 365 安全响应团队、服务团队和其他人员执行的分析，制定适当的抑制和恢复计划，以最大限度地减少安全事件的影响。</span><span class="sxs-lookup"><span data-stu-id="bd916-104">Based on the analysis performed by the Microsoft 365 Security Response team, the service team, and others, an appropriate containment and recovery plan is developed to minimize the effect of the security incident.</span></span> <span data-ttu-id="bd916-105">然后，相应的服务团队在 Microsoft 365 安全响应团队的支持下，在生产中应用该计划。</span><span class="sxs-lookup"><span data-stu-id="bd916-105">The appropriate service teams then apply that plan in production with support from the Microsoft 365 Security Response team.</span></span>

## <a name="containment"></a><span data-ttu-id="bd916-106">包含</span><span class="sxs-lookup"><span data-stu-id="bd916-106">Containment</span></span>

<span data-ttu-id="bd916-107">在检测到安全事件后，在攻击者可以访问更多资源或造成更多损害之前，必须包含入侵。</span><span class="sxs-lookup"><span data-stu-id="bd916-107">After detecting a security incident, it is important to contain the intrusion before the adversary can access more resources or cause more damage.</span></span> <span data-ttu-id="bd916-108">我们的安全事件响应过程的主要目标是限制客户或他们的数据，或 Microsoft 系统、服务和应用程序的影响。</span><span class="sxs-lookup"><span data-stu-id="bd916-108">The primary goal of our security incident response procedures is to limit impact to customers or their data, or to Microsoft systems, services, and applications.</span></span>

## <a name="eradication"></a><span data-ttu-id="bd916-109">一个</span><span class="sxs-lookup"><span data-stu-id="bd916-109">Eradication</span></span>

<span data-ttu-id="bd916-110">解决是一个以高度可信度消除安全事件的根本原因的过程。</span><span class="sxs-lookup"><span data-stu-id="bd916-110">Eradication is the process of eliminating the root cause of the security incident with a high degree of confidence.</span></span> <span data-ttu-id="bd916-111">目标是双重的：</span><span class="sxs-lookup"><span data-stu-id="bd916-111">The goal is two-fold:</span></span>

- <span data-ttu-id="bd916-112">从环境中完全退出攻击者</span><span class="sxs-lookup"><span data-stu-id="bd916-112">to evict the adversary completely from the environment</span></span>
- <span data-ttu-id="bd916-113">缓解漏洞 (如果已知) 启用或可能允许攻击者重新访问环境。</span><span class="sxs-lookup"><span data-stu-id="bd916-113">to mitigate the vulnerability (if known) that enabled or could enable the adversary to reenter the environment.</span></span>

<span data-ttu-id="bd916-114">根据事件的性质、安全事件的范围、渗透的深度和可能的威胁，Microsoft 365 安全响应团队将建议服务团队采用管理技术。</span><span class="sxs-lookup"><span data-stu-id="bd916-114">Depending on the nature of the incident, the scope of the security incident, the depth of the penetration and possible repercussions, the Microsoft 365 Security Response team will recommend that service teams adopt eradication techniques.</span></span> <span data-ttu-id="bd916-115">考虑到这些不一致步骤可能导致的潜在业务影响，如有必要，这些决策由服务团队和 Microsoft 365 安全响应团队在执行事件管理器 (进行详细分析和批准后) 。</span><span class="sxs-lookup"><span data-stu-id="bd916-115">Considering the potential business impact that may be caused by these eradication steps, these decisions will be made by service teams and the Microsoft 365 Security Response team after a detailed analysis and approval from the Executive Incident Manager (if necessary).</span></span>

## <a name="recovery"></a><span data-ttu-id="bd916-116">恢复</span><span class="sxs-lookup"><span data-stu-id="bd916-116">Recovery</span></span>

<span data-ttu-id="bd916-117">当响应团队获得合理的可信度，即攻击者已从环境中退出并且所有已知的易受攻击的路径都已被消除时，各个服务团队将启动还原步骤，以将服务引入已知且良好的配置。</span><span class="sxs-lookup"><span data-stu-id="bd916-117">As the response team gains a reasonable level of confidence that the adversary has been evicted from the environment and all known vulnerable paths have been eliminated, the individual service teams, will initiate restoration steps to bring the service to a known and good configuration.</span></span> <span data-ttu-id="bd916-118">这些还原步骤将咨询 Microsoft 365 安全响应团队。</span><span class="sxs-lookup"><span data-stu-id="bd916-118">These restoration steps will be in consultation with the Microsoft 365 Security Response team.</span></span> <span data-ttu-id="bd916-119">此活动包括标识服务的上次已知良好状态、从备份还原到此状态、检查还原状态中的易受攻击路径等。Microsoft 365 安全响应团队与服务团队一起协作，将确定最适合环境的恢复计划。</span><span class="sxs-lookup"><span data-stu-id="bd916-119">This activity includes identifying the last known good state of the service, restoring from backups to this state, inspecting vulnerable attack paths in the restored state, etc. The Microsoft 365 Security Response team, in consultation with the service teams, will determine the best possible recovery plan for the environment.</span></span>

<span data-ttu-id="bd916-120">恢复的一个关键方面是增强的规划和控制，以验证恢复计划已成功执行，并且环境中不存在泄露的迹象。</span><span class="sxs-lookup"><span data-stu-id="bd916-120">A key aspect to the recovery is to have enhanced vigilance and controls in place to validate that the recovery plan has been successfully executed, and that no signs of breach exist in the environment.</span></span>

## <a name="customer-notification-of-security-incident"></a><span data-ttu-id="bd916-121">客户安全事件通知</span><span class="sxs-lookup"><span data-stu-id="bd916-121">Customer notification of security incident</span></span>

<span data-ttu-id="bd916-122">如果 Microsoft 确定发生了安全事件，我们将在我们同意的合同和合规性要求内，以过度延迟方式通知您。</span><span class="sxs-lookup"><span data-stu-id="bd916-122">If Microsoft determines that a security incident has occurred, we will notify you with undue delay, and within contractual and compliance requirements we have agreed to.</span></span> <span data-ttu-id="bd916-123">确定所有受影响的租户后，Microsoft 365 客户体验 (CxP) 通信团队将努力确定可能适用于受影响租户的任何相关法规。</span><span class="sxs-lookup"><span data-stu-id="bd916-123">After identifying all affected tenants, the Microsoft 365 Customer Experience (CxP) Communications team works to identify any relevant regulations that might apply to affected tenants.</span></span> <span data-ttu-id="bd916-124">Microsoft 365 CxP 通信团队使用适用法规中定义的相应通信通道通知相应的租户联系人。</span><span class="sxs-lookup"><span data-stu-id="bd916-124">The Microsoft 365 CxP Communications team uses the appropriate communication channel defined in applicable regulations to notify the appropriate tenant contact.</span></span>

<span data-ttu-id="bd916-125">通知将包括有关事件的详细信息，例如事件描述、对客户数据的影响（如果有）以及 Microsoft 采取的操作和/或建议客户为解决问题和防止重复采取的操作。</span><span class="sxs-lookup"><span data-stu-id="bd916-125">Notification will include detailed information about the incident, such as a description of the incident, the effect on customer data, if any, actions taken by Microsoft, and/or suggested actions for customers to take to resolve the issue and prevent recurrence.</span></span> <span data-ttu-id="bd916-126">通知将传递给 Microsoft 365 租户 (管理员) 管理员。</span><span class="sxs-lookup"><span data-stu-id="bd916-126">Notification will be delivered to the designated administrator(s) of the Microsoft 365 tenant.</span></span> <span data-ttu-id="bd916-127">若要确保收到通知，应确保管理员在租户配置文件中提供和维护准确的联系信息。</span><span class="sxs-lookup"><span data-stu-id="bd916-127">To ensure notifications are received, you should ensure that your administrators provide and maintain accurate contact information in their tenant profiles.</span></span> <span data-ttu-id="bd916-128">此外，根据事件的性质，还可通过 Microsoft 365 服务运行状况仪表板通知客户[。](http://status.yammer.com/)</span><span class="sxs-lookup"><span data-stu-id="bd916-128">In addition, depending on the nature of the incident, customers can also be notified via the Microsoft 365 Service Health Dashboard[.](http://status.yammer.com/)</span></span>

## <a name="related-articles"></a><span data-ttu-id="bd916-129">相关文章</span><span class="sxs-lookup"><span data-stu-id="bd916-129">Related articles</span></span>

- [<span data-ttu-id="bd916-130">Microsoft 365 安全事件管理</span><span class="sxs-lookup"><span data-stu-id="bd916-130">Microsoft 365 security incident management</span></span>](assurance-security-incident-management.md)
- [<span data-ttu-id="bd916-131">Microsoft 365 安全事件管理准备</span><span class="sxs-lookup"><span data-stu-id="bd916-131">Microsoft 365 security incident management preparation</span></span>](assurance-sim-preparation.md)
- [<span data-ttu-id="bd916-132">Microsoft 365 安全事件管理检测和分析</span><span class="sxs-lookup"><span data-stu-id="bd916-132">Microsoft 365 security incident management detection and analysis</span></span>](assurance-sim-detection-analysis.md)
- [<span data-ttu-id="bd916-133">Microsoft 365 安全事件管理后期活动</span><span class="sxs-lookup"><span data-stu-id="bd916-133">Microsoft 365 security incident management post-incident activity</span></span>](assurance-sim-post-incident-activity.md)
