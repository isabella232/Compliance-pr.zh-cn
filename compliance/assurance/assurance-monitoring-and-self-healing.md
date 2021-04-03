---
title: Microsoft 365 中的数据监视和自修复
description: 本文将介绍 Microsoft 365 的监视和自我修复功能。
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
ms.custom:
- seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: baf73746fff5e4866c36975e082c84017e0b3083
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496941"
---
# <a name="data-monitoring-and-self-healing-in-microsoft-365"></a>Microsoft 365 中的数据监视和自修复

鉴于 Microsoft 365 的规模，如果不进行全面的内置监视、智能警报和快速可靠的自我修复，则不可能保持客户数据的复原和安全免受恶意软件的攻击。 在 Microsoft 365 规模上监视一组服务非常具有挑战性。 需要引入新的意识和方法，需要创建全新的技术集才能在连接的全球环境中运行和管理服务。 我们已从数据收集和筛选的传统监视方法移到基于数据分析的方法创建警报;接收信号并置信于该数据，然后使用自动化恢复或解决问题。 此方法有助于使人员从恢复公式中退出，这反过来会使操作成本更低、速度更快且容易出错。 

Microsoft 365 监视的基础是组成 Data Insights 引擎的技术集合，该引擎基于 Azure、SQL Azure 和开源流式处理数据库 [技术构建](https://cassandra.apache.org/)。 它旨在收集和汇总数据并得出结论。 目前，它每小时处理超过 5 亿个事件，从每天 100，000 多台服务器 (~15 TB) 分散在许多区域的数十个数据中心，并且这些数字不断增加。 

Microsoft 365 使用 *外部监视*，其中包括创建综合事务来测试所有重要的内容。 例如，在 Exchange Online 中，每个方案都以分散方式每五分钟测试一次全球每个数据库，从而提供系统中所有内容近乎连续的覆盖。 从多个位置执行每天 2.5 亿个测试事务，为服务创建可靠的基线或检测信号。 

Microsoft 365 还使用红色警报的概念，该概念将来自我们数据中心中所有计算机的所有监视信号缩减为可人工管理的信号。 概念非常简单：如果多个信号中发生某些情况，则必须发生一些事件。 不是为了在一个信号中建立置信度，而只是让每个信号具有合理的保真度，以便获得更高的准确性。 此监视系统功能强大，因此没有 24x7 工作人员在监视监视器;我们只有一个在检测到问题时唤醒的机子，在这种情况下，它将分页相应的呼叫人员，或者更像现在一样，它会继续操作并解决问题。 开始收集信号并生成红色警报后，我们可以开始跨所有服务分区进行三角分析。 

根据故障警报和红色警报的组合，此警报准确指示哪些组件可能存在问题，并且系统将尝试通过重新启动邮箱服务器自行纠正该问题。 

除了可自行修复的功能（如单页还原）之外，Exchange Online 还包括一些功能，这些功能采用监视和自我修复的方法，侧重于保留最终用户体验。 这些功能包括 *托管可用性（* 提供内置的监视和恢复操作）和 AutoReseed（在磁盘故障后自动还原数据库冗余）。 

## <a name="managed-availability"></a>托管可用性 

托管可用性提供本机运行状况检查和恢复解决方案，通过面向恢复的操作监视和保护最终用户的体验。 托管可用性是内置监视和恢复操作与 Exchange 高可用性平台的集成。 它设计用于在问题出现后立即被系统检测到以检测并恢复。 与 Exchange 之前的外部监视解决方案和技术不同的是，托管可用性不会尝试识别或沟通问题的根本原因。 相反，它侧重于解决最终用户体验的三个关键方面的恢复方面：

- **可用性** - 用户能否访问服务？ 
- **延迟** - 用户体验如何？ 
- **错误** - 用户能否完成所需的操作？ 

托管可用性是一项内部功能，在运行 Exchange Online 的每一台 Microsoft 365 服务器上运行。 它每秒轮询和分析数百个运行状况度量。 如果发现错误，大多数情况下会自动修复错误。 但始终存在托管可用性无法自行修复的问题。 在这种情况下，托管可用性会通过事件日志记录将问题上报给 Microsoft 365 支持团队。

## <a name="autoreseed"></a>自动种子重新设定

Exchange Online 服务器部署在一个配置中，该配置将多个数据库及其日志流存储在同一个非 RAID 磁盘上。 此配置通常只称为一 *批磁盘* (JBOD) 因为没有使用存储冗余机制（如 RAID）来复制磁盘上的数据。 当磁盘在 JBOD 环境中出现故障时，该磁盘上的数据将丢失。 

鉴于 Exchange Online 的大小以及内部部署的磁盘驱动器数百万个，磁盘驱动器故障在 Exchange Online 中经常发生。 事实上，每天超过 100 次失败。 当本地企业部署中的磁盘出现故障时，管理员必须手动更换故障磁盘并还原受影响的数据。 在云部署中，Microsoft 365 的大小，让操作员 (云管理员手动更换) 既不实用也不经济可行。 

自动重新设置子项（即 *AutoReseed）* 是一项功能，它代替了通常由操作员驱动的操作，以响应磁盘故障、数据库损坏事件或其他需要为数据库副本重新设置子级的问题。 AutoReseed 旨在当磁盘故障发生后通过使用系统提供的备用磁盘自动还原数据库冗余。 如果磁盘出现故障，则存储在该磁盘上的数据库副本将自动重新为服务器上预配置的备用磁盘重新设置子项，从而还原冗余。 