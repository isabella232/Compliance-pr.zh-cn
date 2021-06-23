---
title: 美国 DoE 10 CFR 第 810 部分
description: 符合美国 DoE 10 CFR 第 810 部分的出口控制要求的客户可以使用 Azure 政府。
keywords: Microsoft 365, 合规性, 产品/服务
localization_priority: None
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection:
- M365-security-compliance
- MS-Compliance
hideEdit: true
titleSuffix: Microsoft Compliance
ms.openlocfilehash: 1a16495f5cfe3e293910ebe84e6af566aea17621
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/23/2021
ms.locfileid: "53087541"
---
# <a name="us-doe-10-cfr-part-810"></a>美国 DoE 10 CFR 第 810 部分

## <a name="microsoft-and-doe-10-cfr-part-810"></a>Microsoft 和 DoE 10 CFR 第 810 部分

Microsoft Azure政府可通过两项授权，帮助客户遵守美国能源 (DoE) 10 CFR 第 810 部分中的出口控制要求：

- 联合授权委员会 (联合授权) P-ATO (P-ATO) 
- 美国国防部国防信息系统局的 4 级 (5 级) 授权

FedRAMP 提供了适当的基线，用于保证 Azure 政府提供核心基础结构和虚拟化技术以及计算、存储和使用严格的 NIST 控制设计的网络等服务。 这些有助于满足客户数据分离要求，并有助于实现与客户本地环境的安全连接。

此外，Azure 政府是一个美国政府社区云，从物理上与 Azure 云分开。 它提供有关美国政府的特定背景屏蔽要求的其他保证，包括限制对 Azure 操作人员中经过筛选的美国政府公民的信息和系统的访问的特定控制措施。

## <a name="microsoft-in-scope-cloud-services"></a>Microsoft 范围内云服务

- [Azure 政府](https://aka.ms/AzureCompliance)
- Intune

## <a name="how-to-implement"></a>如何实现

- [NERC CIP 标准&](https://aka.ms/AzureNERC)云计算：在 Azure 或 Azure 政府中部署工作负载的电力系统和注册实体指南。

## <a name="about-doe-10-cfr-part-810"></a>关于 DoE 10 CFR 第 810 部分

美国能源 (DoE) 出口控制条例 [10 CFR 第 810](https://www.govinfo.gov/content/pkg/FR-2015-02-23/pdf/2015-03479.pdf) 部分监管未分类的伪造技术和协助的导出。 它有助于确保从美国导出的推广技术仅用于开发目的。 修订的第 810 (年 3 月) 年 3 月生效，并受国家税务局 [管理](https://www.energy.gov/nnsa/national-nuclear-security-administration)。 第 810.6 节指出，需要特定 DoE 授权才能提供"通常授权的"敏感核技术以及需要特定授权的 (如涉及敏感核技术（如扩充和重电生产) ）的帮助。

## <a name="frequently-asked-questions"></a>常见问题解答

**美国国家/法规委员会 10 CFR 第 110 部分是否适用于 Azure 政府？**

不正确。 美国[国家 (监管](https://www.nrc.gov/) (NRC) 根据[10 CFR 第 110](https://www.nrc.gov/reading-rm/doc-collections/cfr/part110/)部分监管了出口和导入出口设施及相关设备和材料。 [](https://www.nrc.gov/about-nrc/ip/export-import.html) NRC 不监管与属于 DoE 管辖的这些项目相关的制造技术和协助。 因此，NRC 10 CFR 第 110 部分法规不适用于 Azure 政府。

**如何提供我遵守 DoE 10 CFR 第 810 部分的证据？**

如果你的组织正在将数据部署到 Azure 政府，你可以依赖 Azure 政府 FedRAMP High P-ATO 作为你以适当受限的方式处理数据的证据。 但是，你负责获取你自己的系统的 DoE 授权，包括云服务的使用。

**我负责对部署到 Azure 政府的数据进行分类吗？**

将数据部署到 Azure 政府的客户负责自己的安全分类过程。 对于受 DoE 导出控制的客户数据，分类系统由美国原子能源法案第 148 节建立的未经分类的受控出口信息 (UCNI) 控制进行扩充[。](https://www.epa.gov/laws-regulations/summary-atomic-energy-act)

## <a name="resources"></a>资源

- [Azure 云服务在美国出口控制](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=c24c11f2-2cd4-444a-9160-19762855ad3a&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)
- [Microsoft 与 FedRAMP](offering-fedramp.md)
- [Microsoft 和 DoD](offering-dod-disa-l2-l4-l5.md)
- [Microsoft 政府云](https://www.microsoft.com/enterprise/government)
- [Microsoft 信任中心内的合规性](https://www.microsoft.com/trust-center/compliance/compliance-overview)
