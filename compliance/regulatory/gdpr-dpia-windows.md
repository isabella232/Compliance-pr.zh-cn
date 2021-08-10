---
title: 数据保护影响评估 （DPIA） - 控制者使用 Windows 诊断数据处理者配置的指南
description: 查找信息以确定在使用 Microsoft Windows 企业数据处理者服务时是否需要进行数据保护影响评估 (DPIA)。
keywords: DPIA, Microsoft 365, Microsoft 365 教育版, Microsoft 365 文档, GDPR
localization_priority: Priority
ROBOTS: NOINDEX, NOFOLLOW
ms.prod: microsoft-365-enterprise
ms.topic: article
f1.keywords:
- NOCSH
ms.author: robmazz
author: robmaz
manager: laurawi
ms.reviewer: delinat
audience: itpro
ms.collection:
- GDPR
- M365-security-compliance
- MS-Compliance
hideEdit: true
ms.openlocfilehash: 912bd80aea4e02eaa7e4d18f2f019eb3a6909e5d011204a1bb2cc299015f78fe
ms.sourcegitcommit: af1925730de60c3b698edc4e1355c38972bdd759
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/05/2021
ms.locfileid: "54289870"
---
# <a name="data-protection-impact-assessments-guidance-for-controllers-using-windows-diagnostic-data-processor-configuration"></a>数据保护影响评估：控制者使用 Windows 诊断数据处理者配置的指南

>[!NOTE]
>本主题适用于 2021 年 7 月更新的版本 1809 及更高版本的 Windows 10 企业版、专业版和教育版。

根据一般数据保护条例 (GDPR)，数据控制者需要为“可能对自然人的权限和自由造成高风险”的处理操作准备数据保护影响评估(DPIA)。 Windows 诊断数据处理者配置本身并不一定要求由使用它的控制者创建 DPIA。 相反，是否需要 DPIA 将取决于控制者部署、配置和使用 [Windows 诊断数据处理者配置](/windows/privacy/configure-windows-diagnostic-data-in-your-organization)的方式的细节和环境。

此文档的目的是为控制者提供 Windows 诊断数据处理者配置的相关信息，帮助他们确定是否需要 DPIA 以及要包含的详细信息（如果需要）。

>[!Note]
>Microsoft 在此文档中未提供任何法律建议。 本文档仅供参考。 我们鼓励客户与其隐私官和法律顾问合作，以确定与使用 Windows 诊断数据处理者配置或任何其他 Microsoft 联机服务相关的任何 DPIA 的必要性和内容。

## <a name="part-1-determining-whether-a-dpia-is-needed"></a>第 1 部分：确定是否需要 DPIA

GDPR 第 35 条规定要求由控制者来创建数据保护影响评估（DPIA），“用于在考虑某种处理类型的本质、范围、环境和目的的情况下评估该处理类型（尤其是使用新技术的处理类型）是否会对自然人的权利和自由产生高风险。”它进一步规定了指示此类高风险的特定因素（将在下表中讨论）。根据控制者具体实施和使用 Windows 诊断数据处理者配置的情况，确定是否需要 DPIA 时，控制者应考虑以下因素，以及任何其他相关因素。

## <a name="table-1-windows-diagnostic-data-processor-configuration-dpia-risk-factors"></a>表 1：Windows 诊断数据处理者配置 DPIA 风险因素

| 高风险因素 | Windows 诊断数据处理者配置的相关信息 |
|:----|:----|
| 基于自动化处理对自然人的私人方面进行系统全面的评估（包括剖析以及会对自然人产生法律效应或显著影响自然人的决策）。 |Windows 数据处理者配置不具有某些自动数据处理功能。 <br><br> 但是，由于其他服务使用按照 Windows 数据处理者配置采集的诊断数据作为数据源，因此数据控制者可能会配置那些服务以用于此类处理。 控制者应根据使用按照 Windows 诊断数据处理者配置收集的诊断数据的服务的使用情况做出此决定。|
| 处理大量特殊类别的数据，如种族或族裔、政治观点、宗教或哲学信仰、工会成员身份、基因数据、用于唯一标识自然人的生物识别数据、关于自然人性生活健康或性取向数据的数据，或与刑事犯罪和违法行为相关的个人数据。 | Windows 诊断数据处理者配置不专用于处理特殊类别的个人数据，并且使用 Windows 诊断数据处理者配置并不会增加控制者处理数据本身所具有的风险。 <br><br> 但是，数据控制者可以使用利用 Windows 诊断数据处理者配置收集的诊断数据的服务来处理枚举的特殊数据类别。 使用按照 Windows 诊断数据处理者配置收集的诊断数据作为数据源的服务可以使客户能够跟踪或处理任何类型的数据，包括特殊类别的个人数据。 但作为数据处理者，Microsoft 不对此类使用进行任何控制，且对此类使用鲜有或没有任何见解。 数据控制者有责任确定数据控制者数据的适当用途。|

## <a name="part-2-contents-of-a-dpia"></a>第 2 部分：DPIA 的内容

第 35(7) 条规定，数据保护影响评估应指定处理的目的和预期处理的系统化说明。综合 DPIA 的系统化说明可能包括所处理数据的类型、数据保留时间、数据存储位置和传输位置以及有权访问数据的第三方等因素。此外，DPIA 还必须包括：

- 对与处理操作的目的相关的必要性和合理性的评估；
- 对自然人的权力和自由带来的风险的评估；以及
- 应对风险的措施（包括保护措施、安全措施和机制），以确保对个人数据的保护并证明符合此条例的规定（将数据使用者和其他相关人员的合法权益考虑在内）。

下表包含与上述每个元素相关的 Windows 诊断数据处理者配置信息。 如第 1 部分中所述，根据控制者实施和使用 Windows 诊断数据处理者配置的具体情况，数据控制者必须考虑下表提供的详细信息，以及任何其他相关因素。

## <a name="table-2-windows-diagnostic-data-processor-configuration-dpia-elements"></a>表 2：Windows 诊断数据处理者配置 DPIA 元素

| DPIA 的元素 | Windows 诊断数据处理者配置的相关信息 |
|:---|:---|
| 处理目的 | 处理按照 Windows 诊断数据处理者配置收集的诊断数据的目的是由实现、配置和使用其的控制者决定。 <br><br> 作为数据处理者，Microsoft 会根据 Microsoft 产品条款中的条款处理Windows 诊断数据。 <br><br> Microsoft 还使用个人数据来支持有限的合法业务运营，包括：(1) 账单和帐户管理；(2) 薪酬（例如，计算员工佣金和合作伙伴奖励）；(3) 内部报告和建模（例如，预测、收入、产能计划、产品策略）；(4) 打击可能影响 Microsoft 或 Microsoft 产品的欺诈、网络犯罪或网络攻击；(5) 改善可访问性、隐私或能效的核心功能；(6) 财务报告和履行法律义务（受 Windows 诊断数据披露的限制）。 <br><br> Microsoft 是用于这些特定合法业务运营的 Windows 诊断数据处理的控制者。通常，Microsoft 在将 Windows 诊断数据用于我们的合法业务运营之前会对其进行汇总处理，从而消除 Microsoft 识别特定个人身份的能力，并以最不易识别的形式使用 Windows 诊断数据，以支持合法业务运营所需的处理。 <br><br> 启用 Windows 诊断数据处理者配置时，Microsoft 不会使用收集的Windows 诊断数据，也不会将其衍生出的信息用于任何广告或类似的商业目的。|
| 处理的个人数据类别 | **Windows 诊断数据** — Windows 设备中有关设备以及 Windows 和相关软件性能的技术数据。 用它可以使 Windows 保持最新、安全、可靠、高性能，并改进产品。 Windows 诊断数据的一些示例包括正在使用的硬件类型、安装的应用程序及其用途，以及设备驱动程序的可靠性信息。 某些 Windows 组件和应用会直接连接到 Microsoft 服务，但它们交换的数据不是 Windows 诊断数据。 例如，交换用户的位置以获取当地天气或新闻不是 Windows 诊断数据的示例。 <br><br> 有关使用 Windows 诊断数据处理者配置时的数据处理的详细信息，请参阅[在组织中配置 Windows 诊断数据](/windows/privacy/configure-windows-diagnostic-data-in-your-organization)，以及[Microsoft 信任中心](https://www.microsoft.com/trust-center)。|
| 数据保留 | 根据 Microsoft 产品条款启用 Windows 诊断数据处理者配置时，Microsoft 将保留并处理收集的 Windows 诊断数据。 客户可以使用[适用于 GDPR 和 CCPA 的 Windows 诊断数据处理者配置数据主体请求](gdpr-dsr-windows.md)中所述的功能 ，根据数据主体请求删除和导出Windows 诊断数据。|
| 个人数据的位置和传输 | 启用 Windows 诊断数据处理者配置时收集的 Windows 诊断数据保留在美国的 Microsoft 数据中心。 |
| 与第三方共享数据 | Microsoft 会与充当下级处理者（即处理个人数据的分包商）角色的第三方共享数据，以实现客户和技术支持、服务维护和其他操作。 Microsoft 向其传输按照 Windows 诊断数据处理者配置收集的 Windows 诊断数据或支持数据的分包商都将与 Microsoft 签订书面协议，这些协议的保护性不低于 Microsoft 产品条款中的条款。 与其分享 Windows 诊断数据或支持数据的所有第三方分包商都包括在[分包商列表](https://www.microsoft.com/zh-CN/trust-center/privacy/data-access#subcontractors)中（请参阅“我们限制分包商的访问”）。 <br><br>Microsoft 产品条款中还规定了 Microsoft 如何回应执法机构和第三方请求按照 Windows 诊断数据处理者配置收集的 Windows 诊断数据和支持数据的情况。Microsoft 会尝试将执法机构或第三方的请求直接转达给客户，除非法律禁止。 |
| 数据主体权力 | 作为数据处理者，Microsoft 会向客户（即控制者）提供其数据主体的个人数据，并赋予客户在数据主体依据 GDPR 行使权利时满足其请求的能力。Microsoft 以符合产品功能和其数据处理者角色的方式实现此目标。如果 Microsoft 收到来自客户数据主体的请求（请求依据 GDPR 行使其一项或多项权利），会将请求转发给数据控制者。<br><br> [适用于 GDPR 和 CCPA 的 Windows 诊断数据处理者配置数据主体请求](gdpr-dsr-windows.md) 介绍了如何支持按照 Windows 诊断数据处理者配置收集的Windows 诊断数据的数据主体权利。 |
| 对与处理操作的目的相关的必要性和合理性的评估 | 这种评估将取决于数据控制者的处理需求和目的。 <br><br> 如 Microsoft 产品条款所反映的处理目的，Microsoft 需要进行某些处理，此类处理是必要且合理的。 |
| 对数据主体的权利和自由带来的风险的评估 | 使用按照 Windows 诊断数据处理者配置收集的 Windows 诊断数据对数据使用者的权利和自由带来的关键风险取决于控制者实施、配置和使用 Windows 诊断数据的方式和环境。 <br><br> 按照 Windows 诊断数据处理者配置收集的 Windows 诊断数据可能存在未经授权的访问或无意泄漏的风险。 Microsoft 产品条款中讨论了 Microsoft 为应对此类风险而采取的措施。 |
| 应对风险的措施（包括保护措施、安全措施和机制），以确保对个人数据的保护并证明符合此 GDPR 的规定（将数据使用者和其他相关人员的合法权益考虑在内）。 | Microsoft 致力于帮助保护 Windows 诊断数据的安全性。Microsoft 产品条款中介绍了 Microsoft 采取的安全措施。 <br><br> Microsoft 采取合理且适当的技术和组织措施来保护其处理的个人数据。这些措施包括但不限于，内部隐私策略和条例、合同承诺以及国际和地区标准认证。有关详细信息，请参阅[信任中心的隐私标准页](https://www.microsoft.com/trustcenter/privacy/we-set-and-adhere-to-stringent-standards)。<br><br> Microsoft 向客户提供重要、透明的安全和隐私材料，帮助 Microsoft 解释对个人数据的使用和处理。客户如有疑问，尽可联系 Microsoft。 <br><br> 此外，Microsoft 履行 GDPR 规定的适用于数据处理者的所有其他义务，包括但不限于数据保护影响评估和记录保存。 <br><br> 当 Microsoft 为其合法业务运营处理 Windows 诊断数据时，它将履行适用于数据控制者的 GDPR 义务。 |

## <a name="learn-more"></a>了解详细信息

- [Microsoft 信任中心](https://www.microsoft.com/trust-center/privacy/gdpr-overview)
