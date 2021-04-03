---
title: Microsoft 365 安全事件管理：包含、消除和恢复
description: 本文概述了 Microsoft 365 中的安全事件管理包含、隔离和恢复过程。
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
hideEdit: true
ms.openlocfilehash: 7fff9c1909f0acd076945e3d569b143fe2324c0f
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496716"
---
# <a name="microsoft-365-security-incident-management-containment-eradication-and-recovery"></a><span data-ttu-id="7a6b1-103">Microsoft 365 安全事件管理：包含、消除和恢复</span><span class="sxs-lookup"><span data-stu-id="7a6b1-103">Microsoft 365 security incident management: Containment, eradication, and recovery</span></span>

<span data-ttu-id="7a6b1-104">根据 Microsoft 365 安全响应团队、服务团队和其他人员执行的分析，制定了适当的抑制和恢复计划，以最大限度地减少安全事件的影响。</span><span class="sxs-lookup"><span data-stu-id="7a6b1-104">Based on the analysis performed by the Microsoft 365 Security Response team, the service team, and others, an appropriate containment and recovery plan is developed to minimize the effect of the security incident.</span></span> <span data-ttu-id="7a6b1-105">然后，相应的服务团队在生产中应用该计划，并获得 Microsoft 365 安全响应团队的支持。</span><span class="sxs-lookup"><span data-stu-id="7a6b1-105">The appropriate service teams then apply that plan in production with support from the Microsoft 365 Security Response team.</span></span>

## <a name="containment"></a><span data-ttu-id="7a6b1-106">包含</span><span class="sxs-lookup"><span data-stu-id="7a6b1-106">Containment</span></span>

<span data-ttu-id="7a6b1-107">在检测到安全事件后，必须包含入侵，然后攻击者才能访问更多资源或造成更多损害。</span><span class="sxs-lookup"><span data-stu-id="7a6b1-107">After detecting a security incident, it is important to contain the intrusion before the adversary can access more resources or cause more damage.</span></span> <span data-ttu-id="7a6b1-108">我们的安全事件响应过程的主要目标是限制客户或他们的数据，或 Microsoft 系统、服务和应用程序的影响。</span><span class="sxs-lookup"><span data-stu-id="7a6b1-108">The primary goal of our security incident response procedures is to limit impact to customers or their data, or to Microsoft systems, services, and applications.</span></span>

## <a name="eradication"></a><span data-ttu-id="7a6b1-109">百年</span><span class="sxs-lookup"><span data-stu-id="7a6b1-109">Eradication</span></span>

<span data-ttu-id="7a6b1-110">"安全"是一个以高可信度消除安全事件的根本原因的过程。</span><span class="sxs-lookup"><span data-stu-id="7a6b1-110">Eradication is the process of eliminating the root cause of the security incident with a high degree of confidence.</span></span> <span data-ttu-id="7a6b1-111">目标是双重的：</span><span class="sxs-lookup"><span data-stu-id="7a6b1-111">The goal is two-fold:</span></span>

- <span data-ttu-id="7a6b1-112">从环境中完全收回攻击者</span><span class="sxs-lookup"><span data-stu-id="7a6b1-112">to evict the adversary completely from the environment</span></span>
- <span data-ttu-id="7a6b1-113">缓解漏洞攻击 (如果已知) 启用或可能允许攻击者重新访问环境。</span><span class="sxs-lookup"><span data-stu-id="7a6b1-113">to mitigate the vulnerability (if known) that enabled or could enable the adversary to reenter the environment.</span></span>

<span data-ttu-id="7a6b1-114">根据事件的性质、安全事件的范围、渗透的深度和可能的威胁，Microsoft 365 安全响应团队将建议服务团队采用管理技术。</span><span class="sxs-lookup"><span data-stu-id="7a6b1-114">Depending on the nature of the incident, the scope of the security incident, the depth of the penetration and possible repercussions, the Microsoft 365 Security Response team will recommend that service teams adopt eradication techniques.</span></span> <span data-ttu-id="7a6b1-115">考虑到这些不明智的步骤可能导致的潜在业务影响，如有必要，这些决策由服务团队和 Microsoft 365 安全响应团队在获得执行事件管理器 (的详细分析和批准后) 。</span><span class="sxs-lookup"><span data-stu-id="7a6b1-115">Considering the potential business impact that may be caused by these eradication steps, these decisions will be made by service teams and the Microsoft 365 Security Response team after a detailed analysis and approval from the Executive Incident Manager (if necessary).</span></span>

## <a name="recovery"></a><span data-ttu-id="7a6b1-116">恢复</span><span class="sxs-lookup"><span data-stu-id="7a6b1-116">Recovery</span></span>

<span data-ttu-id="7a6b1-117">由于响应团队获得合理的置信度，即攻击者已从环境中退出，并且所有已知易受攻击的路径都已被消除，因此各个服务团队将启动还原步骤，以将服务引入已知且良好的配置。</span><span class="sxs-lookup"><span data-stu-id="7a6b1-117">As the response team gains a reasonable level of confidence that the adversary has been evicted from the environment and all known vulnerable paths have been eliminated, the individual service teams, will initiate restoration steps to bring the service to a known and good configuration.</span></span> <span data-ttu-id="7a6b1-118">这些还原步骤将与 Microsoft 365 安全响应团队进行咨询。</span><span class="sxs-lookup"><span data-stu-id="7a6b1-118">These restoration steps will be in consultation with the Microsoft 365 Security Response team.</span></span> <span data-ttu-id="7a6b1-119">此活动包括确定服务上次已知的良好状态、从备份还原到此状态、检查还原状态中的易受攻击路径等。Microsoft 365 安全响应团队与服务团队联系，将确定最适合环境的恢复计划。</span><span class="sxs-lookup"><span data-stu-id="7a6b1-119">This activity includes identifying the last known good state of the service, restoring from backups to this state, inspecting vulnerable attack paths in the restored state, etc. The Microsoft 365 Security Response team, in consultation with the service teams, will determine the best possible recovery plan for the environment.</span></span>

<span data-ttu-id="7a6b1-120">恢复的一个关键方面是增强的改进功能和控制，以验证恢复计划已成功执行，并且环境中不存在泄露的迹象。</span><span class="sxs-lookup"><span data-stu-id="7a6b1-120">A key aspect to the recovery is to have enhanced vigilance and controls in place to validate that the recovery plan has been successfully executed, and that no signs of breach exist in the environment.</span></span>

## <a name="customer-notification-of-security-incident"></a><span data-ttu-id="7a6b1-121">客户安全事件通知</span><span class="sxs-lookup"><span data-stu-id="7a6b1-121">Customer notification of security incident</span></span>

<span data-ttu-id="7a6b1-122">如果 Microsoft 确定发生了安全事件，我们将在我们同意的合同和合规性要求内，以过度延迟方式通知你。</span><span class="sxs-lookup"><span data-stu-id="7a6b1-122">If Microsoft determines that a security incident has occurred, we will notify you with undue delay, and within contractual and compliance requirements we have agreed to.</span></span> <span data-ttu-id="7a6b1-123">确定所有受影响的租户后，Microsoft 365 客户体验 (CxP) 通信团队将努力确定可能适用于受影响租户的任何相关法规。</span><span class="sxs-lookup"><span data-stu-id="7a6b1-123">After identifying all affected tenants, the Microsoft 365 Customer Experience (CxP) Communications team works to identify any relevant regulations that might apply to affected tenants.</span></span> <span data-ttu-id="7a6b1-124">Microsoft 365 CxP 通信团队使用适用法规中定义的相应通信通道通知相应的租户联系人。</span><span class="sxs-lookup"><span data-stu-id="7a6b1-124">The Microsoft 365 CxP Communications team uses the appropriate communication channel defined in applicable regulations to notify the appropriate tenant contact.</span></span>

<span data-ttu-id="7a6b1-125">通知将包括有关事件的详细信息，例如事件描述、客户数据的影响（如果有）以及 Microsoft 采取的操作，以及/或建议客户为解决问题并防止重复采取的操作。</span><span class="sxs-lookup"><span data-stu-id="7a6b1-125">Notification will include detailed information about the incident, such as a description of the incident, the effect on customer data, if any, actions taken by Microsoft, and/or suggested actions for customers to take to resolve the issue and prevent recurrence.</span></span> <span data-ttu-id="7a6b1-126">通知将传递到 Microsoft 365 租户 (管理员) 管理员。</span><span class="sxs-lookup"><span data-stu-id="7a6b1-126">Notification will be delivered to the designated administrator(s) of the Microsoft 365 tenant.</span></span> <span data-ttu-id="7a6b1-127">若要确保收到通知，应确保管理员在租户配置文件中提供和维护准确的联系信息。</span><span class="sxs-lookup"><span data-stu-id="7a6b1-127">To ensure notifications are received, you should ensure that your administrators provide and maintain accurate contact information in their tenant profiles.</span></span> <span data-ttu-id="7a6b1-128">此外，根据事件的性质，还可通过 Microsoft 365 服务运行状况仪表板通知客户[。](http://status.yammer.com/)</span><span class="sxs-lookup"><span data-stu-id="7a6b1-128">In addition, depending on the nature of the incident, customers can also be notified via the Microsoft 365 Service Health Dashboard[.](http://status.yammer.com/)</span></span>

## <a name="related-articles"></a><span data-ttu-id="7a6b1-129">相关文章</span><span class="sxs-lookup"><span data-stu-id="7a6b1-129">Related articles</span></span>

- [<span data-ttu-id="7a6b1-130">Microsoft 365 安全事件管理</span><span class="sxs-lookup"><span data-stu-id="7a6b1-130">Microsoft 365 security incident management</span></span>](assurance-security-incident-management.md)
- [<span data-ttu-id="7a6b1-131">Microsoft 365 安全事件管理准备</span><span class="sxs-lookup"><span data-stu-id="7a6b1-131">Microsoft 365 security incident management preparation</span></span>](assurance-sim-preparation.md)
- [<span data-ttu-id="7a6b1-132">Microsoft 365 安全事件管理检测和分析</span><span class="sxs-lookup"><span data-stu-id="7a6b1-132">Microsoft 365 security incident management detection and analysis</span></span>](assurance-sim-detection-analysis.md)
- [<span data-ttu-id="7a6b1-133">Microsoft 365 安全事件管理事后活动</span><span class="sxs-lookup"><span data-stu-id="7a6b1-133">Microsoft 365 security incident management post-incident activity</span></span>](assurance-sim-post-incident-activity.md)
