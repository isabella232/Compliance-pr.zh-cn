---
title: '美国出口管理条例 (EAR) '
description: Microsoft 云服务帮助客户遵守美国出口管理条例 (EAR) 满足其合规性要求并管理出口控制风险。
keywords: Microsoft 365, 合规性, 产品/服务
ms.localizationpriority: medium
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
ms.openlocfilehash: 859067495b6811b2264ab3a379f305d428771bce
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/09/2021
ms.locfileid: "58947559"
---
# <a name="us-export-administration-regulations-ear"></a>美国出口管理条例 (EAR) 

## <a name="about-the-ear"></a>关于 EAR

美国商务部通过 BIS 工业 () 局强制执行 EAR 出口管理[ () 。 ](https://www.bis.doc.gov/) EAR 对大多数商业商品、软件和技术（包括可用于商业和国防目的以及某些防御项目的"双重用途"项目）的导出和重新导出进行广泛监管和施加控制。

BIS 指南认为，当数据或软件上传到云或在用户节点之间传输时，客户（而非云提供商）是"导出者"，他们负责确保该数据或软件的传输、存储和访问符合 EAR。

根据[BIS，](https://www.bis.doc.gov/index.php/documents/regulation-docs/412-part-734-scope-of-the-export-administration-regulations/file)导出是指将受保护的技术或技术数据传输到一个出口目的地，或将该数据释放给位于美国 (也称为被视为出口) 。  EAR 大致控制：

- 从美国导出。
- 重新导出或重新传输美国源项目和某些具有美国原点内容部分以上部分的某些外源项。 
- 转移或披露给其他国家/地区的人员。

受 EAR 限制的项目可在商业控制列表 (CCL) 中为每个项目分配唯一的"出口控制分类号" ([ECCN) 。 ](https://www.bis.doc.gov/index.php/licensing/commerce-control-list-classification/export-control-classification-number-eccn) 未在 CCL 上列出的项目被指定为 EAR99，大多数 EAR99 商业产品不需要导出许可证。 但是，根据项目的目标、最终用户或最终用途，即使是 EAR99 项目也可能需要 BIS 导出许可证。

2016 年 6 月发布的最后一条规则阐明，如果未分类技术数据和软件是使用 FIPS 140-2 验证的加密模块进行端到端加密的，并且未有意存储在以武器活动的国家/地区或俄语联合身份验证中，则 EAR 许可要求也不适用于传输和存储。 [](https://www.federalregister.gov/documents/2016/06/03/2016-12734/revisions-to-definitions-in-the-export-administration-regulations)

## <a name="microsoft-and-the-ear"></a>Microsoft 和 EAR

Microsoft 技术、产品和服务受美国出口管理条例和 EAR () 。 尽管未针对 EAR、Microsoft Azure、Microsoft Azure 政府以及 Microsoft Office 365 政府 (GCCHigh 和 DoD 环境) 提供重要的功能和工具，以帮助受 EAR 限制的合格客户管理出口控制风险并满足其合规性要求。

强制执行 EAR 的美国商务部已采取这样一个位置，即客户（而非 Microsoft 等云服务提供商）被视为其自己的客户数据的导出者。 虽然大多数客户数据不被视为受 EAR 导出控制限制的"技术"或"技术数据"，但 Microsoft 范围内云服务的结构有助于客户管理和显著缓解他们面临的潜在出口控制风险。 Microsoft 通常（但并非独占）建议为符合条件的客户使用其政府云服务。 通过适当的规划，客户可以使用以下工具和自己的内部过程来帮助确保完全遵守美国出口控制。

- **数据位置上的控件**。 客户可以了解其数据的存储位置以及访问用于限制其存储的稳固工具。 因此，他们可以确保其数据存储在美国，并尽量减少在美国以外传输受控技术或技术数据。 此外，客户数据存储在不符合要求的位置，与"有意存储"数据的 EAR 限制一致：25 个组 D：5 国家/地区或俄语联合身份验证中均没有 Azure 数据中心。
- **端到端加密**。 通过利用在 EAR 中指定的物理存储位置的端到端加密安全港，Microsoft 范围内云服务提供了可帮助防止出口控制风险的加密功能。 它们还为客户提供 [了多种用于](https://aka.ms/Azure-Encryption-Overview) 加密传输中和静态数据的选项，以及选择加密选项的灵活性。
- **防止未经授权的视为导出的工具和协议**。 加密的使用还有助于防止潜在的被视为导出 (或在 EAR 下被视为重新导出) ，因为即使非美国用户有权访问加密数据，如果在加密数据时无法读取或了解数据，则不会显示任何内容;因此，没有受控数据的"释放"。

## <a name="microsoft-in-scope-cloud-platforms--services"></a>Microsoft 范围内的云平台和云服务

- [Azure 与 Azure 政府](https://aka.ms/AzureCompliance)
- [Office 365 政府版 (GCC-High 和 DoD) ](https://aka.ms/Office-365-Export-Controls)
- Intune

## <a name="how-to-implement"></a>如何实现

美国出口控制措施概述，以及客户根据 EAR 评估其义务的指南。

- [Azure](https://aka.ms/Azure-Export-Controls)
- [Office 365](https://aka.ms/Office-365-Export-Controls)

## <a name="frequently-asked-questions"></a>常见问题解答

**使用 Microsoft 云服务时，应执行哪些操作来遵守导出控制？**

在 EAR 下，将数据上载到云服务器（如 Microsoft 云）时，拥有数据的客户（而不是云服务提供商）将被视为导出者。 因此，数据的所有者（即 Microsoft 客户）必须仔细评估他们对 Microsoft 云的使用可能会如何导致美国出口控制，并确定他们想要使用或存储的任何数据是否受 EAR 控制，如果是，则应用哪些控制措施。 了解有关[Azure](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=c24c11f2-2cd4-444a-9160-19762855ad3a&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ_and_White_Papers)和[Office 365](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RE1s5kI)云服务如何帮助客户确保其完全遵守美国出口控制。

**Microsoft 技术、产品和服务是否受 EAR 限制？**

大多数 Microsoft 技术、产品和服务：

- 不受 EAR 影响，因此不在商业控制列表中，并且没有 ECCN;
- 或者，它们符合 MICROSOFT 的 EAR99 或 5D992 批量市场资格，可以导出到没有许可证的非授权国家/地区，如无许可证 (NLR) 。

也就是说，为一些 Microsoft 产品分配了一个 ECCN，此 ECCN 可能需要或不需要许可证。 咨询 EAR 或法律顾问，以确定适当的许可证类型和符合导出条件的国家/地区。

**在 ITAR 中，EAR 和国际武器贸易条例 (之间) ？**

应用最广泛的美国主要出口控件是 EAR，它由美国商务部管理。 EAR 适用于具有商业和商用两用应用程序的两用途项目，以及具有纯商业应用程序的项目。

美国还有单独且更专门的出口控制法规，如管理最敏感项目和技术的 ITAR。 它们由美国国防部管理，对许多国防、国防和情报项目的导出、临时导入、重新导出和传输施加控制 (也称为"防御文章") ，包括相关的技术数据。

## <a name="resources"></a>资源

- [导出 Microsoft 产品：概述](https://www.microsoft.com/exporting/overview.aspx)
- [导出 Microsoft 产品：常见问题解答](https://www.microsoft.com/exporting/faq.aspx)
- [导出 Microsoft 产品：产品查找](https://www.microsoft.com/exporting/exporting-information.aspx)
- [加密的导出限制](/windows/uwp/security/export-restrictions-on-cryptography)
- [Microsoft 和 FIPS 140-2](offering-fips-140-2.md)
- [Microsoft 和 ITAR](offering-itar.md)
- [Microsoft 信任中心内的合规性](https://www.microsoft.com/trust-center/compliance/compliance-overview)
