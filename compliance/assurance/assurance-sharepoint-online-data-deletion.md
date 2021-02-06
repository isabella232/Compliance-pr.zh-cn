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
# <a name="sharepoint-online-data-deletion-in-microsoft-365"></a><span data-ttu-id="7e0a8-103">Microsoft 365 中的 SharePoint Online 数据删除</span><span class="sxs-lookup"><span data-stu-id="7e0a8-103">SharePoint Online data deletion in Microsoft 365</span></span>

<span data-ttu-id="7e0a8-104">SharePoint Online 将对象存储为应用程序数据库中的抽象代码。</span><span class="sxs-lookup"><span data-stu-id="7e0a8-104">SharePoint Online stores objects as abstracted code within application databases.</span></span> <span data-ttu-id="7e0a8-105">当用户将文件上载到 SharePoint Online 时，该文件会分解并转换为应用程序代码，并存储在多个数据库中的多个表中。</span><span class="sxs-lookup"><span data-stu-id="7e0a8-105">When a user uploads a file to SharePoint Online, that file is disassembled and translated into application code and stored in multiple tables across multiple databases.</span></span> <span data-ttu-id="7e0a8-106">在 SharePoint Online 中，客户上载的所有内容都分为多个区块、使用 (多个 AES 256 位密钥加密) 分布在数据中心。</span><span class="sxs-lookup"><span data-stu-id="7e0a8-106">In SharePoint Online, all content that a customer uploads is broken into chunks, encrypted (potentially with multiple AES 256-bit keys), and distributed across the datacenter.</span></span> <span data-ttu-id="7e0a8-107">有关分块和加密过程的特定详细信息，请参阅 [Microsoft 云中的加密](/microsoft-365/compliance/office-365-encryption-in-the-microsoft-cloud-overview)。</span><span class="sxs-lookup"><span data-stu-id="7e0a8-107">For specific details about the chunking and encryption process, see [Encryption in the Microsoft Cloud](/microsoft-365/compliance/office-365-encryption-in-the-microsoft-cloud-overview).</span></span> 

<span data-ttu-id="7e0a8-108">在 SharePoint Online 中，项目从从原始位置删除起保留 93 天。</span><span class="sxs-lookup"><span data-stu-id="7e0a8-108">In SharePoint Online, items are retained for 93 days from the time you delete them from their original location.</span></span> <span data-ttu-id="7e0a8-109">它们一直留在网站回收站中，除非有人从回收站中删除它们或清空该回收站。</span><span class="sxs-lookup"><span data-stu-id="7e0a8-109">They stay in the site Recycle Bin the entire time, unless someone deletes them from there or empties that Recycle Bin.</span></span> <span data-ttu-id="7e0a8-110">在这种情况下，项目将转到网站集回收站，在 93 天的剩余时间内将留在回收站中。</span><span class="sxs-lookup"><span data-stu-id="7e0a8-110">In that case, the items go to the site collection Recycle Bin, where they stay for the remainder of the 93 days.</span></span> <span data-ttu-id="7e0a8-111">有关还原已删除项目的信息，请参阅"还原[SharePoint](https://support.office.com/article/6df466b6-55f2-4898-8d6e-c0dff851a0be#ID0EAADAAA=Online
)网站的回收站中的项目"和"从网站集回收站还原已删除[的项目"。](https://support.office.com/article/5fa924ee-16d7-487b-9a0a-021b9062d14b)</span><span class="sxs-lookup"><span data-stu-id="7e0a8-111">For info about restoring deleted items, see [Restore items in the Recycle Bin of a SharePoint site](https://support.office.com/article/6df466b6-55f2-4898-8d6e-c0dff851a0be#ID0EAADAAA=Online
) and [Restore deleted items from the site collection recycle bin](https://support.office.com/article/5fa924ee-16d7-487b-9a0a-021b9062d14b).</span></span> <span data-ttu-id="7e0a8-112">回收站保留时间在 SharePoint Online 中不可配置。</span><span class="sxs-lookup"><span data-stu-id="7e0a8-112">The Recycle Bin retention time is not configurable in SharePoint Online.</span></span>

<span data-ttu-id="7e0a8-113">删除网站集时，还将删除网站集中的网站层次结构及其中所有内容：</span><span class="sxs-lookup"><span data-stu-id="7e0a8-113">When you delete a site collection, you're also deleting the hierarchy of sites in the collection, and all content within them:</span></span>

- <span data-ttu-id="7e0a8-114">文档和文档库</span><span class="sxs-lookup"><span data-stu-id="7e0a8-114">Documents and document libraries</span></span>
- <span data-ttu-id="7e0a8-115">列表和列表数据</span><span class="sxs-lookup"><span data-stu-id="7e0a8-115">Lists and list data</span></span>
- <span data-ttu-id="7e0a8-116">站点配置设置</span><span class="sxs-lookup"><span data-stu-id="7e0a8-116">Site configuration settings</span></span>
- <span data-ttu-id="7e0a8-117">与网站及其子网站相关的角色和安全信息</span><span class="sxs-lookup"><span data-stu-id="7e0a8-117">Role and security information that is related to the site or its subsites</span></span>
- <span data-ttu-id="7e0a8-118">首要网站的子网站、其内容和用户信息</span><span class="sxs-lookup"><span data-stu-id="7e0a8-118">Subsites of the top-level website, their contents, and user information</span></span>

<span data-ttu-id="7e0a8-119">如果意外删除了网站集，全局管理员或 SharePoint 管理员可以使用 SharePoint 管理中心还原该网站集。</span><span class="sxs-lookup"><span data-stu-id="7e0a8-119">If you accidentally delete a site collection, it can be restored by a global or SharePoint admin using the SharePoint admin center.</span></span>

<span data-ttu-id="7e0a8-120">已删除的网站集将保留 93 天。</span><span class="sxs-lookup"><span data-stu-id="7e0a8-120">Deleted site collections are retained for 93 days.</span></span> <span data-ttu-id="7e0a8-121">93天后，将永久删除网站及其所有内容和设置，包括列表、库、页面和所有子网站。</span><span class="sxs-lookup"><span data-stu-id="7e0a8-121">After 93 days, sites and all their content and settings are permanently deleted, including lists, libraries, pages, and any subsites.</span></span>

<span data-ttu-id="7e0a8-122">硬删除发生在用户清除网站集回收站中的已删除项目、保留期和备份期过期时，或者管理员使用 [Remove-SPODeletedSite cmdlet](/powershell/module/sharepoint-online/remove-spodeletedsite)永久删除网站集时。</span><span class="sxs-lookup"><span data-stu-id="7e0a8-122">Hard deletion occurs when a user purges deleted items from the site collection Recycle Bin, when the retention and backup periods expire, or when an administrator permanently deletes a site collection using the [Remove-SPODeletedSite cmdlet](/powershell/module/sharepoint-online/remove-spodeletedsite).</span></span> <span data-ttu-id="7e0a8-123">当用户硬删除或 (从 SharePoint Online) 内容时，也将删除已删除区块的所有加密密钥。</span><span class="sxs-lookup"><span data-stu-id="7e0a8-123">When a user hard deletes (permanently deletes, or purges) content from SharePoint Online, all encryption keys for the deleted chunks are also deleted.</span></span> <span data-ttu-id="7e0a8-124">以前存储已删除区块的磁盘上的块被标记为未使用且可供重新使用。</span><span class="sxs-lookup"><span data-stu-id="7e0a8-124">The blocks on the disks that previously stored the deleted chunks are marked as unused and available for re-use.</span></span>
