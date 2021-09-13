---
title: 网络安全性
description: 了解 Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
ms.localizationpriority: medium
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 92da9e7bb2716f61088e02c244cb9905af142ead
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/12/2021
ms.locfileid: "59158818"
---
# <a name="network-security-overview"></a>网络安全性概述

## <a name="how-do-microsoft-online-services-secure-the-network-boundary"></a>Microsoft 联机服务如何保护网络边界？

Microsoft 在线服务采用多种策略来保护其网络边界，包括自动检测和防护基于网络的攻击、专用防火墙设备以及 Exchange Online Protection (EOP) 用于反垃圾邮件和反恶意软件保护。 此外，Microsoft 在线服务将生产环境分为逻辑隔离的网络段，仅允许分段之间进行必要的通信。 在边界点使用其他网络防火墙保护网络流量，以帮助检测、防止和减少网络攻击。

## <a name="how-do-microsoft-online-services-defend-against-ddos-attacks"></a>Microsoft 在线服务如何防御 DDoS 攻击？

Microsoft 的大型 Internet 状态使 Microsoft 免受许多分布式拒绝服务攻击和 DDoS (负面影响) 的影响。 每个 Microsoft 联机服务的分布式实例和每个服务的多个路由限制 DDoS 攻击对系统的影响。 这种冗余提高了 Microsoft 联机服务吸收 DDoS 攻击的能力，并增加了在 DDoS 攻击影响服务可用性之前检测并减少 DDoS 攻击的时间量。

除了 Microsoft 的冗余系统体系结构之外，Microsoft 还使用复杂的检测和缓解工具来响应 DDoS 攻击。 专用防火墙在将不需要的流量跨越边界进入网络之前监视和丢弃不需要的流量，从而减少位于网络边界内的系统压力。 为了进一步保护云服务，Microsoft 利用部署为云解决方案一部分的 DDoS Microsoft Azure。 Azure DDoS 防御系统旨在抵御来自外部和其他 Azure 租户的攻击。

## <a name="how-does-microsoft-protect-users-against-spam-and-malware-being-uploaded-or-sent-through-online-services"></a>Microsoft 如何保护用户免受通过联机服务上载或发送的垃圾邮件和恶意软件？

Microsoft 在线服务将反恶意软件保护构建到可能是恶意代码的矢量的服务中，例如 Exchange Online 和 SharePoint Online。 Exchange Online Protection (EOP) 在进入和退出系统时扫描所有电子邮件和电子邮件附件中的恶意软件，以防止被感染的邮件和附件被传递。 高级垃圾邮件筛选自动应用于入站和出站邮件，以帮助客户组织接收和发送垃圾邮件。 此保护层可抵御利用未经请求或未经授权的电子邮件的攻击，如钓鱼攻击。 SharePointOnline 使用相同的病毒检测引擎选择性地扫描上传的文件，以发现恶意软件。 如果文件被标记为已感染，则阻止用户下载或同步文件以保护客户端终结点。 同样，Azure 将上载到 Azure 存储 文件的哈希与已知恶意软件的哈希进行比较。 当找到匹配项时，将在 Azure 安全中心中发出警报，其中将决定警报是否安全以及如何解决。

## <a name="related-external-regulations--certifications"></a>认证的相关&法规

Microsoft 的在线服务会定期进行审核，以遵守外部法规和认证。 有关与网络安全相关的控件的验证，请参阅下表。

### <a name="azure-and-dynamics-365"></a>Azure 和 Dynamics 365

| **外部审核** | **Section** | **最新报告日期** |
|:--------------------|:------------|:-----------------------|
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b8721ebd-af20-42fe-b22f-8332b0a19517&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=234a0f57-83c1-4afc-a586-a0e7a59592f7&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) <br> [SOC 3](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=75c8cbf6-e456-473c-a05e-34fea888ec2a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | VM-1：安全事件日志记录 <br> VM-3：入侵检测和监视 <br> VM-4：恶意事件调查 <br> VM-6：漏洞扫描 <br> VM-7：网络设备配置 <br> VM-8：渗透测试 <br> VM-9：网络设备安全事件日志记录 <br> VM-13：网络设备漏洞缓解 | 3 月 31 日。 2021 |

### <a name="office-365"></a>Office 365

| **外部审核** | **Section** | **最新报告日期** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP](https://compliance.microsoft.com/compliancemanager) | SC-5：拒绝服务保护 <br> SC-7：边界保护 <br> SI-2：缺陷修正 <br> SI-3：恶意代码保护 <br> SI-8：垃圾邮件保护 | 2020 年 9 月 24 日 |
| [SOC 1](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-27：漏洞扫描 | 2020 年 12 月 24 日 |
| [SOC 2](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-27：漏洞扫描 <br> CA-45：反恶意软件 | 2020 年 12 月 24 日 |