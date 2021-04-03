---
title: Microsoft 365 Yammer 企业访问控制
description: 本文包含有关生产环境中的 Yammer 企业访问控制的简短摘要。
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
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: df345d922bbd0c9106cf0714377803a9c0870d82
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497355"
---
# <a name="yammer-enterprise-access-controls"></a><span data-ttu-id="1fdc6-103">Yammer 企业访问控制</span><span class="sxs-lookup"><span data-stu-id="1fdc6-103">Yammer enterprise access controls</span></span> 

<span data-ttu-id="1fdc6-104">对 Yammer 生产环境的物理和逻辑访问仅限于一小组人员 (基础结构和操作) 。</span><span class="sxs-lookup"><span data-stu-id="1fdc6-104">Physical and logical access to the Yammer production environment is restricted to a small set of people (infrastructure and operations).</span></span> <span data-ttu-id="1fdc6-105">与其他 Microsoft 365 工程师一样，Yammer 工程师对客户数据具有零长期访问权限。</span><span class="sxs-lookup"><span data-stu-id="1fdc6-105">As with other Microsoft 365 engineers, Yammer engineers have zero standing access to customer data.</span></span> <span data-ttu-id="1fdc6-106">必须使用基于审批的实时访问控制系统（类似于具有有限数量的审批者锁箱）请求访问。</span><span class="sxs-lookup"><span data-stu-id="1fdc6-106">Access must be requested using an approval-based just-in-time access control system similar to Lockbox with a limited number of approvers.</span></span> <span data-ttu-id="1fdc6-107">审批者验证请求 (例如，他们根据需求、业务案例、时间等验证请求是否合法) 然后批准或拒绝请求。</span><span class="sxs-lookup"><span data-stu-id="1fdc6-107">Approvers verify the request (for example, they verify whether the request is legitimate based on need, business case, time, etc.), and then approve or deny the request.</span></span> <span data-ttu-id="1fdc6-108">如果请求得到批准，则针对定义的有限时间授予 JIT 访问权限。</span><span class="sxs-lookup"><span data-stu-id="1fdc6-108">If the request is approved, JIT access is granted for a defined and limited time.</span></span> <span data-ttu-id="1fdc6-109">超过访问时间后，访问将自动过期。</span><span class="sxs-lookup"><span data-stu-id="1fdc6-109">After access time is exceeded, the access automatically expires.</span></span>

<span data-ttu-id="1fdc6-110">与其他 Microsoft 365 服务一样，对 Yammer 生产环境的所有访问都使用多重身份验证。</span><span class="sxs-lookup"><span data-stu-id="1fdc6-110">As with other Microsoft 365 services, all access to the Yammer production environment uses multi-factor authentication.</span></span> <span data-ttu-id="1fdc6-111">所有访问和命令历史记录都归用户所有，由 Yammer 安全团队定期记录并查看。</span><span class="sxs-lookup"><span data-stu-id="1fdc6-111">All access and command history is attributed to a user, and logged and reviewed regularly by the Yammer security team.</span></span>

<span data-ttu-id="1fdc6-112">有关 Yammer 管理和管理详细信息，请参阅 [Yammer 管理员帮助](/yammer/yammer-landing-page)。</span><span class="sxs-lookup"><span data-stu-id="1fdc6-112">For more information about Yammer administration and management, see [Yammer admin help](/yammer/yammer-landing-page).</span></span>