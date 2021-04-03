---
title: Microsoft 365 安全事件管理：事件后活动
description: 本文概述了 Microsoft 365 中的安全事件管理后期事件活动过程。
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
ms.openlocfilehash: 4ebd31c16f8abb3eddd6ed924a045d88597aba40
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496715"
---
# <a name="microsoft-365-security-incident-management-post-incident-activity"></a><span data-ttu-id="3fbaf-103">Microsoft 365 安全事件管理：事件后活动</span><span class="sxs-lookup"><span data-stu-id="3fbaf-103">Microsoft 365 security incident management: Post-incident activity</span></span>

## <a name="postmortem"></a><span data-ttu-id="3fbaf-104">Postmortem</span><span class="sxs-lookup"><span data-stu-id="3fbaf-104">Postmortem</span></span>

<span data-ttu-id="3fbaf-105">某些安全事件（尤其是影响客户或导致数据泄露的事件）会接受完整的事件事后分析。</span><span class="sxs-lookup"><span data-stu-id="3fbaf-105">Some security incidents, especially those incidents that are customer impacting or result in a data breach, are subject to a full incident postmortem.</span></span> <span data-ttu-id="3fbaf-106">Microsoft 365 安全响应团队与参与安全事件响应的各方一起执行详细的事后调查，以：</span><span class="sxs-lookup"><span data-stu-id="3fbaf-106">The Microsoft 365 Security Response team conducts a detailed postmortem with all the parties involved in security incident response to:</span></span>

- <span data-ttu-id="3fbaf-107">记录导致事件的事件序列</span><span class="sxs-lookup"><span data-stu-id="3fbaf-107">Document the sequence of events that caused the incident</span></span>
- <span data-ttu-id="3fbaf-108">创建事件的技术摘要，该证据支持该证据包括泄露事件所涉及的 (如果已知) 。</span><span class="sxs-lookup"><span data-stu-id="3fbaf-108">Create a technical summary of the incident as supported by the evidence that includes the actors involved in the breach (if known).</span></span> <span data-ttu-id="3fbaf-109">此摘要将包括响应的执行方式和其他关键要点。</span><span class="sxs-lookup"><span data-stu-id="3fbaf-109">This summary will include how the response was executed and other key takeaways.</span></span>
- <span data-ttu-id="3fbaf-110">确定安全事件响应过程中发现的技术缺陷、过程失败、手动错误、流程缺陷和通信故障和/或任何以前未知的攻击途径。</span><span class="sxs-lookup"><span data-stu-id="3fbaf-110">Identify technical lapses, procedural failures, manual errors, process flaws, and communication glitches, and/or any previously unknown attack vectors that were identified during the security incident response.</span></span>

<span data-ttu-id="3fbaf-111">事后分析将在 Microsoft 365 工程开发周期中设置新的优先级，直接影响 Microsoft 365 服务改进、运营流程和文档。</span><span class="sxs-lookup"><span data-stu-id="3fbaf-111">The postmortem will directly influence Microsoft 365 service improvement, operational processes, and documentation by setting new priorities in the Microsoft 365 engineering development cycle.</span></span>

## <a name="documentation"></a><span data-ttu-id="3fbaf-112">文档</span><span class="sxs-lookup"><span data-stu-id="3fbaf-112">Documentation</span></span>

<span data-ttu-id="3fbaf-113">事后分析过程中的所有关键技术成果均以 Bug 或开发更改请求的形式捕获在报告和服务投资或修复中。</span><span class="sxs-lookup"><span data-stu-id="3fbaf-113">All key technical findings in the postmortem process are captured in a report and service investments or fixes in the form of bugs or development change requests.</span></span> <span data-ttu-id="3fbaf-114">这些发现将跟进相应的工程团队。</span><span class="sxs-lookup"><span data-stu-id="3fbaf-114">These findings are followed-up with the appropriate engineering teams.</span></span> <span data-ttu-id="3fbaf-115">对于进程失败和跨组织问题，Microsoft 365 安全响应团队的数据库中记录了问题，并跟进相应的组来解决这些问题。</span><span class="sxs-lookup"><span data-stu-id="3fbaf-115">For process failures and cross-organizational issues, issues are documented in the Microsoft 365 Security Response team's database and followed-up with the appropriate groups to address them.</span></span>

## <a name="process-improvement"></a><span data-ttu-id="3fbaf-116">流程改进</span><span class="sxs-lookup"><span data-stu-id="3fbaf-116">Process improvement</span></span>

<span data-ttu-id="3fbaf-117">在 Microsoft 365 中响应安全事件涉及与分布在 Microsoft 内不同组织，甚至是可能适当的外部组织（如执法机构）的多个组进行协调。</span><span class="sxs-lookup"><span data-stu-id="3fbaf-117">Responding to a security incident in Microsoft 365 involves coordination with multiple groups spread across different organizations within Microsoft, and potentially even appropriate external organizations such as law enforcement.</span></span> <span data-ttu-id="3fbaf-118">我们知道，评估每个安全事件后的响应至关重要，既满足又完整。</span><span class="sxs-lookup"><span data-stu-id="3fbaf-118">We know that it is critical to evaluate our responses after every security incident for both sufficiency and completeness.</span></span> <span data-ttu-id="3fbaf-119">对于任何已确定的改进或更改，Microsoft 365 安全响应团队会与相应的团队和利益干系人共同评估建议，并在适当的时候将它们纳入标准操作过程。</span><span class="sxs-lookup"><span data-stu-id="3fbaf-119">For any identified improvements or changes, the Microsoft 365 Security Response team evaluates the suggestions in consultation with the appropriate teams and stakeholders, and where appropriate incorporates them into standard operating procedures.</span></span> <span data-ttu-id="3fbaf-120">在安全事件响应或事后活动期间发现的所有必需更改、Bug 或服务改进都记录并跟踪在内部 Microsoft 365 工程数据库中。</span><span class="sxs-lookup"><span data-stu-id="3fbaf-120">All required changes, bugs, or service improvements identified during the security incident response or postmortem activity are logged and tracked in an internal Microsoft 365 engineering database.</span></span> <span data-ttu-id="3fbaf-121">所有潜在的 Bug 或功能都分配给相应的所有者。</span><span class="sxs-lookup"><span data-stu-id="3fbaf-121">All potential bugs or features are assigned to the appropriate owner.</span></span> <span data-ttu-id="3fbaf-122">Microsoft 365 安全响应团队会检查所有条目，直到问题得到解决。</span><span class="sxs-lookup"><span data-stu-id="3fbaf-122">The Microsoft 365 Security Response team reviews all entries until the issue is resolved.</span></span>

## <a name="related-articles"></a><span data-ttu-id="3fbaf-123">相关文章</span><span class="sxs-lookup"><span data-stu-id="3fbaf-123">Related articles</span></span>

- [<span data-ttu-id="3fbaf-124">Microsoft 365 安全事件管理</span><span class="sxs-lookup"><span data-stu-id="3fbaf-124">Microsoft 365 security incident management</span></span>](assurance-security-incident-management.md)
- [<span data-ttu-id="3fbaf-125">Microsoft 365 安全事件管理准备</span><span class="sxs-lookup"><span data-stu-id="3fbaf-125">Microsoft 365 security incident management preparation</span></span>](assurance-sim-preparation.md)
- [<span data-ttu-id="3fbaf-126">Microsoft 365 安全事件管理检测和分析</span><span class="sxs-lookup"><span data-stu-id="3fbaf-126">Microsoft 365 security incident management detection and analysis</span></span>](assurance-sim-detection-analysis.md)
- [<span data-ttu-id="3fbaf-127">Microsoft 365 安全事件管理抑制、消除和恢复</span><span class="sxs-lookup"><span data-stu-id="3fbaf-127">Microsoft 365 security incident management containment, eradication, and recovery</span></span>](assurance-sim-containment-eradication-recovery.md)
