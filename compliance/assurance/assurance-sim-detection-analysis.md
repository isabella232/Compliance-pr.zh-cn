---
title: Microsoft 安全事件管理：检测和分析
description: 本文概述了 Microsoft 联机服务中的安全事件管理检测和分析过程。
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
ms.openlocfilehash: 445d812b33214a3d2287268b587607004ef96ab7
ms.sourcegitcommit: 8bf2602d56eedee4447ddb374ef95b0587f254e7
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/12/2021
ms.locfileid: "53377349"
---
# <a name="microsoft-security-incident-management-detection-and-analysis"></a><span data-ttu-id="7a0cf-103">Microsoft 安全事件管理：检测和分析</span><span class="sxs-lookup"><span data-stu-id="7a0cf-103">Microsoft security incident management: Detection and analysis</span></span>

<span data-ttu-id="7a0cf-104">为了检测恶意活动，Microsoft 的每个在线服务都集中记录安全事件和其他数据，并执行各种分析技术以查找异常或可疑活动。</span><span class="sxs-lookup"><span data-stu-id="7a0cf-104">To detect malicious activity, each of Microsoft's online services centrally logs security events and other data and perform various analytical techniques to find anomalous or suspicious activity.</span></span> <span data-ttu-id="7a0cf-105">日志文件从 Microsoft 联机服务服务器和基础结构设备中收集，并存储在中央数据库和合并数据库中。</span><span class="sxs-lookup"><span data-stu-id="7a0cf-105">Log files are collected from Microsoft online services servers and infrastructure devices and stored in central and consolidated databases.</span></span>

<span data-ttu-id="7a0cf-106">Microsoft 采用基于风险的方法来检测恶意活动。</span><span class="sxs-lookup"><span data-stu-id="7a0cf-106">Microsoft takes a risk-based approach to detecting malicious activity.</span></span> <span data-ttu-id="7a0cf-107">我们使用事件数据和威胁智能来定义检测并设置其优先级。</span><span class="sxs-lookup"><span data-stu-id="7a0cf-107">We use incident data and threat intelligence to define and prioritize our detections.</span></span>

<span data-ttu-id="7a0cf-108">在检测和分析阶段，采用一个拥有丰富经验、熟练且技能丰富的人员的团队是取得成功的最重要的支柱之一。</span><span class="sxs-lookup"><span data-stu-id="7a0cf-108">Employing a team of highly experienced, proficient, and skilled people is one of the most important pillars to success in the detection and analysis phase.</span></span> <span data-ttu-id="7a0cf-109">Microsoft 采用多个服务团队，其中包括具有堆栈中所有组件（包括网络、路由器、防火墙、负载平衡器、操作系统和应用程序）的能力的员工。</span><span class="sxs-lookup"><span data-stu-id="7a0cf-109">Microsoft employs multiple service teams that include employees with competencies on all components within the stack, including the network, routers, firewalls, load balancers, operating systems, and applications.</span></span>

<span data-ttu-id="7a0cf-110">Microsoft 联机服务中的安全检测机制还包括由不同源启动的通知和警报。</span><span class="sxs-lookup"><span data-stu-id="7a0cf-110">The security detection mechanisms in Microsoft online services also include notifications and alerts that are initiated by different sources.</span></span> <span data-ttu-id="7a0cf-111">Microsoft 联机服务安全响应团队是安全事件上报过程的重要协调者。</span><span class="sxs-lookup"><span data-stu-id="7a0cf-111">Microsoft online services security response teams are the key orchestrators of the security incident escalation process.</span></span> <span data-ttu-id="7a0cf-112">这些团队接收所有上报，并负责分析和确认安全事件的有效性。</span><span class="sxs-lookup"><span data-stu-id="7a0cf-112">These teams receive all escalations and are responsible for analyzing and confirming the validity of the security incident.</span></span>

![安全事件管理工作流](../media/assurance-sim-workflow.png)

<span data-ttu-id="7a0cf-114">检测的主要支柱之一是通知：</span><span class="sxs-lookup"><span data-stu-id="7a0cf-114">One of the primary pillars of detection is notification:</span></span>

- <span data-ttu-id="7a0cf-115">每个服务团队都负责根据联机服务安全团队的要求记录服务内的任何操作或事件。</span><span class="sxs-lookup"><span data-stu-id="7a0cf-115">Each service team is responsible to log any action or event inside the service based on the requirements from the online service security team.</span></span> <span data-ttu-id="7a0cf-116">由不同服务团队创建的所有日志都由 SIEM (安全信息和事件) 预定义的安全和检测规则进行处理。</span><span class="sxs-lookup"><span data-stu-id="7a0cf-116">All logs created by the different service teams are processed by a Security Information and Event Management (SIEM) solution with predefined security and detection rules.</span></span> <span data-ttu-id="7a0cf-117">这些规则根据安全团队的建议（根据从以前的安全事件获得的信息）进行改进，以确定是否有可疑或恶意活动。</span><span class="sxs-lookup"><span data-stu-id="7a0cf-117">These rules evolve based on security team recommendations, on information learned from previous security incidents, to determine if there is any suspicious or malicious activity.</span></span>
- <span data-ttu-id="7a0cf-118">如果客户确定正在处理安全事件，他们可能会向 Microsoft 开启支持案例，该案例将分配给 Microsoft 通信团队，并转变为向所有相应团队上报。</span><span class="sxs-lookup"><span data-stu-id="7a0cf-118">If a customer determines that a security incident is underway, they may open a support case with Microsoft, which is assigned to the Microsoft communications team and turned into an escalation to all appropriate teams.</span></span>

<span data-ttu-id="7a0cf-119">Azure、Dynamics 365 和 Microsoft 365 服务团队还使用通过安全监视和日志记录在趋势分析中获得的信息来检测 Microsoft 在线服务信息系统中可能指示攻击或安全事件的异常。</span><span class="sxs-lookup"><span data-stu-id="7a0cf-119">Azure, Dynamics 365, and Microsoft 365 service teams also use the intelligence gained in trend analysis through security monitoring and logging to detect abnormalities in Microsoft online services information systems that might indicate an attack or a security incident.</span></span> <span data-ttu-id="7a0cf-120">Microsoft 联机服务系统将生产环境中这些日志的输出聚合到集中日志记录服务器中。</span><span class="sxs-lookup"><span data-stu-id="7a0cf-120">Microsoft online services systems aggregate output from these logs in the production environment into centralized logging servers.</span></span> <span data-ttu-id="7a0cf-121">从这些集中日志记录服务器中，检查日志以发现整个生产环境的趋势。</span><span class="sxs-lookup"><span data-stu-id="7a0cf-121">From these centralized logging servers, logs are examined to spot trends throughout the production environment.</span></span> <span data-ttu-id="7a0cf-122">集中服务器中聚合的数据安全地传输到日志记录服务中，用于高级查询、仪表板生成和检测异常和恶意活动。</span><span class="sxs-lookup"><span data-stu-id="7a0cf-122">Data aggregated in the centralized servers are securely transmitted into a logging service for advanced querying, dashboard building and detecting anomalous and malicious activity.</span></span> <span data-ttu-id="7a0cf-123">该服务还使用机器学习通过日志输出检测异常。</span><span class="sxs-lookup"><span data-stu-id="7a0cf-123">The service also uses machine learning to detect anomalies with log output.</span></span>

<span data-ttu-id="7a0cf-124">在升级阶段，根据安全事件的性质，安全响应团队可能会与来自 Microsoft 各个团队的一个或多个主题专家联系：</span><span class="sxs-lookup"><span data-stu-id="7a0cf-124">During the escalation phase and depending on the nature of the security incident, security response teams may engage one or more subject matter experts from various teams at Microsoft:</span></span>

- <span data-ttu-id="7a0cf-125">联机服务安全与合规团队</span><span class="sxs-lookup"><span data-stu-id="7a0cf-125">Online Services Security and Compliance team</span></span>
- <span data-ttu-id="7a0cf-126">Microsoft 威胁智能中心 (MSTIC) </span><span class="sxs-lookup"><span data-stu-id="7a0cf-126">Microsoft Threat Intelligence Center (MSTIC)</span></span>
- <span data-ttu-id="7a0cf-127">Microsoft 安全响应中心 (MSRC) </span><span class="sxs-lookup"><span data-stu-id="7a0cf-127">Microsoft Security Response Center (MSRC)</span></span>
- <span data-ttu-id="7a0cf-128">CELA (、外部和法律) </span><span class="sxs-lookup"><span data-stu-id="7a0cf-128">Corporate, External, and Legal Affairs (CELA)</span></span>
- <span data-ttu-id="7a0cf-129">Azure 安全性</span><span class="sxs-lookup"><span data-stu-id="7a0cf-129">Azure Security</span></span>
- <span data-ttu-id="7a0cf-130">Microsoft 365工程和其他项目。</span><span class="sxs-lookup"><span data-stu-id="7a0cf-130">Microsoft 365 engineering, and others.</span></span>

<span data-ttu-id="7a0cf-131">在向任何安全响应团队上报之前，服务团队负责根据定义的条件确定和设置安全事件的严重性级别，例如：</span><span class="sxs-lookup"><span data-stu-id="7a0cf-131">Before an escalation to any security response team occurs, the service team is responsible for determining and setting the severity level of the security incident based on defined criteria such as:</span></span>

- <span data-ttu-id="7a0cf-132">隐私</span><span class="sxs-lookup"><span data-stu-id="7a0cf-132">Privacy</span></span>
- <span data-ttu-id="7a0cf-133">影响</span><span class="sxs-lookup"><span data-stu-id="7a0cf-133">Impact</span></span>
- <span data-ttu-id="7a0cf-134">范围</span><span class="sxs-lookup"><span data-stu-id="7a0cf-134">Scope</span></span>
- <span data-ttu-id="7a0cf-135">受影响的租户数</span><span class="sxs-lookup"><span data-stu-id="7a0cf-135">Number of affected tenants</span></span>
- <span data-ttu-id="7a0cf-136">区域</span><span class="sxs-lookup"><span data-stu-id="7a0cf-136">Region</span></span>
- <span data-ttu-id="7a0cf-137">服务</span><span class="sxs-lookup"><span data-stu-id="7a0cf-137">Service</span></span>
- <span data-ttu-id="7a0cf-138">事件的详细信息</span><span class="sxs-lookup"><span data-stu-id="7a0cf-138">Details of the incident</span></span>
- <span data-ttu-id="7a0cf-139">特定客户行业或市场法规。</span><span class="sxs-lookup"><span data-stu-id="7a0cf-139">Specific customer industry or market regulations.</span></span>

<span data-ttu-id="7a0cf-140">事件优先顺序是使用不同因素确定的，包括但不限于事件的功能影响、事件的信息影响以及事件的可恢复性。</span><span class="sxs-lookup"><span data-stu-id="7a0cf-140">Incident prioritization is determined by using distinct factors, including but not limited to the functional impact of the incident, the informational impact of the incident, and the recoverability from the incident.</span></span>

<span data-ttu-id="7a0cf-141">收到有关安全事件的上报后，安全团队将组织一个虚拟团队 (v-team) ，该虚拟团队由来自 Microsoft 联机服务安全响应团队、服务团队和事件通信团队的成员组成。</span><span class="sxs-lookup"><span data-stu-id="7a0cf-141">After receiving an escalation about a security incident, the security team organizes a virtual team (v-team) comprised of members from the Microsoft online service security response team, service teams, and the incident communication team.</span></span> <span data-ttu-id="7a0cf-142">然后，v 团队必须确认安全事件是否安全，并消除任何误报。</span><span class="sxs-lookup"><span data-stu-id="7a0cf-142">The v-team must then confirm the legitimacy of the security incident and eliminate any false positives.</span></span> <span data-ttu-id="7a0cf-143">由准备阶段确定的指示器提供的信息的准确性至关重要。</span><span class="sxs-lookup"><span data-stu-id="7a0cf-143">The accuracy of information provided by the indicators determined during the preparation phase is critical.</span></span> <span data-ttu-id="7a0cf-144">通过按矢量攻击类别分析此信息，v 团队可以确定安全事件是否合理。</span><span class="sxs-lookup"><span data-stu-id="7a0cf-144">By analyzing this information by category of vector attack, the v-team can determine if the security incident is a legitimate concern.</span></span>

<span data-ttu-id="7a0cf-145">在调查开始时，安全事件响应团队根据我们的案例管理策略记录有关事件的所有信息。</span><span class="sxs-lookup"><span data-stu-id="7a0cf-145">At the beginning of the investigation, the security incident response team records all information about the incident according to our case management policies.</span></span> <span data-ttu-id="7a0cf-146">随着案例的进展，我们将跟踪正在进行的操作，并遵循证据处理标准，以在事件生命周期内收集、保留和保护此数据。</span><span class="sxs-lookup"><span data-stu-id="7a0cf-146">As the case progresses, we track ongoing actions and follow evidence handling standards for gathering, retaining, and securing this data throughout the incident lifecycle.</span></span>

<span data-ttu-id="7a0cf-147">这些操作的示例包括：</span><span class="sxs-lookup"><span data-stu-id="7a0cf-147">Some examples of these actions would include:</span></span>

- <span data-ttu-id="7a0cf-148">摘要，简要说明事件及其潜在影响</span><span class="sxs-lookup"><span data-stu-id="7a0cf-148">A summary, which is a brief description of the incident and its potential impact</span></span>
- <span data-ttu-id="7a0cf-149">事件的严重性和优先级，通过评估潜在影响得出</span><span class="sxs-lookup"><span data-stu-id="7a0cf-149">The incident's severity and priority, which are derived by assessing the potential impact</span></span>
- <span data-ttu-id="7a0cf-150">标识的所有指示符列表，这些指标导致检测事件</span><span class="sxs-lookup"><span data-stu-id="7a0cf-150">A list of all indicators identified which led to detection of the incident</span></span>
- <span data-ttu-id="7a0cf-151">任何相关事件的列表</span><span class="sxs-lookup"><span data-stu-id="7a0cf-151">A list of any related incidents</span></span>
- <span data-ttu-id="7a0cf-152">v-team 执行的所有操作的列表</span><span class="sxs-lookup"><span data-stu-id="7a0cf-152">A list of all actions taken by the v-team</span></span>
- <span data-ttu-id="7a0cf-153">收集的任何证据，也将保留用于事后分析和未来取证调查</span><span class="sxs-lookup"><span data-stu-id="7a0cf-153">Any gathered evidence, which will also be preserved for post-mortem analysis and future forensic investigations</span></span>
- <span data-ttu-id="7a0cf-154">推荐的下一步步骤和操作</span><span class="sxs-lookup"><span data-stu-id="7a0cf-154">Recommended next steps and actions</span></span>

<span data-ttu-id="7a0cf-155">在安全事件确认后，安全响应团队和相应服务团队的主要目标是控制攻击、保护服务 () 攻击，并避免更大的全球影响。</span><span class="sxs-lookup"><span data-stu-id="7a0cf-155">After security incident confirmation, the primary goals of the security response team and the appropriate service team are to contain the attack, to protect the service(s) under attack, and to avoid a greater global impact.</span></span> <span data-ttu-id="7a0cf-156">同时，相应的工程团队努力确定根本原因并准备第一个恢复计划。</span><span class="sxs-lookup"><span data-stu-id="7a0cf-156">At the same time, the appropriate engineering teams work to determine the root cause and to prepare the first recovery plan.</span></span>

<span data-ttu-id="7a0cf-157">下一阶段，安全响应团队 (受) 影响的客户（如果有）。</span><span class="sxs-lookup"><span data-stu-id="7a0cf-157">In the next phase, the security response team identifies the customer(s) affected by the security incident, if any.</span></span> <span data-ttu-id="7a0cf-158">影响范围可能需要一些时间才能根据区域、数据中心、服务、服务器场、服务器等确定。</span><span class="sxs-lookup"><span data-stu-id="7a0cf-158">The scope of effect can take some time to determine, based on region, datacenter, service, server farm, server, and so forth.</span></span> <span data-ttu-id="7a0cf-159">受影响客户的列表由服务团队和相应的 Microsoft 通信团队编译，然后这些团队在合同和合规义务内处理客户通知流程。</span><span class="sxs-lookup"><span data-stu-id="7a0cf-159">The list of affected customers is compiled by the service team and the corresponding Microsoft communications team, who then handle the customer notification process within contractual and compliance obligations.</span></span>

## <a name="related-articles"></a><span data-ttu-id="7a0cf-160">相关文章</span><span class="sxs-lookup"><span data-stu-id="7a0cf-160">Related articles</span></span>

- [<span data-ttu-id="7a0cf-161">Microsoft 安全事件管理</span><span class="sxs-lookup"><span data-stu-id="7a0cf-161">Microsoft security incident management</span></span>](assurance-security-incident-management.md)
- [<span data-ttu-id="7a0cf-162">Microsoft 安全事件管理：准备</span><span class="sxs-lookup"><span data-stu-id="7a0cf-162">Microsoft security incident management: Preparation</span></span>](assurance-sim-preparation.md)
- [<span data-ttu-id="7a0cf-163">Microsoft 安全事件管理：包含、隔离和恢复</span><span class="sxs-lookup"><span data-stu-id="7a0cf-163">Microsoft security incident management: Containment, eradication, and recovery</span></span>](assurance-sim-containment-eradication-recovery.md)
- [<span data-ttu-id="7a0cf-164">Microsoft 安全事件管理：事后活动</span><span class="sxs-lookup"><span data-stu-id="7a0cf-164">Microsoft security incident management: Post-incident activity</span></span>](assurance-sim-post-incident-activity.md)
- [<span data-ttu-id="7a0cf-165">如何记录安全事件支持票证</span><span class="sxs-lookup"><span data-stu-id="7a0cf-165">How to Log a Security Event Support Ticket</span></span>](/azure/security/fundamentals/event-support-ticket)
- [<span data-ttu-id="7a0cf-166">GDPR 规定的 Azure 和 Dynamics 365 泄露通知</span><span class="sxs-lookup"><span data-stu-id="7a0cf-166">Azure and Dynamics 365 breach notification under the GDPR</span></span>](/compliance/regulatory/gdpr-breach-azure-dynamics)
