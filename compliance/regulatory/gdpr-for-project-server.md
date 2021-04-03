---
title: 适用于 Project Server 的 GDPR
description: 了解如何解决本地 Project Server 中的一般数据保护条例 (GDPR) 要求。
f1.keywords:
- NOCSH
ms.author: mikeplum
author: MikePlumleyMSFT
manager: pamgreen
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
titleSuffix: Microsoft GDPR
ms.custom: seo-marvel-apr2020
ms.collection: MS-Compliance
hideEdit: true
ms.openlocfilehash: ddbf22523caf1869d0253599216fff07ee14f751
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "51495955"
---
# <a name="gdpr-for-project-server"></a><span data-ttu-id="9b92c-103">适用于 Project Server 的 GDPR</span><span class="sxs-lookup"><span data-stu-id="9b92c-103">GDPR for Project Server</span></span>

<span data-ttu-id="9b92c-p101">Project Server 使用自定义脚本在 Project Web App 中导出和修订用户数据。基本过程是：</span><span class="sxs-lookup"><span data-stu-id="9b92c-p101">Project Server uses custom scripts to export and redact user data in Project Web App. The basic process is:</span></span>

1.  <span data-ttu-id="9b92c-106">在服务器场中找到 Project Web App 网站。</span><span class="sxs-lookup"><span data-stu-id="9b92c-106">Find the Project Web App sites in your farm.</span></span>

2.  <span data-ttu-id="9b92c-107">在包含此用户的每个网站中找到项目。</span><span class="sxs-lookup"><span data-stu-id="9b92c-107">Find the projects in each site that contain the user.</span></span>

3.  <span data-ttu-id="9b92c-108">导出并查看想要查看的数据类型。</span><span class="sxs-lookup"><span data-stu-id="9b92c-108">Export and review the types of data that you want to review.</span></span>

4.  <span data-ttu-id="9b92c-109">根据需要修订数据。</span><span class="sxs-lookup"><span data-stu-id="9b92c-109">Redact data as needed.</span></span>

<span data-ttu-id="9b92c-110">下文详细介绍了这些步骤：</span><span class="sxs-lookup"><span data-stu-id="9b92c-110">These steps are covered in detail in the following articles:</span></span>

- [<span data-ttu-id="9b92c-111">从 Project Server 中导出用户数据</span><span class="sxs-lookup"><span data-stu-id="9b92c-111">Export user data from Project Server</span></span>](/Project/export-user-data-from-project-server?toc=/Office365/Enterprise/toc.json)

- [<span data-ttu-id="9b92c-112">从 Project Server 中删除用户数据</span><span class="sxs-lookup"><span data-stu-id="9b92c-112">Delete user data from Project Server</span></span>](/Project/delete-user-data-from-project-server?toc=/Office365/Enterprise/toc.json)


<span data-ttu-id="9b92c-p102">请注意，Project Server 是在 SharePoint Server 的基础之上构建而成，将事件记录到 SharePoint ULS 日志和使用情况数据库中。有关详细信息，请参阅[适用于 SharePoint Server 的 GDPR](gdpr-for-sharepoint-server.md)。</span><span class="sxs-lookup"><span data-stu-id="9b92c-p102">Note that Project Server is built on top of SharePoint Server and logs events to the SharePoint ULS logs and Usage database. See [GDPR for SharePoint Server](gdpr-for-sharepoint-server.md) for more information.</span></span>
