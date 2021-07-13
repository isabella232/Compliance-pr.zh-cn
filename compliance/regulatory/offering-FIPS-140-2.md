---
title: 联邦信息处理标准 (140-2) FIPS
description: Microsoft 证明其加密模块符合美国联邦信息处理标准。
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
ms.openlocfilehash: 2c51979122aaedda90bac74740e95c9d1265de74
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/12/2021
ms.locfileid: "53385002"
---
# <a name="federal-information-processing-standard-fips-publication-140-2"></a>联邦信息处理标准 (140-2) FIPS

## <a name="fips-140-2-standard-overview"></a>FIPS 140-2 标准概述

联邦信息处理标准 (FIPS) 出版物 140-2 是一项美国政府标准，它定义信息技术产品中加密模块的最低安全要求，如 1996 年信息技术管理变革法案第 5131 节中的定义。

加密模块验证计划[ (](https://csrc.nist.gov/Projects/cryptographic-module-validation-program) CMVP) 是美国国家标准和技术协会 (NIST) 和加拿大网络安全中心 (CCCS) 的一项联合努力，它验证加密模块符合加密模块的安全要求标准 (即 FIPS 140-2) 和相关 FIPS 加密标准。  FIPS 140-2 安全要求涵盖与设计和实现加密模块相关的 11 个方面。 NIST 信息技术实验室运行相关程序，以验证模块中 FIPS 批准的加密算法。

## <a name="microsofts-approach-to-fips-140-2-validation"></a>Microsoft 对 FIPS 140-2 验证的方法

自 2001 年制定标准以来，Microsoft 一直积极致力于满足 140-2 要求，并验证了加密模块。 Microsoft 根据国家标准和技术协会 NIST (加密模块验证计划) CMVP ([](https://csrc.nist.gov/Projects/cryptographic-module-validation-program)加密模块) 。 多个 Microsoft 产品（包括许多云服务）使用这些加密模块。

有关 Microsoft Windows 加密模块、每个模块的安全策略以及 CMVP 证书详细信息目录的技术信息，请参阅 Windows 和[Windows Server FIPS 140-2 内容](https://aka.ms/AA6ehud)。

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Microsoft 范围内云平台&服务

虽然当前的 CMVP FIPS 140-2 实施指南会排除对云服务本身的 FIPS 140-2 验证;云服务提供商可以选择为构成其云服务的计算元素获取和运行 FIPS 140 验证的加密模块。 包括经过 FIPS 140-2 验证的组件的 Microsoft 联机服务包括：

- Azure 与 Azure 政府
- Dynamics 365 和 Dynamics 365 政府版
- Office 365、Office 365 U.S. Government 和 Office 365 U.S. Government Defense

## <a name="azure-dynamics-365-and-fips-140-2"></a>Azure、Dynamics 365 和 FIPS 140-2

有关 Azure、Dynamics 365 和其他在线服务合规性的信息，请参阅 Azure [FIPS 140-2 产品](/azure/compliance/offerings/offering-fips-140-2)/

## <a name="office-365-and-fips-140-2"></a>Office 365和 FIPS 140-2

### <a name="office-365-cloud-environments"></a>Office 365云环境

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a>Office 365适用性和范围内服务

使用下表确定您的 Office 365 服务和订阅的适用性：

| **适用性** | **范围内服务** |
|:------------------|:----------------------|
| Office 365、GCC、GCC High、DoD | 请参阅 [FIPS 140-2 验证](/windows/security/threat-protection/fips-140-validation) |

### <a name="frequently-asked-questions"></a>常见问题解答

**"FIPS 140 Validated"和"FIPS 140 compliant"之间有什么区别？**

"FIPS 140 已验证"意味着 CMVP 已验证加密模块或嵌入模块的产品 () 验证为符合 FIPS 140-2 要求。 "FIPS 140 兼容"是依赖 FIPS 140 验证产品实现加密功能的 IT 产品的行业术语。

**Microsoft 何时执行 FIPS 140 验证？**

启动模块验证的节奏与 Windows 10 和 Windows Server 的功能更新一致。 随着软件行业的发展，随着每月软件更新，操作系统的发布频率也越来越高。 Microsoft 对功能版本进行验证，但在两次发布之间，旨在最大限度地减少对加密模块的更改。

**FIPS 140 验证中包含哪些计算机？**

Microsoft 在运行 Windows 10 和 Windows Server 的具有代表性的硬件配置示例上验证加密模块。 当环境使用硬件时接受此 FIPS 140-2 验证是一种常见做法，这类似于用于验证过程的示例。

**NIST 网站上列出了许多模块。我如何知道哪个适用于我的代理？**

如果需要使用通过 FIPS 140-2 验证的加密模块，则需要验证使用的版本是否显示在验证列表中。 CMVP 和 Microsoft 维护一个经验证的加密模块列表（按产品发布组织）以及用于确定哪些模块安装在 Windows 系统的说明。 有关配置符合标准的系统的信息，请参阅 Windows 和 Windows [Server FIPS 140-2 内容](https://aka.ms/AA6ehud)。

**"在 FIPS 模式下操作时"对证书意味着什么？**

此警告会告知读者，必须遵循必需的配置和安全规则，才能按照与 FIPS 140-2 安全策略一致的方式使用加密模块。 每个模块都有自己的安全策略（一个准确规范其操作依据的安全规则），并且使用批准的加密算法、加密密钥管理和身份验证技术。 安全规则在每个模块的安全策略中定义。 有关详细信息，包括通过 CMVP 验证的每个模块的安全策略链接，请参阅[Windows 和 Windows Server FIPS 140-2 内容](https://aka.ms/AA6ehud)。

**FedRAMP 是否需要 FIPS 140-2 验证？**

是的，联邦风险和授权管理计划 (FedRAMP) 依赖于 [NIST SP 800-53 修订版 4](https://nvd.nist.gov/800-53/Rev4/)定义的控制基线，包括 [SC-13](https://nvd.nist.gov/800-53/Rev4/control/SC-13) 加密保护，管理 FIPS 验证加密或 NSA 批准的加密的使用。

**能否在我的机构认证过程中使用 Microsoft 遵守 FIPS 140-2？**

为了符合 FIPS 140-2，系统必须配置为在 FIPS 批准的操作模式下运行，这包括确保加密模块仅使用 FIPS 批准的算法。 有关配置符合标准的系统的信息，请参阅 Windows 和 Windows [Server FIPS 140-2 内容](https://aka.ms/AA6ehud)。

**FIPS 140-2 和通用条件之间有什么关系？**

这是两个不同的安全标准，用途不同但相互补充。 FIPS 140-2 专用于验证软件和硬件加密模块，而通用条件旨在评估 IT 软件和硬件产品中的安全功能。 通用条件评估通常依赖 FIPS 140-2 验证，以提供基本加密功能正确实现的保证。

### <a name="resources"></a>资源

- [FIPS Pub 140-2 加密模块的安全要求](https://csrc.nist.gov/publications/fips/fips140-2/fips1402.pdf)
- [NIST 加密模块验证程序](https://csrc.nist.gov/groups/STM/cmvp/index.html)
- [Windows、Windows Server 和 FIPS 140-2](/windows/security/threat-protection/fips-140-validation)
- [Microsoft 信任中心内的合规性](https://www.microsoft.com/trust-center/compliance/compliance-overview)
