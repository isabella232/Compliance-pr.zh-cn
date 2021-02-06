---
title: 保护 Microsoft 365 云服务免受拒绝服务攻击
description: 本文将了解 Microsoft 如何防御云服务免受拒绝服务 (DoS) 攻击。
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
ms.openlocfilehash: e632c1524d5cc8c21aec9dab3d95d285a3b8801e
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120571"
---
# <a name="defending-microsoft-365-cloud-services-against-denial-of-service-attacks"></a>保护 Microsoft 365 云服务免受拒绝服务攻击

Microsoft 数据中心受深度防御安全保护，包括外围围栏、摄像机、安全人员和使用生物识别、智能卡和多重身份验证的安全入口。 深度防御安全在设施的每个区域以及每个物理服务器单元中继续进行。 [Microsoft 云基础结构和运营组](https://www.microsoft.com/cloud-platform/global-datacenters)为云服务提供核心基础结构和基础技术。 我们的数据中心符合物理安全和可靠性行业标准，由 Microsoft 运营人员进行管理、监视和管理。

为了进一步保护云服务，Microsoft 提供了 DDoS 防御系统，该系统是 Microsoft Azure 持续监视和渗透测试过程的一部分。 Azure DDoS 防御系统不仅旨在抵御来自外部的攻击，还抵御来自其他 Azure 租户的攻击。 Azure 使用标准检测和缓解技术（如 SYN Cookie、速率限制和连接限制）防止 DDoS 攻击。

Microsoft 云服务受到来自多个来源的攻击威胁。 为了缓解和抵御各种 DoS 威胁，已制定和实施高度可扩展且动态的基于 Azure 的威胁检测和缓解系统，其主要目标是保护底层基础结构免受 DoS 攻击并帮助防止云服务客户的服务中断。 Azure DoS 缓解系统可保护入站、出站和地区到区域流量。

大多数 DoS 攻击针对开放系统互连 (OSI) 模型的 Network (L3) 和传输 ([](/windows-hardware/drivers/network/windows-network-architecture-and-the-osi-model) L4) 层的目标。 针对 L3 和 L4 层的攻击旨在通过攻击流量来淹没网络接口或服务，使资源不足，并拒绝对合法流量做出响应。 具体而言，L3 和 L4 攻击会尝试使网络链接、设备或服务的容量饱和或使支持应用程序的服务器或虚拟机的 CPU 负载过重。

为了防范 L3 和 L4 攻击，Microsoft 已设计、开发并部署了一个解决方案，专门用于通过保护这些层来保护受到攻击的基础结构和客户目标。 保护基础结构可确保针对一个客户的攻击流量不会给其他客户造成附带损坏或降低网络服务质量。 该解决方案使用来自数据中心路由器的流量采样数据。 网络监控服务分析此数据以检测攻击。 检测到攻击时，自动防御机制将启动。

## <a name="application-level-defenses"></a>Application-Level防御
Microsoft 工程团队遵循 [Microsoft](https://www.microsoft.com/SDL/OperationalSecurityAssurance) 运营安全保证所设置的严格标准，以帮助保护客户数据。 Microsoft 的云服务是有意构建的，以支持非常高的负载，以及保护和缓解应用程序级 DoS 攻击。 我们已实现扩展体系结构，其中服务分布在多个全球数据中心，其中某些工作负载具有区域隔离和限制功能。

客户管理员在服务的初始设置过程中标识的每个客户的国家/地区或区域决定了该客户数据的主存储位置。 客户数据根据主/备份策略在冗余数据中心之间复制。 主数据中心托管应用程序软件以及软件上运行的所有主客户数据。 备份数据中心提供自动故障转移。 如果主数据中心因任何原因停止工作，请求将重定向到备份数据中心中的软件和客户数据的副本。 在任何给定时间，客户数据可以在主数据中心或备份数据中心进行处理。 如果一个数据中心受到攻击，跨多个数据中心分布数据可减少受影响的表面区域。 此外，受影响数据中心中的服务可以作为恢复机制之一快速重定向到辅助数据中心，反之亦然 (在还原服务后重定向回主数据中心) 。

单个工作负载包括用于管理资源利用率的内置功能。 例如，Exchange Online 和 SharePoint Online 中的限制机制是抵御 DoS 攻击的多层方法的一部分。 Exchange Online 用户限制基于最终用户使用的资源级别，无论资源位于 Active Directory、Exchange Online 信息存储还是其他地方。 预算分配给每个客户端，以限制用户消耗的资源。 用户活动和系统组件的 Exchange Online 限制基于 [工作负载管理](https://technet.microsoft.com/library/jj150503(v=exchg.150).aspx)。 Exchange Online 工作负载是一种 Exchange Online 功能、协议或服务，已明确定义用于 Exchange Online 系统资源管理。 每个 Exchange Online 工作负载都需要系统资源（如 CPU、邮箱数据库操作或 Active Directory 请求）来执行用户请求或后台工作。 Exchange Online 工作负载的示例包括 Outlook 网页版、Exchange ActiveSync、邮箱迁移和邮箱助理。 租户管理员可以使用 Exchange 命令行管理程序管理用户的 Exchange 工作负载管理限制设置。 Exchange Online 中已实施各种形式的限制，包括 PowerShell、Exchange Web 服务、POP 和 IMAP、Exchange ActiveSync、移动设备连接、收件人等。 虽然本地 Exchange 部署的管理员可以配置限制策略，但管理员无法为 Exchange Online 配置限制策略。

SharePoint Online 中最常见的限制触发器是客户端对象模型 (CSOM) 代码，该代码以太高的频率执行太多操作。 使用 CSOM，可以使用单个请求执行许多操作，这可能会超出使用限制并引起每用户限制。

无论可能会导致限制的活动如何，当用户超过使用限制时，SharePoint Online 都会限制来自该用户帐户的任何进一步请求（通常在短时间内）。 当用户限制生效时，该用户执行的所有操作将受到限制，直到限制过期，根据以下条件：
- 对于用户直接在浏览器中执行的请求，SharePoint Online 重定向到限制信息页，请求将失败。
- 对于所有其他请求（包括 CSOM 调用），SharePoint Online 返回 HTTP 状态代码 429 ("请求过多") 失败。

如果有问题的进程继续超过使用限制，SharePoint Online 可能会完全阻止该进程，并返回 HTTP 状态代码 503 ("服务不可用") 。

## <a name="vulnerability-and-penetration-testing"></a>漏洞和渗透测试
Microsoft 使用[](https://www.microsoft.com/trustcenter/security/threatmanagement)许多安全技术和做法来保护其云[](https://blogs.technet.microsoft.com/hybridcloud/2015/05/05/protecting-your-datacenter-and-cloud-from-emerging-threats/)基础结构和本地网络免受现代、复杂的威胁，包括对云服务、虚拟机 (VM) 和其他系统使用反恶意软件组件和服务。 高级威胁分析，用于监视网络、系统和用户的正常使用模式，并采用机器学习来标记任何不正常和常规渗透测试的行为。

除了执行自己的渗透测试并为客户提供 [Microsoft 云](https://technet.microsoft.com/mt784683)统一渗透测试计划外，我们还与定期对云服务执行漏洞评估和渗透测试的第三方安全专业人员合作。 我们会从服务信任和服务保障门户下载来自这些第三方漏洞评估[的报告](https://aka.ms/ServiceAssurance)。 [](https://aka.ms/STP)
