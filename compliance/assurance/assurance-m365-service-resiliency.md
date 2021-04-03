---
title: Microsoft 365 中的内置服务恢复能力
description: Microsoft 365 服务恢复的说明
author: robmazz
ms.author: robmazz
manager: laurawi
ms.reviewer: sosstah
f1.keywords:
- NOCSH
audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
- MS-Compliance
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: b97e8876f0ef69faefbeb5cf50a1891d36bf8795
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497034"
---
# <a name="built-in-service-resiliency-in-microsoft-365"></a>Microsoft 365 中的内置服务恢复能力

作为云协作提供商，Microsoft 认识到需要通过提供功能一致且深受用户喜爱的解决方案来不断赢得用户的信任。 当任何给定服务不可用时，它称为停机时间。 对于每个 Microsoft 365 服务，停机时间的定义各不相同，但是它们通常集中在用户无法使用服务基本功能的任何时间段。 例如，下面是 Microsoft 365 服务级别协议中规定的 SharePoint Online 的停机时间定义：

**“SharePoint Online 停机时间**：用户无法读取或写入其具有适当权限的 SharePoint Online 网站集的任何部分的任何时间段。”

可以在[服务级别协议](https://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=37)中找到每个服务的停机时间定义。

若要最大限度地减少计划或意外停机时间，Microsoft 365 服务的设计和操作都具有高度可用性，并通过以下四个方面来从故障中恢复：

## <a name="activeactive-design"></a>主动/主动设计

在 Microsoft 365 中，我们正致力于在主动/主动设计中构建和运行所有服务，从而增强复原能力。 此设计意味着始终存在一个服务的多个实例，这些实例可以响应用户请求，并且它们托管在地理位置分散的数据中心中。 所有用户流量都通过 Microsoft Front Door 服务进入，并自动路由到服务的最佳位置实例，并围绕任何服务故障来防止或减少对客户的影响。

## <a name="reduce-incident-scope"></a>缩小事件范围

服务事件的范围由其严重程度、持续时间和受影响的客户数量来衡量。 我们努力通过以下方式限制所有事件的范围：

- 将每个服务的多个实例彼此隔离
- 使用验证通道以受控渐进的方式部署更新，以便在部署过程的早期检测并缓解更新中可能出现的任何问题。 此设计允许根据需要对更新进行回归，并且首先在 Microsoft (内部环) 内的一个小型组中进行，然后再为较大组（如所有 140，000 名 Microsoft 员工）部署更新，如所有 140，000 名 Microsoft 员工 (ring 2) ，然后针对早期采用者圈 (ring 3) 并最终针对全局 (圈 4) 的所有客户。
- 通过自动化推动监视方面的改进。 Microsoft 365 是一项大型服务，SLA 目标运行时间较高。 在服务事件的最开始，如果必须让人参与检测和响应，那么我们的响应速度将无法满足 SLA。 自动化是快速高效地检测和响应服务事件的关键。 我们越早知道问题，就能越快地解决它。

除了 Microsoft 365 服务体系结构中内置的主动/主动功能外，这些工作还降低了服务事件期间受影响客户的严重性、持续时间和数量。  

## <a name="fault-isolation"></a>故障隔离

正如以主动/主动方式设计和操作服务，并彼此隔离，以防止一个服务中的故障影响其他服务，服务的代码库也是使用类似的称为“故障隔离”的分区原则开发的。 故障隔离措施是在代码库自身内进行的增量保护。 这些措施有助于防止某个区域中的问题级联到其他操作区域。
故障隔离措施在服务的开发和交付的多个阶段应用，包括代码开发、服务部署、负载平衡和数据库复制。

Microsoft 安全开发生命周期 (SDL) 进一步提高了恢复能力，由一系列支持安全性和合规性要求的实践组成。 SDL 指导我们的开发人员生成可复原、安全且合规的服务。 SDL 的关键元素包括整个 Microsoft 云中的代码审核、威胁建模、渗透测试和标准化的事件响应流程。

Microsoft 365 服务是高度互连的，但它们后面的系统和技术的设计方式可以限制一个服务事件的影响，防止其溢出到其他服务。 例如，影响 Exchange Online 的问题不会影响 Teams 的核心功能，或者 SharePoint Online 中的搜索功能问题不会影响用户上传或下载文件的功能。

## <a name="continuous-service-improvement"></a>持续服务改进

遇到事件时，我们会认真对待。 毕竟，我们的冗余云架构和严格的内部流程旨在保证服务的可访问性。 在事件期间，我们的监控会快速检测受影响的服务，如果租户受到影响，将立即通过各种渠道通知你。 同时，工程师按照定义良好的流程对问题进行分类，并采取必要的步骤尽快恢复正常运行。 一旦服务恢复正常运行，我们会进行事后审查，作为持续改进服务周期的一部分。 在事后审查中，我们确定事件的根本原因以及修复问题所需的内容。 然后，我们从事件情况中吸取教训，并将其应用到我们所有产品套件的设计和操作中。 通过了解这一知识，我们可以防止相同的根本原因影响其他服务和其他客户。
