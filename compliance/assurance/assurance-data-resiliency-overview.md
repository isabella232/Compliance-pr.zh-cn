---
title: Microsoft 365 中的数据复原能力
description: 本文介绍 Microsoft 365 中数据恢复和恢复的设计和原则。
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
ms.openlocfilehash: 361400bf6330fb82d34f384d17e4d4ee438ccf08
ms.sourcegitcommit: b06fa9f1b230fd5e470817486ea51f460f28b691
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/27/2021
ms.locfileid: "50012898"
---
# <a name="data-resiliency-in-microsoft-365"></a><span data-ttu-id="db192-103">Microsoft 365 中的数据恢复能力</span><span class="sxs-lookup"><span data-stu-id="db192-103">Data resiliency in Microsoft 365</span></span>

<span data-ttu-id="db192-104">鉴于云计算的复杂性质，Microsoft 请注意，问题不是问题是否发生，而是何时发生。</span><span class="sxs-lookup"><span data-stu-id="db192-104">Given the complex nature of cloud computing, Microsoft is mindful that it's not a case of if things will go wrong, but rather when.</span></span> <span data-ttu-id="db192-105">我们将云服务设计得最大化可靠性，并最大限度地减少出现问题时对客户的负面影响。</span><span class="sxs-lookup"><span data-stu-id="db192-105">We design our cloud services to maximize reliability and minimize the negative effects on customers when things do go wrong.</span></span> <span data-ttu-id="db192-106">我们已超越依赖复杂物理基础结构的传统策略，并且直接将冗余内置到云服务中。</span><span class="sxs-lookup"><span data-stu-id="db192-106">We have moved beyond the traditional strategy of relying on complex physical infrastructure, and we have built redundancy directly into our cloud services.</span></span> <span data-ttu-id="db192-107">我们结合使用了不太复杂的物理基础结构和更具智能性的软件，将数据恢复能力构建到服务中，并为客户提供高可用性。</span><span class="sxs-lookup"><span data-stu-id="db192-107">We use a combination of less complex physical infrastructure and more intelligent software that builds data resiliency into our services and delivers high availability to our customers.</span></span>

## <a name="resiliency-and-recoverability-are-built-in"></a><span data-ttu-id="db192-108">内置复原和可恢复性</span><span class="sxs-lookup"><span data-stu-id="db192-108">Resiliency and recoverability are built-in</span></span>

<span data-ttu-id="db192-109">在复原和恢复中构建首先假定基础基础结构和流程将在某些时候失败：硬件 (基础结构) 将失败，用户将出错，软件将具有 Bug。</span><span class="sxs-lookup"><span data-stu-id="db192-109">Building in resiliency and recovery starts with the assumption that the underlying infrastructure and processes will fail at some point: hardware (infrastructure) will fail, humans will make mistakes, and software will have bugs.</span></span> <span data-ttu-id="db192-110">虽然说软件开发人员在云之前没有考虑这些问题是错误的，但是，在典型的 IT 实施中，这些问题的处理方式与云之前有所不同：</span><span class="sxs-lookup"><span data-stu-id="db192-110">While it would be incorrect to say that software developers were not thinking about these things before the cloud, how these issues were handled in a typical IT implementation was different before the cloud:</span></span>

- <span data-ttu-id="db192-111">首先，硬件和基础结构保护十分重要。</span><span class="sxs-lookup"><span data-stu-id="db192-111">First, hardware and infrastructure protections were significant.</span></span> <span data-ttu-id="db192-112">这种结构意味着具有可靠性为 99.99% 的数据中心需要大量电源和网络冗余，并且服务器通过基于硬件的群集、双电源、双网络接口等实现。</span><span class="sxs-lookup"><span data-stu-id="db192-112">This structure meant having datacenters with 99.99% reliability required significant power and network redundancy, and servers were implemented with hardware-based clustering, dual power supplies, dual network interfaces, and the like.</span></span>
- <span data-ttu-id="db192-113">第二，过程至关重要。</span><span class="sxs-lookup"><span data-stu-id="db192-113">Second, process was paramount.</span></span> <span data-ttu-id="db192-114">运营团队维护严格的过程，使用了更改窗口，并且通常存在大量的项目管理开销。</span><span class="sxs-lookup"><span data-stu-id="db192-114">Operations teams maintained rigorous procedures, change windows were employed, and there was often significant project management overhead.</span></span>
- <span data-ttu-id="db192-115">第三，部署以一种淡淡的速度进行。</span><span class="sxs-lookup"><span data-stu-id="db192-115">Third, deployment took place at a glacial pace.</span></span> <span data-ttu-id="db192-116">在不拥有源的情况下部署代码意味着等待修补程序发布，主要版本涉及硬件更换和大量资金投入。</span><span class="sxs-lookup"><span data-stu-id="db192-116">Deploying code without owning the source meant waiting for patch releases, and major version releases involved hardware replacement and significant capital outlay.</span></span> <span data-ttu-id="db192-117">此外，更正问题的唯一方法就是回滚。</span><span class="sxs-lookup"><span data-stu-id="db192-117">Moreover, the only way to correct a problem was to roll back.</span></span> <span data-ttu-id="db192-118">因此，大多数 IT 组织仅部署主要版本，以避免工作保持最新。</span><span class="sxs-lookup"><span data-stu-id="db192-118">Thus, most IT organizations would deploy only major releases to avoid the work to keep up to date.</span></span>
- <span data-ttu-id="db192-119">最后，已部署系统的规模和它们的互连程度过去比现在要小得多。</span><span class="sxs-lookup"><span data-stu-id="db192-119">Finally, the scale of deployed systems and the level of their interconnectedness was historically much smaller than it is now.</span></span>

<span data-ttu-id="db192-120">如今，客户期望 Microsoft 持续创新，而不会损害质量，这也是 Microsoft 服务和软件构建时牢记复原性和可恢复性的原因之一。</span><span class="sxs-lookup"><span data-stu-id="db192-120">Today, customers expect continuous innovation from Microsoft without compromising quality, and this is one of the reasons why Microsoft's services and software are built with resiliency and recoverability in mind.</span></span>

## <a name="microsoft-365-data-resiliency-principles"></a><span data-ttu-id="db192-121">Microsoft 365 数据复原原则</span><span class="sxs-lookup"><span data-stu-id="db192-121">Microsoft 365 data resiliency principles</span></span>

<span data-ttu-id="db192-122">复原是指基于云的服务能够抵御某些类型的故障，但从客户的角度来看仍可以完全正常运行。</span><span class="sxs-lookup"><span data-stu-id="db192-122">Resiliency refers to the ability of a cloud-based service to withstand certain types of failures and yet remain fully functional from the customers' perspective.</span></span> <span data-ttu-id="db192-123">数据恢复能力意味着无论 Microsoft 365 中发生什么故障，关键客户数据都保持不变且不受影响。</span><span class="sxs-lookup"><span data-stu-id="db192-123">Data resiliency means that no matter what failures occur within Microsoft 365, critical customer data remains intact and unaffected.</span></span> <span data-ttu-id="db192-124">为此，Microsoft 365 服务围绕五个特定复原原则进行设计：</span><span class="sxs-lookup"><span data-stu-id="db192-124">To that end, Microsoft 365 services have been designed around five specific resiliency principles:</span></span>

- <span data-ttu-id="db192-125">存在关键和非关键数据。</span><span class="sxs-lookup"><span data-stu-id="db192-125">There is critical and non-critical data.</span></span> <span data-ttu-id="db192-126">例如，非关键 (，例如，在极少数失败) 是否可丢弃邮件。</span><span class="sxs-lookup"><span data-stu-id="db192-126">Non-critical data (for example, whether a message was read) can be dropped in rare failure scenarios.</span></span> <span data-ttu-id="db192-127">关键 (例如，应以极端成本) 电子邮件等客户数据。</span><span class="sxs-lookup"><span data-stu-id="db192-127">Critical data (for example, customer data such as email messages) should be protected at extreme cost.</span></span> <span data-ttu-id="db192-128">作为设计目标，传递的邮件始终至关重要，并且邮件是否已阅读等内容都非关键。</span><span class="sxs-lookup"><span data-stu-id="db192-128">As a design goal, delivered mail messages are always critical, and things like whether a message has been read is non-critical.</span></span>
- <span data-ttu-id="db192-129">客户数据的副本必须分隔到不同的容错区域或尽可能多的故障域中 (例如，数据中心可由单个凭据（进程、服务器或操作员 (进程、服务器或操作员) ）访问，以提供故障隔离。</span><span class="sxs-lookup"><span data-stu-id="db192-129">Copies of customer data must be separated into different fault zones or as many fault domains as possible (for example, datacenters, accessible by single credentials (process, server, or operator)) to provide failure isolation.</span></span> 
- <span data-ttu-id="db192-130">必须对关键客户数据进行监视，以发现任何部分无法通过原子性、一致性、隔离、持久性 (或) 。</span><span class="sxs-lookup"><span data-stu-id="db192-130">Critical customer data must be monitored for failing any part of Atomicity, Consistency, Isolation, Durability (ACID).</span></span>
- <span data-ttu-id="db192-131">必须防止客户数据损坏。</span><span class="sxs-lookup"><span data-stu-id="db192-131">Customer data must be protected from corruption.</span></span> <span data-ttu-id="db192-132">它必须主动扫描或监视、可修复且可恢复。</span><span class="sxs-lookup"><span data-stu-id="db192-132">It must be actively scanned or monitored, repairable, and recoverable.</span></span>
- <span data-ttu-id="db192-133">大多数数据丢失都由客户操作导致，因此允许客户使用 GUI 自行恢复，以便客户能够还原意外删除的项目。</span><span class="sxs-lookup"><span data-stu-id="db192-133">Most data loss results from customer actions, so allow customers to recover on their own using a GUI that enables them to restore accidentally deleted items.</span></span>

<span data-ttu-id="db192-134">通过遵循这些原则构建云服务，以及强大的测试和验证，Microsoft 365 能够满足并超过客户的要求，同时确保提供持续创新和改进的平台。</span><span class="sxs-lookup"><span data-stu-id="db192-134">Through the building of our cloud services to these principles, coupled with robust testing and validation, Microsoft 365 is able to meet and exceed the requirements of customers while ensuring a platform for continuous innovation and improvement.</span></span>

## <a name="related-articles"></a><span data-ttu-id="db192-135">相关文章</span><span class="sxs-lookup"><span data-stu-id="db192-135">Related articles</span></span>

- [<span data-ttu-id="db192-136">处理数据损坏</span><span class="sxs-lookup"><span data-stu-id="db192-136">Dealing with Data Corruption</span></span>](assurance-dealing-with-data-corruption.md)
- [<span data-ttu-id="db192-137">恶意软件和勒索软件防护</span><span class="sxs-lookup"><span data-stu-id="db192-137">Malware and Ransomware Protection</span></span>](assurance-malware-and-ransomware-protection.md)
- [<span data-ttu-id="db192-138">监视和自愈</span><span class="sxs-lookup"><span data-stu-id="db192-138">Monitoring and Self-Healing</span></span>](assurance-monitoring-and-self-healing.md)
- [<span data-ttu-id="db192-139">Exchange 数据恢复能力</span><span class="sxs-lookup"><span data-stu-id="db192-139">Exchange Data Resiliency</span></span>](assurance-exchange-data-resiliency.md)
