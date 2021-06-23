---
title: 保护Microsoft 365基础结构
description: 了解 Microsoft 如何保护Microsoft 365基础结构。
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 224900bd60f2fd5637e7264f1aed98d5ff878b20
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/23/2021
ms.locfileid: "53089605"
---
# <a name="securing-the-microsoft-365-infrastructure"></a><span data-ttu-id="eb130-103">保护Microsoft 365基础结构</span><span class="sxs-lookup"><span data-stu-id="eb130-103">Securing the Microsoft 365 infrastructure</span></span>

<span data-ttu-id="eb130-104">Microsoft 365是世界各地最大的企业和客户云服务之一，在客户群、产品和功能方面继续快速增长。</span><span class="sxs-lookup"><span data-stu-id="eb130-104">Microsoft 365 is one of the largest enterprise and consumer cloud services in the world and continues to grow rapidly, both in customer base, products, and features.</span></span> <span data-ttu-id="eb130-105">客户不仅Microsoft 365世界一流的生产力解决方案，还帮助保护他们的最敏感信息免受不断演变的网络威胁形势的影响。</span><span class="sxs-lookup"><span data-stu-id="eb130-105">Customers turn to Microsoft 365 not only for its world-class productivity solutions, but to help protect their most sensitive information from the constantly evolving cyber threat landscape.</span></span> <span data-ttu-id="eb130-106">确保客户数据安全并保持客户信任是 Microsoft 的首要任务。</span><span class="sxs-lookup"><span data-stu-id="eb130-106">It is Microsoft's top priority to keep customer data secure and maintain customer trust.</span></span>

<span data-ttu-id="eb130-107">如果安全性是一种后天安全，则不可能保护这种规模和复杂性的系统，只有在初始设计过程中集成了安全性时，它才有效。</span><span class="sxs-lookup"><span data-stu-id="eb130-107">Securing a system of this scale and complexity is not possible if security is an afterthought, it is only effective if security is integrated during the initial design process.</span></span> <span data-ttu-id="eb130-108">它需要强大的威胁检测系统，同时提供来自自动化系统和技能熟练工程师的提示响应。</span><span class="sxs-lookup"><span data-stu-id="eb130-108">It requires a robust threat detection system with prompt responses from both automated systems and highly skilled engineers.</span></span> <span data-ttu-id="eb130-109">持续评估和验证这些系统对于确保安全配置保持不变以及识别以前未知的漏洞至关重要。</span><span class="sxs-lookup"><span data-stu-id="eb130-109">Continuous assessment and validation of these systems is essential to ensure secure configurations remain intact and previously unknown vulnerabilities are identified.</span></span>

## <a name="core-security-principles"></a><span data-ttu-id="eb130-110">核心安全原则</span><span class="sxs-lookup"><span data-stu-id="eb130-110">Core security principles</span></span>

<span data-ttu-id="eb130-111">七个安全原则为保护 Microsoft 365 服务免受威胁、检测和响应任何威胁，以及根据这些评估的结果持续评估安全状况和改进服务的框架奠定了基础。 </span><span class="sxs-lookup"><span data-stu-id="eb130-111">Seven security principles lay the foundation for our framework of *protecting* the Microsoft 365 services from threats, *detecting and responding* to any threats, and continuously *assessing* the security posture and improving services based on the results of those assessments.</span></span>

- <span data-ttu-id="eb130-112">**数据隐私**：客户拥有自己的数据，而 Microsoft 是保管人。</span><span class="sxs-lookup"><span data-stu-id="eb130-112">**Data privacy**: Customers own their data and Microsoft is the custodian.</span></span> <span data-ttu-id="eb130-113">Microsoft 365服务旨在无需工程师访问客户数据即可运行，除非客户明确请求和批准。</span><span class="sxs-lookup"><span data-stu-id="eb130-113">Microsoft 365 services are designed to operate without engineers accessing customer data, unless explicitly requested and approved by the customer.</span></span>
- <span data-ttu-id="eb130-114">**假设泄露**：将处理人员和服务，就好像存在泄露的可能性一样。</span><span class="sxs-lookup"><span data-stu-id="eb130-114">**Assume breach**: Personnel and services are treated as though compromise is a real possibility.</span></span>
- <span data-ttu-id="eb130-115">**最小特权**：对资源的访问和权限仅限于执行所需任务所需的内容。</span><span class="sxs-lookup"><span data-stu-id="eb130-115">**Least privilege**: Access and permissions to resources are limited to only what is necessary to perform needed tasks.</span></span>
- <span data-ttu-id="eb130-116">**泄露边界**：一个边界中的标识和基础结构独立于其他边界中的资源。</span><span class="sxs-lookup"><span data-stu-id="eb130-116">**Breach boundaries**: Identities and infrastructure in one boundary are isolated from resources in other boundaries.</span></span> <span data-ttu-id="eb130-117">泄露一个边界不应导致另一个边界的泄露。</span><span class="sxs-lookup"><span data-stu-id="eb130-117">Compromise of one boundary should not lead to compromise of another.</span></span>
- <span data-ttu-id="eb130-118">**服务结构集成安全性**：安全优先级和要求内置于新特性和功能设计中，确保强大的安全状况随每个服务而扩展。</span><span class="sxs-lookup"><span data-stu-id="eb130-118">**Service fabric integrated security**: Security priorities and requirements are built into the design of new features and capabilities, ensuring that a strong security posture scales with each service.</span></span>
- <span data-ttu-id="eb130-119">**自动和** 自动：Microsoft 侧重于开发可智能和自动强制实施服务安全的持久型产品和体系结构，同时使 Microsoft 工程师能够安全地大规模管理对安全威胁的响应。</span><span class="sxs-lookup"><span data-stu-id="eb130-119">**Automated and automatic**: Microsoft focuses on developing durable products and architectures that can intelligently and automatically enforce service security, while giving Microsoft engineers the ability to safely manage responses to security threats at scale.</span></span>
- <span data-ttu-id="eb130-120">**自适应安全性**：Microsoft 的管理功能适应机器学习模型、日常渗透测试和自动评估，并增强了这些功能。</span><span class="sxs-lookup"><span data-stu-id="eb130-120">**Adaptive security**: Microsoft security capabilities adapt to and are enhanced by machine learning models, routine penetration testing, and automated assessments.</span></span>

## <a name="protection"></a><span data-ttu-id="eb130-121">保护</span><span class="sxs-lookup"><span data-stu-id="eb130-121">Protection</span></span>

### <a name="access-control"></a><span data-ttu-id="eb130-122">访问控制</span><span class="sxs-lookup"><span data-stu-id="eb130-122">Access control</span></span>

<span data-ttu-id="eb130-123">默认情况下，负责开发和维护服务Microsoft 365对服务基础结构 (ZSA) 零长期访问权限。</span><span class="sxs-lookup"><span data-stu-id="eb130-123">By default, personnel responsible for developing and maintaining Microsoft 365 services have Zero Standing Access (ZSA) to the service infrastructure.</span></span> <span data-ttu-id="eb130-124">虽然 Microsoft 努力仅雇用最佳工程师，并且需要严格的背景调查，但 Microsoft 不会假定他们在运营服务中默认受信任。</span><span class="sxs-lookup"><span data-stu-id="eb130-124">While Microsoft strives to hire only the best engineers and rigorous background checks are required, Microsoft does not assume that they are trusted by default in operating services.</span></span> <span data-ttu-id="eb130-125">此外，当批准工程师进行特权访问时，他们只能获得有限期限的访问权限，以仅执行服务基础结构的特定范围所需的操作。</span><span class="sxs-lookup"><span data-stu-id="eb130-125">Additionally, when engineers are approved for privileged access, they are only granted access for a limited duration to perform only the actions needed for a specific scope of the service infrastructure.</span></span> <span data-ttu-id="eb130-126">Microsoft 将这些策略称为实时 (JIT) 和 Just-Enough-Access (JEA) 通过称为密码箱的系统实现。</span><span class="sxs-lookup"><span data-stu-id="eb130-126">Microsoft refers to these policies as Just-in-Time (JIT) and Just-Enough-Access (JEA) which are implemented through a system called Lockbox.</span></span>

<span data-ttu-id="eb130-127">为了获取提升的权限，Microsoft 工程师提交特定任务请求并指定执行该任务的时间框架。</span><span class="sxs-lookup"><span data-stu-id="eb130-127">To acquire elevated privileges, Microsoft engineers submit a request for the specific task and specify the time frame to perform it.</span></span> <span data-ttu-id="eb130-128">一旦获得批准，密码箱将生成一个专用 JIT 帐户，该帐户只能执行请求的任务。</span><span class="sxs-lookup"><span data-stu-id="eb130-128">Once approved, Lockbox generates a specialized JIT account with the ability to perform only the requested task.</span></span> <span data-ttu-id="eb130-129">操作通常采用自动工作流的形式，可安全地执行所需的任何故障排除或恢复。</span><span class="sxs-lookup"><span data-stu-id="eb130-129">Actions usually take the form of automated workflows that securely perform any troubleshooting or recovery required.</span></span> <span data-ttu-id="eb130-130">在极少数情况下，当需要直接访问基础结构时，需要严格监视 Privileged Access Workstations (PAW) 要求。</span><span class="sxs-lookup"><span data-stu-id="eb130-130">In rare instances when direct access to the infrastructure is necessary, strictly monitored Privileged Access Workstations (PAWs) are required.</span></span>

<span data-ttu-id="eb130-131">未授权用户和遭到入侵的帐户在任何组织中都有可能存在，我们的访问控制系统旨在防范这些威胁。</span><span class="sxs-lookup"><span data-stu-id="eb130-131">Rogue users and compromised accounts are a real possibility in any organization, and our access control system are designed to protect against these threats.</span></span>

<span data-ttu-id="eb130-132">有关访问控制详细信息，请参阅 [标识和访问管理概述](assurance-identity-and-access-management.md)。</span><span class="sxs-lookup"><span data-stu-id="eb130-132">For more information about access control, see [Identity and access management overview](assurance-identity-and-access-management.md).</span></span>

### <a name="encryption"></a><span data-ttu-id="eb130-133">加密</span><span class="sxs-lookup"><span data-stu-id="eb130-133">Encryption</span></span>

<span data-ttu-id="eb130-134">访问控制在保护服务Microsoft 365至关重要，但加密在整个数据生命周期内用于进一步保护 Microsoft 客户的机密性和隐私。</span><span class="sxs-lookup"><span data-stu-id="eb130-134">While access controls provide a vital role in defending Microsoft 365 services, encryption is used throughout the data lifecycle to further protect confidentiality and privacy for Microsoft customers.</span></span>

<span data-ttu-id="eb130-135">客户端计算机、Microsoft 365服务器和非 Microsoft 365 之间传输的数据使用 TLS 1.2 进行加密。</span><span class="sxs-lookup"><span data-stu-id="eb130-135">Data in transit between client machines, Microsoft 365 servers, and non-Microsoft 365 servers is encrypted using TLS 1.2.</span></span> <span data-ttu-id="eb130-136">我们定期查看使用中的密码和协议，添加改进的协议（如果可用）并根据需要删除较弱的协议。</span><span class="sxs-lookup"><span data-stu-id="eb130-136">We regularly review the ciphers and protocols in use, adding improved protocols when available and removing weaker ones as needed.</span></span>

<span data-ttu-id="eb130-137">Microsoft 服务器上处于其余状态的客户内容使用 BitLocker 在卷级别加密。</span><span class="sxs-lookup"><span data-stu-id="eb130-137">Customer content at rest on Microsoft servers is encrypted at the volume-level using BitLocker.</span></span> <span data-ttu-id="eb130-138">此外，还可使用由 Microsoft 或客户管理的密钥应用应用程序级加密。</span><span class="sxs-lookup"><span data-stu-id="eb130-138">Application-level encryption can additionally be applied using keys managed by either Microsoft or the customer.</span></span> <span data-ttu-id="eb130-139">只有在通过 JIT 和 JEA 过程获得授权和批准后，才能访问 Microsoft 管理的密钥。</span><span class="sxs-lookup"><span data-stu-id="eb130-139">Access to Microsoft-managed keys is only possible when authorized and approved through the JIT and JEA process.</span></span>

<span data-ttu-id="eb130-140">有关加密中加密Microsoft 365，请参阅[加密和密钥管理概述](assurance-encryption.md)。</span><span class="sxs-lookup"><span data-stu-id="eb130-140">For more information about encryption in Microsoft 365, see [Encryption and key management overview](assurance-encryption.md).</span></span>

### <a name="network-isolation"></a><span data-ttu-id="eb130-141">网络隔离</span><span class="sxs-lookup"><span data-stu-id="eb130-141">Network isolation</span></span>

<span data-ttu-id="eb130-142">根据最小特权原则，Microsoft 365服务基础结构的不同部分之间的通信限制为仅操作所需的内容。</span><span class="sxs-lookup"><span data-stu-id="eb130-142">In line with the principle of least privilege, Microsoft 365 restricts communication between different parts of the service infrastructure to only what is necessary to operate.</span></span> <span data-ttu-id="eb130-143">默认情况下，所有网络流量都被拒绝，只允许显式定义的通信。</span><span class="sxs-lookup"><span data-stu-id="eb130-143">All network traffic is denied by default, with only explicitly defined communication being allowed.</span></span> <span data-ttu-id="eb130-144">此限制在整个基础结构中建立了泄露边界。</span><span class="sxs-lookup"><span data-stu-id="eb130-144">This restriction establishes breach boundaries throughout the infrastructure.</span></span> <span data-ttu-id="eb130-145">Teams添加新网络路径以适应其服务的新功能的管理员必须对请求进行评估和批准，然后才能打开该请求。</span><span class="sxs-lookup"><span data-stu-id="eb130-145">Teams that would like to add new network paths to accommodate a new feature to their service must have the request evaluated and approved before it can be opened.</span></span>

<span data-ttu-id="eb130-146">有关网络隔离中网络隔离Microsoft 365，请参阅Microsoft 365[隔离控件](/microsoft-365/enterprise/microsoft-365-isolation-controls)。</span><span class="sxs-lookup"><span data-stu-id="eb130-146">For more information about network isolation in Microsoft 365, see [Microsoft 365 isolation controls](/microsoft-365/enterprise/microsoft-365-isolation-controls).</span></span>

## <a name="detection--response"></a><span data-ttu-id="eb130-147">检测&响应</span><span class="sxs-lookup"><span data-stu-id="eb130-147">Detection & Response</span></span>

### <a name="security-monitoring"></a><span data-ttu-id="eb130-148">安全监视</span><span class="sxs-lookup"><span data-stu-id="eb130-148">Security monitoring</span></span>

<span data-ttu-id="eb130-149">只有在使用基于云的自动化解决方案生成高度准确的警报后，Microsoft 才能大规模进行安全监视。</span><span class="sxs-lookup"><span data-stu-id="eb130-149">Security monitoring at Microsoft's massive scale is only possible by generating highly accurate alerts using automated cloud-based solutions.</span></span> <span data-ttu-id="eb130-150">从整个核心基础结构中收集的每个服务和遥测数据的审核日志将发送到专用的集中式近实时处理和警报解决方案。</span><span class="sxs-lookup"><span data-stu-id="eb130-150">Audit logs from each service and telemetry data gathered from throughout the core infrastructure is sent to a proprietary centralized near-real-time processing and alerting solution.</span></span>

<span data-ttu-id="eb130-151">如果可能，使用自动触发的操作修正检测到的威胁。</span><span class="sxs-lookup"><span data-stu-id="eb130-151">Detected threats are remediated using automatically triggered actions when possible.</span></span> <span data-ttu-id="eb130-152">当自动化解决方案失败或无法解决问题时，呼叫中的 Microsoft 工程师将立即采取措施来缓解威胁。</span><span class="sxs-lookup"><span data-stu-id="eb130-152">When automated solutions are unsuccessful or incapable of resolving the issue, on-call Microsoft engineers immediately take action to mitigate the threat.</span></span>

<span data-ttu-id="eb130-153">有关安全监视中安全监视Microsoft 365，请参阅[安全监视概述](assurance-security-monitoring.md)。</span><span class="sxs-lookup"><span data-stu-id="eb130-153">For more information about security monitoring in Microsoft 365, see [Security monitoring overview](assurance-security-monitoring.md).</span></span>

## <a name="assessment"></a><span data-ttu-id="eb130-154">评估</span><span class="sxs-lookup"><span data-stu-id="eb130-154">Assessment</span></span>

### <a name="automated-assessments"></a><span data-ttu-id="eb130-155">自动评估</span><span class="sxs-lookup"><span data-stu-id="eb130-155">Automated assessments</span></span>

<span data-ttu-id="eb130-156">无论系统是如何设计的，安全状况都会因有意和无意的配置随着时间的推移而降级。</span><span class="sxs-lookup"><span data-stu-id="eb130-156">Regardless of how a system is designed, the security posture can degrade due to intentional and unintentional configuration drift over time.</span></span> <span data-ttu-id="eb130-157">自动化工具会Microsoft 365查找未修补和错误配置的服务的系统。</span><span class="sxs-lookup"><span data-stu-id="eb130-157">Automated tools constantly assess Microsoft 365 systems that look for unpatched and misconfigured services.</span></span> <span data-ttu-id="eb130-158">此评估通常称为 PATCHC (修补、防病毒、漏洞和) 。</span><span class="sxs-lookup"><span data-stu-id="eb130-158">This assessment is often referred to as patching, anti-virus, vulnerability, and configuration scanning (PAVC).</span></span>

<span data-ttu-id="eb130-159">我们的体系结构也经常经过验证，识别未使用的开放端口和具有长期管理访问权限的帐户等实例。</span><span class="sxs-lookup"><span data-stu-id="eb130-159">Our architecture is also frequently validated, identifying instances such as unused open ports and accounts with standing administrative access.</span></span> <span data-ttu-id="eb130-160">与预定义的所需状态偏离的任何服务都会自动恢复对齐。</span><span class="sxs-lookup"><span data-stu-id="eb130-160">Any services that drift from a pre-defined desired state are automatically brought back into alignment.</span></span>

<span data-ttu-id="eb130-161">有关安全监视中安全监视Microsoft 365，请参阅[漏洞管理概述](assurance-vulnerability-management.md)。</span><span class="sxs-lookup"><span data-stu-id="eb130-161">For more information about security monitoring in Microsoft 365, see [Vulnerability management overview](assurance-vulnerability-management.md).</span></span>

### <a name="attack-simulation-and-penetration-testing"></a><span data-ttu-id="eb130-162">攻击模拟和渗透测试</span><span class="sxs-lookup"><span data-stu-id="eb130-162">Attack simulation and penetration testing</span></span>

<span data-ttu-id="eb130-163">Microsoft 365头等要的是防止攻击。</span><span class="sxs-lookup"><span data-stu-id="eb130-163">Microsoft 365's top priority is to prevent attacks from infiltrating defenses.</span></span> <span data-ttu-id="eb130-164">Microsoft 365一个专门的安全专家团队，他们不断进行模拟攻击，以识别以前未知的漏洞，并提供丰富的持续数据流以改进安全监视功能。</span><span class="sxs-lookup"><span data-stu-id="eb130-164">Microsoft 365 has a dedicated team of security experts who are constantly conducting simulated attacks to identify previously unknown vulnerabilities and to provide a constant stream of rich data to improve security monitoring capabilities.</span></span> <span data-ttu-id="eb130-165">这些模拟攻击采用频繁自动小型攻击和专家驱动的深入探究的形式。</span><span class="sxs-lookup"><span data-stu-id="eb130-165">These simulated attacks take the form of frequent automated small-scale attacks and expert-driven deep dives.</span></span> <span data-ttu-id="eb130-166">从这些活动中，Microsoft 评估检测、响应和收回攻击者的能力。</span><span class="sxs-lookup"><span data-stu-id="eb130-166">From these activities, Microsoft evaluates the ability to detect, respond, and evict attackers.</span></span>

<span data-ttu-id="eb130-167">有关安全监视中安全监视Microsoft 365，请参阅攻击[模拟Microsoft 365。](assurance-monitoring-and-testing.md)</span><span class="sxs-lookup"><span data-stu-id="eb130-167">For more information about security monitoring in Microsoft 365, see [Attack simulation in Microsoft 365](assurance-monitoring-and-testing.md).</span></span>

## <a name="resources"></a><span data-ttu-id="eb130-168">资源</span><span class="sxs-lookup"><span data-stu-id="eb130-168">Resources</span></span>

[<span data-ttu-id="eb130-169">后台：保护为 Microsoft 365 服务提供电源的基础结构</span><span class="sxs-lookup"><span data-stu-id="eb130-169">Behind the Scenes: Securing the Infrastructure Powering the Microsoft 365 Service</span></span>](https://download.microsoft.com/download/c/4/5/c45b197e-f0d9-4f40-bd5f-ed8fc7d0cd8c/M365DCSecurityIntro_Whitepaper.pdf)
