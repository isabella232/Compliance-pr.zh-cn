---
title: Microsoft 365 中的 Exchange Online 数据弹性
description: 本文将介绍数据恢复能力在Exchange Online Microsoft 365。
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
ms.openlocfilehash: b7aeaad54c625628292ac9a6841602d0205e0dc40186ce60dfc52f7dc55dc880
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "54291110"
---
# <a name="exchange-online-data-resiliency-in-microsoft-365"></a>Exchange Online数据恢复能力Microsoft 365

>[!IMPORTANT]
>随着我们将继续以不同方式投资来保留邮箱内容，我们宣布停用 Exchange 管理中心 (EAC) Exchange Online 中的 In-Place 保留。 从 2020 年 7 月 1 日开始，将无法创建新的保留In-Place保留。 但你仍然可以在 EAC 中In-Place或通过使用 PowerShell 中的 **Set-MailboxSearch** cmdlet 管理Exchange Online保留。 但是，从 2020 年 10 月 1 日起，你将无法管理In-Place保留。 只能在 EAC 中或通过使用 **Remove-MailboxSearch** cmdlet 删除它们。 使用In-Place保留Exchange Server Exchange混合部署仍将受支持。 有关停用旧版电子数据展示In-Place保留Exchange Online，请参阅停用[旧版电子数据展示工具](/microsoft-365/compliance/legacy-ediscovery-retirement)。

就地保留将保留所有邮箱内容，包括已删除项目和已修改项目的原始版本。 所有此类邮箱项目均会返回到[就地电子数据展示](/exchange/security-and-compliance/in-place-ediscovery/in-place-ediscovery)搜索中。 当您将 In-Place 置于用户邮箱上时，相应的存档邮箱 (中的内容（如果已启用) ）也会置于保留状态，并返回到电子数据展示搜索中。

有两种类型的损坏会影响 Exchange 数据库：物理损坏（通常是由硬件 (导致，特别是存储硬件) 问题）和逻辑损坏（由其他因素导致）。 通常，在数据库内可能发生两种类型的逻辑损坏Exchange损坏：

- **数据库逻辑损坏** - 数据库页校验和匹配，但页面上的数据逻辑错误。 当数据库引擎 (可扩展 存储 引擎 (ESE) ) 尝试写入数据库页时，可能会发生这种情况，即使操作系统返回成功消息，数据也永远不会写入磁盘或写入错误的位置。 这称为丢失 *刷新*。 ESE 包括许多旨在防止数据库和其他数据丢失情况的物理损坏的功能和安全措施。 为了防止丢失刷新丢失数据，ESE 在数据库中包括丢失刷新检测机制，以及一个功能 (单个页面还原) 进行更正。
- **存储逻辑** 损坏 - 以用户不想的方式添加、删除或操作数据。 这些情况由第三方应用程序导致。 从用户认为损坏的意义上来说，它通常是损坏的。 Exchange 存储会考虑产生一系列有效 MAPI 操作的逻辑损坏的事务。 Exchange Online[中的](/exchange/security-and-compliance/create-or-remove-in-place-holds)就地保留功能可防止存储逻辑损坏 (因为它可以防止用户或应用程序用户或应用程序) 。 

Exchange Online在日志检查和日志重播期间对复制的日志文件执行几个一致性检查。 这些一致性检查可防止系统复制物理损坏。 例如，在日志检查期间，存在一个物理完整性检查，用于验证 日志文件并验证记录在 日志文件 中的校验和是否与内存中生成的校验和匹配。 此外，检查日志文件标头以确保日志标头日志文件记录的内容签名与记录日志日志文件。 在日志重播期间，日志文件进一步审查。 例如，数据库标头还包含日志签名，该日志签名与日志文件签名进行比较以确保它们相匹配。 

通过使用 Exchange Native Data Protection（一种复原策略，利用跨多个服务器和多个数据中心的应用程序级复制以及其他功能来帮助防止由于损坏或其他原因丢失数据）在 Exchange Online 中防止邮箱数据的损坏。 这些功能包括由 Microsoft 或应用程序本身Exchange Online本机功能，例如：

- [数据可用性组](/exchange/back-up-email)
- 单位更正 
- 联机数据库扫描 
- 丢失刷新检测 
- 单页还原 
- 邮箱复制服务 
- 日志文件检查 
- 在复原文件系统上部署 

有关前面列出的本机功能的详细信息，请选择超链接，并查看以下内容，了解其他信息以及没有超链接的项目的详细信息。 除了这些本机功能，Exchange Online还包括客户可以管理的数据复原功能，例如： 
- [默认情况下启用 (项目恢复) ](/exchange/recipients-in-exchange-online/manage-user-mailboxes/recover-deleted-messages) 
- [就地保留和诉讼保留](/exchange/security-and-compliance/in-place-and-litigation-holds) 
- [已删除邮件保留Soft-Deleted邮箱 (都默认启用) ](/exchange/recipients-in-exchange-online/delete-or-restore-mailboxes) 

## <a name="database-availability-groups"></a>数据库可用性组 
每个邮箱数据库Microsoft 365 [DAG](/exchange/back-up-email) (数据库可用性组中) 复制到同一区域内地理位置不同的数据中心。 最常见的配置是四个数据中心中的四个数据库副本;但是，一些区域的数据中心 (数据库复制到印度三个数据中心，而澳大利亚和日本有两个数据中心) 。 但所有情况下，每个邮箱数据库都有四个副本分布在多个数据中心，从而确保邮箱数据免受软件、硬件甚至数据中心故障的影响。 

这四个副本中，其中三个副本配置为高度可用。 第四个副本配置为滞后 [数据库副本](/Exchange/high-availability/manage-ha/activate-lagged-db-copies)。 滞后的数据库副本不用于单个邮箱恢复或邮箱项目恢复。 它的目的是为系统范围内的灾难性逻辑损坏的罕见事件提供恢复机制。 

延迟数据库副本Exchange Online重播延迟时间配置为七日志文件延迟时间。 此外，Exchange重播延迟管理器为滞后副本提供动态 日志文件 减少功能，以允许滞后数据库副本自行修复和管理日志文件增长。 尽管滞后数据库副本用于Exchange Online，但必须了解它们不是有保证的时间点备份。 Exchange Online 中的滞后数据库副本具有可用性阈值，通常约为 90%，因为包含滞后副本的磁盘因磁盘故障而丢失，滞后副本由于自动减少) 而变为高度可用的副本 (，以及滞后数据库副本重建日志重播队列的时间段。 

## <a name="transport-resilience"></a>传输恢复能力 
Exchange Online两个主要传输恢复功能：卷影冗余和安全网络。 卷影冗余在邮件传输过程中保留邮件的冗余副本。 安全网络在邮件成功传递后保留邮件的冗余副本。 

使用卷影冗余，Exchange Online服务器在确认成功将邮件接收到发送服务器之前，会复制它接收的每封邮件。 这会使传输管道中所有邮件在传输过程中冗余。 如果Exchange Online确定原始邮件在传输过程中丢失，则重新传递邮件的冗余副本。 

Safety Net 是一个与邮箱服务器上传输服务关联的传输队列。 此队列存储服务器已成功处理的邮件的副本。 当邮箱数据库或服务器故障需要激活邮箱数据库的过期副本时，安全网络队列中的邮件将自动重新提交到邮箱数据库的新主动副本。 Safety Net 也是冗余的，因此无需将传输作为单一故障点。 它使用 Primary Safety Net 和 Shadow Safety Net 的概念，其中，如果 Primary Safety Net 不可用的时间超过 12 小时，重新提交请求将成为卷影重新提交请求，并且从 Shadow Safety Net 重新传递邮件。

从 Safety Net 重新提交邮件由管理 DAG 和邮箱数据库副本的 Microsoft Exchange 复制服务的 Active Manager 组件自动启动。 从 Safety Net 重新提交邮件不需要手动操作。 

## <a name="single-bit-correction"></a>单位更正 
ESE 包括一种检测和解决单位 CRC 错误 (也称为单位翻转) ，这是硬件错误 (因此它们表示物理损坏) 。 出现这些错误时，ESE 会自动更正错误，并记录事件日志中的事件。 

## <a name="online-database-scanning"></a>联机数据库扫描 
联机数据库 (也称为数据库检查求 *和)* ESE 使用数据库一致性检查器读取每个页面并检查页面损坏的过程。 主要用途是检测事务操作可能未检测到的物理损坏和丢失刷新。 数据库扫描还执行存储后崩溃操作。 空间可能会由于崩溃而泄露，联机数据库扫描可查找和恢复丢失的空间。 系统的设计预期是每七天完全扫描一次每个数据库。 

## <a name="lost-flush-detection"></a>丢失刷新检测 
如果返回为已完成的磁盘子系统/操作系统的数据库写入操作实际上未写入磁盘或写入错误的位置，则会发生丢失刷新。 丢失刷新事件可能导致数据库逻辑损坏，因此为了防止丢失刷新导致数据丢失，ESE 包括丢失刷新检测机制。 当数据库页面写入被动副本时，将检查主动副本上的丢失刷新。 如果检测到丢失刷新，ESE 可以使用页面修补过程修复进程。 

## <a name="single-page-restore"></a>单页还原 
单页还原（也称为页面修补）是一个自动过程，其中损坏的数据库页面替换为正常副本中的正常副本。 损坏页面的修复过程取决于数据库副本是主动还是被动。 当活动数据库副本遇到损坏的页面时，它可以从其中一个副本复制页面，只要它复制的页面是最新的。 此过程通过将页面请求放入日志流（这是邮箱数据库复制的基础）完成。 副本一旦遇到页面请求，就会通过向请求的数据库副本发送页面副本来做出响应。 单页还原还为活动提供从副本请求页面的异步通信机制，即使副本当前处于脱机状态也是如此。 

如果被动数据库副本（包括滞后数据库副本）损坏，由于这些副本始终位于主动副本之后，因此始终可以安全地将任何页面从主动副本复制到被动副本。 被动数据库副本本质上是高度可用的，因此在页面修补过程中，日志重播将暂停，但日志复制将继续。 被动数据库副本从主动副本检索损坏页面的副本，等待复制并检查满足最大所需日志生成要求的 日志文件，然后修补损坏的页面。 修复页面后，日志重播恢复。 对于滞后数据库副本，此过程是相同的，只是滞后数据库首先重播实现可修补状态所需的所有日志文件。 

## <a name="mailbox-replication-service"></a>邮箱复制服务 
移动邮箱是管理大型电子邮件服务的关键部分。 始终有更新的技术、硬件和版本升级要处理，因此，具有稳固的受限系统，我们的工程师可以在保持邮箱对用户 (透明移动的同时，确保在整个过程中保持联机状态) 是关键，并确保当邮箱不断变大时，此过程可以正常扩展。 

THE Exchange Mailbox Replication Service (MRS) is responsible for moving mailboxes between databases. 在移动过程中，MRS 对邮箱内的所有项目执行一致性检查。 如果发现一致性问题，MRS 将更正该问题，或跳过损坏的项目，从而从邮箱中删除损坏。 

由于 MRS 是 Exchange Online的组件，因此我们可以更改其代码，以解决将来检测到的新的损坏形式。 例如，如果我们检测到 MRS 无法修复的一致性问题，我们可以分析损坏、更改 MRS 代码并更正不一 (如果我们知道如何修复) 。 

## <a name="log-file-checks"></a>日志文件检查 
由数据库生成的所有事务日志文件Exchange进行多种形式的一致性检查。 创建日志文件时，首先会编写位模式，然后执行一系列日志写入。 此结构Exchange Online执行一系列检查 (丢失刷新、CRC 和其他检查) 以在写入时验证每个 日志文件，在复制时再次进行验证。 

## <a name="deployment-on-resilient-file-system"></a>在复原文件系统上部署 
为了帮助防止在文件系统级别发生损坏，Exchange Online正在复原文件系统 (ReFS) 分区上部署，以提供改进的恢复功能。 ReFS 是 Windows Server 2012 及更高版本中的文件系统，旨在更能够抵御数据损坏，从而最大限度地提高数据可用性和完整性。 具体来说，ReFS 在元数据更新方式方面进行了改进，从而更好地保护数据并减少数据损坏情况。 它还使用校验和来验证文件数据和元数据的完整性，以确保可以轻松找到并修复数据损坏。 

Exchange Online多个 ReFS 优势： 
- 数据完整性的复原性提高意味着数据损坏事件更少。 减少损坏事件数意味着减少了不必要的数据库重新种数。 
- 在元数据上运行的校验和可以更快、更确定地检测损坏情况，从而允许我们在数据卷上出现灰色故障之前修复客户数据损坏。
- 设计用于大型数据集（千兆字节和更大）而不会影响性能
- 支持设备使用的其他Exchange Online，如 BitLocker 加密。 

Exchange Online ReFS 功能也可从中获益： 
- **完整性 (流)** - ReFS 以一种保护数据免受通常可能导致数据丢失的常见错误影响的方式存储数据。 Microsoft 365搜索使用完整性流来帮助进行早期磁盘损坏检测和文件内容的校验和。 当写入操作由于断电等原因 (写入操作完成时，该功能还可以减少"写入"操作导致的损坏) 。 
- **可用性 (Salvage)** - ReFS 优先确定数据的可用性。 过去，文件系统经常容易发生数据损坏，数据损坏需要使系统脱机进行修复。 尽管很少见，但如果确实发生损坏，ReFS 会实施回收，这是一项功能，用于从活动卷上的命名空间中删除损坏的数据，并确保良好的数据不受不可修复的损坏数据负面影响。 将"回收"功能并隔离数据损坏Exchange Online数据库卷意味着我们可以在损坏的卷上保持损坏的卷在损坏和修复操作之间的运行状态。 此结构提高了通常受此类磁盘损坏问题影响的数据库的可用性。 
