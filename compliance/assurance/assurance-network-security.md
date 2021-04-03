---
title: 网络安全性
description: 了解 Microsoft 365 中的网络安全
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: a2b153b2f2f57a011c28ee65cbe03019cbaa27a1
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496924"
---
# <a name="network-security-overview"></a><span data-ttu-id="e8ad5-103">网络安全性概述</span><span class="sxs-lookup"><span data-stu-id="e8ad5-103">Network security overview</span></span>

## <a name="how-does-microsoft-365-secure-the-network-boundary"></a><span data-ttu-id="e8ad5-104">Microsoft 365 如何保护网络边界？</span><span class="sxs-lookup"><span data-stu-id="e8ad5-104">How does Microsoft 365 secure the network boundary?</span></span>

<span data-ttu-id="e8ad5-105">Microsoft 365 采用多种策略来保护其网络边界，包括自动检测和防护基于网络的攻击、专用防火墙设备以及 Exchange Online Protection (EOP) 用于反垃圾邮件和反恶意软件保护。</span><span class="sxs-lookup"><span data-stu-id="e8ad5-105">Microsoft 365 employs multiple strategies for securing its network boundary, including automated detection and prevention of network-based attacks, specialized firewall devices, and Exchange Online Protection (EOP) for anti-spam and anti-malware protection.</span></span> <span data-ttu-id="e8ad5-106">此外，Microsoft 365 将生产环境分为逻辑隔离的网络段，仅允许分段之间进行必要的通信。</span><span class="sxs-lookup"><span data-stu-id="e8ad5-106">In addition, Microsoft 365 separates its production environment into logically isolated network segments, with only necessary communication permitted between segments.</span></span> <span data-ttu-id="e8ad5-107">在边界点使用其他网络防火墙保护网络流量，以帮助检测、防止和减少网络攻击。</span><span class="sxs-lookup"><span data-stu-id="e8ad5-107">Network traffic is secured using additional network firewalls at boundary points to help detect, prevent, and mitigate network attacks.</span></span>

## <a name="how-does-microsoft-365-defend-against-ddos-attacks"></a><span data-ttu-id="e8ad5-108">Microsoft 365 如何防御 DDoS 攻击？</span><span class="sxs-lookup"><span data-stu-id="e8ad5-108">How does Microsoft 365 defend against DDoS attacks?</span></span>

<span data-ttu-id="e8ad5-109">Microsoft 的大型 Internet 状态使 Microsoft 无法免受许多分布式拒绝服务攻击和 DDoS (攻击) 负面影响。</span><span class="sxs-lookup"><span data-stu-id="e8ad5-109">Microsoft's large internet presence insulates it from the negative effects of many distributed denial-of-service (DDoS) attacks.</span></span> <span data-ttu-id="e8ad5-110">每个 Microsoft 365 服务的分布式实例和每个服务的多个路由限制 DDoS 攻击对系统的影响。</span><span class="sxs-lookup"><span data-stu-id="e8ad5-110">Distributed instances of each Microsoft 365 service and multiple routes to each service limit the impact of DDoS attacks against the system.</span></span> <span data-ttu-id="e8ad5-111">这种冗余提高了 Microsoft 365 吸收 DDoS 攻击的能力，并增加了在 DDoS 攻击影响服务可用性之前检测并减少 DDoS 攻击的时间量。</span><span class="sxs-lookup"><span data-stu-id="e8ad5-111">This redundancy improves Microsoft 365's ability to absorb DDoS attacks and increases the amount of time available to detect and mitigate DDoS attacks before they impact service availability.</span></span>

<span data-ttu-id="e8ad5-112">除了 Microsoft 的冗余系统体系结构之外，Microsoft 还使用复杂的检测和缓解工具来响应 DDoS 攻击。</span><span class="sxs-lookup"><span data-stu-id="e8ad5-112">In addition to Microsoft's redundant system architecture, Microsoft uses sophisticated detection and mitigation tools to respond to DDoS attacks.</span></span> <span data-ttu-id="e8ad5-113">专用防火墙在将不需要的流量跨越边界进入网络之前监视和丢弃不需要的流量，从而减少位于网络边界内的系统压力。</span><span class="sxs-lookup"><span data-stu-id="e8ad5-113">Special-purpose firewalls monitor and drop unwanted traffic before it crosses the boundary into the network, reducing stress on systems located inside the network boundary.</span></span> <span data-ttu-id="e8ad5-114">为了进一步保护云服务，Microsoft 利用部署为 Microsoft Azure 一部分的 DDoS 防御系统。</span><span class="sxs-lookup"><span data-stu-id="e8ad5-114">To further protect our cloud services, Microsoft utilizes a DDoS defense system deployed as part of Microsoft Azure.</span></span> <span data-ttu-id="e8ad5-115">Azure DDoS 防御系统旨在抵御来自外部以及其他 Azure 租户的攻击。</span><span class="sxs-lookup"><span data-stu-id="e8ad5-115">The Azure DDoS defense system is designed to withstand attacks from the outside as well as from other Azure tenants.</span></span>

## <a name="how-does-microsoft-365-protect-users-against-spam-and-malware-being-uploaded-or-sent-through-online-services"></a><span data-ttu-id="e8ad5-116">Microsoft 365 如何保护用户免受通过联机服务上载或发送的垃圾邮件和恶意软件的侵害？</span><span class="sxs-lookup"><span data-stu-id="e8ad5-116">How does Microsoft 365 protect users against spam and malware being uploaded or sent through online services?</span></span>

<span data-ttu-id="e8ad5-117">Microsoft 365 将反恶意软件保护构建到可能是恶意代码矢量的服务中，例如 Exchange Online 和 SharePoint Online。</span><span class="sxs-lookup"><span data-stu-id="e8ad5-117">Microsoft 365 builds antimalware protection into services that might be vectors for malicious code, such as Exchange Online and SharePoint Online.</span></span> <span data-ttu-id="e8ad5-118">Exchange Online Protection (EOP) 在进入和退出系统时扫描所有电子邮件和电子邮件附件中的恶意软件，以防止被感染的邮件和附件被传递。</span><span class="sxs-lookup"><span data-stu-id="e8ad5-118">Exchange Online Protection (EOP) scans all emails and email attachments for malware as they enter and exit the system, preventing infected messages and attachments from being delivered.</span></span> <span data-ttu-id="e8ad5-119">高级垃圾邮件筛选自动应用于入站和出站邮件，以帮助客户组织接收和发送垃圾邮件。</span><span class="sxs-lookup"><span data-stu-id="e8ad5-119">Advanced spam filtering is automatically applied to inbound and outbound messages to help prevent customer organizations from receiving and sending spam.</span></span> <span data-ttu-id="e8ad5-120">此保护层可抵御利用未经请求或未经授权的电子邮件的攻击，如钓鱼攻击。</span><span class="sxs-lookup"><span data-stu-id="e8ad5-120">This layer of protection guards against attacks that take advantage of unsolicited or unauthorized email, such as phishing attacks.</span></span> <span data-ttu-id="e8ad5-121">SharePoint Online 使用相同的病毒检测引擎选择性地扫描上传的文件，以发现恶意软件。</span><span class="sxs-lookup"><span data-stu-id="e8ad5-121">SharePoint Online uses the same virus detection engine to selectively scan uploaded files for malware.</span></span> <span data-ttu-id="e8ad5-122">如果文件被标记为已感染，则阻止用户下载或同步文件以保护客户端终结点。</span><span class="sxs-lookup"><span data-stu-id="e8ad5-122">If a file is marked as infected, users are prevented from downloading or syncing the file to protect client endpoints.</span></span>

## <a name="related-external-regulations--certifications"></a><span data-ttu-id="e8ad5-123">认证的相关&法规</span><span class="sxs-lookup"><span data-stu-id="e8ad5-123">Related external regulations & certifications</span></span>

<span data-ttu-id="e8ad5-124">Microsoft 的在线服务会定期进行审核，以遵守外部法规和认证。</span><span class="sxs-lookup"><span data-stu-id="e8ad5-124">Microsoft's online services are regularly audited for compliance with external regulations and certifications.</span></span> <span data-ttu-id="e8ad5-125">请参阅下表，以验证与网络安全相关的控制措施。</span><span class="sxs-lookup"><span data-stu-id="e8ad5-125">Please refer to the following table for validation of controls related to network security.</span></span>

| <span data-ttu-id="e8ad5-126">**外部审核**</span><span class="sxs-lookup"><span data-stu-id="e8ad5-126">**External audits**</span></span> | <span data-ttu-id="e8ad5-127">**Section**</span><span class="sxs-lookup"><span data-stu-id="e8ad5-127">**Section**</span></span> | <span data-ttu-id="e8ad5-128">**最新报告日期**</span><span class="sxs-lookup"><span data-stu-id="e8ad5-128">**Latest report date**</span></span> |
|:--------------------|:------------|:-----------------------|
| [<span data-ttu-id="e8ad5-129">FedRAMP (Office 365) </span><span class="sxs-lookup"><span data-stu-id="e8ad5-129">FedRAMP (Office 365)</span></span>](https://compliance.microsoft.com/compliancemanager) | <span data-ttu-id="e8ad5-130">SC-5：拒绝服务保护</span><span class="sxs-lookup"><span data-stu-id="e8ad5-130">SC-5: Denial of service protection</span></span> <br> <span data-ttu-id="e8ad5-131">SC-7：边界保护</span><span class="sxs-lookup"><span data-stu-id="e8ad5-131">SC-7: Boundary protection</span></span> <br> <span data-ttu-id="e8ad5-132">SI-2：缺陷修正</span><span class="sxs-lookup"><span data-stu-id="e8ad5-132">SI-2: Flaw remediation</span></span> <br> <span data-ttu-id="e8ad5-133">SI-3：恶意代码保护</span><span class="sxs-lookup"><span data-stu-id="e8ad5-133">SI-3: Malicious code protection</span></span> <br> <span data-ttu-id="e8ad5-134">SI-8：垃圾邮件保护</span><span class="sxs-lookup"><span data-stu-id="e8ad5-134">SI-8: Spam protection</span></span> | <span data-ttu-id="e8ad5-135">2020 年 9 月 24 日</span><span class="sxs-lookup"><span data-stu-id="e8ad5-135">September 24, 2020</span></span> |
| [<span data-ttu-id="e8ad5-136">SOC 1 (Office 365)</span><span class="sxs-lookup"><span data-stu-id="e8ad5-136">SOC 1 (Office 365)</span></span>](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | <span data-ttu-id="e8ad5-137">CA-27：漏洞扫描</span><span class="sxs-lookup"><span data-stu-id="e8ad5-137">CA-27: Vulnerability Scanning</span></span> | <span data-ttu-id="e8ad5-138">2020 年 12 月 24 日</span><span class="sxs-lookup"><span data-stu-id="e8ad5-138">December 24, 2020</span></span> |
| [<span data-ttu-id="e8ad5-139">SOC 2 (Office 365) </span><span class="sxs-lookup"><span data-stu-id="e8ad5-139">SOC 2 (Office 365)</span></span>](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | <span data-ttu-id="e8ad5-140">CA-27：漏洞扫描</span><span class="sxs-lookup"><span data-stu-id="e8ad5-140">CA-27: Vulnerability Scanning</span></span> <br> <span data-ttu-id="e8ad5-141">CA-45：反恶意软件</span><span class="sxs-lookup"><span data-stu-id="e8ad5-141">CA-45: Anti-malware</span></span> | <span data-ttu-id="e8ad5-142">2020 年 12 月 24 日</span><span class="sxs-lookup"><span data-stu-id="e8ad5-142">December 24, 2020</span></span> |