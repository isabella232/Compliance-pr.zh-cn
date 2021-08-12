---
title: Microsoft 365 中的数据韧性
description: 本文将了解数据恢复能力的设计以及数据恢复在 Microsoft 365。
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
hideEdit: true
ms.openlocfilehash: a0745cda440b2262f4b09764e71514aeab946a6e8e0adcd4cdbccaffd14c5fe3
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "54291330"
---
# <a name="data-resiliency-in-microsoft-365"></a>数据恢复能力Microsoft 365

鉴于云计算的复杂性质，Microsoft 请注意，问题不是何时会出错。 我们设计的云服务可最大限度地提高可靠性，并最大限度地减少出现问题时对客户的负面影响。 我们已超越依赖复杂物理基础结构的传统策略，并且已经将冗余直接内置到云服务中。 我们结合使用不太复杂的物理基础结构和更具智能性的软件，将数据复原构建到我们的服务中，并为客户提供高可用性。

## <a name="resiliency-and-recoverability-are-built-in"></a>复原和可恢复性内置

在复原和恢复中构建时，首先假定基础基础结构和流程将在某些时候失败：硬件 (基础结构) 将失败，用户会出错，并且软件将存在 Bug。 虽然说软件开发人员在云之前没有考虑这些问题是不正确的，但是，在典型的 IT 实施中如何处理这些问题与在云之前有所不同：

- 首先，硬件和基础结构保护十分重要。 这种结构意味着使具有 99.99% 可靠性的数据中心需要大量电源和网络冗余，并且使用基于硬件的群集、双电源、双网络接口等实现服务器。
- 第二，进程至关重要。 运营团队维护了严格的过程，使用了更改窗口，并且通常会存在大量的项目管理开销。
- 第三，部署以淡紫色的速度进行。 在未拥有源的情况下部署代码意味着等待修补程序发布，主要版本涉及硬件更换和大量资金推出。 此外，更正问题的唯一方法就是回滚。 因此，大多数 IT 组织仅部署主要版本，以避免保持最新状态的工作。
- 最后，已部署系统的规模和相互连接的级别以往比现在要小得多。

如今，客户期望 Microsoft 持续创新而不会损害质量，这是 Microsoft 服务和软件构建时牢记复原性和可恢复性的原因之一。

## <a name="microsoft-365-data-resiliency-principles"></a>Microsoft 365数据复原原则

复原是指基于云的服务能够抵御某些类型的故障，但从客户的角度来看，该服务仍可以完全正常运行。 数据恢复能力意味着无论内部发生什么Microsoft 365，关键客户数据将保持不变且不受影响。 为此，Microsoft 365服务围绕五个特定复原原则进行设计：

- 存在关键和非关键数据。 非关键 (例如，是否读取消息) 在极少数失败情况下可以丢弃。 关键 (例如，应以极端成本) 电子邮件等客户数据。 作为设计目标，传递的邮件始终至关重要，并且邮件是否已阅读等内容都非关键。
- 客户数据的副本必须分隔到不同的故障区域或尽可能多的故障域 (例如数据中心，由单个凭据（ (进程、服务器或操作员) ) ）访问以提供故障隔离。 
- 必须监视关键客户数据，以发现任何部分"原子性、一致性、隔离性"和" (或) 。
- 必须防止客户数据损坏。 必须主动扫描或监视它、可修复和可恢复。
- 大多数数据丢失都由客户操作导致，因此允许客户使用 GUI 自行恢复，以便客户能够还原意外删除的项目。

通过针对这些原则构建云服务，再加上强大的测试和验证，Microsoft 365 能够满足并超过客户的要求，同时确保获得持续创新和改进的平台。

## <a name="related-articles"></a>相关文章

- [处理数据损坏](assurance-dealing-with-data-corruption.md)
- [恶意软件和勒索软件防护](assurance-malware-and-ransomware-protection.md)
- [监视和自愈](assurance-monitoring-and-self-healing.md)
- [Exchange数据恢复能力](assurance-exchange-data-resiliency.md)
