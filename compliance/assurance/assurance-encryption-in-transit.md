---
title: 传输中数据的加密
description: 本文将简要介绍 Microsoft 如何加密传输Microsoft 365客户数据。
ms.author: krowley
author: kccross
manager: laurawi
ms.reviewer: sosstah
f1.keywords:
- NOCSH
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.localizationpriority: medium
search.appverid:
- MET150
ms.collection:
- Strat_O365_Enterprise
- M365-security-compliance
- Strat_O365_Enterprise
- MS-Compliance
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: ebeface33b0d5ba419773c13305c277d681e8400
ms.sourcegitcommit: 4c00fd65d418065d7f53216c91f455ccb3891c77
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/23/2021
ms.locfileid: "58482014"
---
# <a name="encryption-for-data-in-transit"></a>传输中数据的加密

除了保护静态客户数据之外，Microsoft 还使用加密技术来保护传输中的客户数据。 数据正在传输：

- 当客户端计算机与 Microsoft 服务器通信时;
- 当 Microsoft 服务器与其他 Microsoft 服务器通信时;和
- 例如，当 Microsoft 服务器与非 Microsoft (通信时，Exchange Online将电子邮件传送给第三方电子邮件) 。

Microsoft 服务器之间的数据中心间通信通过 TLS 或 IPsec 进行，所有面向客户的服务器都使用 TLS 与客户端计算机协商安全会话 (例如，Exchange Online 使用 TLS 1.2 和 256 位加密强度 (FIPS 140-2 级别 2 验证) 。  (请参阅有关[](/microsoft-365/compliance/technical-reference-details-about-encryption)加密的技术参考详细信息，了解 Office 365.) 支持的 TLS 密码套件列表。这适用于 Outlook、Skype for Business、Microsoft Teams 和 Outlook 网页版 (等客户端使用的协议，例如 HTTP、POP3 等 ) 。

公共证书由 Microsoft IT SSL 使用 SSLAdmin 颁发，这是一种用于保护传输信息的机密性的内部 Microsoft 工具。 Microsoft IT 颁发的所有证书长度至少为 2048 位，并且 Webtrust 合规性要求 SSLAdmin 确保仅将证书颁发给 Microsoft 所有的公用 IP 地址。 任何不符合此标准的 IP 地址都通过异常过程进行路由。

所有实现详细信息（如所使用的 TLS 版本、是否启用前向保密 (FS) 、密码套件的顺序等）都公开提供。 查看这些详细信息的一种方式是使用第三方网站，如[Qualys SSL Labs。](https://www.ssllabs.com) 下面是指向 Qualys 中的自动测试页面的链接，这些页面显示以下服务的信息：

- [Office 365门户](https://www.ssllabs.com/ssltest/analyze.html?d=portal.office.com&hideResults=on)
- [Exchange Online](https://www.ssllabs.com/ssltest/analyze.html?d=outlook.office365.com&hideResults=on)
- [SharePoint Online](https://www.ssllabs.com/ssltest/analyze.html?d=microsoft-my.sharepoint.com&hideResults=on)
- [Skype for Business (SIP) ](https://www.ssllabs.com/ssltest/analyze.html?d=sipdir.online.lync.com)
- [Skype for Business (Web) ](https://www.ssllabs.com/ssltest/analyze.html?d=webdir.online.lync.com&hideResults=on)
- [Exchange Online Protection](https://ssl-tools.net/mailservers/microsoft-com.mail.protection.outlook.com)
- [Microsoft Teams](https://www.ssllabs.com/ssltest/analyze.html?d=teams.microsoft.com&latest)

例如Exchange Online Protection，URL 因租户名称而异;但是，所有客户都可以使用 Microsoft 365 测试 **microsoft-com.mail.protection.outlook.com。**
