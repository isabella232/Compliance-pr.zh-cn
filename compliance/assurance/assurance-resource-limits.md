---
title: Microsoft 365 资源限制
description: 本文将介绍 Microsoft 365 中各种应用程序的资源限制。
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
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 632a0b78c5c5ba02a59f8863c2e751f009cc968e
ms.sourcegitcommit: 21ed42335efd37774ff5d17d9586d5546147241a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/05/2021
ms.locfileid: "50120751"
---
# <a name="service-resource-limits"></a>服务资源限制

资源限制是使用配额和 (限制) 强制实施的。 Azure Active Directory (Azure AD) 和单个 Microsoft 365 服务均使用这两者。 限制特定于服务，并随着新功能的添加而发生变化。 有关各种服务的当前限制的详细信息，请参阅下列主题：

- [Azure AD 服务限制](/azure/azure-resource-manager/management/azure-subscription-service-limits)
- [Exchange Online 限制](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits)
- [SharePoint Online 软件边界和限制](https://support.office.com/article/SharePoint-Online-software-boundaries-and-limits-8F34FF47-B749-408B-ABC0-B605E1F6D498)
- [Skype for Business 限制](https://technet.microsoft.com/library/skype-for-business-online-limits.aspx)
- [Yammer REST API 和速率限制](https://developer.yammer.com/docs/rest-api-rate-limits)
- [Sway 中的文件大小限制](https://support.office.com/article/File-size-limits-in-Sway-4db21bc6-b42b-499f-9272-66e089db109f)

除了这些限制之外，Azure AD 和 Microsoft 365 中还使用了多个限制机制。 鉴于 Microsoft 数据中心中的网络资源已针对使用服务的广泛客户进行了优化，服务中的限制尤其重要。 限制机制包括：

- Azure AD 和 Microsoft 365 功能用户级限制，通过脚本或代码限制 (可以由单个用户执行的) 或并发呼叫数。
- 创建租户时，会为每个租户分配一个默认的 PowerShell 限制策略。 这些设置会影响其他项目，例如单个管理员可同时打开的最大 PowerShell 会话数。
- 每个 Exchange Online 客户都有一个默认的 Exchange Web Services (EWS) 策略，该策略针对 EWS 客户端操作进行了调整，并且限制适用于所有 Outlook 客户端。
