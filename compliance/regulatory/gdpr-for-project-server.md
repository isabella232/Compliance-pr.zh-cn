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
ms.openlocfilehash: 092bbe9e7abe0329e822b011d41b5db96f33d169606945f5801bc36771a1944c
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "54292939"
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
