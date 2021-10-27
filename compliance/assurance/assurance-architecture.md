---
title: 体系结构概述
description: 了解 Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
ms.localizationpriority: medium
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 513fe8b9f9a4ed5db71606704738cb46a6af8ed1
ms.sourcegitcommit: 1f30616328d7deb04e41dcbd44a330ea937fe94f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/26/2021
ms.locfileid: "60582665"
---
# <a name="architecture-overview"></a>体系结构概述

## <a name="what-are-microsoft-online-services"></a>什么是 Microsoft 联机服务？

Microsoft 在线服务是指 Microsoft 提供的基于云的服务，其中包括 Azure、Dynamics 365 和 Microsoft 365。  每项服务都提供独特的解决方案以满足常见的业务运营和生产力需求，为世界各地的客户提供服务，范围从小型企业到大型企业和政府。 由 Microsoft 独立管理的网络基础结构连接的全球分布式数据中心充当支持在线服务的中枢，提供在几乎每一种情况下保持可用性的能力，并扩展为大规模全球需求。

所有 Microsoft 联机服务具有相同的目标，即保护他们管理的服务基础结构及其客户数据，但每个联机服务由单独的业务部门运营。 在许多情况下，安全控制在所有服务中以相同方式实现，但在某些情况下，它们采用不同方法履行客户承诺和合规义务。

## <a name="what-is-azure"></a>什么是 Azure？

Microsoft Azure是一个云计算平台，用于通过 Microsoft 和第三方托管数据中心的全球网络生成、部署和管理应用程序。 它支持平台即服务 (PaaS) 和基础结构即服务 (IaaS) 云服务模型，并启用将云服务与客户本地资源集成在一起的混合解决方案。 Microsoft Azure支持跨各种产品和服务、地理位置和行业的许多客户、合作伙伴和政府组织。 Microsoft Azure旨在满足其安全性、机密性和合规性要求。

## <a name="what-is-dynamics-365"></a>什么是 Dynamics 365？

Dynamics 365 是一个联机业务应用程序套件，将客户关系管理 (CRM) 功能及其扩展与 Enterprise 资源规划 (ERP) 功能集成。 这些端到端业务应用程序帮助客户将关系转变为收益、赢得客户并加快业务增长。 Dynamics 365 是一款基于 Azure 基础结构构建的软件即服务 (SaaS) 套件，并通过全球分布式数据中心提供给世界各地的客户。

## <a name="what-is-microsoft-365"></a>什么是 Microsoft 365？

Microsoft 365支持云的、基于订阅的 Office、Windows 10、企业移动性 + 安全性 和合规性版本。 Microsoft 365客户获取 Outlook 和 Windows 等客户端，并且他们还可以从 Microsoft 代表自己托管的服务（如 Exchange Online、Microsoft Teams 和 SharePoint Online）中获益。 服务的所有组件会定期作为订阅模型的一部分进行更新，以便我们的客户拥有"常青"产品。 Microsoft 代表客户管理服务基础结构，这意味着 Microsoft 负责保护存储客户数据的基础结构。

就规模而言，Microsoft 目前使用近一百万台计算机来为Microsoft 365电源。 为这些服务提供电源的基础结构因 Azure、Windows 和 Linux 以及多租户和专用平台中的特定于服务的硬件和虚拟化环境而有很大差异。 Microsoft 365 的业务范围遍及全球，我们的基础结构分布在世界各地的数据中心，使我们的客户能够满足数据驻留和主权要求。

## <a name="how-do-microsoft-online-services-ensure-isolation-between-customer-tenants"></a>Microsoft 联机服务如何确保客户租户之间的隔离？

Microsoft 的云服务基于以下假设：所有租户都有可能危害所有其他租户。 为了正确地将租户彼此隔离，Microsoft 实施了各种隔离技术和控件。 这些控件旨在防止信息泄露或跨租户未经授权访问客户数据，并防止一个租户的操作对另一个租户的服务造成负面影响。

客户内容在逻辑上隔离在租户内，使用Azure Active Directory (Azure AD) 。 Microsoft 联机服务中的用户身份验证不仅验证用户标识，还验证用户帐户包含的租户标识，从而阻止用户访问租户环境外部的数据。 为了补充客户内容的逻辑Azure AD，客户内容始终在处于其余状态和在传输过程中进行加密。 个别服务也可能提供附加的租户隔离层，例如SharePoint、加密的数据库中的租户数据进行联机隔离。

## <a name="how-do-microsoft-online-services-engineer-resilient-services-that-avoid-single-points-of-failure"></a>Microsoft 联机服务如何设计避免单点故障的复原服务？

Microsoft 设计和构建云服务，以最大程度地提高可靠性，并最大程度地降低客户在正常运行时面临的故障和挑战带来的负面影响。 此策略从连接地理位置分散的数据中心的网络设计开始。 Microsoft 的网络体系结构包括直接互连和多个网络路径。 Microsoft 联机服务使用此冗余自动路由故障周围的流量，以提高服务质量。

只要有可能，Microsoft 联机服务就部署在主动/主动配置中，并自动进行服务运行状况监视，使该服务可以检测和恢复许多常见故障，而无需人为干预。 除了主动/主动配置之外，Microsoft 联机服务还通过确保服务部署在单独的错误区域中来增加容错能力，以防止一个区域中的错误影响其他区域的可用性。

数据复原通过保护 Microsoft 联机服务中数据的完整性和可用性来补充服务恢复能力。 我们的服务使用本地存储冗余和地理位置冗余将客户数据的副本复制到不同的容错区域。 如果数据在一个故障区损坏或丢失，可以在另一个故障区访问，而不会损失可用性。 自动完整性检查自动还原受多种物理或逻辑损坏影响的数据。 Microsoft 还为客户提供了一些工具，用于还原客户在服务（如 Exchange Online 和 SharePoint Online）中意外删除或修改的数据。

## <a name="how-do-microsoft-online-services-track-dependencies-and-prevent-unauthorized-external-system-connections"></a>Microsoft 联机服务如何跟踪依赖项并防止未经授权的外部系统连接？

Microsoft 联机服务团队将关键系统组件及其依赖项标识为业务连续性管理的一部分。 此外，Microsoft 还记录并跟踪所有外部系统连接，以确保网络防火墙配置中只允许授权连接。 Microsoft 联机服务系统、依赖项和外部连接记录在 Microsoft 联机服务的信息安全体系结构中。 信息安全体系结构和相应的数据流图将至少每年查看和更新一次，并且只要对系统进行了重大更改。

定期自动验证 Microsoft 在线服务体系结构，并自动使用基于云的工具验证是否符合我们的安全原则，并持续测试隔离和恢复能力功能。 体系结构验证可自动标识服务当前状态偏离所需状态的实例，并标记任何偏差以便进行审阅和缓解。 体系结构验证的目标是确保服务基础结构的管理功能继续正常工作。

## <a name="related-external-regulations--certifications"></a>认证的相关&法规

Microsoft 的在线服务会定期进行审核，以遵守外部法规和认证。 有关与体系结构相关的控件的验证，请参阅下表。

### <a name="azure-and-dynamics-365"></a>Azure 和 Dynamics 365

| **外部审核** | **Section** | **最新报告日期** |
|:--------------------|:------------|:-----------------------|
| [ISO 27001/27002](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=00af6c3e-7f3e-4e0d-8b0e-79f45ef2cef1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7af5304-3a31-40e6-9abb-e26352305d41&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6：信息安全组织 <br> A.13.1：网络安全管理 <br> A.17.2：冗余 | 2020 年 12 月 2 日 |
| [ISO 27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=e9116047-f327-430c-a83f-166b7e561ad6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a3bca0ac-867d-4204-b66b-13665f5f1e8d&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=25718a8a-f34d-41e1-a95a-c49246508787&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6：信息安全组织 <br> A.13.1：网络安全管理 <br> A.17.2：冗余 | 2020 年 12 月 2 日 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | BC-1：业务连续性计划 <br> BC-3：BCDR 过程 <br> BC-4：BCDR 测试 <br> BC-5：业务连续性风险评估 <br> BC-6：第三方业务连续性 <br> BC-7：数据中心业务连续性过程 <br> BC-8：数据中心业务连续性测试 <br> BC-9：数据中心复原评估 <br>  DS-6：关键组件的冗余 <br> DS-7：复制客户数据 <br> DS-14：还原客户服务 <br> DS-16：客户数据分离 | 2021 年 3 月 31 日 |

### <a name="office-365"></a>Office 365

| **外部审核** | **Section** | **最新报告日期** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | AC-4：信息流强制 <br> CP-9：信息系统备份 <br> PL-8：信息安全体系结构 <br> SC-7：边界保护 <br> SC-22：体系结构和设置 | 2020 年 9 月 24 日 |
| [ISO 27001/27002/27017](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6：信息安全组织 <br> A.13.1：网络安全管理 <br> A.17.2：冗余 | 2021 年 4 月 20 日 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-37：租户隔离 <br> CA-49：备份策略 <br> CA-51：数据复制 | 2020 年 12 月 24 日 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-05：数据流图 <br> CA-37：租户隔离 <br> CA-49：备份策略 <br> CA-51：数据复制 | 2020 年 12 月 24 日 |