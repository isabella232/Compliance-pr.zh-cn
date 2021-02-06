---
title: Microsoft 365 SharePoint Online 数据删除
description: 了解数据删除在 SharePoint Online 中的工作方式，例如存储已删除内容的位置和时间。
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
- SPO_Content
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 89281b32dbc577f935224396fd358ed753348ea1
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120741"
---
# <a name="sharepoint-online-data-deletion-in-microsoft-365"></a>Microsoft 365 中的 SharePoint Online 数据删除

SharePoint Online 将对象存储为应用程序数据库中的抽象代码。 当用户将文件上载到 SharePoint Online 时，该文件会分解并转换为应用程序代码，并存储在多个数据库中的多个表中。 在 SharePoint Online 中，客户上载的所有内容都分为多个区块、使用 (多个 AES 256 位密钥加密) 分布在数据中心。 有关分块和加密过程的特定详细信息，请参阅 [Microsoft 云中的加密](/microsoft-365/compliance/office-365-encryption-in-the-microsoft-cloud-overview)。 

在 SharePoint Online 中，项目从从原始位置删除起保留 93 天。 它们一直留在网站回收站中，除非有人从回收站中删除它们或清空该回收站。 在这种情况下，项目将转到网站集回收站，在 93 天的剩余时间内将留在回收站中。 有关还原已删除项目的信息，请参阅"还原[SharePoint](https://support.office.com/article/6df466b6-55f2-4898-8d6e-c0dff851a0be#ID0EAADAAA=Online
)网站的回收站中的项目"和"从网站集回收站还原已删除[的项目"。](https://support.office.com/article/5fa924ee-16d7-487b-9a0a-021b9062d14b) 回收站保留时间在 SharePoint Online 中不可配置。

删除网站集时，还将删除网站集中的网站层次结构及其中所有内容：

- 文档和文档库
- 列表和列表数据
- 站点配置设置
- 与网站及其子网站相关的角色和安全信息
- 首要网站的子网站、其内容和用户信息

如果意外删除了网站集，全局管理员或 SharePoint 管理员可以使用 SharePoint 管理中心还原该网站集。

已删除的网站集将保留 93 天。 93天后，将永久删除网站及其所有内容和设置，包括列表、库、页面和所有子网站。

硬删除发生在用户清除网站集回收站中的已删除项目、保留期和备份期过期时，或者管理员使用 [Remove-SPODeletedSite cmdlet](/powershell/module/sharepoint-online/remove-spodeletedsite)永久删除网站集时。 当用户硬删除或 (从 SharePoint Online) 内容时，也将删除已删除区块的所有加密密钥。 以前存储已删除区块的磁盘上的块被标记为未使用且可供重新使用。
