---
title: 网络安全
description: 了解 Microsoft 365 中的网络安全性
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
ms.openlocfilehash: c063460fdfba44265b3a1504a049a4772b484dff
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/30/2020
ms.locfileid: "49505910"
---
# <a name="network-security-overview"></a>网络安全概述

## <a name="how-does-microsoft-365-secure-the-network-boundary"></a>Microsoft 365 如何保护网络边界？

Microsoft 365 采用多种策略来保护其网络边界，包括自动检测和阻止基于网络的攻击、专用防火墙设备以及 Exchange Online Protection (EOP) 用于反垃圾邮件和反恶意软件保护。 此外，Microsoft 365 将其生产环境划分为逻辑隔离的网络段，仅允许在分段之间进行必要的通信。 使用边界点的其他网络防火墙保护网络流量，以帮助检测、阻止和缓解网络攻击。

## <a name="how-does-microsoft-365-defend-against-ddos-attacks"></a>Microsoft 365 如何防御 DDoS 攻击？

Microsoft 的大型 internet 状态将其与许多分布式拒绝服务 (DDoS) 攻击的负面影响隔离开来。 每个 Microsoft 365 服务的分布式实例和每个服务的多个路由都会限制针对系统的 DDoS 攻击的影响。 此冗余改进了 Microsoft 365 吸收 DDoS 攻击的能力，并增加了在影响服务可用性之前检测和缓解 DDoS 攻击的可用时间量。

除了 Microsoft 的冗余系统体系结构之外，Microsoft 还使用完善的检测和缓解工具来响应 DDoS 攻击。 特殊用途的防火墙会监视并丢弃不需要的流量，然后将边界与网络交叉，从而减少了网络边界内的系统上的压力。 为了进一步保护我们的云服务，Microsoft 利用了在 Microsoft Azure 中部署的 DDoS 防御系统。 Azure DDoS 防御系统旨在抵御来自外部的攻击以及来自其他 Azure 租户的攻击。

## <a name="how-does-microsoft-365-protect-users-against-spam-and-malware-being-uploaded-or-sent-through-online-services"></a>Microsoft 365 如何保护用户免受通过在线服务上传或发送的垃圾邮件和恶意软件的侵害？

Microsoft 365 将反恶意软件保护转换为可能是恶意代码的媒介的服务，例如 Exchange Online 和 SharePoint Online。 Exchange Online Protection (EOP) 在电子邮件和电子邮件附件进入和退出系统时对其进行扫描，以防止传递受感染的邮件和附件。 高级垃圾邮件筛选功能将自动应用于入站和出站邮件，以帮助防止客户组织接收和发送垃圾邮件。 这一层保护可抵御利用未经请求或未经授权的电子邮件的攻击，如网络钓鱼攻击。 SharePoint Online 使用相同的病毒检测引擎来选择性地扫描上载的文件中的恶意软件。 如果文件被标记为 "已感染"，则将阻止用户下载或同步文件以保护客户端终结点。

## <a name="related-external-regulations--certifications"></a>& 认证的相关外部法规

将定期审核 Microsoft 的在线服务，以遵守外部法规和认证。 有关与网络安全相关的控件的验证，请参阅下表。

| **外部审核** | **Section** | **最新报告日期** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365) ](https://compliance.microsoft.com/compliancemanager) | SC-5：拒绝服务保护 <br> SC-7：边界保护 <br> SI-2：缺陷修正 <br> SI-3：恶意代码保护 <br> SI-8：垃圾邮件保护 | 2020年9月24日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-27：漏洞扫描 | 2019 年 9 月 30 日 |
| [SOC 2 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-27：漏洞扫描 <br> CA-45：反恶意软件 | 2019 年 9 月 30 日 |