---
title: 根据 GDPR 对 Azure 进行 DPIA
description: 查找信息以确定在使用 Microsoft Azure 时是否需要进行数据保护影响评估 (DPIA)。
keywords: DPIA, Microsoft 365, Microsoft 365 教育版, Microsoft 365 文档, GDPR
ms.localizationpriority: high
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmazz
manager: laurawi
audience: itpro
ms.collection:
- GDPR
- M365-security-compliance
- MS-Compliance
hideEdit: true
titleSuffix: Microsoft GDPR
ms.custom: seo-marvel-mar2020
ms.openlocfilehash: a4b04fe9e72986b9fa706a81c61a781e46695599
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/12/2021
ms.locfileid: "59158190"
---
# <a name="data-protection-impact-assessments-guidance-for-data-controllers-using-microsoft-azure"></a>数据保护影响评估：使用 Microsoft Azure 的数据控制者指南

根据一般数据保护条例 (GDPR)，数据控制者需要为“可能对自然人的权限和自由造成高风险”的处理操作准备数据保护影响评估(DPIA)。 Microsoft Azure 本身并不一定要求由使用它的数据控制者创建 DPIA。 相反，是否需要 DPIA 将取决于数据控制者部署、配置和使用 Microsoft Azure 的 *方式* 的细节和环境。 无论何种情况，DPIA 都应在项目生命周期的早期开始，并与规划和开发过程同步进行。

此文档的目的是为数据控制者提供 Microsoft Azure 的相关信息，帮助他们确定是否需要 DPIA 以及要包含的详细信息。

>[!Note]
>Microsoft 未在本文中提供任何法律建议。本文仅供参考。建议客户与其隐私官（和/或指定的数据保护官 (DPO)）和/或法律顾问和/或顾问合作，以确定与使用 Microsoft Azure 或任何其他 Microsoft 联机服务相关的任何 DIA 的必要性和内容。Microsoft 在本文中不提供任何法律建议。

## <a name="part-1-determining-whether-a-dpia-is-needed"></a>第 1 部分：确定是否需要 DPIA

GDPR 第 35 条规定要求由数据控制者来创建数据保护影响评估（DPIA），“用于在考虑某种处理类型的本质、范围、环境和目的的情况下评估该处理类型（尤其是使用新技术的处理类型）是否会对自然人的权利和自由产生高风险。”它进一步规定了指示此类高风险的特定因素（将在下表中讨论）。根据控制者具体实施和使用 Microsoft Azure 的情况，确定是否需要 DPIA 时，数据控制者应考虑以下因素，以及任何其他相关因素。

|**高风险因素**|**Microsoft Azure 的相关信息**|
|:----|:----|
| 基于自动化处理对自然人的私人方面进行系统全面的评估（包括剖析以及会对自然人产生法律效应或显著影响自然人的决策）。| Microsoft Azure 不具有特定的自动数据处理功能。 <br><br> *但是，由于 Azure 是一项高度可定制的服务，数据控制者可对其进行配置，以用于此类处理*。控制者应根据 Azure 的使用情况决定是否对其进行配置。 |
| 处理大量特殊类别的数据，如种族或族裔、政治观点、宗教或哲学信仰、工会成员身份、基因数据、用于唯一标识自然人的生物识别数据、关于自然人性生活健康或性取向数据的数据，或与刑事犯罪和违法行为相关的个人数据。 | Microsoft Azure 不专用于处理特殊类别的个人数据，并且使用 Azure 并不会增加控制者处理数据本身所具有的风险。 <br><br> *不过，数据控制者可使用 Microsoft Azure 处理枚举的特殊类别的数据*。Microsoft Azure 是一项高度可定制的服务，支持客户跟踪或处理任何类型的数据，包括特殊类别的个人数据。但作为数据处理者，Microsoft 不对此类使用进行任何控制，且通常对此类使用鲜有或没有任何见解。数据控制者应确保恰当使用数据控制者的数据。 |
| 大规模系统化监视公开可访问区域  | Microsoft Azure 不专用于进行或帮助此类监视。 <br><br> *不过，数据控制者可使用 Microsoft Azure 处理通过此类监视收集的数据。* Microsoft Azure 是一项高度可定制的服务，支持客户跟踪或处理任何类型的数据，包括监视数据。但作为数据处理者，Microsoft 不对此类使用进行任何控制，且通常对此类使用鲜有或没有任何见解。数据控制者应确保恰当使用数据控制者的数据。 |

## <a name="part-2-contents-of-a-dpia"></a>第 2 部分：DPIA 的内容

第 35(7) 条规定，数据保护影响评估应指定处理的目的和预期处理的系统化说明。综合 DPIA 的系统化说明可能包括所处理数据的类型、数据保留时间、数据存储位置和传输位置以及有权访问数据的第三方等因素。此外，DPIA 还必须包括：

- 对与处理操作的目的相关的必要性和合理性的评估；
- 对自然人的权力和自由带来的风险的评估；以及
- 应对风险的措施（包括保护措施、安全措施和机制），以确保对个人数据的保护并证明符合此条例的规定（将数据使用者和其他相关人员的合法权益考虑在内）。

下表包含与上述每个元素相关的 Microsoft Azure 信息。如第 1 部分中所述，根据控制者的具体实施和 Microsoft Azure 的使用情况，数据控制者必须考虑下表提供的详细信息，以及任何其他相关因素。

|**DPIA 的元素**|**Microsoft Azure 的相关信息**|
|:---|:---|
| 处理目的 | 使用 Microsoft Azure 处理数据的目的由实施、配置和使用它的控制者确定。 <br><br> 正如[联机服务条款](https://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=46)和[数据保护附录](https://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=67)中所规定，作为数据处理者，Microsoft 处理客户数据以根据客户的书面说明为客户提供联机服务。 <br><br> 正如[联机服务条款](https://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=46)和[数据保护附录](https://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=67)标准中的详细信息中，Microsoft 还使用个人数据来支持有限的合法业务运营，包括：(1) 账单和帐户管理；(2) 薪酬（例如，计算员工佣金和合作伙伴奖励）；(3) 内部报告和建模（例如，预测、收入、产能计划、产品策略）；(4) 打击可能影响 Microsoft 或 Microsoft 产品的欺诈、网络犯罪或网络攻击；(5) 改善可访问性、隐私或能效的核心功能；(6) 财务报告和履行法律义务（受联机服务条款中概述的客户数据披露的限制）。 <br><br> Microsoft 是用于支持这些特定合法业务运营的个人数据处理的控制者。 通常，Microsoft 在将个人数据用于我们的合法业务运营之前会对其进行汇总处理，从而消除 Microsoft 识别特定个人身份的能力，并以最不易识别的形式使用个人数据，以支持合法业务运营所需的处理。 <br><br> Microsoft 不会将因此获得的客户数据或信息用于分析、广告或类似商业目的。 |
| 处理的个人数据类别  | *客户数据 - 客户或代表客户通过使用企业服务提供给 Microsoft 的所有数据，包括所有文本、声音、视频或图像文件以及软件。客户数据包括（1）最终用户的身份信息（例如，Azure Active Directory 中的用户名和联系信息）和客户上传到特定服务或者在特定服务中创建的客户内容（例如，Azure 存储帐户中的客户内容，Azure SQL 数据库的客户内容，或 Azure 虚拟机中的客户虚拟机映像）。<br><br> *系统生成日志 - Microsoft 生成的用于帮助 Microsoft 向用户提供企业服务的日志和相关数据。系统生成日志主要包括化名数据，其带有系统生成的唯一标识符，无法单独识别个人，但可用于向用户提供企业服务。系统生成日志还可能包含最终用户的身份信息，例如用户名。<br><br> *支持数据 - 客户或代表客户通过与 Microsoft 签订协定以获取联机服务技术支持而提供给 Microsoft 的数据（或客户授权 Microsoft 从联机服务获取的数据）。 <br><br> 有关 Azure 所处理数据的详细信息，请参阅[联机服务条款](https://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=46)（包括数据处理协议）和 [Microsoft 信任中心](https://www.microsoft.com/trustcenter)。</p> |
| 数据保留 | Microsoft 将在客户有权使用该联机服务期间保留和处理客户数据，直到客户检索所有客户数据或根据 OST 的条款删除所有客户数据。 在客户订阅期内，客户可随时访问和提取每个联机服务中存储的客户数据。 除免费试用版和领英服务外，如果客户订阅到期或终止，帐户功能将受到限制，Microsoft 会将该帐户存储在该联机服务中的客户数据保留 90 天，便于客户提取数据。 90 天保留期结束后，Microsoft 将禁用客户帐户并删除客户数据。 客户可使用 [Azure 数据使用者请求 GDPR 文档](https://servicetrust.microsoft.com/ViewPage/GDPRDSR)中介绍的功能根据数据使用者请求删除个人数据。 |
| 个人数据的位置和传输 | 客户能够在指定的[地理区域](https://azuredatacentermap.azurewebsites.net/)中预配静态的客户数据，但 OST 中规定了一些例外情况。 有关服务部署和数据驻留的其他详细信息，请参阅联机服务条款 (OST) 的 [Microsoft 数据保护附录 (DPA)](https://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=67)和 [Azure 全球基础结构](https://azure.microsoft.com/global-infrastructure/)网页。<br><br>对于来自欧洲经济区，瑞士和英国的个人数据，Microsoft 将确保在向第三方国家/地区或国际组织传输的个人数据时实施 GDPR 第 46 条中规定的相应安全措施。 在遵守针对数据处理者的标准合同条款以及其他模范合同以外，Microsoft 还将继续遵守[隐私保护协议框架](https://www.privacyshield.gov/)的条款，但不再将其作为从欧盟/欧洲经济区向美国传输数据的基础。 |
| 与第三方下级处理者分享的数据 | Microsoft 会与充当下级处理者角色的第三方共享数据，以支持客户和技术支持、服务维护和其他操作等功能。Microsoft 将向其传输客户数据或支持数据的任何分包商都会与 Microsoft 签订书面协议，该协议的效力不低于[联机服务条款](https://www.microsoftvolumelicensing.com/DocumentSearch.aspx?Mode=3&DocumentTypeId=46)中的数据保护条款。与其共享来自 Microsoft 核心联机服务的客户数据的所有第三方下级处理者都包含在联机服务分包商列表中。可以访问支持数据的所有第三方下级处理者（包括客户在其支持互动期间选择共享的客户数据）都包含在 [Microsoft 商业支持承包商](https://www.microsoft.com/trustcenter/privacy/who-can-access-your-data-and-on-what-terms#subcontractors)列表中。 |
| 数据主体权利 | 作为数据处理者，Microsoft 会向客户（也称为数据控制者）提供其数据主体的个人数据，并赋予客户在数据主体依据 GDPR 行使权利时满足其请求的能力。Microsoft 以符合产品功能和其数据处理者角色的方式实现此目标。如果 Microsoft 收到来自客户数据主体的请求（请求依据 GDPR 行使其一项或多项权利），则会将请求转发给数据控制者。<br><br> Azure 数据主体请求指南向数据控制者介绍了如何使用 Azure 中的功能来支持数据主体权限。 <br><br> 对于为支持合法业务流程而处理的个人数据，来自需要依据 GDPR 行使权力的数据主体的请求应定向到 Microsoft，如 Microsoft 隐私声明中所述。 <br><br> Microsoft 在将个人数据用于我们的合法业务运营之前通常会对其进行汇总处理，并且无法在汇总中识别特定个人的个人数据。 此操作将极大地降低个人的隐私风险。  如果 Microsoft 不能识别个人身份，它将无法支持数据主体的访问权、擦除权、可移植权或对处理的限制权或反对权。 <br><br> [Azure 数据使用者请求 GDPR 文档](https://servicetrust.microsoft.com/ViewPage/GDPRDSR)介绍如何使用 Azure 中的功能支持数据使用者权力。 |
| 对与处理操作的目的相关的必要性和合理性的评估 | 这种评估将取决于数据控制者的处理需求和目的。<br><br> Microsoft 采取相关措施来支持提供服务，例如对用于支持其合法业务运营的个人数据进行匿名化或汇总处理，以便最大程度地降低对使用该服务的数据主体进行此类处理的风险。 <br><br> 为了向数据控制者提供服务，Microsoft 需要进行某些处理，此类是必要且合理的。Microsoft 在 OST 中做出此承诺。 |
| 对数据使用者的权力和自由带来的风险的评估 | 使用 Microsoft Azure 对数据使用者的权力和自由带来的关键风险取决于数据控制者实施、配置和使用 Microsoft Azure 的方式和背景。<br><br> 然而，与其他所有服务一样，该服务中保存的个人数据可能存在未经授权的访问或意外泄漏的风险。OST 中说明了 Microsoft 用于应对此类风险的措施，本文后面将进一步详细讨论。 |
| 应对风险的措施（包括保护措施、安全措施和机制），以确保对个人数据的保护并证明符合此 GDPR 的规定（将数据使用者和其他相关人员的合法权益考虑在内）。 | Microsoft 致力于帮助保护客户数据的安全。OST 中详细说明了 Microsoft 采取的安全措施。 <br><br> Microsoft 遵守严格的安全标准和行业领先的数据保护方法。Microsoft 不断改进其体系，以应对新的威胁。有关云治理和隐私条例的详细信息，请参阅[信任中心的云治理和隐私](https://www.microsoft.com/trustcenter/guidance/ensure-compliance)页。 <br><br> Microsoft 采取合理且适当的技术和组织措施来保护其处理的个人数据。这些措施包括但不限于，内部隐私策略和条例、合同承诺以及国际和地区标准认证。有关详细信息，请参阅[信任中心的隐私标准页](https://www.microsoft.com/trustcenter/privacy/we-set-and-adhere-to-stringent-standards)。 <br><br> Microsoft 向客户提供重要、透明的安全和隐私材料，帮助 Microsoft 解释对个人数据的使用和处理。客户如有疑问，尽可联系 Microsoft。 <br><br> 此外，Microsoft 履行 GDPR 规定的适用于数据处理者的所有其他义务，包括但不限于数据保护影响评估和记录保存。 <br><br> 当 Microsoft 为其合法业务运营处理个人数据时，它将履行适用于数据控制者的 GDPR 义务。 |

## <a name="learn-more"></a>了解详细信息

- [Microsoft 信任中心](https://www.microsoft.com/trust-center/privacy/gdpr-overview)
