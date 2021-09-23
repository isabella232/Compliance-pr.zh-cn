---
title: Microsoft 拒绝服务防御策略
description: 本文将概述拒绝服务攻击和 DoS 攻击的 Microsoft (策略) 策略。
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
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
ms.openlocfilehash: e1613765d3ffb7b43b80d07823fe8aef45719b70
ms.sourcegitcommit: cb0b058800d3a8f04921066b4c59fb427eb9c268
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/23/2021
ms.locfileid: "59486189"
---
# <a name="microsoft-denial-of-service-defense-strategy"></a>Microsoft 拒绝服务防御策略

## <a name="denial-of-service-defense-strategy"></a>拒绝服务防御策略

Microsoft 防御基于网络的分布式拒绝服务 (DDoS) 攻击的策略是唯一的，因为全局占用空间很大，因此 Microsoft 可以利用大多数其他组织都不可用的策略和技术。 此外，Microsoft 为广泛的威胁智能网络（包括 Microsoft 合作伙伴和更广泛的 Internet 安全社区）聚合的集体知识做贡献和学习。 此智能与从联机服务和 Microsoft 的全球客户群收集的信息一起持续改进 Microsoft 的 DDoS 防御系统，以保护所有 Microsoft 联机服务的资产。

Microsoft DDoS 策略的基础是全局状态。 Microsoft 与 Internet 提供商、对等 (以及) 和私有公司合作。 此服务活动为 Microsoft 提供了重要的 Internet 状态，使 Microsoft 能够在较大的图面区域中吸收攻击

随着 Microsoft 的边缘容量逐渐增加，对各个边缘的攻击的重要性已大大降低。 由于这一减少，Microsoft 已分离其 DDoS 防护系统的检测和缓解组件。 Microsoft 在区域数据中心部署多层检测系统，以检测接近其饱和点的攻击，同时在边缘节点维持全局缓解。 此策略可确保Microsoft 服务可以处理多个同时攻击。

Microsoft 用于防御 DDoS 攻击的最有效且成本较低的防御之一是减少服务攻击面。 不需要的流量会丢弃在网络边缘，而不是分析、处理和内联擦除数据。

在公用网络的接口上，Microsoft 将专用安全设备用于防火墙、网络地址转换和 IP 筛选功能。 Microsoft 还使用全局等价多路径 (ECMP) 路由。 全局 ECMP 路由是一个网络框架，可确保有多个全局路径可到达一个服务。 通过每个服务的多个路径，DDoS 攻击仅限于发起攻击的区域。 其他区域应不受攻击的影响，因为最终用户将使用其他路径到达这些地区的服务。 Microsoft 还开发了内部 DDoS 关联和检测系统，这些系统使用流数据、性能指标和其他信息来快速检测 DDoS 攻击。

为了进一步保护云服务，Microsoft 使用 Azure DDoS Protection，这是一个内置于 Microsoft Azure 持续监视和渗透测试流程的 DDoS 防御系统。 Azure DDoS Protection 不仅设计用于抵御外部攻击，还旨在抵御来自其他 Azure 租户的攻击。 Azure 使用标准检测和缓解技术（如 SYN Cookie、速率限制和连接限制）防止 DDoS 攻击。 为了支持自动保护，跨工作负载 DDoS 事件响应团队标识了各个团队的角色和职责、升级标准以及受影响团队的事件处理协议。

针对目标发起的大多数 DDoS 攻击都位于开放系统互连 (OSI) 模型的 Network (L3) 和 Transport [](/windows-hardware/drivers/network/windows-network-architecture-and-the-osi-model) (L4) 层。 针对 L3 和 L4 层的攻击旨在用攻击流量来淹没网络接口或服务，使资源消耗过重，并拒绝响应合法流量的能力。 为了防范 L3 和 L4 攻击，Microsoft 的 DDoS 解决方案使用来自数据中心路由器的流量采样数据来保护基础结构和客户目标。 流量采样数据由网络监控服务进行分析以检测攻击。 检测到攻击时，自动防御机制将启动以缓解攻击，并确保针对一个客户的攻击流量不会给其他客户造成附属损坏或网络服务质量降低。

Microsoft 还对 DDoS 防御采取冒犯性方法。 Botnet 是执行 DDoS 攻击以攻击并维护匿名攻击的常见命令和控制源。 Microsoft DigitalIng Unit (DCU) 专注于识别、调查和中断恶意软件分发和通信基础结构，以减少机器人网络的规模和影响。

## <a name="application-level-defenses"></a>应用程序级防御

Microsoft 工程团队遵循 Microsoft 运营安全保证 [所](https://www.microsoft.com/SDL/OperationalSecurityAssurance) 设置的严格标准，以帮助保护客户数据。 Microsoft 的云服务专为支持高负载而特意构建，可帮助抵御应用程序级 DDoS 攻击。 Microsoft 的扩展体系结构跨多个全球数据中心分布服务，具有区域隔离和工作负荷特定的相关工作负载限制功能。

客户管理员在服务的初始配置过程中标识的每个客户的一个或多个国家/地区决定了该客户数据的主存储位置。 客户数据根据主/备份策略在冗余数据中心之间复制。 主数据中心承载应用程序软件以及软件上运行的所有主客户数据。 备份数据中心提供自动故障转移。 如果主数据中心因任何原因停止运行，请求将重定向到备份数据中心中的软件和客户数据的副本。 在任何给定时间，客户数据可以在主数据中心或备份数据中心进行处理。 跨多个数据中心分布数据可减少受影响的表面区域，以防一个数据中心受到攻击。 此外，受影响数据中心中的服务可以快速重定向到辅助数据中心，以在攻击期间保持可用性，在攻击得到缓解后重定向回主数据中心。

作为抵御 DDoS 攻击的另一种缓解措施，各个工作负载包括用于管理资源利用率的内置功能。 例如，Exchange Online 和 SharePoint Online 中的限制机制是抵御 DDoS 攻击的多层方法的一部分。

Azure SQL 数据库网关服务具有一层额外的安全保护，该服务称为 DoSGuard，可基于 IP 地址跟踪失败的登录尝试。 如果达到来自同一 IP 的登录失败尝试的阈值，DoSGuard 将阻止该地址的预定时间。

## <a name="resources"></a>资源

- [Azure DDoS Protection Standard 概述](/azure/ddos-protection/ddos-protection-overview)
- [Azure DDoS Protection Standard 基本最佳做法](/azure/ddos-protection/fundamental-best-practices)
- [DDoS 响应策略的组成部分](/azure/ddos-protection/ddos-response-strategy)
