---
title: 数据中心安全概述
description: 了解 Microsoft 365 中的数据中心安全性
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
f1.keywords:
- NOCSH
audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.SupervisoryReview
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
ms.openlocfilehash: b67fad5e0901af3384b5a3b4717763e6edab1bcd
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/30/2020
ms.locfileid: "49506308"
---
# <a name="datacenter-security-overview"></a>数据中心安全概述

## <a name="how-does-microsoft-host-its-online-services"></a>Microsoft 如何托管其在线服务？

Microsoft 提供了200以上的云服务，包括企业服务（如 Microsoft Azure、Microsoft 365 和 Microsoft Dynamics 365），到客户24x7x365。 这些服务托管在 Microsoft 的云基础结构中，由全局分布式数据中心、边缘计算节点和服务运营中心组成。 它们受世界上最大的全局网络的支持和连接，且具有广泛的光纤空间。

为我们的云服务提供动力的数据中心将重点放在全球范围内的高可靠性、卓越运营、成本效益、环境可持续性和可信赖的在线体验上。 Microsoft 通过内部和第三方审核定期测试我们的数据中心安全性。 因此，与任何其他云服务提供商相比，全球最受管控的组织都信任 Microsoft 云，与其他云服务提供商的认证更兼容。

## <a name="how-does-microsoft-protect-its-datacenters-from-unauthorized-access"></a>Microsoft 如何保护其数据中心免遭未经授权的访问？

对物理数据中心设施的访问受外部和内部外围环境的严格控制，每个级别的安全性都各不相同，包括外围设备防护、安全主管、锁定的服务器机架、集成的警报系统、运营中心的全天候视频监控以及多重访问控制。 只有需要的人员才有权访问 Microsoft 数据中心。 在 Microsoft 数据中心内完全禁止逻辑访问 Microsoft 365 基础结构，包括客户数据。

我们的安全操作中心将视频监控与集成的电子访问控制系统结合使用，以监控数据中心网站和设施。 相机在战略位置定位，以有效覆盖设施外围、入口、装运厅、服务器 cages、内部通道和其他敏感安全点。 作为我们的多层安全状态的一部分，由集成安全系统检测到的任何未经授权的进入尝试都会为安全人员生成警报，以即时响应和修正。

## <a name="how-does-microsoft-protect-its-datacenters-from-environmental-hazards"></a>Microsoft 如何保护其数据中心不受环境危害？

Microsoft 采用各种安全措施来防范对数据中心可用性的环境威胁。 对数据中心网站进行战略选择，以最大限度地减少各种因素（包括洪水、地震、飓风和其他自然灾害）的风险。 我们的数据中心使用气候控制来监视和维护员工、设备和硬件的优化的可调空间。 防火检测和抑制系统和水传感器可帮助检测并阻止设备的火灾和水源损坏。

灾难是不可预知的，但 Microsoft 数据中心和操作人员准备灾难以提供操作的连续性，应会发生意外事件。 弹性体系结构和最新的已测试连续性计划可缓解潜在损坏，并促进数据中心操作的迅速恢复。 危机管理计划在发生危机之前、期间和之后对角色、职责和缓解活动提供了明确性。 这些计划中定义的角色和联系人有助于在危机情况下提升命令链的效率。

## <a name="how-does-microsoft-verify-the-effectiveness-of-datacenter-security"></a>Microsoft 如何验证数据中心安全性的有效性？

我们了解，为了让我们的客户能够充分实现云的优势，他们必须能够信任其云服务提供商。 我们的基础结构和云服务套件是从头开始构建的，以满足客户的严格安全和隐私要求。 我们通过提供任意云服务提供商的一组最全面的兼容性产品，帮助我们的客户遵守国家、地区和特定于行业的要求，以控制个人数据的收集和使用。

我们的云基础结构和产品服务符合一系列国际和特定于行业的合规性标准，如 ISO、HIPAA、FedRAMP 和 SOC 以及特定于国家/地区的标准，如澳大利亚 IRAP、英国的 G-云和新加坡的 MTCS。 严格的第三方审核验证我们是否遵守严格的安全控制这些标准要求。 在 [Microsoft 服务信任门户](https://servicetrust.microsoft.com/)中提供了我们的数据中心基础结构和云产品的审核报告。

## <a name="related-external-regulations--certifications"></a>& 认证的相关外部法规

将定期审核 Microsoft 的在线服务，以遵守外部法规和认证。 请参阅下表以验证与数据中心安全性相关的控件。

| **外部审核** | **Section** | **最新报告日期** |
|:--------------------|:------------|:-----------------------|  
| [FedRAMP (Office 365) ](https://compliance.microsoft.com/compliancemanager) | PE-2：物理访问授权 <br> PE-3：物理访问控制 <br> PE-6：监视物理访问 <br> PE-11：紧急电源 <br> PE-13：防火防护 <br> PE-14：温度和湿度控制 <br> PE-15：水源损坏保护 | 2020年9月24日 |
| [ISO 27001/27002 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 11：物理和环境安全性 | 2020 年 2 月 22 日 |
| [ISO 27017 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [认证] (https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports | 11：物理和环境安全性 | 2020 年 2 月 22 日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=b07c0f7b-6bd5-4544-8255-7a5f14bf914a&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-39：数据中心访问控制 <br> CA-40：数据中心网络身份验证 <br> CA-41：数据中心双因素身份验证 <br> CA-48：数据中心日志记录 | 2019 年 9 月 30 日 |
| [SOC 2 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-39：数据中心访问控制 <br> CA-40：数据中心网络身份验证 <br> CA-41：数据中心双因素身份验证 <br> CA-48：数据中心日志记录 | 2019 年 9 月 30 日 |
