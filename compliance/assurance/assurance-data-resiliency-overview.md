---
title: Microsoft 365 中的数据复原能力
description: 本文介绍 Microsoft 365 中数据复原和恢复的设计和原则。
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
hideEdit: true
ms.openlocfilehash: 6e990facde47b07d50f594afb55353a5ef81dd78
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497617"
---
# <a name="data-resiliency-in-microsoft-365"></a><span data-ttu-id="1e340-103">Microsoft 365 中的数据恢复能力</span><span class="sxs-lookup"><span data-stu-id="1e340-103">Data resiliency in Microsoft 365</span></span>

<span data-ttu-id="1e340-104">鉴于云计算的复杂性质，Microsoft 请注意，问题不是何时会出错。</span><span class="sxs-lookup"><span data-stu-id="1e340-104">Given the complex nature of cloud computing, Microsoft is mindful that it's not a case of if things will go wrong, but rather when.</span></span> <span data-ttu-id="1e340-105">我们设计的云服务可最大限度地提高可靠性，并最大限度地减少出现问题时对客户的负面影响。</span><span class="sxs-lookup"><span data-stu-id="1e340-105">We design our cloud services to maximize reliability and minimize the negative effects on customers when things do go wrong.</span></span> <span data-ttu-id="1e340-106">我们已超越依赖复杂物理基础结构的传统策略，并且已经将冗余直接内置到云服务中。</span><span class="sxs-lookup"><span data-stu-id="1e340-106">We have moved beyond the traditional strategy of relying on complex physical infrastructure, and we have built redundancy directly into our cloud services.</span></span> <span data-ttu-id="1e340-107">我们结合使用不太复杂的物理基础结构和更具智能性的软件，将数据复原构建到我们的服务中，并为客户提供高可用性。</span><span class="sxs-lookup"><span data-stu-id="1e340-107">We use a combination of less complex physical infrastructure and more intelligent software that builds data resiliency into our services and delivers high availability to our customers.</span></span>

## <a name="resiliency-and-recoverability-are-built-in"></a><span data-ttu-id="1e340-108">复原和可恢复性内置</span><span class="sxs-lookup"><span data-stu-id="1e340-108">Resiliency and recoverability are built-in</span></span>

<span data-ttu-id="1e340-109">在复原和恢复中构建时，首先假定基础基础结构和流程将在某些时候失败：硬件 (基础结构) 将失败，用户会出错，并且软件将存在 Bug。</span><span class="sxs-lookup"><span data-stu-id="1e340-109">Building in resiliency and recovery starts with the assumption that the underlying infrastructure and processes will fail at some point: hardware (infrastructure) will fail, humans will make mistakes, and software will have bugs.</span></span> <span data-ttu-id="1e340-110">虽然说软件开发人员在云之前没有考虑这些问题是不正确的，但是，在典型的 IT 实施中如何处理这些问题与在云之前有所不同：</span><span class="sxs-lookup"><span data-stu-id="1e340-110">While it would be incorrect to say that software developers were not thinking about these things before the cloud, how these issues were handled in a typical IT implementation was different before the cloud:</span></span>

- <span data-ttu-id="1e340-111">首先，硬件和基础结构保护十分重要。</span><span class="sxs-lookup"><span data-stu-id="1e340-111">First, hardware and infrastructure protections were significant.</span></span> <span data-ttu-id="1e340-112">这种结构意味着使具有 99.99% 可靠性的数据中心需要大量电源和网络冗余，并且使用基于硬件的群集、双电源、双网络接口等实现服务器。</span><span class="sxs-lookup"><span data-stu-id="1e340-112">This structure meant having datacenters with 99.99% reliability required significant power and network redundancy, and servers were implemented with hardware-based clustering, dual power supplies, dual network interfaces, and the like.</span></span>
- <span data-ttu-id="1e340-113">第二，进程至关重要。</span><span class="sxs-lookup"><span data-stu-id="1e340-113">Second, process was paramount.</span></span> <span data-ttu-id="1e340-114">运营团队维护了严格的过程，使用了更改窗口，并且通常会存在大量的项目管理开销。</span><span class="sxs-lookup"><span data-stu-id="1e340-114">Operations teams maintained rigorous procedures, change windows were employed, and there was often significant project management overhead.</span></span>
- <span data-ttu-id="1e340-115">第三，部署以淡紫色的速度进行。</span><span class="sxs-lookup"><span data-stu-id="1e340-115">Third, deployment took place at a glacial pace.</span></span> <span data-ttu-id="1e340-116">在未拥有源的情况下部署代码意味着等待修补程序发布，主要版本涉及硬件更换和大量资金推出。</span><span class="sxs-lookup"><span data-stu-id="1e340-116">Deploying code without owning the source meant waiting for patch releases, and major version releases involved hardware replacement and significant capital outlay.</span></span> <span data-ttu-id="1e340-117">此外，更正问题的唯一方法就是回滚。</span><span class="sxs-lookup"><span data-stu-id="1e340-117">Moreover, the only way to correct a problem was to roll back.</span></span> <span data-ttu-id="1e340-118">因此，大多数 IT 组织仅部署主要版本，以避免保持最新状态的工作。</span><span class="sxs-lookup"><span data-stu-id="1e340-118">Thus, most IT organizations would deploy only major releases to avoid the work to keep up to date.</span></span>
- <span data-ttu-id="1e340-119">最后，已部署系统的规模和相互连接的级别以往比现在要小得多。</span><span class="sxs-lookup"><span data-stu-id="1e340-119">Finally, the scale of deployed systems and the level of their interconnectedness was historically much smaller than it is now.</span></span>

<span data-ttu-id="1e340-120">如今，客户期望 Microsoft 持续创新而不会损害质量，这是 Microsoft 服务和软件构建时牢记复原性和可恢复性的原因之一。</span><span class="sxs-lookup"><span data-stu-id="1e340-120">Today, customers expect continuous innovation from Microsoft without compromising quality, and this is one of the reasons why Microsoft's services and software are built with resiliency and recoverability in mind.</span></span>

## <a name="microsoft-365-data-resiliency-principles"></a><span data-ttu-id="1e340-121">Microsoft 365 数据复原原则</span><span class="sxs-lookup"><span data-stu-id="1e340-121">Microsoft 365 data resiliency principles</span></span>

<span data-ttu-id="1e340-122">复原是指基于云的服务能够抵御某些类型的故障，但从客户的角度来看，该服务仍可以完全正常运行。</span><span class="sxs-lookup"><span data-stu-id="1e340-122">Resiliency refers to the ability of a cloud-based service to withstand certain types of failures and yet remain fully functional from the customers' perspective.</span></span> <span data-ttu-id="1e340-123">数据复原意味着无论 Microsoft 365 中发生什么故障，关键客户数据都保持不变且不受影响。</span><span class="sxs-lookup"><span data-stu-id="1e340-123">Data resiliency means that no matter what failures occur within Microsoft 365, critical customer data remains intact and unaffected.</span></span> <span data-ttu-id="1e340-124">为此，Microsoft 365 服务围绕五个特定复原原则进行设计：</span><span class="sxs-lookup"><span data-stu-id="1e340-124">To that end, Microsoft 365 services have been designed around five specific resiliency principles:</span></span>

- <span data-ttu-id="1e340-125">存在关键和非关键数据。</span><span class="sxs-lookup"><span data-stu-id="1e340-125">There is critical and non-critical data.</span></span> <span data-ttu-id="1e340-126">非关键 (例如，是否读取消息) 在极少数失败情况下可以丢弃。</span><span class="sxs-lookup"><span data-stu-id="1e340-126">Non-critical data (for example, whether a message was read) can be dropped in rare failure scenarios.</span></span> <span data-ttu-id="1e340-127">关键 (例如，应以极端成本) 电子邮件等客户数据。</span><span class="sxs-lookup"><span data-stu-id="1e340-127">Critical data (for example, customer data such as email messages) should be protected at extreme cost.</span></span> <span data-ttu-id="1e340-128">作为设计目标，传递的邮件始终至关重要，并且邮件是否已阅读等内容都非关键。</span><span class="sxs-lookup"><span data-stu-id="1e340-128">As a design goal, delivered mail messages are always critical, and things like whether a message has been read is non-critical.</span></span>
- <span data-ttu-id="1e340-129">客户数据的副本必须分隔到不同的故障区域或尽可能多的故障域 (例如数据中心，由单个凭据（ (进程、服务器或操作员) ) ）访问以提供故障隔离。</span><span class="sxs-lookup"><span data-stu-id="1e340-129">Copies of customer data must be separated into different fault zones or as many fault domains as possible (for example, datacenters, accessible by single credentials (process, server, or operator)) to provide failure isolation.</span></span> 
- <span data-ttu-id="1e340-130">必须监视关键客户数据，以发现任何部分"原子性、一致性、隔离性"和" (或) 。</span><span class="sxs-lookup"><span data-stu-id="1e340-130">Critical customer data must be monitored for failing any part of Atomicity, Consistency, Isolation, Durability (ACID).</span></span>
- <span data-ttu-id="1e340-131">必须防止客户数据损坏。</span><span class="sxs-lookup"><span data-stu-id="1e340-131">Customer data must be protected from corruption.</span></span> <span data-ttu-id="1e340-132">必须主动扫描或监视它、可修复和可恢复。</span><span class="sxs-lookup"><span data-stu-id="1e340-132">It must be actively scanned or monitored, repairable, and recoverable.</span></span>
- <span data-ttu-id="1e340-133">大多数数据丢失都由客户操作导致，因此允许客户使用 GUI 自行恢复，以便客户能够还原意外删除的项目。</span><span class="sxs-lookup"><span data-stu-id="1e340-133">Most data loss results from customer actions, so allow customers to recover on their own using a GUI that enables them to restore accidentally deleted items.</span></span>

<span data-ttu-id="1e340-134">通过构建遵守这些原则的云服务，再加上强大的测试和验证，Microsoft 365 能够满足并超过客户的要求，同时确保获得持续创新和改进的平台。</span><span class="sxs-lookup"><span data-stu-id="1e340-134">Through the building of our cloud services to these principles, coupled with robust testing and validation, Microsoft 365 is able to meet and exceed the requirements of customers while ensuring a platform for continuous innovation and improvement.</span></span>

## <a name="related-articles"></a><span data-ttu-id="1e340-135">相关文章</span><span class="sxs-lookup"><span data-stu-id="1e340-135">Related articles</span></span>

- [<span data-ttu-id="1e340-136">处理数据损坏</span><span class="sxs-lookup"><span data-stu-id="1e340-136">Dealing with Data Corruption</span></span>](assurance-dealing-with-data-corruption.md)
- [<span data-ttu-id="1e340-137">恶意软件和勒索软件防护</span><span class="sxs-lookup"><span data-stu-id="1e340-137">Malware and Ransomware Protection</span></span>](assurance-malware-and-ransomware-protection.md)
- [<span data-ttu-id="1e340-138">监视和自愈</span><span class="sxs-lookup"><span data-stu-id="1e340-138">Monitoring and Self-Healing</span></span>](assurance-monitoring-and-self-healing.md)
- [<span data-ttu-id="1e340-139">Exchange 数据恢复能力</span><span class="sxs-lookup"><span data-stu-id="1e340-139">Exchange Data Resiliency</span></span>](assurance-exchange-data-resiliency.md)
