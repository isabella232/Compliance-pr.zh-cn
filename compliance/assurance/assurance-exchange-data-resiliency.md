---
title: Microsoft 365 中的 Exchange Online 数据恢复能力
description: 本文介绍 Exchange Online 和 Microsoft 365 中数据恢复的各个方面。
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
ms.openlocfilehash: 2cdd37d34612421cc7a9e4687134e2a1e2b1aeec
ms.sourcegitcommit: b06fa9f1b230fd5e470817486ea51f460f28b691
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/27/2021
ms.locfileid: "50012938"
---
# <a name="exchange-online-data-resiliency-in-microsoft-365"></a>Microsoft 365 中的 Exchange Online 数据恢复能力

>[!IMPORTANT]
>由于我们将继续以不同方式投资来保留邮箱内容，我们宣布在 Exchange Online 的 Exchange 管理中心 (EAC) 停用 In-Place 保留。 从 2020 年 7 月 1 日开始，将无法创建新的保留In-Place保留。 但你仍然可以在 EAC 中In-Place Exchange Online PowerShell 中的 **Set-MailboxSearch** cmdlet 管理保留项。 但是，从 2020 年 10 月 1 日起，你将无法管理In-Place保留。 只能在 EAC 中或通过使用 **Remove-MailboxSearch** cmdlet 删除它们。 在 In-Place 和 Exchange 混合Exchange Server中仍支持使用保留。 有关在 Exchange Online 中停用保留In-Place，请参阅停用 [旧版电子数据展示工具](https://docs.microsoft.com/microsoft-365/compliance/legacy-ediscovery-retirement)。

就地保留将保留所有邮箱内容，包括已删除项目和已修改项目的原始版本。 所有此类邮箱项目均会返回到[就地电子数据展示](https://docs.microsoft.com/exchange/security-and-compliance/in-place-ediscovery/in-place-ediscovery)搜索中。 当您将In-Place邮箱置于"保留"时，对应的存档邮箱 (（如果已启用) ）中的内容也会置于保留状态，并返回到电子数据展示搜索中。

有两种类型的损坏可能会影响 Exchange 数据库：物理损坏（通常是由硬件 (导致，特别是存储硬件) 问题）和逻辑损坏（由其他因素导致）。 通常，Exchange 数据库中可能会发生两种类型的逻辑损坏：

- **数据库逻辑损坏** - 数据库页校验和匹配，但页面上的数据逻辑错误。 当数据库引擎 (可扩展存储引擎 (ESE) ) 尝试写入数据库页时，可能会发生此情况，即使操作系统返回成功消息，数据也永远不会写入磁盘或写入错误的位置。 这称为丢失 *刷新*。 ESE 包括许多功能和安全措施，旨在防止数据库和其他数据丢失方案的物理损坏。 为了防止丢失的刷新丢失数据，ESE 在数据库中包括丢失的刷新检测机制，以及用于 (页面还原) 功能。
- **存储逻辑** 损坏 - 以用户不需要的方式添加、删除或操作数据。 这些情况由第三方应用程序导致。 从用户认为它损坏的意义上来说，它通常是损坏的。 Exchange 存储会考虑产生一系列有效 MAPI 操作的逻辑损坏的事务。 Exchange Online [中的](https://docs.microsoft.com/exchange/security-and-compliance/create-or-remove-in-place-holds) 就地保留功能可防止存储逻辑损坏 (因为它可防止用户或应用程序永久删除) 。 

Exchange Online 在日志检查和日志重播期间对复制的日志文件执行多项一致性检查。 这些一致性检查可防止系统复制物理损坏。 例如，在日志检查期间，存在一个物理完整性检查，用于验证 日志文件 并验证记录在 日志文件 中的校验和是否与内存中生成的校验和匹配。 此外，检查日志文件标头以确保日志日志文件记录在日志标头中的签名与记录日志文件。 在日志重播期间，日志文件进一步审查。 例如，数据库标头还包含日志签名，该签名与日志文件签名进行比较以确保它们匹配。 

通过使用 Exchange Native Data Protection（一种利用跨多个服务器和多个数据中心的应用程序级复制以及其他功能来帮助防止由于损坏或其他原因丢失数据）的复原策略，Exchange Online 中的邮箱数据损坏防护已实现。 这些功能包括由 Microsoft 或 Exchange Online 应用程序本身管理的本机功能，例如：

- [数据可用性组](https://docs.microsoft.com/exchange/back-up-email)
- 单位更正 
- 联机数据库扫描 
- 丢失刷新检测 
- 单页还原 
- 邮箱复制服务 
- 日志文件检查 
- 在复原文件系统上部署 

有关前面列出的本机功能的详细信息，请选择超链接，并参阅以下内容，了解其他信息和有关没有超链接的项目的详细信息。 除了这些本机功能之外，Exchange Online 还包括客户可以管理的数据恢复能力功能，例如： 
- [默认情况下启用 (项目恢复) ](https://docs.microsoft.com/exchange/recipients-in-exchange-online/manage-user-mailboxes/recover-deleted-messages) 
- [就地保留和诉讼保留](https://docs.microsoft.com/exchange/security-and-compliance/in-place-and-litigation-holds) 
- [已删除邮件保留Soft-Deleted邮箱 (都默认启用) ](https://docs.microsoft.com/exchange/recipients-in-exchange-online/delete-or-restore-mailboxes) 

## <a name="database-availability-groups"></a>数据库可用性组 
Microsoft 365 中的每个邮箱数据库都托管在数据库可用性组 [ (DAG) ](https://docs.microsoft.com/exchange/back-up-email) 中，并复制到同一地区中地理位置不同的数据中心。 最常见的配置是四个数据中心中的四个数据库副本;但是，一些区域的数据中心 (复制到印度三个数据中心，澳大利亚和日本有两个数据中心) 。 但是，在所有情况下，每个邮箱数据库都有四个副本分布在多个数据中心，从而确保邮箱数据免受软件、硬件甚至数据中心故障的影响。 

在四个副本中，其中三个副本配置为高度可用。 第四个副本配置为滞后 [数据库副本](https://docs.microsoft.com/Exchange/high-availability/manage-ha/activate-lagged-db-copies)。 滞后数据库副本不用于单个邮箱恢复或邮箱项目恢复。 它的目的是为系统范围内出现灾难性逻辑损坏的罕见事件提供恢复机制。 

Exchange Online 中的滞后数据库副本使用七天的重播延迟日志文件时间进行配置。 此外，启用了 Exchange 重播延迟管理器为滞后日志文件提供动态延迟，以允许滞后数据库副本自行修复和管理日志文件增长。 尽管滞后数据库副本在 Exchange Online 中使用，但必须了解它们不是有保证的时间点备份。 Exchange Online 中的滞后数据库副本具有可用性阈值，通常约为 90%，因为包含滞后副本的磁盘由于磁盘故障而丢失，滞后副本由于自动减少) 而变为高度可用的副本 (，以及滞后数据库副本重建日志重播队列的时间段。 

## <a name="transport-resilience"></a>传输恢复能力 
Exchange Online 包括两个主要传输恢复功能：卷影冗余和安全网络。 卷影冗余在邮件传输过程中保留邮件的冗余副本。 安全网络在邮件成功传递后保留邮件的冗余副本。 

使用卷影冗余，每个 Exchange Online 传输服务器会创建它接收的每封邮件的副本，然后确认已成功将邮件接收到发送服务器。 这会使传输管道中所有邮件在传输过程中冗余。 如果 Exchange Online 确定原始邮件在传输过程中丢失，则重新传递邮件的冗余副本。 

Safety Net 是一个与邮箱服务器上传输服务关联的传输队列。 此队列存储服务器成功处理的邮件的副本。 当邮箱数据库或服务器故障需要激活邮箱数据库的过期副本时，安全网络队列中的邮件会自动重新提交到邮箱数据库的新主动副本。 Safety Net 也是冗余的，因此无需将传输作为单一故障点。 它使用 Primary Safety Net 和 Shadow Safety Net 的概念，其中如果 Primary Safety Net 不可用超过 12 小时，重新提交请求将成为卷影重新提交请求，并且邮件从 Shadow Safety Net 重新传递。

从 Safety Net 重新提交邮件由管理 DAG 和邮箱数据库副本的 Microsoft Exchange 复制服务的 Active Manager 组件自动启动。 从 Safety Net 重新提交邮件不需要手动操作。 

## <a name="single-bit-correction"></a>单位更正 
ESE 包括一种检测和解决单位 CRC 错误的机制 (也称为单位翻转) ，这些错误是硬件错误 (的结果，因此它们表示物理损坏) 。 出现这些错误时，ESE 会自动更正错误，并记录事件日志中的事件。 

## <a name="online-database-scanning"></a>联机数据库扫描 
联机数据库扫描 (数据库检查求和 *)* 是 ESE 使用数据库一致性检查器读取每个页面并检查页面损坏的过程。 主要用途是检测事务操作可能未检测到的物理损坏和丢失刷新。 数据库扫描还执行存储后崩溃操作。 由于崩溃，空间可能会泄露，联机数据库扫描会查找和恢复丢失的空间。 系统的设计预期是每七天完全扫描一次每个数据库。 

## <a name="lost-flush-detection"></a>丢失刷新检测 
如果返回为已完成的磁盘子系统/操作系统的数据库写入操作实际上未写入磁盘或写入错误的位置，则会发生丢失刷新。 丢失刷新事件可能导致数据库逻辑损坏，因此为了防止丢失刷新导致数据丢失，ESE 包括丢失的刷新检测机制。 当数据库页写入被动副本时，将检查主动副本上的丢失刷新。 如果检测到丢失刷新，ESE 可以使用页面修补过程修复进程。 

## <a name="single-page-restore"></a>单页还原 
单页还原（也称为页面 *修补*）是一个自动过程，其中损坏的数据库页面将替换为正常副本中的正常副本。 损坏页面的修复过程取决于数据库副本是主动还是被动。 当活动数据库副本遇到损坏的页面时，它可以从其中一个副本复制页面，只要它复制的页面是最新的。 此过程通过将页面请求放入日志流（这是邮箱数据库复制的基础）完成。 副本一旦遇到页面请求，就会通过向请求的数据库副本发送页面副本进行响应。 单页还原还为活动提供从副本请求页面的异步通信机制，即使副本当前处于脱机状态也是如此。 

如果被动数据库副本（包括滞后数据库副本）损坏，由于这些副本始终位于主动副本后面，因此始终可以安全地将任何页面从主动副本复制到被动副本。 被动数据库副本本质上是高度可用的，因此在页面修补过程中，日志重播将暂停，但日志复制将继续进行。 被动数据库副本从主动副本中检索损坏页面的副本，等待直到复制并检查满足最大所需日志生成要求的 日志文件，然后修补损坏的页面。 修补页面后，日志重播恢复。 对于滞后数据库副本，此过程是相同的，只是滞后数据库首先重播实现可修补状态所需的所有日志文件。 

## <a name="mailbox-replication-service"></a>邮箱复制服务 
移动邮箱是管理大型电子邮件服务的关键部分。 始终有更新的技术、硬件和版本升级要处理，因此，具有一个稳固的受限系统，我们的工程师可以在保持邮箱对用户透明移动的同时完成此工作 (确保用户在整个过程中保持联机状态) 是关键，并确保当邮箱不断变大时，此过程可以正常扩展。 

Exchange 邮箱复制服务 (MRS) 负责在数据库之间移动邮箱。 在移动过程中，MRS 对邮箱内的所有项目执行一致性检查。 如果发现一致性问题，MRS 将更正该问题，或跳过损坏的项目，从而从邮箱中删除损坏。 

由于 MRS 是 Exchange Online 的一个组件，因此我们可以更改其代码，以解决将来检测到的新损坏形式。 例如，如果我们检测到 MRS 无法修复的一致性问题，我们可以分析损坏、更改 MRS 代码并更正不一致 (如果我们了解如何进行) 。 

## <a name="log-file-checks"></a>日志文件检查 
Exchange 数据库生成的所有事务日志文件都经过多种形式的一致性检查。 创建日志文件时，首先会编写位模式，然后执行一系列日志写入。 利用此结构，Exchange Online 可以执行一系列检查 (丢失刷新、CRC 和其他) 检查，以在写入时验证每个 日志文件，在复制时再次进行验证。 

## <a name="deployment-on-resilient-file-system"></a>在复原文件系统上部署 
为了帮助防止在文件系统级别发生损坏，Exchange Online 正在复原文件系统 (ReFS) 分区上部署，以提供改进的恢复功能。 ReFS 是一个Windows Server 2012及更高版本中的文件系统，旨在更加有弹性地抵御数据损坏，从而最大限度地提高数据可用性和完整性。 具体来说，ReFS 改进了元数据的更新方式，从而更好地保护数据并减少数据损坏情况。 它还使用校验和来验证文件数据和元数据的完整性，以确保可以轻松找到并修复数据损坏。 

Exchange Online 利用多个 ReFS 优势： 
- 数据完整性的复原性提高意味着数据损坏事件更少。 减少损坏事件数意味着减少了不必要的数据库重新种。 
- 在元数据上运行的校验和可以更快、更确定地检测损坏案例，从而允许我们在数据卷上出现灰色故障之前修复客户数据损坏。
- 设计为适用于大型数据集（数兆字节和更大）而不会影响性能
- 支持 Exchange Online 使用的其他功能，例如 BitLocker 加密。 

Exchange Online 还受益于其他 ReFS 功能： 
- **完整性 (流**) - ReFS 存储数据的方式可保护数据免受通常可能导致数据丢失的许多常见错误影响。 Microsoft 365 搜索使用完整性流来帮助进行早期磁盘损坏检测和文件内容的校验和。 当写入操作因断电等原因 (写入操作完成时，该功能还可以减少"写入"操作导致的损坏) 。 
- **可用性 (回收)** - ReFS 设置数据可用性的优先级。 过去，文件系统经常容易发生数据损坏，需要使系统脱机进行修复。 尽管很少见，但如果确实发生损坏，ReFS 会实施回收，这是一项功能，用于从实时卷上的命名空间中删除损坏的数据，并确保良好的数据不会受到不可修复的损坏数据的影响。 将"回收"功能应用于 Exchange Online 数据库卷并隔离数据损坏意味着我们可以在损坏的卷上保持损坏的卷在损坏和修复操作之间保持正常运行。 此结构提高了通常受此类磁盘损坏问题影响的数据库的可用性。 
