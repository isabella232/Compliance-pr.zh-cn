---
title: Microsoft 365 Exchange Online数据删除
description: 了解邮箱内邮箱和项目的软数据删除和硬数据删除在Exchange Online。
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
ms.openlocfilehash: 9dd365e075226d8fdbfd1a9f9e371df2668f814d
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/12/2021
ms.locfileid: "59158206"
---
# <a name="exchange-online-data-deletion-in-microsoft-365"></a>Exchange Online数据删除Microsoft 365

在Exchange Online，有两种类型的删除：软删除和硬删除。 这适用于邮箱和邮箱中的项目。

## <a name="soft-deleted-and-hard-deleted-mailboxes"></a>软删除和硬删除的邮箱

软删除的用户邮箱是使用 Microsoft 365 管理中心 或 Remove-Mailbox cmdlet 删除的邮箱，并且仍在 Azure Active Directory 回收站中保留不到 30 天。 邮箱可以通过以下任一方式变为软删除：

- 如果用户对象的作用域Azure Active Directory回收站容器或回收站 (，则用户邮箱与用户帐户的关联会) 。
- 用户邮箱与用户帐户Azure Active Directory已硬删除，但 Exchange Online 邮箱位于诉讼保留或电子数据展示保留下。
- 用户邮箱与用户帐户Azure Active Directory最近 30 天内已清除;这是在永久清除Exchange Online无法恢复之前，邮箱保持软删除状态的最大保留长度。

硬删除的用户邮箱是已经通过以下方法之一删除的邮箱：

- 用户邮箱已软删除 30 天以上，并且Azure Active Directory用户已硬删除。 将永久删除所有邮箱内容，如电子邮件、联系人和文件。
- 与用户邮箱关联的用户帐户已被硬删除Azure Active Directory。 用户邮箱现以软Exchange Online状态保留 30 天。 如果在 30 天期间，新 Azure Active Directory 用户从原始收件人帐户与同一 **ExchangeGuid** 或 **ArchiveGuid** 同步，并且该新帐户已获得 Exchange Online 的许可，则会导致硬删除原始用户邮箱。 将永久删除所有邮箱内容，如电子邮件、联系人和文件。
- 使用 **Remove-Mailbox -PermanentlyDelete 删除软删除的邮箱**。

上述删除方案假定用户邮箱未在任何保留状态，如诉讼保留或电子数据展示保留。 如果邮箱上存在任何类型的保留，则不能删除该邮箱。 对于所有邮件用户收件人类型，任何 [保留](https://support.office.com/article/manage-legal-investigations-in-office-365-2e5fbe9f-ee4d-4178-8ff8-4356bc1b168e?ui=en-US&rs=en-US&ad=US) 设置将被忽略，并且对硬删除或软删除没有影响。

## <a name="soft-deleted-and-hard-deleted-items"></a>软删除和硬删除的项目

当用户删除邮箱项目 (如电子邮件、联系人、日历约会或任务) 时，该项目将移动到"可恢复的项目"文件夹，并放入名为"Deletions"的子文件夹中。 这称为软删除。 已删除的项目保留在" 删除"文件夹中的时间取决于为邮箱设置的"已删除项目保留期限"。 默认情况下Exchange Online邮箱将已删除项目保留 14 天，但 Exchange Online 管理员可以更改此设置以将期限最长增加至 30 天。  (有关增加 Exchange Online 邮箱的已删除邮件保留期限的详细步骤，请参阅更改[为 Exchange Online](/exchange/recipients-in-exchange-online/manage-user-mailboxes/change-deleted-item-retention)邮箱保留永久删除的项目的时间。) 用户可以在已删除项目的保留时间过期之前恢复或清除已删除的项目。 为此，他们使用 Microsoft Outlook 或 Outlook 网页版 中的"恢复已删除邮件"功能。

如果用户使用"恢复已删除项目"功能清除已删除项目，Outlook Outlook 网页版"硬删除"。 在 Exchange Online中，新建邮箱时，默认情况下启用单个项目恢复，因此管理员仍可在已删除项目的保留期过期之前[](/Exchange/recipients/user-mailboxes/recover-deleted-messages)恢复硬删除的项目。 此外，如果单个项目恢复已启用，那么当用户或进程更改邮件时，原始项目的副本也会予以保留。

## <a name="page-zeroing"></a>页清零

*清零* 是一种安全机制，它通过已删除的数据写入零或二进制模式，以便删除的数据更难恢复。 在Exchange Online中，邮箱数据库使用 *页面* 作为存储单元，并实现了一个称为页面清零 *的覆盖过程*。 默认情况下，页面清零处于启用状态，客户或 Microsoft 无法禁用它。 在事务日志文件中记录页清零操作，以便以类似方式将给定数据库的所有副本都清零页。 对主动数据库副本上的页进行清零会使该页在数据库的被动副本上清零。

页清零会写入硬删除记录的二进制模式。 页清零模式特定于可扩展 存储 引擎 (ESE) 操作 (Exchange Online) 中服务器使用的内部数据库引擎的名称，与后台数据库维护操作相比，它对于运行时操作有所不同。  (后台数据库维护是一个持续校验和扫描每个数据库的过程。 其主要功能是校验和数据库页，但还处理清理空间以及清零由于 Store 崩溃而未清零的记录和) 

下表列出对应于特定运行时操作的填充模式。

| ESE 运行时操作   | 填充模式 |
|--------------------------|--------------|
| 替换                  | R            |
| 记录/长数值删除 | D            |
| 释放的页空间         | H            |

下表列出对应于在 ESE 后台数据库维护期间进行的特定操作的填充模式。

| ESE 后台数据库维护操作 | 填充模式 |
|-----------------------------------------------|--------------|
| 记录删除                                 | D            |
| 长数值删除                             | L            |
| 部分使用的页的释放页空间       | Z            |
| 未使用的页的释放页空间               | U            |

### <a name="page-zeroing-process"></a>页清零过程

页清零的过程取决于删除方案。 下表讨论数据库删除方案以及页清零功能的执行时间。

| 数据库删除方案 | 对数据库数据清零的 ESE 过程和时间范围 |
|:--------------------------|:------------------------------------------------|
| 项目根据已删除项目的保留期过期。 | 一个异步线程对删除的数据写入二进制模式。 此操作在数毫秒的记录删除过程中发生。 如果当异步清零工作仍未完成时存储进程崩溃 (或版本存储清理因版本存储增长) 而取消，则当后台数据库维护处理数据库的这一部分时，将完成清零。 |
| 视图方案：文件夹视图中Outlook/Outlook 网页版过期 (会话视图)  | 当后台数据库维护处理该部分数据库时会进行数据清零。 |
| 移动邮箱/删除邮箱方案：已删除的邮箱 (源邮箱已删除)  | 当后台数据库维护处理该部分数据库时会进行数据清零。 |

### <a name="mailbox-data-types-without-page-zeroing"></a>没有页清零的邮箱数据类型

以下邮箱数据类型没有页面清零设置：

- **邮箱数据库事务** 日志 - 当作为正常操作一部分删除事务日志时，没有进程将存储已删除邮件的邮箱的文件系统中的日志文件 (清零) 。 文件系统可能会快速重新利用新创建的日志的可用空间，但无法保证会发生此情况。
- **内容索引目录文件**- Exchange Online使用 Search Foundation (也称为FAST) 索引功能。 搜索索引目录由存储在与邮箱数据库文件相同的卷上的几十个文件组成。 当从邮箱数据库中硬删除邮件时，不会立即删除搜索编录中的关联内容。 当 Search Foundation 执行卷影 (或主合并) 将许多小目录文件合并到一个较大的文件中时，将发生内容删除。 主合并完成后，会删除较小的编录文件。 没有将存储已删除目录文件的块清零的过程。

## <a name="continuous-replication"></a>连续复制

连续 (也称为日志交付和重播) 是 Exchange Online 中的一种技术，用于创建和维护每个邮箱数据库的副本，以提供高可用性、站点恢复和灾难恢复。 连续复制使用Exchange Server崩溃恢复支持来提供用于对邮箱数据库的一个或多个副本执行异步更新的技术。 每个邮箱服务器记录对活动数据库数据库 (例如，用户电子邮件活动) 一组 1 MB 事务日志文件中的日志记录。 这组文件称为日志流。 在连续复制中，日志流还用于异步更新数据库的一个或多个副本。 这是通过以下方法完成的：将日志传输到包含主动数据库被动副本的位置，然后将这些日志重播到被动数据库副本中。 如果针对数据库的被动副本重播活动数据库的所有日志，则两个数据库是等效的，并且通过此过程，对活动数据库进行的任何物理更改都将被复制到该数据库的所有被动副本。

从邮箱数据库执行的任何删除操作（无论是邮箱项目还是整个邮箱，以及软删除还是硬删除）都表示对活动数据库的物理更改。 页清零还需要对活动数据库进行物理更改。 这些更改通过称为连续复制的过程写入日志文件，当针对数据库的被动副本重播这些日志文件时，将针对这些被动数据库进行相同的物理更改。
