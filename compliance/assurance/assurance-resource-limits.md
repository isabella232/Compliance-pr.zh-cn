---
title: Microsoft 365资源限制
description: 在本文中，您可以找到有关应用程序内各种应用程序的资源Microsoft 365。
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
ms.openlocfilehash: 764259e22b23ecc7cea363283fc313a94875a2d1
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/12/2021
ms.locfileid: "59158302"
---
# <a name="service-resource-limits"></a>服务资源限制

使用配额和限制 (限制) 资源限制。 Azure Active Directory (Azure AD) 和单个 Microsoft 365 服务都使用这两者。 限制特定于服务，并随着新功能的添加而发生变化。 有关各种服务的当前限制的详细信息，请参阅下列主题：

- [Azure AD 服务限制](/azure/azure-resource-manager/management/azure-subscription-service-limits)
- [Exchange Online 限制](/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits)
- [SharePoint联机软件边界和限制](https://support.office.com/article/SharePoint-Online-software-boundaries-and-limits-8F34FF47-B749-408B-ABC0-B605E1F6D498)
- [Skype for Business限制](https://technet.microsoft.com/library/skype-for-business-online-limits.aspx)
- [YammerREST API 和速率限制](https://developer.yammer.com/docs/rest-api-rate-limits)
- [Sway 中的文件大小限制](https://support.office.com/article/File-size-limits-in-Sway-4db21bc6-b42b-499f-9272-66e089db109f)

除了这些限制之外，Azure AD 和 Azure 服务中还使用了一些Microsoft 365。 服务中的限制尤为重要，因为 Microsoft 数据中心的网络资源已针对使用服务的广泛客户进行了优化。 限制机制包括：

- Azure AD 和 Microsoft 365 功能用户级别限制，通过脚本或代码) 按单个用户执行的 (限制事务数或并发呼叫数。
- 默认 PowerShell 限制策略在租户创建时分配给每个租户。 这些设置会影响其他项目，例如单个管理员可同时打开的最大 PowerShell 会话数。
- 每个Exchange Online客户都有一个针对 EWS 客户端操作Exchange EWS (EWS) 的默认策略，以及适用于所有 Outlook 客户端Outlook策略。
