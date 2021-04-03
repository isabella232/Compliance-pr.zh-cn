---
title: 传输中数据的加密
description: 本文介绍 Microsoft 如何加密传输中的 Microsoft 365 客户数据。
ms.author: krowley
author: kccross
manager: laurawi
ms.reviewer: sosstah
f1.keywords:
- NOCSH
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
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
ms.openlocfilehash: 227f74140ecd9b6283b92e8b0e87bd70912ec8e3
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497254"
---
# <a name="encryption-for-data-in-transit"></a><span data-ttu-id="ecbb1-103">传输中数据的加密</span><span class="sxs-lookup"><span data-stu-id="ecbb1-103">Encryption for data-in-transit</span></span>

<span data-ttu-id="ecbb1-104">除了保护静态客户数据之外，Microsoft 还使用加密技术来保护传输中的客户数据。</span><span class="sxs-lookup"><span data-stu-id="ecbb1-104">In addition to protecting customer data at rest, Microsoft uses encryption technologies to protect customer data in transit.</span></span> <span data-ttu-id="ecbb1-105">数据正在传输：</span><span class="sxs-lookup"><span data-stu-id="ecbb1-105">Data is in transit:</span></span>

- <span data-ttu-id="ecbb1-106">当客户端计算机与 Microsoft 服务器通信时;</span><span class="sxs-lookup"><span data-stu-id="ecbb1-106">when a client machine communicates with a Microsoft server;</span></span>
- <span data-ttu-id="ecbb1-107">当 Microsoft 服务器与其他 Microsoft 服务器通信时;和</span><span class="sxs-lookup"><span data-stu-id="ecbb1-107">when a Microsoft server communicates with another Microsoft server; and</span></span>
- <span data-ttu-id="ecbb1-108">当 Microsoft 服务器与非 Microsoft 服务器通信时 (例如，Exchange Online 将电子邮件传递至第三方电子邮件服务器) 。</span><span class="sxs-lookup"><span data-stu-id="ecbb1-108">when a Microsoft server communicates with a non-Microsoft server (for example, Exchange Online delivering email to a third-party email server).</span></span>

<span data-ttu-id="ecbb1-109">Microsoft 服务器之间的数据中心间通信通过 TLS 或 IPsec 进行，所有面向客户的服务器都使用 TLS 与客户端计算机协商安全会话 (例如，Exchange Online 使用 TLS 1.2 和 256 位加密强度 (FIPS 140-2 级别 2 验证) 。</span><span class="sxs-lookup"><span data-stu-id="ecbb1-109">Inter-data center communications between Microsoft servers take place over TLS or IPsec, and all customer-facing servers negotiate a secure session using TLS with client machines (for example, Exchange Online uses TLS 1.2 with 256-bit cipher strength is used (FIPS 140-2 Level 2-validated).</span></span> <span data-ttu-id="ecbb1-110"> (请参阅有关加密[](/microsoft-365/compliance/technical-reference-details-about-encryption)的技术参考详细信息，了解 Office 365.) 支持的 TLS 密码套件列表。这适用于 Outlook、Skype for Business、Microsoft Teams 和 Web 上的 Outlook (例如 HTTP、POP3 等 ) 等客户端使用的协议。</span><span class="sxs-lookup"><span data-stu-id="ecbb1-110">(See [Technical reference details about encryption](/microsoft-365/compliance/technical-reference-details-about-encryption) for a list of TLS cipher suites supported by Office 365.) This applies to the protocols that are used by clients such as Outlook, Skype for Business, Microsoft Teams, and Outlook on the web (for example, HTTP, POP3, etc.).</span></span>

<span data-ttu-id="ecbb1-111">公共证书由 Microsoft IT SSL 使用 SSLAdmin 颁发，这是一种用于保护传输信息的机密性的内部 Microsoft 工具。</span><span class="sxs-lookup"><span data-stu-id="ecbb1-111">The public certificates are issued by Microsoft IT SSL using SSLAdmin, an internal Microsoft tool to protect confidentiality of transmitted information.</span></span> <span data-ttu-id="ecbb1-112">Microsoft IT 颁发的所有证书长度至少为 2048 位，并且 Webtrust 合规性要求 SSLAdmin 确保证书仅颁发给 Microsoft 拥有的公用 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="ecbb1-112">All certificates issued by Microsoft IT have a minimum of 2048 bits in length, and Webtrust compliance requires SSLAdmin to make sure that certificates are issued only to public IP addresses owned by Microsoft.</span></span> <span data-ttu-id="ecbb1-113">任何不符合此标准的 IP 地址都通过异常过程进行路由。</span><span class="sxs-lookup"><span data-stu-id="ecbb1-113">Any IP addresses that fail to meet this criterion are routed through an exception process.</span></span>

<span data-ttu-id="ecbb1-114">所有实现详细信息（如所使用的 TLS 版本、是否启用前向保密 (FS) 、密码套件的顺序等）都公开提供。</span><span class="sxs-lookup"><span data-stu-id="ecbb1-114">All implementation details such as the version of TLS being used, whether Forward Secrecy (FS) is enabled, the order of cipher suites, etc., are available publicly.</span></span> <span data-ttu-id="ecbb1-115">查看这些详细信息的一种方式是使用第三方网站，如[Qualys SSL Labs。](https://www.ssllabs.com)</span><span class="sxs-lookup"><span data-stu-id="ecbb1-115">One way to see these details is to use a third-party website, such as [Qualys SSL Labs](https://www.ssllabs.com).</span></span> <span data-ttu-id="ecbb1-116">下面是指向 Qualys 中的自动测试页面的链接，这些页面显示以下服务的信息：</span><span class="sxs-lookup"><span data-stu-id="ecbb1-116">Below are the links to automated test pages from Qualys that display information for the following services:</span></span>

- [<span data-ttu-id="ecbb1-117">Office 365 门户</span><span class="sxs-lookup"><span data-stu-id="ecbb1-117">Office 365 Portal</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=portal.office.com&hideResults=on)
- [<span data-ttu-id="ecbb1-118">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="ecbb1-118">Exchange Online</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=outlook.office365.com&hideResults=on)
- [<span data-ttu-id="ecbb1-119">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="ecbb1-119">SharePoint Online</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=microsoft-my.sharepoint.com&hideResults=on)
- [<span data-ttu-id="ecbb1-120">Skype for Business (SIP) </span><span class="sxs-lookup"><span data-stu-id="ecbb1-120">Skype for Business (SIP)</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=sipdir.online.lync.com)
- [<span data-ttu-id="ecbb1-121">Skype for Business (Web) </span><span class="sxs-lookup"><span data-stu-id="ecbb1-121">Skype for Business (Web)</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=webdir.online.lync.com&hideResults=on)
- [<span data-ttu-id="ecbb1-122">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="ecbb1-122">Exchange Online Protection</span></span>](https://ssl-tools.net/mailservers/microsoft-com.mail.protection.outlook.com)
- [<span data-ttu-id="ecbb1-123">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="ecbb1-123">Microsoft Teams</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=teams.microsoft.com&latest)

<span data-ttu-id="ecbb1-124">对于 Exchange Online Protection，URL 因租户名称而异;但是，所有客户都可以使用 microsoft-com.mail.protection.outlook.com 测试 Microsoft 365。 </span><span class="sxs-lookup"><span data-stu-id="ecbb1-124">For Exchange Online Protection, URLs vary by tenant names; however, all customers can test Microsoft 365 using **microsoft-com.mail.protection.outlook.com**.</span></span>
