---
title: Microsoft 365 Exchange Online 数据删除
description: 了解如何在 Exchange Online 中处理邮箱和邮箱中的项目的软和硬数据删除。
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
ms.openlocfilehash: b86c855a113706731ac6037a2851ae0f1adaccb9
ms.sourcegitcommit: b06fa9f1b230fd5e470817486ea51f460f28b691
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/27/2021
ms.locfileid: "50012958"
---
# <a name="exchange-online-data-deletion-in-microsoft-365"></a>Microsoft 365 中的 Exchange Online 数据删除

在 Exchange Online 中，有两种类型的删除：软删除和硬删除。 这适用于邮箱和邮箱中的项目。

## <a name="soft-deleted-and-hard-deleted-mailboxes"></a>软删除和硬删除的邮箱

软删除的用户邮箱是一个已使用 Microsoft 365 管理中心或 Remove-Mailbox cmdlet 删除且仍在 Azure Active Directory 回收站中保留少于 30 天的邮箱。 邮箱可以通过以下任一方式软删除：

- 用户邮箱的关联 Azure Active Directory 用户帐户被软删除 (用户对象超出范围或位于回收站容器) 。
- 用户邮箱的关联 Azure Active Directory 用户帐户已被硬删除，但 Exchange Online 邮箱位于诉讼保留或电子数据展示保留下。
- 用户邮箱的关联 Azure Active Directory 用户帐户已过去 30 天内清除;这是 Exchange Online 在永久清除和无法恢复邮箱之前将邮箱保持软删除状态的最大保留长度。

硬删除的用户邮箱是已经通过以下方法之一删除的邮箱：

- 用户邮箱已软删除超过 30 天，并且已硬删除关联的 Azure Active Directory 用户。 将永久删除所有邮箱内容，如电子邮件、联系人和文件。
- 已硬从 Azure Active Directory 中删除与用户邮箱关联的用户帐户。 用户邮箱现在在 Exchange Online 中软删除，并处于软删除状态 30 天。 如果在 30 天期间，新 Azure Active Directory 用户从具有相同 **ExchangeGuid** 或 **ArchiveGuid** 的原始收件人帐户同步，并且该新帐户已获得 Exchange Online 许可，则会导致硬删除原始用户邮箱。 将永久删除所有邮箱内容，如电子邮件、联系人和文件。
- 使用 **Remove-Mailbox -PermanentlyDelete 删除软删除的邮箱**。

上述删除方案假定用户邮箱未在任何保留状态，如诉讼保留或电子数据展示保留。 如果邮箱上存在任何类型的保留，则不能删除该邮箱。 对于所有邮件用户收件人类型，任何 [保留](https://support.office.com/article/manage-legal-investigations-in-office-365-2e5fbe9f-ee4d-4178-8ff8-4356bc1b168e?ui=en-US&rs=en-US&ad=US) 设置将被忽略，并且对硬删除或软删除没有影响。

## <a name="soft-deleted-and-hard-deleted-items"></a>软删除和硬删除的项目

当用户删除邮箱项目 (例如电子邮件、联系人、日历约会或任务) 时，该项目将移动到"可恢复的项目"文件夹，并移动到名为"Deletions"的子文件夹中。 这称为软删除。 已删除的项目保留在" 删除"文件夹中的时间取决于为邮箱设置的"已删除项目保留期限"。 默认情况下，Exchange Online 邮箱将已删除项目保留 14 天，但 Exchange Online 管理员可以更改此设置，将期限最长增加 30 天。  (有关增加 Exchange Online 邮箱的已删除邮件保留期限的详细步骤，请参阅"更改 [Exchange Online](https://docs.microsoft.com/exchange/recipients-in-exchange-online/manage-user-mailboxes/change-deleted-item-retention)邮箱的永久删除项目保留的时间"。) 用户可以在已删除项目的保留时间过期之前恢复或清除已删除的项目。 为此，他们使用 Microsoft Outlook 或 Web 上的 Outlook 中的"恢复已删除邮件"功能。

如果用户使用 Outlook 或 Web 上的 Outlook 中的"恢复已删除邮件"功能清除已删除的项目，这称为硬删除。 在 Exchange Online 中，新建邮箱时，默认情况下启用单个项目恢复，因此管理员仍可在已删除[](https://docs.microsoft.com/Exchange/recipients/user-mailboxes/recover-deleted-messages)项目的保留期过期之前恢复硬删除的项目。 此外，如果单个项目恢复已启用，那么当用户或进程更改邮件时，原始项目的副本也会予以保留。

## <a name="page-zeroing"></a>页清零

*清零* 是一种安全机制，它通过删除的数据写入零或二进制模式，以便删除的数据更难恢复。 在 Exchange Online 中，邮箱数据库使用 *页面* 作为存储单元，并实现了一个称为页清零 *的覆盖过程*。 默认情况下启用页面清零，客户或 Microsoft 无法禁用它。 在事务日志文件中记录页清零操作，以便以类似方式对给定数据库的所有副本进行页清零。 对主动数据库副本上的页面进行清零会导致在数据库的被动副本上将页面清零。

页清零将二进制模式写入硬删除的记录。 页清零模式特定于可扩展存储引擎 (ESE) 操作 (Exchange Online) 中的服务器使用的内部数据库引擎的名称，与后台数据库维护操作不同。  (后台数据库维护是一个持续校验和和扫描每个数据库的过程。 其主要功能是校验和数据库页，但也处理清理空间和清零由于应用商店崩溃而未清零的记录和页面。) 

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
| 项目根据已删除项目的保留期过期。 | 一个异步线程对删除的数据写入二进制模式。 此操作在数毫秒的记录删除过程中发生。 如果存储进程在异步清零工作仍未完成时崩溃 (或者由于版本存储增长) 而取消版本存储清理，则当后台数据库维护处理数据库的这一部分时，将完成清零。 |
| 视图方案：Outlook/Outlook 网页文件夹视图中的项过期 (例如，会话视图)  | 当后台数据库维护处理该部分数据库时会进行数据清零。 |
| 移动邮箱/删除邮箱方案：已删除的邮箱 (已删除的源邮箱)  | 当后台数据库维护处理该部分数据库时会进行数据清零。 |

### <a name="mailbox-data-types-without-page-zeroing"></a>没有页清零的邮箱数据类型

以下邮箱数据类型没有页面清零设置：

- **邮箱数据库事务** 日志 - 当作为正常操作一部分删除事务日志时，没有进程将存储已删除邮件的日志文件 (文件系统中的块清零) 。 文件系统可能会快速重新利用新创建的日志的可用空间，但无法保证会发生此情况。
- **内容索引目录文件** - Exchange Online 使用 Search Foundation (也称为 FAST) 搜索索引功能。 搜索索引目录由存储在与邮箱数据库文件相同的卷上的几十个文件组成。 当从邮箱数据库中硬删除邮件时，不会立即删除搜索编录中的关联内容。 当 Search Foundation 对多个小 (文件执行卷影) 或主合并操作时，内容删除发生。 主合并完成后，会删除较小的编录文件。 没有将存储已删除目录文件的块清零的过程。

## <a name="continuous-replication"></a>连续复制

连续 (也称为日志寄送和重播) 是 Exchange Online 中的一项技术，用于创建和维护每个邮箱数据库的副本，以提供高可用性、站点恢复和灾难恢复。 连续复制使用Exchange Server故障恢复支持来提供对邮箱数据库的一个或多个副本执行异步更新的技术。 每个邮箱服务器记录对活动数据库数据库 (例如，用户电子邮件活动) 在一组 1 MB 的事务日志文件中作为日志记录。 这组文件称为日志流。 在连续复制中，日志流还用于异步更新数据库的一个或多个副本。 这是通过以下方法完成的：将日志传输到包含主动数据库被动副本的位置，然后将这些日志重播到被动数据库副本中。 如果针对数据库的被动副本重播活动数据库的所有日志，则两个数据库是等效的，并且通过此过程，对活动数据库进行的任何物理更改都将被复制到该数据库的所有被动副本。

从邮箱数据库执行的任何删除操作（无论是邮箱项目还是整个邮箱）以及软删除还是硬删除都表示对活动数据库的物理更改。 页清零还需要对活动数据库进行物理更改。 这些更改通过称为连续复制的过程写入日志文件，当针对数据库的被动副本重播这些日志文件时，将针对这些被动数据库进行相同的物理更改。
