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
# <a name="federal-information-processing-standard-fips-publication-140-2"></a><span data-ttu-id="b6edf-104">联邦信息处理标准 (140-2) FIPS</span><span class="sxs-lookup"><span data-stu-id="b6edf-104">Federal Information Processing Standard (FIPS) Publication 140-2</span></span>

## <a name="fips-140-2-standard-overview"></a><span data-ttu-id="b6edf-105">FIPS 140-2 标准概述</span><span class="sxs-lookup"><span data-stu-id="b6edf-105">FIPS 140-2 standard overview</span></span>

<span data-ttu-id="b6edf-106">联邦信息处理标准 (FIPS) 出版物 140-2 是一项美国政府标准，它定义信息技术产品中加密模块的最低安全要求，如 1996 年信息技术管理变革法案第 5131 节中的定义。</span><span class="sxs-lookup"><span data-stu-id="b6edf-106">The Federal Information Processing Standard (FIPS) Publication 140-2 is a U.S. government standard that defines minimum security requirements for cryptographic modules in information technology products, as defined in Section 5131 of the Information Technology Management Reform Act of 1996.</span></span>

<span data-ttu-id="b6edf-107">加密模块验证计划[ (](https://csrc.nist.gov/Projects/cryptographic-module-validation-program) CMVP) 是美国国家标准和技术协会 (NIST) 和加拿大网络安全中心 (CCCS) 的一项联合努力，它验证加密模块符合加密模块的安全要求标准 (即 FIPS 140-2) 和相关 FIPS 加密标准。 </span><span class="sxs-lookup"><span data-stu-id="b6edf-107">The [Cryptographic Module Validation Program](https://csrc.nist.gov/Projects/cryptographic-module-validation-program) (CMVP), a joint effort of the U.S. National Institute of Standards and Technology (NIST) and the Canadian Centre for Cyber Security (CCCS), validates cryptographic modules to the *Security Requirements for Cryptographic Modules* standard (i.e., FIPS 140-2) and related FIPS cryptography standards.</span></span> <span data-ttu-id="b6edf-108">FIPS 140-2 安全要求涵盖与设计和实现加密模块相关的 11 个方面。</span><span class="sxs-lookup"><span data-stu-id="b6edf-108">The FIPS 140-2 security requirements cover 11 areas related to the design and implementation of a cryptographic module.</span></span> <span data-ttu-id="b6edf-109">NIST 信息技术实验室运行相关程序，以验证模块中 FIPS 批准的加密算法。</span><span class="sxs-lookup"><span data-stu-id="b6edf-109">The NIST Information Technology Laboratory operates a related program that validates the FIPS approved cryptographic algorithms in the module.</span></span>

## <a name="microsofts-approach-to-fips-140-2-validation"></a><span data-ttu-id="b6edf-110">Microsoft 对 FIPS 140-2 验证的方法</span><span class="sxs-lookup"><span data-stu-id="b6edf-110">Microsoft's approach to FIPS 140-2 validation</span></span>

<span data-ttu-id="b6edf-111">自 2001 年制定标准以来，Microsoft 一直积极致力于满足 140-2 要求，并验证了加密模块。</span><span class="sxs-lookup"><span data-stu-id="b6edf-111">Microsoft maintains an active commitment to meeting the 140-2 requirements, having validated cryptographic modules since the standard's inception in 2001.</span></span> <span data-ttu-id="b6edf-112">Microsoft 根据国家标准和技术协会 NIST (加密模块验证计划) CMVP ([](https://csrc.nist.gov/Projects/cryptographic-module-validation-program)加密模块) 。</span><span class="sxs-lookup"><span data-stu-id="b6edf-112">Microsoft validates its cryptographic modules under the National Institute of Standards and Technology (NIST) [Cryptographic Module Validation Program](https://csrc.nist.gov/Projects/cryptographic-module-validation-program) (CMVP).</span></span> <span data-ttu-id="b6edf-113">多个 Microsoft 产品（包括许多云服务）使用这些加密模块。</span><span class="sxs-lookup"><span data-stu-id="b6edf-113">Multiple Microsoft products, including many cloud services, use these cryptographic modules.</span></span>

<span data-ttu-id="b6edf-114">有关 Microsoft Windows 加密模块、每个模块的安全策略以及 CMVP 证书详细信息目录的技术信息，请参阅 Windows 和[Windows Server FIPS 140-2 内容](https://aka.ms/AA6ehud)。</span><span class="sxs-lookup"><span data-stu-id="b6edf-114">For technical information on Microsoft Windows cryptographic modules, the security policy for each module, and the catalog of CMVP certificate details, see the [Windows and Windows Server FIPS 140-2 content](https://aka.ms/AA6ehud).</span></span>

## <a name="microsoft-in-scope-cloud-platforms--services"></a><span data-ttu-id="b6edf-115">Microsoft 范围内云平台&服务</span><span class="sxs-lookup"><span data-stu-id="b6edf-115">Microsoft in-scope cloud platforms & services</span></span>

<span data-ttu-id="b6edf-116">虽然当前的 CMVP FIPS 140-2 实施指南会排除对云服务本身的 FIPS 140-2 验证;云服务提供商可以选择为构成其云服务的计算元素获取和运行 FIPS 140 验证的加密模块。</span><span class="sxs-lookup"><span data-stu-id="b6edf-116">While the current CMVP FIPS 140-2 implementation guidance precludes a FIPS 140-2 validation for a cloud service itself; cloud service providers can choose to obtain and operate FIPS 140 validated cryptographic modules for the computing elements that comprise their cloud service.</span></span> <span data-ttu-id="b6edf-117">包括经过 FIPS 140-2 验证的组件的 Microsoft 联机服务包括：</span><span class="sxs-lookup"><span data-stu-id="b6edf-117">Microsoft online services that include components, which have been FIPS 140-2 validated include, among others:</span></span>

- <span data-ttu-id="b6edf-118">Azure 与 Azure 政府</span><span class="sxs-lookup"><span data-stu-id="b6edf-118">Azure and Azure Government</span></span>
- <span data-ttu-id="b6edf-119">Dynamics 365 和 Dynamics 365 政府版</span><span class="sxs-lookup"><span data-stu-id="b6edf-119">Dynamics 365 and Dynamics 365 Government</span></span>
- <span data-ttu-id="b6edf-120">Office 365、Office 365 U.S. Government 和 Office 365 U.S. Government Defense</span><span class="sxs-lookup"><span data-stu-id="b6edf-120">Office 365, Office 365 U.S. Government, and Office 365 U.S. Government Defense</span></span>

## <a name="azure-dynamics-365-and-fips-140-2"></a><span data-ttu-id="b6edf-121">Azure、Dynamics 365 和 FIPS 140-2</span><span class="sxs-lookup"><span data-stu-id="b6edf-121">Azure, Dynamics 365, and FIPS 140-2</span></span>

<span data-ttu-id="b6edf-122">有关 Azure、Dynamics 365 和其他在线服务合规性的信息，请参阅 Azure [FIPS 140-2 产品](/azure/compliance/offerings/offering-fips-140-2)/</span><span class="sxs-lookup"><span data-stu-id="b6edf-122">For more information about Azure, Dynamics 365, and other online services compliance, see the [Azure FIPS 140-2 offering](/azure/compliance/offerings/offering-fips-140-2).</span></span>

## <a name="office-365-and-fips-140-2"></a><span data-ttu-id="b6edf-123">Office 365和 FIPS 140-2</span><span class="sxs-lookup"><span data-stu-id="b6edf-123">Office 365 and FIPS 140-2</span></span>

### <a name="office-365-cloud-environments"></a><span data-ttu-id="b6edf-124">Office 365云环境</span><span class="sxs-lookup"><span data-stu-id="b6edf-124">Office 365 cloud environments</span></span>

[!INCLUDE [Office 365 offering intro](../includes/o365-offering-introduction.md)]

### <a name="office-365-applicability-and-in-scope-services"></a><span data-ttu-id="b6edf-125">Office 365适用性和范围内服务</span><span class="sxs-lookup"><span data-stu-id="b6edf-125">Office 365 applicability and in-scope services</span></span>

<span data-ttu-id="b6edf-126">使用下表确定您的 Office 365 服务和订阅的适用性：</span><span class="sxs-lookup"><span data-stu-id="b6edf-126">Use the following table to determine applicability for your Office 365 services and subscription:</span></span>

| <span data-ttu-id="b6edf-127">**适用性**</span><span class="sxs-lookup"><span data-stu-id="b6edf-127">**Applicability**</span></span> | <span data-ttu-id="b6edf-128">**范围内服务**</span><span class="sxs-lookup"><span data-stu-id="b6edf-128">**In-scope services**</span></span> |
|:------------------|:----------------------|
| <span data-ttu-id="b6edf-129">Office 365、GCC、GCC High、DoD</span><span class="sxs-lookup"><span data-stu-id="b6edf-129">Office 365, GCC, GCC High, DoD</span></span> | <span data-ttu-id="b6edf-130">请参阅 [FIPS 140-2 验证](/windows/security/threat-protection/fips-140-validation)</span><span class="sxs-lookup"><span data-stu-id="b6edf-130">See [FIPS 140-2 Validation](/windows/security/threat-protection/fips-140-validation)</span></span> |

### <a name="frequently-asked-questions"></a><span data-ttu-id="b6edf-131">常见问题解答</span><span class="sxs-lookup"><span data-stu-id="b6edf-131">Frequently asked questions</span></span>

<span data-ttu-id="b6edf-132">**"FIPS 140 Validated"和"FIPS 140 compliant"之间有什么区别？**</span><span class="sxs-lookup"><span data-stu-id="b6edf-132">**What is the difference between 'FIPS 140 Validated' and 'FIPS 140 compliant'?**</span></span>

<span data-ttu-id="b6edf-133">"FIPS 140 已验证"意味着 CMVP 已验证加密模块或嵌入模块的产品 () 验证为符合 FIPS 140-2 要求。</span><span class="sxs-lookup"><span data-stu-id="b6edf-133">'FIPS 140 Validated' means that the cryptographic module, or a product that embeds the module has been validated ('certified') by the CMVP as meeting the FIPS 140-2 requirements.</span></span> <span data-ttu-id="b6edf-134">"FIPS 140 兼容"是依赖 FIPS 140 验证产品实现加密功能的 IT 产品的行业术语。</span><span class="sxs-lookup"><span data-stu-id="b6edf-134">'FIPS 140 compliant' is an industry term for IT products that rely on FIPS 140 Validated products for cryptographic functionality.</span></span>

<span data-ttu-id="b6edf-135">**Microsoft 何时执行 FIPS 140 验证？**</span><span class="sxs-lookup"><span data-stu-id="b6edf-135">**When does Microsoft undertake a FIPS 140 validation?**</span></span>

<span data-ttu-id="b6edf-136">启动模块验证的节奏与 Windows 10 和 Windows Server 的功能更新一致。</span><span class="sxs-lookup"><span data-stu-id="b6edf-136">The cadence for starting a module validation aligns with the feature updates of Windows 10 and Windows Server.</span></span> <span data-ttu-id="b6edf-137">随着软件行业的发展，随着每月软件更新，操作系统的发布频率也越来越高。</span><span class="sxs-lookup"><span data-stu-id="b6edf-137">As the software industry evolved, operating systems are released more frequently, with monthly software updates.</span></span> <span data-ttu-id="b6edf-138">Microsoft 对功能版本进行验证，但在两次发布之间，旨在最大限度地减少对加密模块的更改。</span><span class="sxs-lookup"><span data-stu-id="b6edf-138">Microsoft undertakes validation for feature releases, but in between releases, seeks to minimize the changes to the cryptographic modules.</span></span>

<span data-ttu-id="b6edf-139">**FIPS 140 验证中包含哪些计算机？**</span><span class="sxs-lookup"><span data-stu-id="b6edf-139">**Which computers are included in a FIPS 140 validation?**</span></span>

<span data-ttu-id="b6edf-140">Microsoft 在运行 Windows 10 和 Windows Server 的具有代表性的硬件配置示例上验证加密模块。</span><span class="sxs-lookup"><span data-stu-id="b6edf-140">Microsoft validates cryptographic modules on a representative sample of hardware configurations running Windows 10 and Windows Server.</span></span> <span data-ttu-id="b6edf-141">当环境使用硬件时接受此 FIPS 140-2 验证是一种常见做法，这类似于用于验证过程的示例。</span><span class="sxs-lookup"><span data-stu-id="b6edf-141">It is common industry practice to accept this FIPS 140-2 validation when an environment uses hardware, which is similar to the samples used for the validation process.</span></span>

<span data-ttu-id="b6edf-142">**NIST 网站上列出了许多模块。我如何知道哪个适用于我的代理？**</span><span class="sxs-lookup"><span data-stu-id="b6edf-142">**There are many modules listed on the NIST website. How do I know which one applies to my agency?**</span></span>

<span data-ttu-id="b6edf-143">如果需要使用通过 FIPS 140-2 验证的加密模块，则需要验证使用的版本是否显示在验证列表中。</span><span class="sxs-lookup"><span data-stu-id="b6edf-143">If you are required to use cryptographic modules validated through FIPS 140-2, you need to verify that the version you use appears on the validation list.</span></span> <span data-ttu-id="b6edf-144">CMVP 和 Microsoft 维护一个经验证的加密模块列表（按产品发布组织）以及用于确定哪些模块安装在 Windows 系统的说明。</span><span class="sxs-lookup"><span data-stu-id="b6edf-144">The CMVP and Microsoft maintain a list of validated cryptographic modules, organized by product release, along with instructions for identifying which modules are installed on a Windows system.</span></span> <span data-ttu-id="b6edf-145">有关配置符合标准的系统的信息，请参阅 Windows 和 Windows [Server FIPS 140-2 内容](https://aka.ms/AA6ehud)。</span><span class="sxs-lookup"><span data-stu-id="b6edf-145">For more information on configuring systems to be compliant, see the [Windows and Windows Server FIPS 140-2 content](https://aka.ms/AA6ehud).</span></span>

<span data-ttu-id="b6edf-146">**"在 FIPS 模式下操作时"对证书意味着什么？**</span><span class="sxs-lookup"><span data-stu-id="b6edf-146">**What does 'When operated in FIPS mode' mean on a certificate?**</span></span>

<span data-ttu-id="b6edf-147">此警告会告知读者，必须遵循必需的配置和安全规则，才能按照与 FIPS 140-2 安全策略一致的方式使用加密模块。</span><span class="sxs-lookup"><span data-stu-id="b6edf-147">This caveat informs the reader that required configuration and security rules must be followed to use the cryptographic module in a way that is consistent with its FIPS 140-2 security policy.</span></span> <span data-ttu-id="b6edf-148">每个模块都有自己的安全策略（一个准确规范其操作依据的安全规则），并且使用批准的加密算法、加密密钥管理和身份验证技术。</span><span class="sxs-lookup"><span data-stu-id="b6edf-148">Each module has its own security policy — a precise specification of the security rules under which it will operate — and employs approved cryptographic algorithms, cryptographic key management, and authentication techniques.</span></span> <span data-ttu-id="b6edf-149">安全规则在每个模块的安全策略中定义。</span><span class="sxs-lookup"><span data-stu-id="b6edf-149">The security rules are defined in the security policy for each module.</span></span> <span data-ttu-id="b6edf-150">有关详细信息，包括通过 CMVP 验证的每个模块的安全策略链接，请参阅[Windows 和 Windows Server FIPS 140-2 内容](https://aka.ms/AA6ehud)。</span><span class="sxs-lookup"><span data-stu-id="b6edf-150">For more information, including links to the security policy for each module validated through the CMVP, see the [Windows and Windows Server FIPS 140-2 content](https://aka.ms/AA6ehud).</span></span>

<span data-ttu-id="b6edf-151">**FedRAMP 是否需要 FIPS 140-2 验证？**</span><span class="sxs-lookup"><span data-stu-id="b6edf-151">**Does FedRAMP require FIPS 140-2 validation?**</span></span>

<span data-ttu-id="b6edf-152">是的，联邦风险和授权管理计划 (FedRAMP) 依赖于 [NIST SP 800-53 修订版 4](https://nvd.nist.gov/800-53/Rev4/)定义的控制基线，包括 [SC-13](https://nvd.nist.gov/800-53/Rev4/control/SC-13) 加密保护，管理 FIPS 验证加密或 NSA 批准的加密的使用。</span><span class="sxs-lookup"><span data-stu-id="b6edf-152">Yes, the Federal Risk and Authorization Management Program (FedRAMP) relies on control baselines defined by the [NIST SP 800-53 Revision 4](https://nvd.nist.gov/800-53/Rev4/), including [SC-13 Cryptographic Protection](https://nvd.nist.gov/800-53/Rev4/control/SC-13) mandating the use of FIPS-validated cryptography or NSA-approved cryptography.</span></span>

<span data-ttu-id="b6edf-153">**能否在我的机构认证过程中使用 Microsoft 遵守 FIPS 140-2？**</span><span class="sxs-lookup"><span data-stu-id="b6edf-153">**Can I use Microsoft's adherence to FIPS 140-2 in my agency's certification process?**</span></span>

<span data-ttu-id="b6edf-154">为了符合 FIPS 140-2，系统必须配置为在 FIPS 批准的操作模式下运行，这包括确保加密模块仅使用 FIPS 批准的算法。</span><span class="sxs-lookup"><span data-stu-id="b6edf-154">To comply with FIPS 140-2, your system must be configured to run in a FIPS approved mode of operation, which includes ensuring that a cryptographic module uses only FIPS-approved algorithms.</span></span> <span data-ttu-id="b6edf-155">有关配置符合标准的系统的信息，请参阅 Windows 和 Windows [Server FIPS 140-2 内容](https://aka.ms/AA6ehud)。</span><span class="sxs-lookup"><span data-stu-id="b6edf-155">For more information on configuring systems to be compliant, see the [Windows and Windows Server FIPS 140-2 content](https://aka.ms/AA6ehud).</span></span>

<span data-ttu-id="b6edf-156">**FIPS 140-2 和通用条件之间有什么关系？**</span><span class="sxs-lookup"><span data-stu-id="b6edf-156">**What is the relationship between FIPS 140-2 and Common Criteria?**</span></span>

<span data-ttu-id="b6edf-157">这是两个不同的安全标准，用途不同但相互补充。</span><span class="sxs-lookup"><span data-stu-id="b6edf-157">These are two separate security standards with different, but complementary, purposes.</span></span> <span data-ttu-id="b6edf-158">FIPS 140-2 专用于验证软件和硬件加密模块，而通用条件旨在评估 IT 软件和硬件产品中的安全功能。</span><span class="sxs-lookup"><span data-stu-id="b6edf-158">FIPS 140-2 is designed specifically for validating software and hardware cryptographic modules, while the Common Criteria is designed to evaluate security functions in IT software and hardware products.</span></span> <span data-ttu-id="b6edf-159">通用条件评估通常依赖 FIPS 140-2 验证，以提供基本加密功能正确实现的保证。</span><span class="sxs-lookup"><span data-stu-id="b6edf-159">Common Criteria evaluations often rely on FIPS 140-2 validations to provide assurance that basic cryptographic functionality is implemented properly.</span></span>

### <a name="resources"></a><span data-ttu-id="b6edf-160">资源</span><span class="sxs-lookup"><span data-stu-id="b6edf-160">Resources</span></span>

- [<span data-ttu-id="b6edf-161">FIPS Pub 140-2 加密模块的安全要求</span><span class="sxs-lookup"><span data-stu-id="b6edf-161">FIPS Pub 140-2 Security Requirements for Cryptographic Modules</span></span>](https://csrc.nist.gov/publications/fips/fips140-2/fips1402.pdf)
- [<span data-ttu-id="b6edf-162">NIST 加密模块验证程序</span><span class="sxs-lookup"><span data-stu-id="b6edf-162">NIST Cryptographic Module Validation Program</span></span>](https://csrc.nist.gov/groups/STM/cmvp/index.html)
- [<span data-ttu-id="b6edf-163">Windows、Windows Server 和 FIPS 140-2</span><span class="sxs-lookup"><span data-stu-id="b6edf-163">Windows, Windows Server, and FIPS 140-2</span></span>](/windows/security/threat-protection/fips-140-validation)
- [<span data-ttu-id="b6edf-164">Microsoft 信任中心内的合规性</span><span class="sxs-lookup"><span data-stu-id="b6edf-164">Compliance on the Microsoft Trust Center</span></span>](https://www.microsoft.com/trust-center/compliance/compliance-overview)
