---
title: Microsoft 365 监视和审核访问控制
description: 摘要：Microsoft 365 中提供的各种监视和审核访问控制的摘要。
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
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 3021ce1dd59d5d071edec22286ae9c63833f1277
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120441"
---
# <a name="monitoring-and-auditing-access-controls-in-microsoft-365"></a><span data-ttu-id="1da14-103">监视和审核 Microsoft 365 中的访问控制</span><span class="sxs-lookup"><span data-stu-id="1da14-103">Monitoring and auditing access controls in Microsoft 365</span></span>

<span data-ttu-id="1da14-104">Microsoft 对 Microsoft 365 中发生的所有委派、权限和操作执行广泛的监视和审核。</span><span class="sxs-lookup"><span data-stu-id="1da14-104">Microsoft performs extensive monitoring and auditing of all delegation, privileges, and operations that occur within Microsoft 365.</span></span> <span data-ttu-id="1da14-105">Microsoft 365 访问控制是一个基于最小特权原则构建的自动化过程，包含数据访问控件和审核：</span><span class="sxs-lookup"><span data-stu-id="1da14-105">Microsoft 365 access control is an automated process built on the principle of least privilege and incorporating data access controls and audits:</span></span>

- <span data-ttu-id="1da14-106">所有允许的访问都可跟踪到唯一用户。</span><span class="sxs-lookup"><span data-stu-id="1da14-106">All permitted access is traceable to a unique user.</span></span> <span data-ttu-id="1da14-107">管理员负责处理客户内容。</span><span class="sxs-lookup"><span data-stu-id="1da14-107">Administrators are accountable for their handling of customer content.</span></span>
- <span data-ttu-id="1da14-108">将捕获访问控制请求、审批和管理操作日志，以分析安全和恶意事件。</span><span class="sxs-lookup"><span data-stu-id="1da14-108">Access control requests, approvals, and administrative operations logs are captured for analysis of security and malicious events.</span></span>
- <span data-ttu-id="1da14-109">将基于安全组成员身份以近实时方式检查访问级别，以确保只有具有授权业务理由并满足资格要求的用户才能访问系统。</span><span class="sxs-lookup"><span data-stu-id="1da14-109">Access levels are reviewed in near real-time based on security group membership to ensure that only users who have authorized business justifications and meet the eligibility requirements have access to the systems.</span></span>
- <span data-ttu-id="1da14-110">Microsoft 365、其访问控制和支持服务（包括 Azure Active Directory 和物理数据中心）定期由独立第三方审核是否符合[ISO/IEC 27001、ISO/IEC](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27001) [27018、SOC、FedRAMP](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27018) [ (Office 365) ](https://www.microsoft.com/TrustCenter/Compliance/FedRAMP)和其他标准。 [](https://www.microsoft.com/TrustCenter/Compliance/SOC) [](https://www.microsoft.com/TrustCenter/Compliance?service=Office#Icons)</span><span class="sxs-lookup"><span data-stu-id="1da14-110">Microsoft 365, its access controls, and supporting services, including Azure Active Directory and physical datacenters, are regularly audited by independent third-parties for compliance with [ISO/IEC 27001](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27001), [ISO/IEC 27018](https://www.microsoft.com/TrustCenter/Compliance/iso-iec-27018), [SOC](https://www.microsoft.com/TrustCenter/Compliance/SOC), [FedRAMP (Office 365)](https://www.microsoft.com/TrustCenter/Compliance/FedRAMP), and other [standards](https://www.microsoft.com/TrustCenter/Compliance?service=Office#Icons).</span></span>
- <span data-ttu-id="1da14-111">Microsoft 365 工程师必须每年参加一次安全培训，查看提升的访问最佳过程，并确认 Microsoft 的安全和隐私策略，以维护对服务的权利。</span><span class="sxs-lookup"><span data-stu-id="1da14-111">Microsoft 365 engineers must take yearly security training, review elevated access best procedures, and acknowledge Microsoft's security and privacy policies to maintain entitlements to the service.</span></span>

<span data-ttu-id="1da14-112">自动警报在检测到可疑活动时触发，例如在短时间内多次登录失败。</span><span class="sxs-lookup"><span data-stu-id="1da14-112">Automated alerts trigger when suspicious activity is detected, such as multiple failed logins within a short period.</span></span> <span data-ttu-id="1da14-113">Microsoft 365 安全响应团队使用机器学习和大数据分析来审阅和分析活动，查找异常访问模式，并主动响应异常和非法活动。</span><span class="sxs-lookup"><span data-stu-id="1da14-113">The Microsoft 365 Security Response team uses machine learning and big data analysis to review and analyze activity, look for irregular access patterns, and proactively respond to anomalous and illicit activities.</span></span> <span data-ttu-id="1da14-114">Microsoft 还采用由渗透测试人员参与的专用团队，并参与定期红队和蓝队练习，以查找服务中的安全和访问控制问题。</span><span class="sxs-lookup"><span data-stu-id="1da14-114">Microsoft also employs a dedicated team of penetration testers and engages in periodic Red Team and Blue Team exercises to find security and access control issues in the service.</span></span> <span data-ttu-id="1da14-115">客户可以使用 Microsoft 365 提供的审核报告和管理活动 API 验证访问控制系统的有效性。</span><span class="sxs-lookup"><span data-stu-id="1da14-115">Customers can verify the effectiveness of access control systems by using audit reports and the management activity API provided by Microsoft 365.</span></span>

<span data-ttu-id="1da14-116">有关详细信息，请参阅 [Office 365 管理活动 API 参考](/office/office-365-management-api/office-365-management-activity-api-reference) 以及 Microsoft [365 中的审核和报告](assurance-auditing-and-reporting-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="1da14-116">For more information, see [Office 365 Management Activity API reference](/office/office-365-management-api/office-365-management-activity-api-reference) and [Auditing and reporting in Microsoft 365](assurance-auditing-and-reporting-overview.md).</span></span>
