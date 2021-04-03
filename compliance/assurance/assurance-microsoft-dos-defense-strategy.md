---
title: Microsoft 365 拒绝服务防御策略
description: 本文将概述拒绝服务攻击和 DoS 攻击的 Microsoft (策略) 策略。
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
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
ms.openlocfilehash: 5776b3eb6c0b79b5f272d6e24dd8680967ca2eb4
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496955"
---
# <a name="microsoft-365-denial-of-service-defense-strategy"></a>Microsoft 365 拒绝服务防御策略

## <a name="core-principles-of-defense-against-denial-of-service-attacks"></a>防御拒绝服务攻击的核心原则

防御基于网络的拒绝服务攻击和 DoS (攻击时，) 三个核心原则：预防、检测和缓解。 抑制在检测之前发生，并且必须先进行检测，然后才能开始缓解。 如果即使是一个小的 DoS 攻击也无法得到解决，那么服务将无法在足够长的长时间内生存，无法检测到该攻击。 通过检测系统无法承受的攻击，防御者可以实施响应计划。

以下公式可帮助估计受 DoS 攻击影响的时间：

  **Maximum Capacity (in bytes/sec) / Growth Rate (in bytes/sec) = 影响 (的时间（以秒为单位)**

如果检测时间长于影响时间，则 DoS 攻击可能会成功。 如果检测时间短于影响时间，如果缓解策略成功，受攻击服务应保持联机和可访问。

因此，有两种主要的防御 DoS 攻击的策略：

- 增加容量以提高最大容量限制 (这反过来会有更多的时间来检测攻击) ;或
- 减少检测攻击的时间。

使用 Microsoft 云服务的一个安全优势是大型 Microsoft 服务如何以经济高效的方式为云客户提供强大的网络保护。 即使在大规模上，还必须在吸收、检测和缓解之间保持平衡。 为了找到此平衡，Microsoft 研究攻击速率以估计需要吸收的 Microsoft 服务量。

## <a name="denial-of-service-defense-strategy"></a>拒绝服务防御策略

Microsoft 防御基于网络的 DoS 攻击的策略是唯一的，因为我们的规模和全局占用空间。 此规模允许 Microsoft 利用对大多数其他组织不可用的策略和技术。 DoS 策略的基础是全局状态。 Microsoft 与 Internet 提供商、对等 (以及) 和私有公司合作。 此参与为 Microsoft 提供了重要的 Internet 状态，使 Microsoft 能够在较大的图面区域中吸收攻击。

随着 Microsoft 的边缘容量逐渐增加，对各个边缘的攻击的重要性已大大降低。 由于这一减少，Microsoft 已分离 DoS 防护系统的检测和缓解组件。 Microsoft 在区域数据中心部署多层检测系统，以检测接近其饱和点的攻击，同时在边缘节点维持全局缓解。 此策略可确保 Microsoft 服务可以处理多个同时攻击。

Microsoft 针对 DoS 攻击采用的最有效且成本较低的防御措施之一是减少服务攻击面。 不需要的流量会丢弃在网络边缘，而不是分析、处理和内联擦除数据。

在公用网络的接口上，Microsoft 将专用安全设备用于防火墙、网络地址转换和 IP 筛选功能。 Microsoft 还使用全局等价多路径 (ECMP) 路由。 全局 ECMP 路由是一个网络框架，可确保有多个全局路径可到达一个服务。 通过每个服务的多个路径，DoS 攻击仅限于发起攻击的区域。 其他区域应不受攻击的影响，因为最终用户将使用其他路径到达这些地区的服务。 Microsoft 还开发了内部 DoS 关联和检测系统，使用流数据、性能指标和其他信息快速检测 DoS 攻击。

为了进一步保护云服务，Microsoft 365 使用内置于 Microsoft Azure 持续监视和渗透测试流程的分布式拒绝服务 (DDoS) 防御系统。 Azure DDoS 防御系统不仅设计用于抵御外部攻击，还旨在抵御来自其他 Azure 租户的攻击。 Azure 使用标准检测和缓解技术（如 SYN Cookie、速率限制和连接限制）防止 DDoS 攻击。 为了支持我们的自动保护，跨工作负载 DoS 事件响应团队标识了各个团队的角色和职责、升级标准以及受影响团队的事件处理协议。

针对目标发起的大多数 DoS 攻击都位于开放系统互连 (OSI) 模型的 Network (L3) 和传输[](/windows-hardware/drivers/network/windows-network-architecture-and-the-osi-model) (L4) 层。 针对 L3 和 L4 层的攻击旨在用攻击流量来淹没网络接口或服务，使资源消耗过重，并拒绝响应合法流量的能力。 为了防范 L3 和 L4 攻击，Microsoft DoS 解决方案使用来自数据中心路由器的流量采样数据来保护基础结构和客户目标。 流量采样数据由网络监控服务进行分析以检测攻击。 检测到攻击时，自动防御机制将启动以缓解攻击，并确保针对一个客户的攻击流量不会为其他客户造成附属损坏或网络服务质量降低。

## <a name="application-level-defenses"></a>应用程序级防御

Microsoft 工程团队遵循 Microsoft 运营安全保证 [所](https://www.microsoft.com/SDL/OperationalSecurityAssurance) 设置的严格标准，以帮助保护客户数据。 Microsoft 的云服务专为支持高负载而特意构建，可帮助抵御应用程序级 DoS 攻击。 Microsoft 365 的扩展体系结构跨多个全球数据中心分布服务，具有区域隔离和工作负荷特定的相关工作负载限制功能。

客户管理员在服务的初始设置过程中标识的每个客户的一个或多个国家/地区决定了该客户数据的主存储位置。 客户数据根据主/备份策略在冗余数据中心之间复制。 主数据中心承载应用程序软件以及软件上运行的所有主客户数据。 备份数据中心提供自动故障转移。 如果主数据中心因任何原因停止运行，请求将重定向到备份数据中心中的软件和客户数据的副本。 在任何给定时间，客户数据可以在主数据中心或备份数据中心进行处理。 跨多个数据中心分布数据可减少受影响的表面区域，以防一个数据中心受到攻击。 此外，受影响数据中心中的服务可以快速重定向到辅助数据中心，以在攻击期间保持可用性，在缓解攻击后重定向回主数据中心。

作为针对 DoS 攻击的另一种缓解措施，个别工作负载包括用于管理资源利用率的内置功能。 例如，Exchange Online 和 SharePoint Online 中的限制机制是抵御 DoS 攻击的多层方法的一部分。
