---
title: Microsoft 365 安全事件管理：检测和分析
description: 本文概述了 Microsoft 365 中的安全事件管理检测和分析过程。
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
ms.openlocfilehash: 1fbdca0c0b08c793732ba31414bedd943d4dc115
ms.sourcegitcommit: d67e4d4fdc664f1da450c8ef2f6732e19bdd403a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/28/2021
ms.locfileid: "50037577"
---
# <a name="microsoft-365-security-incident-management-detection-and-analysis"></a><span data-ttu-id="74526-103">Microsoft 365 安全事件管理：检测和分析</span><span class="sxs-lookup"><span data-stu-id="74526-103">Microsoft 365 security incident management: Detection and analysis</span></span>

<span data-ttu-id="74526-104">为了检测恶意活动，Microsoft 365 集中记录安全事件和其他数据，并执行各种分析技术以查找异常或可疑活动。</span><span class="sxs-lookup"><span data-stu-id="74526-104">To detect malicious activity, Microsoft 365 centrally logs security events and other data and performs various analytical techniques to find anomalous or suspicious activity.</span></span> <span data-ttu-id="74526-105">日志文件从 Microsoft 365 服务器和基础结构设备收集，并存储在中央合并数据库中。</span><span class="sxs-lookup"><span data-stu-id="74526-105">Log files are collected from Microsoft 365 servers and infrastructure devices and stored in a central and consolidated database.</span></span>

<span data-ttu-id="74526-106">Microsoft 采用基于风险的方法检测恶意活动。</span><span class="sxs-lookup"><span data-stu-id="74526-106">Microsoft takes a risk-based approach to detecting malicious activity.</span></span> <span data-ttu-id="74526-107">我们使用事件数据和威胁智能来定义检测并设置其优先级。</span><span class="sxs-lookup"><span data-stu-id="74526-107">We use incident data and threat intelligence to define and prioritize our detections.</span></span>

<span data-ttu-id="74526-108">在检测和分析阶段，使用一个拥有丰富经验、熟练且技能丰富的人员的团队是成功的关键支柱之一。</span><span class="sxs-lookup"><span data-stu-id="74526-108">Employing a team of highly experienced, proficient, and skilled people is one of the most important pillars to success in the detection and analysis phase.</span></span> <span data-ttu-id="74526-109">Microsoft 365 采用多个服务团队，这些团队包括具有堆栈中所有组件（包括网络、路由器、防火墙、负载平衡器、操作系统和应用程序）的能力的员工。</span><span class="sxs-lookup"><span data-stu-id="74526-109">Microsoft 365 employs multiple service teams, and those teams include employees with competencies on all components within the stack, including the network, routers, firewalls, load balancers, operating systems, and applications.</span></span>

<span data-ttu-id="74526-110">Microsoft 365 中的安全检测机制还包括由不同来源启动的通知和警报。</span><span class="sxs-lookup"><span data-stu-id="74526-110">The security detection mechanisms in Microsoft 365 also include notification and alerts that are initiated by different sources.</span></span> <span data-ttu-id="74526-111">Microsoft 365 安全响应团队是安全事件升级过程的重要协调者。</span><span class="sxs-lookup"><span data-stu-id="74526-111">The Microsoft 365 Security Response team is the key orchestrator of the security incident escalation process.</span></span> <span data-ttu-id="74526-112">此团队接收所有上报，并负责分析和确认安全事件的有效性。</span><span class="sxs-lookup"><span data-stu-id="74526-112">This team receives all escalations and is responsible for analyzing and confirming the validity of the security incident.</span></span>

<span data-ttu-id="74526-113">检测的主要支柱之一是通知：</span><span class="sxs-lookup"><span data-stu-id="74526-113">One of the primary pillars of detection is notification:</span></span>

- <span data-ttu-id="74526-114">每个服务团队都负责根据 Microsoft 365 安全团队的要求记录服务内的任何操作或事件。</span><span class="sxs-lookup"><span data-stu-id="74526-114">Each service team is responsible to log any action or event inside the service based on the requirements from the Microsoft 365 Security team.</span></span> <span data-ttu-id="74526-115">由不同服务团队创建的所有日志都由 SIEM (安全) 和检测规则处理。</span><span class="sxs-lookup"><span data-stu-id="74526-115">All logs created by the different service teams are processed by a Security Information and Event Management (SIEM) solution with predefined security and detection rules.</span></span> <span data-ttu-id="74526-116">这些规则根据 Microsoft 365 安全团队的建议，根据从以前的安全事件中获得的信息进行改进，以确定是否有可疑或恶意活动。</span><span class="sxs-lookup"><span data-stu-id="74526-116">These rules evolve based on the Microsoft 365 Security team’s recommendation, on information learned from previous security incidents, to determine if there is any suspicious or malicious activity.</span></span>
- <span data-ttu-id="74526-117">如果客户确定正在处理安全事件，他们可能会向 Microsoft 开启支持案例，该案例分配给 Microsoft 365 客户体验 (CxP) 通信团队，并转变为向所有相应团队上报。</span><span class="sxs-lookup"><span data-stu-id="74526-117">If a customer determines that a security incident is underway, they may open a support case with Microsoft, which is assigned to the Microsoft 365 Customer Experience (CxP) Communications team and turned into an escalation to all appropriate teams.</span></span>

<span data-ttu-id="74526-118">Microsoft 365 服务团队还使用通过安全监视和日志记录在趋势分析中获得的信息来检测 Microsoft 365 信息系统中可能指示攻击或安全事件的异常。</span><span class="sxs-lookup"><span data-stu-id="74526-118">Microsoft 365 service teams also use the intelligence gained in trend analysis through security monitoring and logging to detect abnormalities in Microsoft 365 information systems that might indicate an attack or a security incident.</span></span> <span data-ttu-id="74526-119">Microsoft 365 服务器将生产环境中这些日志的输出聚合到集中日志记录服务器中。</span><span class="sxs-lookup"><span data-stu-id="74526-119">Microsoft 365 servers aggregate output from these logs in the production environment into a centralized logging server.</span></span> <span data-ttu-id="74526-120">通过此集中日志记录服务器，检查日志以发现整个生产环境的趋势。</span><span class="sxs-lookup"><span data-stu-id="74526-120">From this centralized logging server, logs are examined to spot trends throughout the production environment.</span></span> <span data-ttu-id="74526-121">集中服务器中聚合的数据安全地传输到日志记录服务中，以用于高级查询、仪表板生成和检测异常和恶意活动。</span><span class="sxs-lookup"><span data-stu-id="74526-121">Data aggregated in the centralized server is securely transmitted into a logging service for advanced querying, dashboard building and detecting anomalous and malicious activity.</span></span> <span data-ttu-id="74526-122">该服务还使用机器学习来检测日志输出的异常。</span><span class="sxs-lookup"><span data-stu-id="74526-122">The service also uses machine learning to detect anomalies with log output.</span></span>

<span data-ttu-id="74526-123">在升级阶段，根据安全事件的性质，Microsoft 365 安全响应团队可能会与来自 Microsoft 各团队的一个或多个主题专家联系：</span><span class="sxs-lookup"><span data-stu-id="74526-123">During the escalation phase and depending on the nature of the security incident, the Microsoft 365 Security Response team may engage one or more subject matter experts from various teams at Microsoft:</span></span>

- <span data-ttu-id="74526-124">联机服务安全与合规团队</span><span class="sxs-lookup"><span data-stu-id="74526-124">Online Services Security and Compliance team</span></span>
- <span data-ttu-id="74526-125">Microsoft 威胁智能中心 (MSTIC) </span><span class="sxs-lookup"><span data-stu-id="74526-125">Microsoft Threat Intelligence Center (MSTIC)</span></span>
- <span data-ttu-id="74526-126">Microsoft 安全响应中心 (MSRC) </span><span class="sxs-lookup"><span data-stu-id="74526-126">Microsoft Security Response Center (MSRC)</span></span>
- <span data-ttu-id="74526-127">CELA (、外部和法律) </span><span class="sxs-lookup"><span data-stu-id="74526-127">Corporate, External, and Legal Affairs (CELA)</span></span>
- <span data-ttu-id="74526-128">Azure 安全性</span><span class="sxs-lookup"><span data-stu-id="74526-128">Azure Security</span></span>
- <span data-ttu-id="74526-129">Microsoft 365 工程和其他项目。</span><span class="sxs-lookup"><span data-stu-id="74526-129">Microsoft 365 engineering, and others.</span></span>

<span data-ttu-id="74526-130">在向 Microsoft 365 安全响应团队进行任何上报之前，服务团队负责根据定义的条件确定和设置安全事件的严重性级别，例如：</span><span class="sxs-lookup"><span data-stu-id="74526-130">Before any escalation to the Microsoft 365 Security Response team occurs, the service team is responsible for determining and setting the severity level of the security incident based on defined criteria such as:</span></span>

- <span data-ttu-id="74526-131">隐私</span><span class="sxs-lookup"><span data-stu-id="74526-131">Privacy</span></span>
- <span data-ttu-id="74526-132">影响</span><span class="sxs-lookup"><span data-stu-id="74526-132">Impact</span></span>
- <span data-ttu-id="74526-133">范围</span><span class="sxs-lookup"><span data-stu-id="74526-133">Scope</span></span>
- <span data-ttu-id="74526-134">受影响的租户数</span><span class="sxs-lookup"><span data-stu-id="74526-134">Number of affected tenants</span></span>
- <span data-ttu-id="74526-135">地区</span><span class="sxs-lookup"><span data-stu-id="74526-135">Region</span></span>
- <span data-ttu-id="74526-136">服务</span><span class="sxs-lookup"><span data-stu-id="74526-136">Service</span></span>
- <span data-ttu-id="74526-137">事件的详细信息</span><span class="sxs-lookup"><span data-stu-id="74526-137">Details of the incident</span></span>
- <span data-ttu-id="74526-138">特定客户行业或市场法规。</span><span class="sxs-lookup"><span data-stu-id="74526-138">Specific customer industry or market regulations.</span></span>

<span data-ttu-id="74526-139">事件优先顺序是使用不同因素确定的，包括但不限于事件的功能影响、事件的信息影响以及事件的可恢复性。</span><span class="sxs-lookup"><span data-stu-id="74526-139">Incident prioritization is determined by using distinct factors, including but not limited to the functional impact of the incident, the informational impact of the incident, and the recoverability from the incident.</span></span>

<span data-ttu-id="74526-140">在收到有关安全事件的上报后，Microsoft 365 安全团队将组织一个由 Microsoft 365 安全响应团队、服务团队和 Microsoft 365 事件通信团队的成员组成的虚拟团队 (v-team) 。</span><span class="sxs-lookup"><span data-stu-id="74526-140">After receiving an escalation about a security incident, the Microsoft 365 Security team organizes a virtual team (v-team) comprised of members from Microsoft 365 Security Response team, service teams, and the Microsoft 365 Incident Communication team.</span></span> <span data-ttu-id="74526-141">此 v 团队的活动更复杂的部分是确认安全事件并消除任何误报。</span><span class="sxs-lookup"><span data-stu-id="74526-141">The more complex part of activities of this v-team is to confirm the security incident and to eliminate any false positives.</span></span> <span data-ttu-id="74526-142">由准备阶段确定的指标提供的信息的准确性至关重要。</span><span class="sxs-lookup"><span data-stu-id="74526-142">The accuracy of information provided by the indicators determined in the preparation phase is critical.</span></span> <span data-ttu-id="74526-143">通过按矢量攻击类别分析此信息，v 团队可以确定安全事件是否合法。</span><span class="sxs-lookup"><span data-stu-id="74526-143">By analyzing this information by category of vector attack, the v-team can determine if the security incident is a legitimate concern.</span></span>

<span data-ttu-id="74526-144">在调查开始时，Office 安全事件响应团队根据我们的案例管理策略记录有关事件的所有信息。</span><span class="sxs-lookup"><span data-stu-id="74526-144">At the beginning of the investigation, the Office Security Incident Response team records all information about the incident according to our case management policies.</span></span> <span data-ttu-id="74526-145">随着案例的进展，我们将跟踪正在进行的操作，并遵循证据处理标准，以收集、保留和保护整个事件生命周期中的此数据。</span><span class="sxs-lookup"><span data-stu-id="74526-145">As the case progresses, we track ongoing actions and follow evidence handling standards for gathering, retaining, and securing this data throughout the incident lifecycle.</span></span>

<span data-ttu-id="74526-146">这些操作的示例包括：</span><span class="sxs-lookup"><span data-stu-id="74526-146">Some examples of these actions would include:</span></span>

- <span data-ttu-id="74526-147">摘要，简要说明事件及其潜在影响</span><span class="sxs-lookup"><span data-stu-id="74526-147">A summary, which is a brief description of the incident and its potential impact</span></span>
- <span data-ttu-id="74526-148">事件的严重性和优先级，通过评估潜在影响派生</span><span class="sxs-lookup"><span data-stu-id="74526-148">The incident's severity and priority, which are derived by assessing the potential impact</span></span>
- <span data-ttu-id="74526-149">标识了导致检测事件的所有指标的列表</span><span class="sxs-lookup"><span data-stu-id="74526-149">A list of all indicators identified which led to detection of the incident</span></span>
- <span data-ttu-id="74526-150">任何相关事件的列表</span><span class="sxs-lookup"><span data-stu-id="74526-150">A list of any related incidents</span></span>
- <span data-ttu-id="74526-151">v-team 执行的所有操作的列表</span><span class="sxs-lookup"><span data-stu-id="74526-151">A list of all actions taken by the v-team</span></span>
- <span data-ttu-id="74526-152">收集的任何证据，还将保留这些证据，用于事后分析和将来的取证调查</span><span class="sxs-lookup"><span data-stu-id="74526-152">Any gathered evidence, which will also be preserved for post-mortem analysis and future forensic investigations</span></span>
- <span data-ttu-id="74526-153">建议的下一步和操作</span><span class="sxs-lookup"><span data-stu-id="74526-153">Recommended next steps and actions</span></span>

<span data-ttu-id="74526-154">在安全事件确认后，Microsoft 365 安全响应团队和相应服务团队的主要目标是控制攻击，保护服务 () 受到攻击，并避免更大的全球影响。</span><span class="sxs-lookup"><span data-stu-id="74526-154">After security incident confirmation, the primary goals of the Microsoft 365 Security Response team and the appropriate service team are to contain the attack, to protect the service(s) under attack, and to avoid a greater global impact.</span></span> <span data-ttu-id="74526-155">同时，相应的工程团队努力确定根本原因并准备第一个恢复计划。</span><span class="sxs-lookup"><span data-stu-id="74526-155">At the same time, the appropriate engineering teams work to determine the root cause and to prepare the first recovery plan.</span></span>

<span data-ttu-id="74526-156">下一阶段，Microsoft 365 安全响应团队将 (受) 事件影响的客户的标识（如果有）。</span><span class="sxs-lookup"><span data-stu-id="74526-156">In the next phase, the Microsoft 365 Security Response team identifies the customer(s) affected by the security incident, if any.</span></span> <span data-ttu-id="74526-157">影响范围可能需要一些时间才能根据区域、数据中心、服务、服务器场、服务器等确定。</span><span class="sxs-lookup"><span data-stu-id="74526-157">The scope of effect can take some time to determine, based on region, datacenter, service, server farm, server, and so forth.</span></span> <span data-ttu-id="74526-158">受影响的客户列表由服务团队和 Microsoft 365 CxP 通信团队编译，然后由他们处理合同和合规性义务中的客户通知流程。</span><span class="sxs-lookup"><span data-stu-id="74526-158">The list of affected customers is compiled by the service team and the Microsoft 365 CxP Communications team, who then handle the customer notification process within contractual and compliance obligations.</span></span>

## <a name="related-articles"></a><span data-ttu-id="74526-159">相关文章</span><span class="sxs-lookup"><span data-stu-id="74526-159">Related articles</span></span>

- [<span data-ttu-id="74526-160">Microsoft 365 安全事件管理</span><span class="sxs-lookup"><span data-stu-id="74526-160">Microsoft 365 security incident management</span></span>](assurance-security-incident-management.md)
- [<span data-ttu-id="74526-161">Microsoft 365 安全事件管理准备</span><span class="sxs-lookup"><span data-stu-id="74526-161">Microsoft 365 security incident management preparation</span></span>](assurance-sim-preparation.md)
- [<span data-ttu-id="74526-162">Microsoft 365 安全事件管理包含、限制和恢复</span><span class="sxs-lookup"><span data-stu-id="74526-162">Microsoft 365 security incident management containment, eradication, and recovery</span></span>](assurance-sim-containment-eradication-recovery.md)
- [<span data-ttu-id="74526-163">Microsoft 365 安全事件管理后期活动</span><span class="sxs-lookup"><span data-stu-id="74526-163">Microsoft 365 security incident management post-incident activity</span></span>](assurance-sim-post-incident-activity.md)
