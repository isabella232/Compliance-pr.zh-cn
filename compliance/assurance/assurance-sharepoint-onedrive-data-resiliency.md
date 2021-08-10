---
title: Microsoft 365 中的 SharePoint和OneDrive 数据弹性
description: 本文概述了数据恢复SharePoint OneDrive数据复原Microsoft 365。
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
f1.keywords:
- NOCSH
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 8b2c0cea5ea9af46b947fe8e3f76a8c17bd86494837073be77e1c7894270e97b
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "54292072"
---
# <a name="sharepoint-and-onedrive-data-resiliency-in-microsoft-365"></a>Microsoft 365 中的 SharePoint和OneDrive 数据弹性

在Microsoft 365中，OneDrive构建于 SharePoint 文件平台的顶部。 本文仅SharePoint引用这两个产品。 本文的内容与使用者服务Microsoft 365，不适用于消费者服务。

有两种主要资产，它们决定着网站的核心SharePoint：

- **元数据**：每个文件的元数据存储在Azure SQL 数据库。 Azure SQL提供了完整的业务连续性情景，SharePoint本文稍后将介绍具体使用和详细信息。
- **Blob 存储**：上载到服务器的用户SharePoint存储在Azure 存储。 SharePoint构建了一个自定义恢复能力计划，Azure 存储以确保几乎实时复制用户内容和真正处于活动状态/主动的系统。

用于确保数据恢复的完整控件集在更多部分中进行了说明。

## <a name="blob-storage-resilience"></a>Blob 存储恢复

SharePoint一个自定义解决方案，用于将客户数据存储在 Azure 存储。 每个文件同时写入主和辅助数据中心区域。 如果写入任一 Azure 区域失败，文件保存将失败。 将内容写入 Azure 存储 后，校验和会与元数据一起单独存储，并用于确保在以后读取过程中，提交写入与发送到 SharePoint 的原始文件相同。 在所有工作流中使用相同的技术，以防止应发生任何损坏的传播。 在每个区域内，Azure 本地冗余存储 (LRS) 提供了高级别的可靠性。 有关详细信息[，Azure 存储](/azure/storage/common/storage-redundancy-lrs)冗余一文。

SharePoint使用Append-Only存储。 此过程可确保在初始保存后文件不会更改或损坏，但通过使用产品内版本控制，可以检索任何以前版本的文件内容。

![Blob 存储恢复](../media/assurance-blob-storage-resiliency-diagram.png)

SharePoint数据中心内的环境可以访问两个 Azure 区域的存储容器。 出于性能原因，始终首选同一本地数据中心中的存储容器，但是，未在所需阈值内查看结果的读取请求将具有从远程数据中心请求的相同内容，以确保数据始终可用。

## <a name="metadata-resilience"></a>元数据恢复

SharePoint元数据对于访问用户内容也至关重要，因为它存储存储在用户内容中的内容的位置和访问Azure 存储。 这些数据库存储在 Azure SQL中，其中具有广泛的[业务连续性计划](/azure/sql-database/sql-database-business-continuity)。

SharePoint Azure SQL 提供的复制模型，并构建了专有自动化技术来确定需要故障转移并在必要时启动操作。 因此，从 Azure 和 Azure 的角度看，它属于"手动数据库SQL类别。 Azure 数据库可恢复SQL的最新指标在此处[提供](/azure/azure-sql/database/business-continuity-high-availability-disaster-recover-hadr-overview#recover-a-database-to-the-existing-server)。

![元数据恢复](../media/assurance-metadata-resiliency-diagram.png)

SharePoint Azure SQL 备份系统在 PITR (启用时间点还原) 最多 14 天。 将稍后部分对 PITR [进行更多介绍。](#deletion-backup-and-point-in-time-restore)

## <a name="automated-failover"></a>自动故障转移

SharePoint自定义的自动化故障转移，以在特定于位置的事件发生时最大程度地降低对客户体验的影响。 监控驱动的自动化检测超出特定阈值的单组件或多组件故障将导致所有用户的活动从有问题的环境中自动重定向到温辅助环境。 故障转移会导致元数据和计算存储完全从新数据中心提供。 由于 blob 存储始终完全处于活动状态/处于活动状态，因此故障转移不需要任何更改。 计算层将首选最近的 blob 容器，但将随时使用本地和远程 blob 存储位置以确保可用性。

SharePoint Azure Front Door 服务提供到 Microsoft 网络内部的路由。 此配置允许独立于 DNS 的故障转移重定向，并减少本地计算机缓存的影响。 大多数故障转移操作对最终用户都是透明的。 如果存在故障转移，则客户无需进行任何更改，即维护对服务的访问权限。

## <a name="versioning-and-files-restore"></a>版本控制与文件还原

对于新创建的文档库，SharePoint每个文件默认为 500 个版本，并可以配置为保留更多版本（如果需要）。 UI 不允许设置少于 100 个版本的值，但可以设置系统以使用公用 API 存储较少的版本。 为了可靠性，不建议使用小于 100 的任何值，这可能会导致用户活动导致意外的数据丢失。

有关版本控制详细信息，请参阅 SharePoint 中的[版本控制](/microsoft-365/community/versioning-basics-best-practices)。

文件还原是一种在任意时间上"返回"文档库SharePoint到过去 30 天内的任何秒。 此过程可用于从勒索软件、批量删除、损坏或其他任何事件恢复。 此功能使用文件版本，因此减少默认版本会降低此还原的有效性。

文件还原功能已针对 OneDrive 和[SharePoint](https://support.office.com/article/restore-your-onedrive-fa231298-759d-41cf-bcd0-25ac53eb8a15)进行[记录](https://support.office.com/article/Restore-a-document-library-317791c3-8bd0-4dfd-8254-3ca90883d39a)。

## <a name="deletion-backup-and-point-in-time-restore"></a>删除、备份和时间点还原

从网站中删除的用户SharePoint将经过以下删除流。

已删除的项目在回收站中保留一段时间。 对于SharePoint，保留时间为 93 天。 从项目的原始位置删除项目时，它将开始。 当您从网站回收站中删除项目时，它会进入 [网站集回收站](https://support.office.com/article/restore-deleted-items-from-the-site-collection-recycle-bin-5fa924ee-16d7-487b-9a0a-021b9062d14b)。 它将在剩余的 93 天内保留，然后永久删除。 有关如何使用回收站的信息，请参阅以下链接：

- [还原回收站中的项目](https://support.office.com/article/Restore-items-in-the-Recycle-Bin-of-a-SharePoint-site-6df466b6-55f2-4898-8d6e-c0dff851a0be)
- [从网站集回收站还原已删除的项目](https://support.office.com/article/Restore-deleted-items-from-the-site-collection-recycle-bin-5fa924ee-16d7-487b-9a0a-021b9062d14b)。

此过程是默认删除流，不会考虑保留策略或标签。 有关详细信息，请参阅了解[SharePoint 和 OneDrive](/microsoft-365/compliance/retention-policies-sharepoint)的保留。

完成 93 天的回收管道后，将单独对元数据和 Blob 项目执行存储。 将立即从数据库中删除元数据，这使得内容不可读，除非从备份中还原元数据。 SharePoint维护 14 天的元数据备份。 根据此发布时的文档，这些备份以近实时状态本地进行，然后推送到冗余 Azure 存储 容器中的存储[](/azure/sql-database/sql-database-automated-backups)，计划为 5-10 分钟。

删除 Blob 存储内容时，SharePoint Azure Blob 文件的软删除存储防止意外或恶意删除。 使用此功能，我们总共有 14 天的时间在内容被永久删除之前还原内容。

>[!Note]
>虽然 Microsoft 应用程序将内容发送到标准进程的回收站，SharePoint提供允许跳过回收站并强制立即删除的 API。 检查应用程序以确保仅在出于合规性原因需要时完成此操作。

## <a name="integrity-checks"></a>完整性检查

SharePoint使用各种方法来确保数据生命周期所有阶段的 blob 和元数据的完整性：

- **存储在元数据中的** 文件哈希：整个文件的哈希与文件元数据一起存储，以确保在所有操作过程中保持文档级别数据完整性
- **存储在元数据中的 Blob** 哈希：每个 blob 项存储加密内容的哈希，以防范基础 Azure 存储中的损坏。
- **数据完整性作业**：每 14 天，通过列出数据库中的项目，并匹配 Azure 存储中所列 blob 来扫描每个网站的完整性。 作业报告任何缺少存储 blob 的 blob 引用，并在需要时通过 Azure 存储 [软删除](/azure/storage/blobs/soft-delete-blob-overview) 功能检索这些 blob。
