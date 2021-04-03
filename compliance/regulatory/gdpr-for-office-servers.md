---
title: 用于 Office Server 的 GDPR
description: 了解如何解决 Office 本地服务器中的一般数据保护条例 (GDPR) 要求。
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
ms.collection: MS-Compliance
ms.custom: seo-marvel-apr2020
hideEdit: true
ms.openlocfilehash: 58f3d9108fe36175c2ce879054a35c2cc94d93c8
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496082"
---
# <a name="gdpr-for-office-on-premises-servers"></a>用于本地 Office 服务器的 GDPR

一般数据保护条例 (GDPR) 为组织提供了保护个人数据和适当回应数据主体请求的要求。本系列文章为本地工作负载提供了推荐的方法：

- [SharePoint Server](gdpr-for-sharepoint-server.md)

- [Exchange Server](gdpr-for-exchange-server.md)

- [Skype for Business Server](gdpr-for-skype-for-business-server.md)

- [Project Server](gdpr-for-project-server.md)

- [Office Web Apps Server 和 Office Online Server](gdpr-for-office-online-server.md)

- [本地文件共享](gdpr-for-on-premises-file-shares.md)

有关 GDPR 以及 Microsoft 如何为你提供帮助的详细信息，请参阅 [Microsoft 信任中心](https://www.microsoft.com/trust-center/privacy/gdpr-overview
)。

在开展有关本地数据的任何工作之前，请咨询你的法律和合规性团队以寻求指导并了解现有分类架构和处理个人数据的方法。Microsoft 提供了有关在 Microsoft GDPR 数据发现工具包（位于 [https://aka.ms/gdprpartners](<https://aka.ms/gdprpartners>)）中开发和扩展分类架构的建议。此工具包还介绍了将本地数据移动到云的方法，可以使用更复杂的数据治理功能（如果需要）。该部分中的文章提供了有关保留在本地的数据的建议。

下图列出了在各个工作负载中使用的推荐功能，用于发现、保护和监视个人数据并对其进行分类。有关更多信息，请参阅该部分中的文章。

![描述跨工作负载发现、分类、保护和监视个人数据的功能图表](../media/gdpr-for-office-servers-image1.png)

## <a name="illustration-description"></a>图示说明

为便于访问，下表提供了上图中的相同示例。

****

|操作|Windows Server 文件共享|SharePoint Server|Exchange Server|Skype for Business|Project Server|
|---|---|---|---|---|---|
|发现|Azure 信息保护扫描程序<sup>\*</sup>|搜索中心或电子数据展示（对数据进行分类后） <br/><br/> Azure 信息保护扫描程序<sup>\*</sup>|Exchange 电子数据展示门户|Exchange 电子数据展示门户|用于发现和导出的 SQL 脚本|
|分类|Azure 信息保护扫描程序<sup>\*</sup> <br/><br/> Office 365 敏感信息类型|Azure 信息保护扫描程序<sup>\*</sup> <br/><br/> Office 365 敏感信息类型|Exchange 保留标记和保留策略|Exchange 保留标记和保留策略||
|保护||Exchange Server 数据丢失防护规则 <br/><br/> 权限、库 IRM-保护|Exchange Server 数据丢失防护规则 <br/><br/> IRM 与 Exchange Server 的集成|||
|监视|将日志与 SIEM 工具集成|将日志与 SIEM 工具集成|将日志与 SIEM 工具集成|将日志与 SIEM 工具集成|将日志与 SIEM 工具集成|
|

<sup>\*</sup>注意，保护功能会加密文件。 因此，SharePoint Server 无法在受保护的文件中查找敏感信息类型。
