---
title: Microsoft 365安全事件管理：检测和分析
description: 本文概述了安全事件管理检测和分析过程中的安全Microsoft 365。
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
ms.openlocfilehash: 3eb42b340ed6a137d0bec7b58d015009a1b20621
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/23/2021
ms.locfileid: "53087572"
---
# <a name="microsoft-365-security-incident-management-detection-and-analysis"></a><span data-ttu-id="cd833-103">Microsoft 365安全事件管理：检测和分析</span><span class="sxs-lookup"><span data-stu-id="cd833-103">Microsoft 365 security incident management: Detection and analysis</span></span>

<span data-ttu-id="cd833-104">若要检测恶意活动，Microsoft 365集中记录安全事件和其他数据，并执行各种分析技术以查找异常或可疑活动。</span><span class="sxs-lookup"><span data-stu-id="cd833-104">To detect malicious activity, Microsoft 365 centrally logs security events and other data and performs various analytical techniques to find anomalous or suspicious activity.</span></span> <span data-ttu-id="cd833-105">日志文件收集在Microsoft 365和基础结构设备中，并存储在中央和合并数据库中。</span><span class="sxs-lookup"><span data-stu-id="cd833-105">Log files are collected from Microsoft 365 servers and infrastructure devices and stored in a central and consolidated database.</span></span>

<span data-ttu-id="cd833-106">Microsoft 采用基于风险的方法来检测恶意活动。</span><span class="sxs-lookup"><span data-stu-id="cd833-106">Microsoft takes a risk-based approach to detecting malicious activity.</span></span> <span data-ttu-id="cd833-107">我们使用事件数据和威胁智能来定义检测并设置其优先级。</span><span class="sxs-lookup"><span data-stu-id="cd833-107">We use incident data and threat intelligence to define and prioritize our detections.</span></span>

<span data-ttu-id="cd833-108">在检测和分析阶段，采用一个拥有丰富经验、熟练且技能丰富的人员的团队是取得成功的最重要的支柱之一。</span><span class="sxs-lookup"><span data-stu-id="cd833-108">Employing a team of highly experienced, proficient, and skilled people is one of the most important pillars to success in the detection and analysis phase.</span></span> <span data-ttu-id="cd833-109">Microsoft 365多个服务团队，这些团队包括具有堆栈中所有组件（包括网络、路由器、防火墙、负载平衡器、操作系统和应用程序）的能力的员工。</span><span class="sxs-lookup"><span data-stu-id="cd833-109">Microsoft 365 employs multiple service teams, and those teams include employees with competencies on all components within the stack, including the network, routers, firewalls, load balancers, operating systems, and applications.</span></span>

<span data-ttu-id="cd833-110">安全检测机制Microsoft 365由不同源启动的通知和警报。</span><span class="sxs-lookup"><span data-stu-id="cd833-110">The security detection mechanisms in Microsoft 365 also include notification and alerts that are initiated by different sources.</span></span> <span data-ttu-id="cd833-111">安全Microsoft 365团队是安全事件上报过程的重要协调者。</span><span class="sxs-lookup"><span data-stu-id="cd833-111">The Microsoft 365 Security Response team is the key orchestrator of the security incident escalation process.</span></span> <span data-ttu-id="cd833-112">此团队接收所有上报，并负责分析和确认安全事件的有效性。</span><span class="sxs-lookup"><span data-stu-id="cd833-112">This team receives all escalations and is responsible for analyzing and confirming the validity of the security incident.</span></span>

![安全事件管理工作流](../media/assurance-sim-workflow.png)

<span data-ttu-id="cd833-114">检测的主要支柱之一是通知：</span><span class="sxs-lookup"><span data-stu-id="cd833-114">One of the primary pillars of detection is notification:</span></span>

- <span data-ttu-id="cd833-115">每个服务团队都负责根据安全团队的要求记录服务Microsoft 365事件。</span><span class="sxs-lookup"><span data-stu-id="cd833-115">Each service team is responsible to log any action or event inside the service based on the requirements from the Microsoft 365 Security team.</span></span> <span data-ttu-id="cd833-116">由不同服务团队创建的所有日志都由 SIEM (安全信息和事件) 预定义的安全和检测规则进行处理。</span><span class="sxs-lookup"><span data-stu-id="cd833-116">All logs created by the different service teams are processed by a Security Information and Event Management (SIEM) solution with predefined security and detection rules.</span></span> <span data-ttu-id="cd833-117">这些规则根据安全Microsoft 365的建议，根据从以前的安全事件获得的信息来改进，以确定是否有可疑或恶意活动。</span><span class="sxs-lookup"><span data-stu-id="cd833-117">These rules evolve based on the Microsoft 365 Security team's recommendation, on information learned from previous security incidents, to determine if there is any suspicious or malicious activity.</span></span>
- <span data-ttu-id="cd833-118">如果客户确定正在处理安全事件，他们可能会向 Microsoft 开启支持案例，该案例分配给 Microsoft 365 客户体验 (CxP) 通信团队，并转变为向所有相应团队上报。</span><span class="sxs-lookup"><span data-stu-id="cd833-118">If a customer determines that a security incident is underway, they may open a support case with Microsoft, which is assigned to the Microsoft 365 Customer Experience (CxP) Communications team and turned into an escalation to all appropriate teams.</span></span>

<span data-ttu-id="cd833-119">Microsoft 365服务团队还使用通过安全监视和日志记录在趋势分析中获得的信息来检测 Microsoft 365 信息系统中可能指示攻击或安全事件的异常。</span><span class="sxs-lookup"><span data-stu-id="cd833-119">Microsoft 365 service teams also use the intelligence gained in trend analysis through security monitoring and logging to detect abnormalities in Microsoft 365 information systems that might indicate an attack or a security incident.</span></span> <span data-ttu-id="cd833-120">Microsoft 365将生产环境中这些日志的输出聚合到集中日志记录服务器中。</span><span class="sxs-lookup"><span data-stu-id="cd833-120">Microsoft 365 servers aggregate output from these logs in the production environment into a centralized logging server.</span></span> <span data-ttu-id="cd833-121">通过此集中日志记录服务器，检查日志以发现整个生产环境的趋势。</span><span class="sxs-lookup"><span data-stu-id="cd833-121">From this centralized logging server, logs are examined to spot trends throughout the production environment.</span></span> <span data-ttu-id="cd833-122">集中服务器中聚合的数据安全地传输到日志记录服务中，用于高级查询、仪表板生成和检测异常和恶意活动。</span><span class="sxs-lookup"><span data-stu-id="cd833-122">Data aggregated in the centralized server is securely transmitted into a logging service for advanced querying, dashboard building and detecting anomalous and malicious activity.</span></span> <span data-ttu-id="cd833-123">该服务还使用机器学习通过日志输出检测异常。</span><span class="sxs-lookup"><span data-stu-id="cd833-123">The service also uses machine learning to detect anomalies with log output.</span></span>

<span data-ttu-id="cd833-124">在升级阶段，根据安全事件的性质，Microsoft 365安全响应团队可能会与来自 Microsoft 各个团队的一个或多个行业专家联系：</span><span class="sxs-lookup"><span data-stu-id="cd833-124">During the escalation phase and depending on the nature of the security incident, the Microsoft 365 Security Response team may engage one or more subject matter experts from various teams at Microsoft:</span></span>

- <span data-ttu-id="cd833-125">联机服务安全与合规团队</span><span class="sxs-lookup"><span data-stu-id="cd833-125">Online Services Security and Compliance team</span></span>
- <span data-ttu-id="cd833-126">Microsoft 威胁智能中心 (MSTIC) </span><span class="sxs-lookup"><span data-stu-id="cd833-126">Microsoft Threat Intelligence Center (MSTIC)</span></span>
- <span data-ttu-id="cd833-127">Microsoft 安全响应中心 (MSRC) </span><span class="sxs-lookup"><span data-stu-id="cd833-127">Microsoft Security Response Center (MSRC)</span></span>
- <span data-ttu-id="cd833-128">CELA (、外部和法律) </span><span class="sxs-lookup"><span data-stu-id="cd833-128">Corporate, External, and Legal Affairs (CELA)</span></span>
- <span data-ttu-id="cd833-129">Azure 安全性</span><span class="sxs-lookup"><span data-stu-id="cd833-129">Azure Security</span></span>
- <span data-ttu-id="cd833-130">Microsoft 365工程和其他项目。</span><span class="sxs-lookup"><span data-stu-id="cd833-130">Microsoft 365 engineering, and others.</span></span>

<span data-ttu-id="cd833-131">在向安全Microsoft 365团队上报之前，服务团队负责根据定义的条件确定和设置安全事件的严重性级别，例如：</span><span class="sxs-lookup"><span data-stu-id="cd833-131">Before any escalation to the Microsoft 365 Security Response team occurs, the service team is responsible for determining and setting the severity level of the security incident based on defined criteria such as:</span></span>

- <span data-ttu-id="cd833-132">隐私</span><span class="sxs-lookup"><span data-stu-id="cd833-132">Privacy</span></span>
- <span data-ttu-id="cd833-133">影响</span><span class="sxs-lookup"><span data-stu-id="cd833-133">Impact</span></span>
- <span data-ttu-id="cd833-134">范围</span><span class="sxs-lookup"><span data-stu-id="cd833-134">Scope</span></span>
- <span data-ttu-id="cd833-135">受影响的租户数</span><span class="sxs-lookup"><span data-stu-id="cd833-135">Number of affected tenants</span></span>
- <span data-ttu-id="cd833-136">区域</span><span class="sxs-lookup"><span data-stu-id="cd833-136">Region</span></span>
- <span data-ttu-id="cd833-137">服务</span><span class="sxs-lookup"><span data-stu-id="cd833-137">Service</span></span>
- <span data-ttu-id="cd833-138">事件的详细信息</span><span class="sxs-lookup"><span data-stu-id="cd833-138">Details of the incident</span></span>
- <span data-ttu-id="cd833-139">特定客户行业或市场法规。</span><span class="sxs-lookup"><span data-stu-id="cd833-139">Specific customer industry or market regulations.</span></span>

<span data-ttu-id="cd833-140">事件优先顺序是使用不同因素确定的，包括但不限于事件的功能影响、事件的信息影响以及事件的可恢复性。</span><span class="sxs-lookup"><span data-stu-id="cd833-140">Incident prioritization is determined by using distinct factors, including but not limited to the functional impact of the incident, the informational impact of the incident, and the recoverability from the incident.</span></span>

<span data-ttu-id="cd833-141">收到有关安全事件的上报后，Microsoft 365 安全团队将组织一个虚拟团队 (v-team) ，该虚拟团队由 Microsoft 365 安全响应团队、服务团队和 Microsoft 365 事件通信团队的成员组成。</span><span class="sxs-lookup"><span data-stu-id="cd833-141">After receiving an escalation about a security incident, the Microsoft 365 Security team organizes a virtual team (v-team) comprised of members from Microsoft 365 Security Response team, service teams, and the Microsoft 365 Incident Communication team.</span></span> <span data-ttu-id="cd833-142">此 v 团队活动的更复杂的部分是确认安全事件并消除任何误报。</span><span class="sxs-lookup"><span data-stu-id="cd833-142">The more complex part of activities of this v-team is to confirm the security incident and to eliminate any false positives.</span></span> <span data-ttu-id="cd833-143">由准备阶段确定的指示器提供的信息的准确性至关重要。</span><span class="sxs-lookup"><span data-stu-id="cd833-143">The accuracy of information provided by the indicators determined in the preparation phase is critical.</span></span> <span data-ttu-id="cd833-144">通过按矢量攻击类别分析此信息，v 团队可以确定安全事件是否合理。</span><span class="sxs-lookup"><span data-stu-id="cd833-144">By analyzing this information by category of vector attack, the v-team can determine if the security incident is a legitimate concern.</span></span>

<span data-ttu-id="cd833-145">在调查开始时，Office事件响应团队根据我们的案例管理策略记录有关事件的所有信息。</span><span class="sxs-lookup"><span data-stu-id="cd833-145">At the beginning of the investigation, the Office Security Incident Response team records all information about the incident according to our case management policies.</span></span> <span data-ttu-id="cd833-146">随着案例的进展，我们将跟踪正在进行的操作，并遵循证据处理标准，以在事件生命周期内收集、保留和保护此数据。</span><span class="sxs-lookup"><span data-stu-id="cd833-146">As the case progresses, we track ongoing actions and follow evidence handling standards for gathering, retaining, and securing this data throughout the incident lifecycle.</span></span>

<span data-ttu-id="cd833-147">这些操作的示例包括：</span><span class="sxs-lookup"><span data-stu-id="cd833-147">Some examples of these actions would include:</span></span>

- <span data-ttu-id="cd833-148">摘要，简要说明事件及其潜在影响</span><span class="sxs-lookup"><span data-stu-id="cd833-148">A summary, which is a brief description of the incident and its potential impact</span></span>
- <span data-ttu-id="cd833-149">事件的严重性和优先级，通过评估潜在影响得出</span><span class="sxs-lookup"><span data-stu-id="cd833-149">The incident's severity and priority, which are derived by assessing the potential impact</span></span>
- <span data-ttu-id="cd833-150">标识的所有指示符列表，这些指标导致检测事件</span><span class="sxs-lookup"><span data-stu-id="cd833-150">A list of all indicators identified which led to detection of the incident</span></span>
- <span data-ttu-id="cd833-151">任何相关事件的列表</span><span class="sxs-lookup"><span data-stu-id="cd833-151">A list of any related incidents</span></span>
- <span data-ttu-id="cd833-152">v-team 执行的所有操作的列表</span><span class="sxs-lookup"><span data-stu-id="cd833-152">A list of all actions taken by the v-team</span></span>
- <span data-ttu-id="cd833-153">收集的任何证据，也将保留用于事后分析和未来取证调查</span><span class="sxs-lookup"><span data-stu-id="cd833-153">Any gathered evidence, which will also be preserved for post-mortem analysis and future forensic investigations</span></span>
- <span data-ttu-id="cd833-154">推荐的下一步步骤和操作</span><span class="sxs-lookup"><span data-stu-id="cd833-154">Recommended next steps and actions</span></span>

<span data-ttu-id="cd833-155">在安全事件确认后，Microsoft 365 安全响应团队和相应服务团队的主要目标是控制攻击、保护服务 () 受到攻击，并避免更大的全球影响。</span><span class="sxs-lookup"><span data-stu-id="cd833-155">After security incident confirmation, the primary goals of the Microsoft 365 Security Response team and the appropriate service team are to contain the attack, to protect the service(s) under attack, and to avoid a greater global impact.</span></span> <span data-ttu-id="cd833-156">同时，相应的工程团队努力确定根本原因并准备第一个恢复计划。</span><span class="sxs-lookup"><span data-stu-id="cd833-156">At the same time, the appropriate engineering teams work to determine the root cause and to prepare the first recovery plan.</span></span>

<span data-ttu-id="cd833-157">下一阶段，Microsoft 365安全响应团队 (受) 影响的客户（如果有）。</span><span class="sxs-lookup"><span data-stu-id="cd833-157">In the next phase, the Microsoft 365 Security Response team identifies the customer(s) affected by the security incident, if any.</span></span> <span data-ttu-id="cd833-158">影响范围可能需要一些时间才能根据区域、数据中心、服务、服务器场、服务器等确定。</span><span class="sxs-lookup"><span data-stu-id="cd833-158">The scope of effect can take some time to determine, based on region, datacenter, service, server farm, server, and so forth.</span></span> <span data-ttu-id="cd833-159">受影响的客户列表由服务团队和 Microsoft 365 CxP 通信团队编译，然后这些团队在合同和合规性义务内处理客户通知流程。</span><span class="sxs-lookup"><span data-stu-id="cd833-159">The list of affected customers is compiled by the service team and the Microsoft 365 CxP Communications team, who then handle the customer notification process within contractual and compliance obligations.</span></span>

## <a name="related-articles"></a><span data-ttu-id="cd833-160">相关文章</span><span class="sxs-lookup"><span data-stu-id="cd833-160">Related articles</span></span>

- [<span data-ttu-id="cd833-161">Microsoft 365 安全事件管理</span><span class="sxs-lookup"><span data-stu-id="cd833-161">Microsoft 365 security incident management</span></span>](assurance-security-incident-management.md)
- [<span data-ttu-id="cd833-162">Microsoft 365安全事件管理准备</span><span class="sxs-lookup"><span data-stu-id="cd833-162">Microsoft 365 security incident management preparation</span></span>](assurance-sim-preparation.md)
- [<span data-ttu-id="cd833-163">Microsoft 365 安全事件管理抑制、消除和恢复</span><span class="sxs-lookup"><span data-stu-id="cd833-163">Microsoft 365 security incident management containment, eradication, and recovery</span></span>](assurance-sim-containment-eradication-recovery.md)
- [<span data-ttu-id="cd833-164">Microsoft 365 安全事件管理事后活动</span><span class="sxs-lookup"><span data-stu-id="cd833-164">Microsoft 365 security incident management post-incident activity</span></span>](assurance-sim-post-incident-activity.md)
