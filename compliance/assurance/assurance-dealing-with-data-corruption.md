---
title: Microsoft 365 处理数据损坏
description: 本文介绍了 Microsoft 365 中的数据损坏，以及 Microsoft 为阻止和恢复数据而做出的工作。
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
ms.openlocfilehash: 9e9f0951f7e349cc70bc96bb6a2d62275848cf04
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497595"
---
# <a name="dealing-with-data-corruption-in-microsoft-365"></a><span data-ttu-id="804cb-103">在 Microsoft 365 中处理数据损坏</span><span class="sxs-lookup"><span data-stu-id="804cb-103">Dealing with data corruption in Microsoft 365</span></span>

<span data-ttu-id="804cb-104">在具有大量数据和独立系统时，运行大规模云服务的一个难题是如何处理数据损坏。</span><span class="sxs-lookup"><span data-stu-id="804cb-104">One of the challenging aspects of running a large-scale cloud service is how to handle data corruption, given the large volume of data and independent systems.</span></span> <span data-ttu-id="804cb-105">数据损坏可能是由：</span><span class="sxs-lookup"><span data-stu-id="804cb-105">Data corruption can be caused by:</span></span>

- <span data-ttu-id="804cb-106">应用程序或基础结构错误，损坏部分或所有应用程序状态</span><span class="sxs-lookup"><span data-stu-id="804cb-106">Application or infrastructure bugs, corrupting some or all of the application state</span></span>
- <span data-ttu-id="804cb-107">导致数据丢失或无法读取数据的硬件问题</span><span class="sxs-lookup"><span data-stu-id="804cb-107">Hardware issues that result in lost data or an inability to read data</span></span>
- <span data-ttu-id="804cb-108">人为操作错误</span><span class="sxs-lookup"><span data-stu-id="804cb-108">Human operational errors</span></span>
- <span data-ttu-id="804cb-109">恶意黑客和解除攻击的员工</span><span class="sxs-lookup"><span data-stu-id="804cb-109">Malicious hackers and disgruntled employees</span></span>
- <span data-ttu-id="804cb-110">导致数据部分丢失的外部服务中的事件</span><span class="sxs-lookup"><span data-stu-id="804cb-110">Incidents in external services that result in some loss of data</span></span>

<span data-ttu-id="804cb-111">由于数据完整性的复原能力更大意味着数据损坏事件更少，因此 Microsoft 内置了 Microsoft 365 保护机制以防止发生损坏，以及能够让我们在出现损坏时恢复数据的系统和流程。</span><span class="sxs-lookup"><span data-stu-id="804cb-111">Because greater resiliency in data integrity means fewer data corruption incidents, Microsoft has built into Microsoft 365 protection mechanisms to prevent corruption from happening, as well as systems and processes that enable us to recover data if it does.</span></span> <span data-ttu-id="804cb-112">检查和过程存在于工程发布过程的各个阶段，以提高防止数据损坏的复原能力，包括：</span><span class="sxs-lookup"><span data-stu-id="804cb-112">Checks and processes exist within the various stages of the engineering release process to increase resiliency against data corruption, including:</span></span>

- <span data-ttu-id="804cb-113">系统设计</span><span class="sxs-lookup"><span data-stu-id="804cb-113">System Design</span></span>
- <span data-ttu-id="804cb-114">代码组织和结构</span><span class="sxs-lookup"><span data-stu-id="804cb-114">Code organization and structure</span></span>
- <span data-ttu-id="804cb-115">代码审阅</span><span class="sxs-lookup"><span data-stu-id="804cb-115">Code review</span></span>
- <span data-ttu-id="804cb-116">单元测试、集成测试和系统测试</span><span class="sxs-lookup"><span data-stu-id="804cb-116">Unit tests, integration tests, and system tests</span></span>
- <span data-ttu-id="804cb-117">旅行线测试/入口</span><span class="sxs-lookup"><span data-stu-id="804cb-117">Trip wires tests/gates</span></span>

<span data-ttu-id="804cb-118">在 Microsoft 365 生产环境中，数据中心之间的对等复制可确保始终存在任何数据的多个实时副本。</span><span class="sxs-lookup"><span data-stu-id="804cb-118">Within Microsoft 365 production environments, peer replication between datacenters ensures that there are always multiple live copies of any data.</span></span> <span data-ttu-id="804cb-119">标准映像和脚本用于恢复丢失的服务器，复制的数据用于还原客户数据。</span><span class="sxs-lookup"><span data-stu-id="804cb-119">Standard images and scripts are used to recover lost servers, and replicated data is used to restore customer data.</span></span> <span data-ttu-id="804cb-120">由于内置了数据复原检查和过程，Microsoft 仅保留 Microsoft 365 信息系统文档 (包括与安全相关的文档) 的备份，同时使用 SharePoint Online 中的内置复制和内部代码存储库工具 Source Repository。</span><span class="sxs-lookup"><span data-stu-id="804cb-120">Because of the built-in data resiliency checks and processes, Microsoft maintains backups only of Microsoft 365 information system documentation (including security-related documentation), using built-in replication in SharePoint Online and our internal code repository tool, Source Depot.</span></span> <span data-ttu-id="804cb-121">系统文档存储在 SharePoint Online 中，Source 则包含系统和应用程序映像。</span><span class="sxs-lookup"><span data-stu-id="804cb-121">System documentation is stored in SharePoint Online, and Source Depot contains system and application images.</span></span> <span data-ttu-id="804cb-122">SharePoint Online 和 Source 则使用版本控制，并且几乎可以实时复制。</span><span class="sxs-lookup"><span data-stu-id="804cb-122">Both SharePoint Online and Source Depot use versioning and are replicated in near real time.</span></span>
