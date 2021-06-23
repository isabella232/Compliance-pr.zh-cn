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
ms.openlocfilehash: 9af5296cce34db6362638f025f38315f2e1d7b05
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/23/2021
ms.locfileid: "53088531"
---
# <a name="architecture-overview"></a>体系结构概述

## <a name="what-is-microsoft-365"></a>什么是 Microsoft 365？

Microsoft 365由云支持、基于订阅的 Office、Windows 10、企业移动性 + 安全性 和合规性版本。 Microsoft 365客户获取 Outlook 和 Windows 等客户端，并且他们还可以从 Microsoft 代表自己托管的服务（如 Exchange Online、Microsoft Teams 和 SharePoint Online）中获益。 服务的所有组件会定期作为订阅模型的一部分进行更新，以便我们的客户拥有"常青"产品。 Microsoft 代表客户管理服务基础结构，这意味着 Microsoft 负责保护存储客户数据的基础结构。

就规模而言，我们目前使用近一百万台计算机来为Microsoft 365电源。 支持这些服务的基础结构因 Azure、Windows 和 Linux 以及多租户和专用平台中的特定于服务的硬件和虚拟化环境而有很大差异。 Microsoft 365是一家全球业务，我们的基础结构分布于世界各地的数据中心，使我们的客户能够满足数据驻留和公民要求。

简而言之，该服务非常复杂，运行规模之大，并且需要数千个 Microsoft 工程师进行构建和维护。 保护所有这些基础结构的安全是我们的首要任务。

## <a name="how-does-microsoft-365-ensure-isolation-between-customer-tenants"></a>如何Microsoft 365客户租户之间的隔离？

Microsoft 的云服务基于以下假设：所有租户都有可能危害所有其他租户。 为了正确地将租户彼此隔离，Microsoft 实施了各种隔离技术和控件。 这些控件旨在防止信息泄露或跨租户未经授权访问客户数据，并防止一个租户的操作对另一个租户的服务造成负面影响。

客户内容在逻辑上隔离Microsoft 365 Azure AD Azure Active Directory (租户) 。 Microsoft 365身份验证不仅验证用户标识，还验证用户帐户属于的租户标识，从而阻止用户访问其租户环境外部的数据。 为了补充 Azure AD 的逻辑隔离，客户内容始终在其余和传输过程中进行加密。 个别服务也可能提供附加的租户隔离层，例如SharePoint、加密的数据库中的租户数据进行联机隔离。

## <a name="how-does-microsoft-365-engineer-resilient-services-that-avoid-single-points-of-failure"></a>如何Microsoft 365能够避免单点故障的复原服务？

Microsoft 设计和构建云服务，以最大程度地提高可靠性，并最大程度地降低客户在正常运行时面临的故障和挑战带来的负面影响。 此策略从连接地理位置分散的数据中心的网络设计开始。 Microsoft 的网络体系结构包括直接互连和多个网络路径。 Microsoft 365服务利用此冗余自动路由故障周围的流量以提高服务质量。

在服务级别，Microsoft 365策略优先处理软件复原。 只要有可能，我们的服务将部署在主动/主动配置中，并自动进行服务运行状况监视，从而允许服务在无需人为干预的情况下从许多常见错误和故障中检测和恢复。 除了主动/主动配置之外，Microsoft 365服务还通过确保服务部署在单独的容错区域中来增加容错能力，以防止一个区域中的错误影响其他区域的可用性。

数据复原通过保护服务中数据的完整性和可用性来补充Microsoft 365恢复能力。 我们的服务使用本地存储冗余和地理位置冗余将客户数据的副本复制到不同的容错区域。 如果一个故障区域中的数据已损坏或丢失，可以在另一个故障区域中访问该数据，而不会丢失可用性。 自动完整性检查自动还原受多种物理或逻辑损坏影响的数据。 Microsoft 365还可以为客户提供工具，以还原客户在 Exchange Online 和 SharePoint Online 中意外删除或修改的数据。

## <a name="how-does-microsoft-365-track-dependencies-and-prevent-unauthorized-external-system-connections"></a>如何Microsoft 365依赖项并防止未经授权的外部系统连接？

Microsoft 365服务团队将关键系统组件及其依赖项标识为业务连续性管理的一部分。 此外，Microsoft 365文档并跟踪所有外部系统连接，以确保网络防火墙配置中只允许授权连接。 Microsoft 365、依赖关系和外部连接都记录在 Microsoft 365信息安全体系结构中。 信息安全体系结构和相应的数据流图将至少每年查看和更新一次，并且只要对系统进行了重大更改。

Microsoft 365验证体系结构，并自动使用基于云的工具验证是否符合我们的安全原则，并持续测试隔离和恢复能力功能。 体系结构验证可自动识别服务当前状态偏离所需状态的实例，并标记任何偏差以便进行审阅和缓解。 体系结构验证的目标是确保服务基础结构的管理功能继续正常工作。

## <a name="related-external-regulations--certifications"></a>认证的相关&法规

Microsoft 的在线服务会定期进行审核，以遵守外部法规和认证。 有关与应用程序体系结构相关的控件的验证，请参阅Microsoft 365。

| **外部审核** | **Section** | **最新报告日期** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365) ](https://compliance.microsoft.com/compliancemanager) | AC-4：信息流强制 <br> CP-9：信息系统备份 <br> PL-8：信息安全体系结构 <br> SC-7：边界保护 <br> SC-22：体系结构和设置 | 2020 年 9 月 24 日 |
| [ISO 27001/27002 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6：信息安全组织 <br> A.13.1：网络安全管理 <br> A.17.2：冗余 | 2021 年 4 月 20 日 |
| [ISO 27017 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=8d625374-4f2d-49f8-9d37-a4281ba98222&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=c0df4ce8-c77e-4183-84eb-c8688470d8b1&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.6：信息安全组织 <br> A.13.1：网络安全管理 | 2021 年 4 月 20 日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-37：租户隔离 <br> CA-49：备份策略 <br> CA-51：数据复制 | 2020 年 12 月 24 日 |
| [SOC 2 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-05：数据流图 <br> CA-37：租户隔离 <br> CA-49：备份策略 <br> CA-51：数据复制 | 2020 年 12 月 24 日 |