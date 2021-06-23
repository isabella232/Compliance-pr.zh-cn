---
title: Microsoft 员工转接和离职
description: 了解 Microsoft 员工离职和离职Microsoft 365
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
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: b31dd13f4a6209712a9cc212ab3bcd9c5addf6b7
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/23/2021
ms.locfileid: "53089601"
---
# <a name="microsoft-employee-transfer-and-termination"></a><span data-ttu-id="f0464-103">Microsoft 员工转接和离职</span><span class="sxs-lookup"><span data-stu-id="f0464-103">Microsoft employee transfer and termination</span></span>

<span data-ttu-id="f0464-104">员工转移和离职是每个组织正常业务运营的一部分。</span><span class="sxs-lookup"><span data-stu-id="f0464-104">Employee transfers and terminations are a part of every organization's normal business operations.</span></span> <span data-ttu-id="f0464-105">当员工更改职位或离开公司时，必须及时撤销不适当的访问权限。</span><span class="sxs-lookup"><span data-stu-id="f0464-105">When an employee changes positions or leaves the company, it is essential to revoke inappropriate access in a timely manner.</span></span> <span data-ttu-id="f0464-106">为了推动高效的访问更改和访问吊销，Microsoft 365 使用标准化过程和自动化过程来协调人力资源信息系统 (HRIS) 与身份管理 (IDM) 系统。</span><span class="sxs-lookup"><span data-stu-id="f0464-106">To facilitate efficient access changes and access revocations, Microsoft 365 uses standardized procedures and automated processes to coordinate the Human Resources Information System (HRIS) with the Identity Management (IDM) system.</span></span> <span data-ttu-id="f0464-107">这两个系统之间的自动化协调对于维护运营一致性、Microsoft 365服务和数据、防止特权危害并降低与内部威胁相关的风险至关重要。</span><span class="sxs-lookup"><span data-stu-id="f0464-107">Automated orchestration between these two systems is essential to maintaining operational consistency, safeguarding Microsoft 365's services and data, preventing privilege creep, and reducing risks related to insider threats.</span></span>

<span data-ttu-id="f0464-108">Microsoft 365系统旨在运行，无需对工程师长期管理对生产环境的管理访问权限。</span><span class="sxs-lookup"><span data-stu-id="f0464-108">Microsoft 365 systems are designed to operate without standing administrative access to production environments for our engineers.</span></span> <span data-ttu-id="f0464-109">Microsoft 使用实时 (JIT) Just-Enough-Access (JEA) 模型为工程师提供所需的临时访问权限，以便根据需要支持他们的服务。</span><span class="sxs-lookup"><span data-stu-id="f0464-109">Microsoft uses a Just-In-Time (JIT), Just-Enough-Access (JEA) model to provide engineers with the temporary access needed to support their service when required.</span></span> <span data-ttu-id="f0464-110">若要请求并使用服务团队帐户进行 JIT 访问，工程师必须通过 IDM 工具请求和维护资格。</span><span class="sxs-lookup"><span data-stu-id="f0464-110">To request and use a service team account for JIT access, engineers must request and maintain eligibilities through the IDM tool.</span></span> <span data-ttu-id="f0464-111">当员工被转移或离职时，将自动修改其服务团队帐户和相关资格，以防止不当访问。</span><span class="sxs-lookup"><span data-stu-id="f0464-111">When employees are transferred or terminated, their service team account and related eligibilities are automatically modified to prevent inappropriate access.</span></span>

## <a name="transfer-and-reassignment"></a><span data-ttu-id="f0464-112">转移和重新分配</span><span class="sxs-lookup"><span data-stu-id="f0464-112">Transfer and reassignment</span></span>

<span data-ttu-id="f0464-113">员工转移是通过员工经理的转移交易请求启动的。</span><span class="sxs-lookup"><span data-stu-id="f0464-113">Employee transfers are initiated through a transfer transaction request by the employee's manager.</span></span> <span data-ttu-id="f0464-114">经理创建了一个工厂，并参与全球人才招聘流程。</span><span class="sxs-lookup"><span data-stu-id="f0464-114">The manager creates a requisition and engages with Global Talent Acquisition for the offer letter process.</span></span> <span data-ttu-id="f0464-115">员工接受新角色的优惠后，HR 服务将完成 HR 核心工具中的转移，从而触发 IDM 设置所有员工资格的到期日期。</span><span class="sxs-lookup"><span data-stu-id="f0464-115">Once the employee accepts the offer for the new role, HR services completes the transfer in the HR core tools, triggering IDM to set an expiration date for all the employee's eligibilities.</span></span> <span data-ttu-id="f0464-116">员工必须提交请求并收到新经理的批准，以保留其资格。</span><span class="sxs-lookup"><span data-stu-id="f0464-116">The employee must submit a request and receive approval from their new manager to retain their eligibilities.</span></span> <span data-ttu-id="f0464-117">提交请求或接收经理批准失败会导致被转移的员工资格吊销。</span><span class="sxs-lookup"><span data-stu-id="f0464-117">Failure to submit a request or receive manager approval results in the revocation of the transferred employee's eligibilities.</span></span> <span data-ttu-id="f0464-118">对于包含特定安全隐患的传输，将立即重新评估系统访问和安全组成员身份以反映其新角色。</span><span class="sxs-lookup"><span data-stu-id="f0464-118">For transfers that include specific security implications, system accesses and security group memberships are reevaluated immediately to reflect their new role.</span></span>

## <a name="termination"></a><span data-ttu-id="f0464-119">终止</span><span class="sxs-lookup"><span data-stu-id="f0464-119">Termination</span></span>

<span data-ttu-id="f0464-120">当员工离职时，Microsoft 使用明确定义的策略和过程来立即撤消对 Microsoft 系统和资源的物理和逻辑访问。</span><span class="sxs-lookup"><span data-stu-id="f0464-120">Microsoft uses clearly defined policies and procedures to promptly revoke physical and logical access to Microsoft systems and resources when an employee is terminated.</span></span> <span data-ttu-id="f0464-121">当员工发出通知时，员工的经理会向 HRIS 输入终止日期。</span><span class="sxs-lookup"><span data-stu-id="f0464-121">When an employee gives their notice, the employee's manager enters the termination date into the HRIS.</span></span> <span data-ttu-id="f0464-122">在员工最后一个工作日之后，HRIS 将员工标记为已终止，并共享信息给 IDM，这将自动删除所有服务团队帐户和资格。</span><span class="sxs-lookup"><span data-stu-id="f0464-122">Following the employee's last working day, the HRIS marks the employee as terminated and shares the information to IDM, which removes all service team accounts and eligibilities automatically.</span></span>

<span data-ttu-id="f0464-123">对于雇佣终止，HR 与员工的经理合作，以按照相应步骤终止和离职员工。</span><span class="sxs-lookup"><span data-stu-id="f0464-123">For involuntary terminations, HR works with the employee's manager to follow the appropriate steps to terminate and offboard the employee.</span></span> <span data-ttu-id="f0464-124">与自愿终止类似，终止信息连同任何必要步骤（如有效日期协调、删除访问）一起输入到 HRIS 中。</span><span class="sxs-lookup"><span data-stu-id="f0464-124">Similar to a voluntary termination, the termination information is entered into the HRIS along with any necessary steps such as effective date coordination, access removal.</span></span> <span data-ttu-id="f0464-125">和与转换角色相关的任何其他步骤。</span><span class="sxs-lookup"><span data-stu-id="f0464-125">and any other steps relative to transitioning out of role.</span></span>
