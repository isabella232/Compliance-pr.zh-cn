---
title: Windows 诊断数据处理器配置 GDPR 和 CCPA 的数据主体请求
description: 了解如何使用 Microsoft 产品、服务和管理工具来查找和处理个人数据以响应 DSR。
keywords: Microsoft 365, Microsoft 365 教育版, Microsoft 365 文档, GDPR
ms.localizationpriority: high
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
ms.openlocfilehash: 202b8aa75d3dd6fc94025a1a30f922563fc73e7b
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/12/2021
ms.locfileid: "59158176"
---
# <a name="windows-diagnostic-data-processor-configuration-data-subject-requests-for-the-gdpr-and-ccpa"></a>Windows 诊断数据处理器配置 GDPR 和 CCPA 的数据主体请求

>[!NOTE]
>本主题适用于 2021 年 7 月更新的版本 1809 及更高版本的 Windows 10 企业版、专业版和教育版。

## <a name="introduction-to-data-subject-requests-dsrs"></a>数据主体请求 (DSR) 简介

一般数据保护条例 (GDPR) 赋予民众（在条例中称为 _数据主体_）权利，即管理已由雇主或其他类型机构或组织（称为 _数据控制者_ 或简称为 _控制者_）收集的个人数据。 根据 GDPR，个人数据的定义很宽泛，即指与已识别或可识别的自然人相关的任何数据。 GDPR 赋予数据主体对其个人数据的特定权利；这些权利包括，获取个人数据副本、请求更正个人数据、限制个人数据处理、删除个人数据，或接收能转移给另一个控制者的电子格式个人数据。 数据主体向控制者发出的对其个人数据执行操作的正式请求，称为 _数据主体请求_ (DSR)。

同样，加州消费者隐私法案 (CCPA) 规定了加州消费者的隐私权和义务，包括与 GDPR 的数据主体权利类似的权利，例如删除、访问和接收（可移植性）其个人信息的权利。 CCPA 还就某些披露规定了在选择行使权限时防止歧视的保障措施，并就分类为“销售”的特定数据传输提出了“选择退出/选择加入”要求。 “出售”广义定义为包含共享数据来换取有值对价的行为。 有关 CCPA 的详细信息，请参阅[加州消费者隐私法案](/microsoft-365/compliance/offering-ccpa)和[加州消费者隐私法案常见问题解答](/microsoft-365/compliance/ccpa-faq)。

本指南讨论了如何使用 Microsoft 产品、服务和管理工具帮助我们的控制者客户查找和操作个人数据以响应 DSR。具体而言，这包括如何在启用Windows 诊断数据处理器配置时在 Microsoft 收集的Windows 诊断数据中查找、访问和处理个人数据。下面是本指南中所列流程的快速概述：

1. **访问** - 检索与数据主体关联的 Windows 诊断数据，如果请求，创建可供数据主体使用的副本。
2. **删除** - 永久删除与数据主体关联的 Windows 诊断数据。
3. **导出** - 向数据主体提供 Windows 诊断数据的电子副本（采用机器可读格式）。

根据 CCPA 的定义，个人信息是指与已识别或可识别人员相关的任何信息。 个人的私人、公共或工作角色之间没有任何区别。 所定义的“个人信息”术语与 GDPR 下的“个人信息”一致。 但是，CCPA 还包括家人和家庭数据。 有关 CCPA 的详细信息，请参阅[加州消费者隐私法案](/microsoft-365/compliance/offering-ccpa)和[加州消费者隐私法案常见问题解答](/microsoft-365/compliance/ccpa-faq)。

本指南中的每个部分都概述了数据控制器组织在启用 Windows 诊断数据处理器配置时，为 Microsoft 收集的 Windows 诊断数据响应 DSR 所采取的技术过程。

## <a name="terminology"></a>术语

以下列表提供了与本指南相关的术语定义。

* _控制者_ - 单独或与其他人一起确定个人数据处理的用途和途径的自然人或法人、公共机构、机关或其他实体；如果欧盟或成员国法律确定了此类处理的用途和途径，欧盟或成员国法律可能会规定控制者或具体提名条件。

* _个人数据和数据主体_ — 身份已识别或可识别的自然人（“数据主体”）的任何相关信息；身份可识别的自然人是指可被直接或间接识别的自然人，尤其是通过参考姓名、证件号码、位置数据、联机标识符等标识，或通过参考特定于该自然人的身体、生理、基因、精神、经济、文化或社会标识的一个或多个因素进行识别。

* _处理者_ — 指代表控制者处理个人数据的自然人或法人、公共机关、代理或其他团体。。

* _客户数据_ — 客户或代表客户通过使用企业服务提供给 Microsoft 的所有数据，包括所有文字、声音、视频或图像文件以及软件。 

* _Windows 诊断数据_ - Windows 设备中有关设备以及 Windows 和相关软件性能的技术数据。 用它可以使 Windows 保持最新、安全、可靠、高性能，并改进产品。 Windows 诊断数据的一些示例包括正在使用的硬件类型、安装的应用程序及其用途，以及设备驱动程序的可靠性信息。 某些 Windows 组件和应用会直接连接到 Microsoft 服务，但它们交换的数据不是 Windows 诊断数据。 例如，交换用户的位置以获取当地天气或新闻不是 Windows 诊断数据的示例。

## <a name="how-to-use-this-guide"></a>如何使用本指南

启用Windows 诊断数据处理器配置时，你将成为从设备收集的 Windows 诊断数据的控制器。 有关此配置的详细信息，请参阅 [在组织中配置 Windows 诊断数据](/windows/privacy/configure-windows-diagnostic-data-in-your-organization)。

## <a name="windows-diagnostic-data"></a>Windows 诊断数据

Microsoft 使你能够访问、删除和导出与用户使用启用了 Windows 诊断数据处理器配置的设备相关的Windows 诊断数据。

> [!IMPORTANT]
> 某些 Windows 诊断数据仅与设备标识符相关联，不与特定用户关联。 此类型的设备级别数据不会导出，并且会在 30 天内从我们的系统中删除。<br><br>
> 不支持修正 Windows 诊断数据的功能。 Windows 诊断数据构成 Windows 内执行的实际操作，对此类数据的修改将会损坏操作的历史记录，增加安全风险并危害可靠性。

下一部分提供有关如何对与 Azure Active Directory (AAD) 用户 ID 关联的 Windows 诊断数据执行数据主体请求的步骤。 有关详细信息，请参阅 [Windows 10 和隐私合规性：面向 IT 和合规专业人员的指南](/windows/privacy/windows-10-and-privacy-compliance)。

## <a name="executing-dsrs-against-windows-diagnostic-data"></a>针对 Windows 诊断数据执行 DSR

Microsoft 让你能够通过 Azure 门户访问、删除和导出某些 Windows 诊断数据，也可直接通过预先存在的应用程序编程接口 (API) 执行此类操作。

### <a name="step-1-access"></a>步骤 1：访问

Microsoft 为组织内的租户管理员提供了一种方法来访问与特定用户使用启用了 Windows 诊断数据处理器配置的设备相关的 Windows 诊断数据。为访问请求检索到的数据将通过导出方式以机器可读格式提供，并在允许用户知道数据与哪些设备和服务关联的文件中提供。如前文所述，检索到的数据不包括可能会危及 Windows 设备安全性或稳定性的数据。

Azure 门户让企业客户的租户管理员能够管理 DSR 访问请求。 [Azure DSR，第 2 部分，步骤 3：导出](/microsoft-365/compliance/gdpr-dsr-azure#step-3-export)介绍如何通过 Azure 门户以导出方式对 Windows 诊断数据执行 DSR 访问请求。

### <a name="step-2-delete"></a>步骤 2：删除

Microsoft 提供了基于特定用户的 Azure Active Directory 对象执行基于用户的 DSR 删除请求的方法。

对于基于用户的删除请求，Microsoft 提供了两种解决方案。  门户体验，让企业客户的租户管理员能够管理 DSR 删除请求。 [Azure DSR，第 1 部分，步骤 5：删除](/microsoft-365/compliance/gdpr-dsr-azure#step-5-delete)，介绍了如何通过删除用户和关联的数据，通过 Azure 门户对 Windows 诊断数据执行 DSR 删除请求。

Microsoft 还提供了通过预先存在的应用程序编程接口 (API) 直接删除用户（进而删除 Windows 诊断数据）的功能。 有关详细信息，请参阅 [API 参考文档](/graph/api/directory-deleteditems-delete)。

>[!IMPORTANT]
>删除收集的数据不会停止从设备进一步收集。 若要关闭数据收集，请按照[各个服务的参考文档](/windows/privacy/configure-windows-diagnostic-data-in-your-organization#enterprise-management)中所述的步骤进行操作。

### <a name="step-3-export"></a>步骤 3：导出

租户管理员是组织中唯一可以访问与特定用户使用启用了 Windows 诊断数据处理器配置的设备相关的 Windows 诊断数据的人员。 为导出请求检索到的数据将以机器可读格式提供，并在允许用户知道数据与哪些设备和服务关联的文件中提供。 如前文所述，检索到的数据不包括可能会危及 Windows 设备安全性或稳定性的数据。 [Azure DSR，第 2 部分，步骤 3：导出](/microsoft-365/compliance/gdpr-dsr-azure#step-3-export)，介绍了如何通过 Azure 门户对 Windows 诊断数据执行 DSR 导出请求。

Microsoft 还提供通过预先存在的应用程序编程接口 (API) 直接导出 Windows 诊断数据的功能。 有关详细信息，请参阅 [API 参考文档](/graph/api/user-exportpersonaldata)。

## <a name="notify-us-about-exporting-or-deleting-issues"></a>通知我们有关导出或删除问题

如果在从 Azure 门户导出或删除 Windows 诊断数据时遇到问题，请转到 Azure 门户“**帮助 + 支持**”边栏选项卡，并在“**订阅管理”>“订阅的隐私与合规请求”>“隐私边栏选项卡和 GDPR 请求**”下提交新票证。

>[!NOTE]
>最多可能需要 5 天才能完成 Windows 诊断数据导出请求。 如果您遇到问题，请在开具支持票证前至少等待 7 天。
