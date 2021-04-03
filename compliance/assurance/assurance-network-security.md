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
# <a name="network-security-overview"></a>网络安全性概述

## <a name="how-does-microsoft-365-secure-the-network-boundary"></a>Microsoft 365 如何保护网络边界？

Microsoft 365 采用多种策略来保护其网络边界，包括自动检测和防护基于网络的攻击、专用防火墙设备以及 Exchange Online Protection (EOP) 用于反垃圾邮件和反恶意软件保护。 此外，Microsoft 365 将生产环境分为逻辑隔离的网络段，仅允许分段之间进行必要的通信。 在边界点使用其他网络防火墙保护网络流量，以帮助检测、防止和减少网络攻击。

## <a name="how-does-microsoft-365-defend-against-ddos-attacks"></a>Microsoft 365 如何防御 DDoS 攻击？

Microsoft 的大型 Internet 状态使 Microsoft 无法免受许多分布式拒绝服务攻击和 DDoS (攻击) 负面影响。 每个 Microsoft 365 服务的分布式实例和每个服务的多个路由限制 DDoS 攻击对系统的影响。 这种冗余提高了 Microsoft 365 吸收 DDoS 攻击的能力，并增加了在 DDoS 攻击影响服务可用性之前检测并减少 DDoS 攻击的时间量。

除了 Microsoft 的冗余系统体系结构之外，Microsoft 还使用复杂的检测和缓解工具来响应 DDoS 攻击。 专用防火墙在将不需要的流量跨越边界进入网络之前监视和丢弃不需要的流量，从而减少位于网络边界内的系统压力。 为了进一步保护云服务，Microsoft 利用部署为 Microsoft Azure 一部分的 DDoS 防御系统。 Azure DDoS 防御系统旨在抵御来自外部以及其他 Azure 租户的攻击。

## <a name="how-does-microsoft-365-protect-users-against-spam-and-malware-being-uploaded-or-sent-through-online-services"></a>Microsoft 365 如何保护用户免受通过联机服务上载或发送的垃圾邮件和恶意软件的侵害？

Microsoft 365 将反恶意软件保护构建到可能是恶意代码矢量的服务中，例如 Exchange Online 和 SharePoint Online。 Exchange Online Protection (EOP) 在进入和退出系统时扫描所有电子邮件和电子邮件附件中的恶意软件，以防止被感染的邮件和附件被传递。 高级垃圾邮件筛选自动应用于入站和出站邮件，以帮助客户组织接收和发送垃圾邮件。 此保护层可抵御利用未经请求或未经授权的电子邮件的攻击，如钓鱼攻击。 SharePoint Online 使用相同的病毒检测引擎选择性地扫描上传的文件，以发现恶意软件。 如果文件被标记为已感染，则阻止用户下载或同步文件以保护客户端终结点。

## <a name="related-external-regulations--certifications"></a>认证的相关&法规

Microsoft 的在线服务会定期进行审核，以遵守外部法规和认证。 请参阅下表，以验证与网络安全相关的控制措施。

| **外部审核** | **Section** | **最新报告日期** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365) ](https://compliance.microsoft.com/compliancemanager) | SC-5：拒绝服务保护 <br> SC-7：边界保护 <br> SI-2：缺陷修正 <br> SI-3：恶意代码保护 <br> SI-8：垃圾邮件保护 | 2020 年 9 月 24 日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-27：漏洞扫描 | 2020 年 12 月 24 日 |
| [SOC 2 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-27：漏洞扫描 <br> CA-45：反恶意软件 | 2020 年 12 月 24 日 |