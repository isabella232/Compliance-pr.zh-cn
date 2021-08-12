---
title: Microsoft 365 隔离控制
description: 了解数据中的隔离Microsoft 365
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
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 2278a2475887e93733ce32b82a1d7d0b15cce91a1f1e70dbe72a6469bdd3e0b7
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "54290597"
---
# <a name="microsoft-365-isolation-controls"></a>Microsoft 365 隔离控制

Microsoft 持续致力于确保网站的多租户Microsoft 365支持企业级安全性、机密性、隐私、完整性、本地、国际和可用性[标准](https://www.microsoft.com/trust-center/compliance/compliance-overview)。 Microsoft 提供的服务规模和范围使得管理具有大量人工交互Microsoft 365非常困难且非经济。 Microsoft 365服务通过全球分布式数据中心提供，每个数据中心都经过几个需要人工接触或客户内容的任何访问的操作，实现高度自动化。 我们的员工使用自动化工具和高度安全的远程访问支持这些服务和数据中心。

Microsoft 365由多个服务组成，这些服务提供重要的业务功能并有助于实现整个Microsoft 365体验。 其中每个服务都是独立的，旨在相互集成。 Microsoft 365设计有以下原则：

- 面向服务的体系结构：以提供明确定义的业务功能的可互操作服务的形式设计和开发软件。
- [](https://www.microsoft.com/securityengineering/osa)操作安全保证：一个框架，包含通过[Microsoft](https://www.microsoft.com/sdl/default.aspx)特有的各种功能获得的知识，包括 Microsoft 安全开发生命周期[、Microsoft](https://www.microsoft.com/msrc)安全响应中心，以及网络安全威胁形势的深层意识。

Microsoft 365服务相互交互，但设计和实现，以便它们可以作为自治服务部署和运行，相互独立。 Microsoft 隔离组织的职责Microsoft 365，以减少未经授权或无意修改或滥用组织资产的机会。 Microsoft 365团队将角色定义为全面的基于角色的访问控制机制的一部分。

## <a name="tenant-isolation"></a>租户隔离

云计算的主要好处之一是同时跨多个客户共享、通用的基础结构的概念，这导致规模下降。 Microsoft 不断努力确保我们云服务的多租户体系结构支持企业级的安全性、机密性、隐私性、完整性和可用性标准。

Microsoft 云服务的设计假定所有租户都可能对所有其他租户造成危害，并且我们实施了安全措施，以防止一个租户的操作影响另一个租户的安全或服务或访问另一个租户的内容。

在多租户环境中维护租户隔离的两个主要目标是：

- 防止跨租户泄露客户内容或未经授权访问客户内容;和
- 防止一个租户的操作对另一个租户的服务造成负面影响

在整个 Microsoft 365 中实施了多种形式的保护，以防止客户危害 Microsoft 365 服务或应用程序，或获取对其他租户或 Microsoft 365 系统本身信息的未经授权的访问，包括：

- 通过基于授权和基于角色的访问控制Microsoft 365租户中的客户内容Azure Active Directory逻辑隔离。
- SharePointOnline 在存储级别提供数据隔离机制。
- Microsoft 使用严格的物理安全、背景屏蔽和多层加密策略来保护客户内容的机密性和完整性。 数据中心Microsoft 365均具有生物识别访问控制，大多数要求使用打印的指纹才能获得物理访问权限。 此外，作为招聘过程的一部分，所有美国 Microsoft 员工都需要成功完成标准背景检查。 有关在管理中用于管理访问的控件Microsoft 365，请参阅Microsoft 365[访问控制"。](assurance-administrative-access-controls-overview.md)
- Microsoft 365使用对静态和传输中的客户内容进行加密的服务器端技术，包括 BitLocker、每个文件加密、传输层安全性 (TLS) 和 Internet 协议安全性 (IPsec) 。 有关加密中加密的特定Microsoft 365，请参阅数据[加密技术Microsoft 365。](/microsoft-365/compliance/office-365-encryption-in-the-microsoft-cloud-overview)

同时，上面列出的保护提供了强大的逻辑隔离控件，提供与单独由物理隔离提供的威胁保护和缓解等效。

## <a name="resources"></a>资源

- [隔离和访问控制Azure Active Directory](/microsoft-365/enterprise/microsoft-365-isolation-in-azure-active-directory)
- [监视和测试租户边界](assurance-monitoring-and-testing.md)
- [隔离和访问控制Microsoft 365](/microsoft-365/enterprise/microsoft-365-isolation-in-microsoft-365)
