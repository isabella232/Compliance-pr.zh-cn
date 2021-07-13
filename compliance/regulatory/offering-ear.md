---
title: '美国出口管理条例 (EAR) '
description: Microsoft 云服务可帮助客户遵守美国出口管理条例 (EAR) 满足其合规性要求并管理出口控制风险。
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
ms.openlocfilehash: b3867c9d8c165c451813929d49dc5936e643e95c
ms.sourcegitcommit: 9b0c8852e73e2be54a0f9c6570da67f4964f616c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/12/2021
ms.locfileid: "53384222"
---
# <a name="us-export-administration-regulations-ear"></a><span data-ttu-id="f7d37-104">美国出口管理条例 (EAR) </span><span class="sxs-lookup"><span data-stu-id="f7d37-104">US Export Administration Regulations (EAR)</span></span>

## <a name="about-the-ear"></a><span data-ttu-id="f7d37-105">关于 EAR</span><span class="sxs-lookup"><span data-stu-id="f7d37-105">About the EAR</span></span>

<span data-ttu-id="f7d37-106">美国商务部通过 BIS (工业) 局强制执行美国出口管理 ([EAR) 。 ](https://www.bis.doc.gov/)</span><span class="sxs-lookup"><span data-stu-id="f7d37-106">The US Department of Commerce enforces the Export Administration Regulations (EAR) through the [Bureau of Industry and Security (BIS)](https://www.bis.doc.gov/).</span></span> <span data-ttu-id="f7d37-107">EAR 对大多数商业商品、软件和技术（包括可用于商业和国防目的以及某些防御项目的"双重用途"项目）的导出和重新导出进行广泛监管和施加控制。</span><span class="sxs-lookup"><span data-stu-id="f7d37-107">The EAR broadly governs and imposes controls on the export and re-export of most commercial goods, software, and technology, including 'dual-use” items that can be used both for commercial and military purposes and certain defense items.</span></span>

<span data-ttu-id="f7d37-108">BIS 指南认为，当数据或软件上传到云或在用户节点之间传输时，客户（而非云提供商）是"导出者"，他们负责确保该数据或软件的传输、存储和访问符合 EAR。</span><span class="sxs-lookup"><span data-stu-id="f7d37-108">BIS guidance holds that, when data or software is uploaded to the cloud or transferred between user nodes, the customer, not the cloud provider, is the 'exporter” who has the responsibility to ensure that transfers of, storage of, and access to that data or software complies with the EAR.</span></span>

<span data-ttu-id="f7d37-109">根据[BIS，](https://www.bis.doc.gov/index.php/documents/regulation-docs/412-part-734-scope-of-the-export-administration-regulations/file)导出是指将受保护的技术或技术数据传输到一个出口目的地，或将该数据释放给位于美国 (也称为被视为出口) 。 </span><span class="sxs-lookup"><span data-stu-id="f7d37-109">[According to the BIS](https://www.bis.doc.gov/index.php/documents/regulation-docs/412-part-734-scope-of-the-export-administration-regulations/file), *export* refers to the transfer of protected technology or technical data to a foreign destination or its release to a foreign person in the United States (also referred to as a *deemed export*).</span></span> <span data-ttu-id="f7d37-110">EAR 大致控制：</span><span class="sxs-lookup"><span data-stu-id="f7d37-110">The EAR broadly governs:</span></span>

- <span data-ttu-id="f7d37-111">从美国导出。</span><span class="sxs-lookup"><span data-stu-id="f7d37-111">Exports from the United States.</span></span>
- <span data-ttu-id="f7d37-112">重新导出或重新传输美国源项目和某些具有美国原点内容部分以上部分的某些外源项。 </span><span class="sxs-lookup"><span data-stu-id="f7d37-112">Re-exports or retransfers of US-origin items and certain foreign-origin items with more than a *de minimis* portion of US-origin content.</span></span>
- <span data-ttu-id="f7d37-113">转移或披露给其他国家/地区的人员。</span><span class="sxs-lookup"><span data-stu-id="f7d37-113">Transfers or disclosures to persons from other countries.</span></span>

<span data-ttu-id="f7d37-114">受 EAR 限制的项目可在商业控制列表 (CCL) 中为每个项目分配唯一的"出口控制分类号" ([ECCN) 。 ](https://www.bis.doc.gov/index.php/licensing/commerce-control-list-classification/export-control-classification-number-eccn)</span><span class="sxs-lookup"><span data-stu-id="f7d37-114">Items subject to the EAR can be found on the Commerce Control List (CCL) where each item is assigned a unique [Export Control Classification Number (ECCN)](https://www.bis.doc.gov/index.php/licensing/commerce-control-list-classification/export-control-classification-number-eccn).</span></span> <span data-ttu-id="f7d37-115">未在 CCL 上列出的项目被指定为 EAR99，大多数 EAR99 商业产品不需要导出许可证。</span><span class="sxs-lookup"><span data-stu-id="f7d37-115">Items not listed on the CCL are designated as EAR99 and most EAR99 commercial products will not require a license to be exported.</span></span> <span data-ttu-id="f7d37-116">但是，根据项目的目标、最终用户或最终用途，即使是 EAR99 项目也可能需要 BIS 导出许可证。</span><span class="sxs-lookup"><span data-stu-id="f7d37-116">However, depending on the destination, end user, or end use of the item, even an EAR99 item may require a BIS export license.</span></span>

<span data-ttu-id="f7d37-117">2016 年 6 月发布的最后一条规则阐明，如果未分类技术数据和软件是使用 FIPS 140-2 验证的加密模块进行端到端加密的，并且未有意存储在以武器活动的国家/地区或俄语联盟中，则 EAR 许可要求也不应用于传输和存储。 [](https://www.federalregister.gov/documents/2016/06/03/2016-12734/revisions-to-definitions-in-the-export-administration-regulations)</span><span class="sxs-lookup"><span data-stu-id="f7d37-117">The [final rule](https://www.federalregister.gov/documents/2016/06/03/2016-12734/revisions-to-definitions-in-the-export-administration-regulations), published in June 2016, clarified that EAR licensing requirements also would not apply to the transmission and storage of unclassified technical data and software if they were encrypted end-to-end using FIPS 140-2 validated cryptographic modules and were not intentionally stored in a military-embargoed country or in the Russian Federation.</span></span>

## <a name="microsoft-and-the-ear"></a><span data-ttu-id="f7d37-118">Microsoft 和 EAR</span><span class="sxs-lookup"><span data-stu-id="f7d37-118">Microsoft and the EAR</span></span>

<span data-ttu-id="f7d37-119">Microsoft 技术、产品和服务受美国出口管理条例和 EAR () 。</span><span class="sxs-lookup"><span data-stu-id="f7d37-119">Microsoft technologies, products, and services are subject to the US Export Administration Regulations (EAR).</span></span> <span data-ttu-id="f7d37-120">尽管未针对 EAR、Microsoft Azure、Microsoft Azure 政府以及 Microsoft Office 365 政府 (GCCHigh 和 DoD 环境) 提供重要的功能和工具，以帮助受 EAR 限制的合格客户管理出口控制风险并满足其合规性要求。</span><span class="sxs-lookup"><span data-stu-id="f7d37-120">While there is no compliance certification for the EAR, Microsoft Azure, Microsoft Azure Government, and Microsoft Office 365 Government (GCCHigh and DoD environments) offer important features and tools to help eligible customers subject to the EAR manage export control risks and meet their compliance requirements.</span></span>

<span data-ttu-id="f7d37-121">强制执行 EAR 的美国商务部已采取这样一个位置，即客户（而非 Microsoft 等云服务提供商）被视为其自己的客户数据的导出者。</span><span class="sxs-lookup"><span data-stu-id="f7d37-121">The US Commerce Department, which enforces the EAR, has taken the position that customers, not cloud service providers such as Microsoft, are considered to be exporters of their own customer data.</span></span> <span data-ttu-id="f7d37-122">虽然大部分客户数据不被视为受 EAR 导出控制的"技术"或"技术数据"，但 Microsoft 范围内云服务的结构有助于客户管理和显著缓解他们面临的潜在的出口控制风险。</span><span class="sxs-lookup"><span data-stu-id="f7d37-122">While most customer data is not considered 'technology” or 'technical data” subject to EAR export controls, Microsoft in-scope cloud services are structured to help customers manage and significantly mitigate the potential export control risks they face.</span></span> <span data-ttu-id="f7d37-123">Microsoft 通常（但并非独占）建议为符合条件的客户使用其政府云服务。</span><span class="sxs-lookup"><span data-stu-id="f7d37-123">Microsoft generally, but not exclusively, recommends the use of its government cloud services for eligible customers.</span></span> <span data-ttu-id="f7d37-124">通过适当的规划，客户可以使用以下工具和自己的内部过程来帮助确保完全遵守美国出口控制。</span><span class="sxs-lookup"><span data-stu-id="f7d37-124">With appropriate planning, customers can use the following tools and their own internal procedures to help ensure full compliance with US export controls.</span></span>

- <span data-ttu-id="f7d37-125">**数据位置上的控件**。</span><span class="sxs-lookup"><span data-stu-id="f7d37-125">**Controls on data location**.</span></span> <span data-ttu-id="f7d37-126">客户可以了解其数据的存储位置以及访问用于限制其存储的稳固工具。</span><span class="sxs-lookup"><span data-stu-id="f7d37-126">Customers have visibility into where their data is stored and access to robust tools to restrict its storage.</span></span> <span data-ttu-id="f7d37-127">因此，他们可以确保其数据存储在美国，并尽量减少在美国以外传输受控技术或技术数据。</span><span class="sxs-lookup"><span data-stu-id="f7d37-127">They may therefore ensure that their data is stored in the United States and minimize transfer of controlled technology or technical data outside the United States.</span></span> <span data-ttu-id="f7d37-128">此外，客户数据存储在不符合要求的位置，与"有意存储"数据的 EAR 限制一致：25 个组 D：5 国家/地区或俄语联合身份验证中均没有 Azure 数据中心。</span><span class="sxs-lookup"><span data-stu-id="f7d37-128">Furthermore, customer data is not stored in a non-conforming location, consistent with EAR prohibitions on where data is 'intentionally stored”: no Azure datacenter is located in any of the 25 Group D:5 countries or the Russian Federation.</span></span>
- <span data-ttu-id="f7d37-129">**端到端加密**。</span><span class="sxs-lookup"><span data-stu-id="f7d37-129">**End-to-end encryption**.</span></span> <span data-ttu-id="f7d37-130">通过利用在 EAR 中指定的物理存储位置的端到端加密安全港，Microsoft 范围内云服务提供了可帮助防止出口控制风险的加密功能。</span><span class="sxs-lookup"><span data-stu-id="f7d37-130">By taking advantage of the end-to-end encryption safe harbor for physical storage locations specified in the EAR, Microsoft in-scope cloud services deliver encryption features that can help protect against export control risks.</span></span> <span data-ttu-id="f7d37-131">它们还为客户提供 [多种用于](https://aka.ms/Azure-Encryption-Overview) 加密传输中和静态数据的选项，以及选择加密选项的灵活性。</span><span class="sxs-lookup"><span data-stu-id="f7d37-131">They also offer customers a [wide range of options for encrypting data](https://aka.ms/Azure-Encryption-Overview) in transit and at rest, and the flexibility to choose among encryption options.</span></span>
- <span data-ttu-id="f7d37-132">**防止未经授权的视为导出的工具和协议**。</span><span class="sxs-lookup"><span data-stu-id="f7d37-132">**Tools and protocols to prevent unauthorized deemed export**.</span></span> <span data-ttu-id="f7d37-133">加密的使用还有助于防止在 EAR 下潜在的被视为导出 (或被视为重新导出) ，因为即使非美国用户有权访问加密数据，如果在加密时无法读取或了解数据，则不会显示任何内容;因此，没有受控数据的"释放"。</span><span class="sxs-lookup"><span data-stu-id="f7d37-133">The use of encryption also helps protect against a potential deemed export (or deemed re-export) under the EAR, because even if a non-US person has access to encrypted data, nothing is revealed if they cannot read or understand the data while it is encrypted; thus there is no 'release” of controlled data.</span></span>

## <a name="microsoft-in-scope-cloud-platforms--services"></a><span data-ttu-id="f7d37-134">Microsoft 范围内云平台&服务</span><span class="sxs-lookup"><span data-stu-id="f7d37-134">Microsoft in-scope cloud platforms & services</span></span>

- [<span data-ttu-id="f7d37-135">Azure 与 Azure 政府</span><span class="sxs-lookup"><span data-stu-id="f7d37-135">Azure and Azure Government</span></span>](https://aka.ms/AzureCompliance)
- [<span data-ttu-id="f7d37-136">Office 365 政府版 (GCC-High 和 DoD) </span><span class="sxs-lookup"><span data-stu-id="f7d37-136">Office 365 Government (GCC-High and DoD)</span></span>](https://aka.ms/Office-365-Export-Controls)
- <span data-ttu-id="f7d37-137">Intune</span><span class="sxs-lookup"><span data-stu-id="f7d37-137">Intune</span></span>

## <a name="how-to-implement"></a><span data-ttu-id="f7d37-138">如何实现</span><span class="sxs-lookup"><span data-stu-id="f7d37-138">How to implement</span></span>

<span data-ttu-id="f7d37-139">针对客户评估在 EAR 下的义务的美国出口控制和指南概述。</span><span class="sxs-lookup"><span data-stu-id="f7d37-139">Overview of US export controls and guidance for customers assessing their obligations under the EAR.</span></span>

- [<span data-ttu-id="f7d37-140">Azure</span><span class="sxs-lookup"><span data-stu-id="f7d37-140">Azure</span></span>](https://aka.ms/Azure-Export-Controls)
- [<span data-ttu-id="f7d37-141">Office 365</span><span class="sxs-lookup"><span data-stu-id="f7d37-141">Office 365</span></span>](https://aka.ms/Office-365-Export-Controls)

## <a name="frequently-asked-questions"></a><span data-ttu-id="f7d37-142">常见问题解答</span><span class="sxs-lookup"><span data-stu-id="f7d37-142">Frequently asked questions</span></span>

<span data-ttu-id="f7d37-143">**使用 Microsoft 云服务时，应执行哪些操作来遵守导出控制？**</span><span class="sxs-lookup"><span data-stu-id="f7d37-143">**What should I do to comply with export controls when using Microsoft cloud services?**</span></span>

<span data-ttu-id="f7d37-144">在 EAR 下，将数据上载到云服务器（如 Microsoft 云）时，拥有数据的客户（而不是云服务提供商）将被视为导出者。</span><span class="sxs-lookup"><span data-stu-id="f7d37-144">Under the EAR, when data is uploaded to a cloud server such as the Microsoft cloud, the customer who owns the data — not the cloud services provider — is considered to be the exporter.</span></span> <span data-ttu-id="f7d37-145">因此，数据的所有者（即 Microsoft 客户）必须仔细评估其使用 Microsoft 云可能会如何设置美国出口控制，并确定他们想要使用或存储的任何数据是否受 EAR 控制，如果是，则应用哪些控制措施。</span><span class="sxs-lookup"><span data-stu-id="f7d37-145">For that reason, the owner of the data — that is, the Microsoft customer — must carefully assess how their use of the Microsoft cloud may implicate US export controls and determine whether any of the data they want to use or store there may be subject to EAR controls, and if so, what controls apply.</span></span> <span data-ttu-id="f7d37-146">详细了解 Azure 和[](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RE1s5kI)[Office 365](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=c24c11f2-2cd4-444a-9160-19762855ad3a&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)云服务如何帮助客户确保完全遵守美国出口控制。</span><span class="sxs-lookup"><span data-stu-id="f7d37-146">Learn more about how [Azure](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=c24c11f2-2cd4-444a-9160-19762855ad3a&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers) and [Office 365](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RE1s5kI) cloud services can help customers ensure their full compliance with US export controls.</span></span>

<span data-ttu-id="f7d37-147">**Microsoft 技术、产品和服务是否受 EAR 限制？**</span><span class="sxs-lookup"><span data-stu-id="f7d37-147">**Are Microsoft technologies, products, and services subject to the EAR?**</span></span>

<span data-ttu-id="f7d37-148">大多数 Microsoft 技术、产品和服务：</span><span class="sxs-lookup"><span data-stu-id="f7d37-148">Most Microsoft technologies, products, and services either:</span></span>

- <span data-ttu-id="f7d37-149">不受 EAR 影响，因此不在商业控制列表中，并且没有 ECCN;</span><span class="sxs-lookup"><span data-stu-id="f7d37-149">Are not subject to the EAR and thus are not on the Commerce Control List and have no ECCN;</span></span>
- <span data-ttu-id="f7d37-150">或者，它们符合 MICROSOFT 的 EAR99 或 5D992 批量市场自我分类条件，并且可能会导出到没有许可证的非授权国家/地区，如无许可证 (NLR) 。</span><span class="sxs-lookup"><span data-stu-id="f7d37-150">Or they are EAR99 or 5D992 Mass Market-eligible for self-classification by Microsoft and may be exported to non-embargoed countries without a license as No License Required (NLR).</span></span>

<span data-ttu-id="f7d37-151">也就是说，为一些 Microsoft 产品分配了一个 ECCN，此 ECCN 可能需要或不需要许可证。</span><span class="sxs-lookup"><span data-stu-id="f7d37-151">That said, a few Microsoft products have been assigned an ECCN that may or may not require a license.</span></span> <span data-ttu-id="f7d37-152">咨询 EAR 或法律顾问，以确定适当的许可证类型和符合导出条件的国家/地区。</span><span class="sxs-lookup"><span data-stu-id="f7d37-152">Consult the EAR or legal counsel to determine the appropriate license type and eligible countries for export purposes.</span></span>

<span data-ttu-id="f7d37-153">**在 ITAR 中，EAR 和国际武器贸易条例 (之间) ？**</span><span class="sxs-lookup"><span data-stu-id="f7d37-153">**What's the difference between the EAR and International Traffic in Arms Regulations (ITAR)?**</span></span>

<span data-ttu-id="f7d37-154">应用最广泛的美国主要出口控件是 EAR，它由美国商务部管理。</span><span class="sxs-lookup"><span data-stu-id="f7d37-154">The primary US export controls with the broadest application are the EAR, administered by the US Department of Commerce.</span></span> <span data-ttu-id="f7d37-155">EAR 适用于具有商业和商用两用应用程序的两用途项目，以及具有纯商业应用程序的项目。</span><span class="sxs-lookup"><span data-stu-id="f7d37-155">The EAR is applicable to dual-use items that have both commercial and military applications, and to items with purely commercial applications.</span></span>

<span data-ttu-id="f7d37-156">美国还有单独且更专门的出口控制法规，如管理最敏感项目和技术的 ITAR。</span><span class="sxs-lookup"><span data-stu-id="f7d37-156">The United States also has separate and more specialized export control regulations, such as the ITAR, that governs the most sensitive items and technology.</span></span> <span data-ttu-id="f7d37-157">它们由美国国防部管理，对许多国防、国防和情报项目的导出、临时导入、重新导出和传输施加控制 (也称为"防御文章") ，包括相关的技术数据。</span><span class="sxs-lookup"><span data-stu-id="f7d37-157">Administered by the US Department of State, they impose controls on the export, temporary import, re-export, and transfer of many military, defense, and intelligence items (also known as 'defense articles”), including related technical data.</span></span>

## <a name="resources"></a><span data-ttu-id="f7d37-158">资源</span><span class="sxs-lookup"><span data-stu-id="f7d37-158">Resources</span></span>

- [<span data-ttu-id="f7d37-159">导出 Microsoft 产品：概述</span><span class="sxs-lookup"><span data-stu-id="f7d37-159">Exporting Microsoft Products: Overview</span></span>](https://www.microsoft.com/exporting/overview.aspx)
- [<span data-ttu-id="f7d37-160">导出 Microsoft 产品：常见问题解答</span><span class="sxs-lookup"><span data-stu-id="f7d37-160">Exporting Microsoft Products: FAQ</span></span>](https://www.microsoft.com/exporting/faq.aspx)
- [<span data-ttu-id="f7d37-161">导出 Microsoft 产品：产品查找</span><span class="sxs-lookup"><span data-stu-id="f7d37-161">Exporting Microsoft Products: Product Lookup</span></span>](https://www.microsoft.com/exporting/exporting-information.aspx)
- [<span data-ttu-id="f7d37-162">对加密的导出限制</span><span class="sxs-lookup"><span data-stu-id="f7d37-162">Export restrictions on cryptography</span></span>](/windows/uwp/security/export-restrictions-on-cryptography)
- [<span data-ttu-id="f7d37-163">Microsoft 和 FIPS 140-2</span><span class="sxs-lookup"><span data-stu-id="f7d37-163">Microsoft and FIPS 140-2</span></span>](offering-fips-140-2.md)
- [<span data-ttu-id="f7d37-164">Microsoft 和 ITAR</span><span class="sxs-lookup"><span data-stu-id="f7d37-164">Microsoft and ITAR</span></span>](offering-itar.md)
- [<span data-ttu-id="f7d37-165">Microsoft 信任中心内的合规性</span><span class="sxs-lookup"><span data-stu-id="f7d37-165">Compliance on the Microsoft Trust Center</span></span>](https://www.microsoft.com/trust-center/compliance/compliance-overview)
