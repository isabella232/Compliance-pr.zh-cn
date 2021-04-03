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
# <a name="gdpr-for-project-server"></a>适用于 Project Server 的 GDPR

Project Server 使用自定义脚本在 Project Web App 中导出和修订用户数据。基本过程是：

1.  在服务器场中找到 Project Web App 网站。

2.  在包含此用户的每个网站中找到项目。

3.  导出并查看想要查看的数据类型。

4.  根据需要修订数据。

下文详细介绍了这些步骤：

- [从 Project Server 中导出用户数据](/Project/export-user-data-from-project-server?toc=/Office365/Enterprise/toc.json)

- [从 Project Server 中删除用户数据](/Project/delete-user-data-from-project-server?toc=/Office365/Enterprise/toc.json)


请注意，Project Server 是在 SharePoint Server 的基础之上构建而成，将事件记录到 SharePoint ULS 日志和使用情况数据库中。有关详细信息，请参阅[适用于 SharePoint Server 的 GDPR](gdpr-for-sharepoint-server.md)。
