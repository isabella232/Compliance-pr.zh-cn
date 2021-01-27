---
title: Microsoft 365 中的数据复原能力
description: 本文介绍 Microsoft 365 中数据恢复和恢复的设计和原则。
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
ms.openlocfilehash: 361400bf6330fb82d34f384d17e4d4ee438ccf08
ms.sourcegitcommit: b06fa9f1b230fd5e470817486ea51f460f28b691
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/27/2021
ms.locfileid: "50012898"
---
# <a name="data-resiliency-in-microsoft-365"></a>Microsoft 365 中的数据恢复能力

鉴于云计算的复杂性质，Microsoft 请注意，问题不是问题是否发生，而是何时发生。 我们将云服务设计得最大化可靠性，并最大限度地减少出现问题时对客户的负面影响。 我们已超越依赖复杂物理基础结构的传统策略，并且直接将冗余内置到云服务中。 我们结合使用了不太复杂的物理基础结构和更具智能性的软件，将数据恢复能力构建到服务中，并为客户提供高可用性。

## <a name="resiliency-and-recoverability-are-built-in"></a>内置复原和可恢复性

在复原和恢复中构建首先假定基础基础结构和流程将在某些时候失败：硬件 (基础结构) 将失败，用户将出错，软件将具有 Bug。 虽然说软件开发人员在云之前没有考虑这些问题是错误的，但是，在典型的 IT 实施中，这些问题的处理方式与云之前有所不同：

- 首先，硬件和基础结构保护十分重要。 这种结构意味着具有可靠性为 99.99% 的数据中心需要大量电源和网络冗余，并且服务器通过基于硬件的群集、双电源、双网络接口等实现。
- 第二，过程至关重要。 运营团队维护严格的过程，使用了更改窗口，并且通常存在大量的项目管理开销。
- 第三，部署以一种淡淡的速度进行。 在不拥有源的情况下部署代码意味着等待修补程序发布，主要版本涉及硬件更换和大量资金投入。 此外，更正问题的唯一方法就是回滚。 因此，大多数 IT 组织仅部署主要版本，以避免工作保持最新。
- 最后，已部署系统的规模和它们的互连程度过去比现在要小得多。

如今，客户期望 Microsoft 持续创新，而不会损害质量，这也是 Microsoft 服务和软件构建时牢记复原性和可恢复性的原因之一。

## <a name="microsoft-365-data-resiliency-principles"></a>Microsoft 365 数据复原原则

复原是指基于云的服务能够抵御某些类型的故障，但从客户的角度来看仍可以完全正常运行。 数据恢复能力意味着无论 Microsoft 365 中发生什么故障，关键客户数据都保持不变且不受影响。 为此，Microsoft 365 服务围绕五个特定复原原则进行设计：

- 存在关键和非关键数据。 例如，非关键 (，例如，在极少数失败) 是否可丢弃邮件。 关键 (例如，应以极端成本) 电子邮件等客户数据。 作为设计目标，传递的邮件始终至关重要，并且邮件是否已阅读等内容都非关键。
- 客户数据的副本必须分隔到不同的容错区域或尽可能多的故障域中 (例如，数据中心可由单个凭据（进程、服务器或操作员 (进程、服务器或操作员) ）访问，以提供故障隔离。 
- 必须对关键客户数据进行监视，以发现任何部分无法通过原子性、一致性、隔离、持久性 (或) 。
- 必须防止客户数据损坏。 它必须主动扫描或监视、可修复且可恢复。
- 大多数数据丢失都由客户操作导致，因此允许客户使用 GUI 自行恢复，以便客户能够还原意外删除的项目。

通过遵循这些原则构建云服务，以及强大的测试和验证，Microsoft 365 能够满足并超过客户的要求，同时确保提供持续创新和改进的平台。

## <a name="related-articles"></a>相关文章

- [处理数据损坏](assurance-dealing-with-data-corruption.md)
- [恶意软件和勒索软件防护](assurance-malware-and-ransomware-protection.md)
- [监视和自愈](assurance-monitoring-and-self-healing.md)
- [Exchange 数据恢复能力](assurance-exchange-data-resiliency.md)
