---
title: Microsoft 365 报告功能
description: 了解 Microsoft 365 中的各种报告功能，包括 Azure Active Directory 和 Exchange Online。
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-analytics
f1.keywords:
- NOCSH
ms.custom: seo-marvel-apr2020
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 2cc91f650dcaf5fdafd9f32f3c6991976b49ea04
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497516"
---
# <a name="microsoft-365-reporting-features"></a>Microsoft 365 报告功能

Microsoft 365 中的报告功能为 Azure Active Directory (Azure AD) 、Exchange Online、设备管理、监管审核和数据丢失防护提供了各种审核报告 (DLP) 。 这些报告不同于 Microsoft 365 活动报告，

## <a name="microsoft-365-reports-dashboard"></a>Microsoft 365 报表仪表板

Microsoft 365 管理中心预览中的"报告"仪表板显示 Microsoft 365 中的使用活动。 Microsoft 365 全局管理员或 Exchange Online、SharePoint Online 或 Skype for Business 管理员可以精细地了解该服务的使用情况。 例如，特定 Microsoft 365 服务中的用户数、已激活 Microsoft 365 企业应用版 (之前名为 Office 365 专业增强版) 的用户数，以及邮件在组织中流动的数量。 报告可用于最近 7、30、90 和 180 天。

可使用以下报告：

- [电子邮件活动报告](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--Email-activity-1cbe2c00-ca65-4fb9-9663-1bbfa58ebe44)
- [Microsoft Office激活报告](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--Microsoft-Office-activations-87c24ae2-82e0-4d1e-be01-c3bcc3f18c60)
- [SharePoint Online 网站使用情况报告](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--SharePoint-site-usage-4ecfb843-e5d5-464d-8bf6-7ed512a9b213)
- [OneDrive for Business 使用情况报告](https://support.office.com/article/Office-365-Reports-in-the-Admin-Center-Preview--OneDrive-for-Business-usage-0de3b312-c4e8-4e4b-a02d-32b2f726a680)
- [Yammer 活动报告](https://support.office.com/article/View-the-Yammer-Activity-report-in-the-Office-365-admin-center-preview-c7c9f938-5b8e-4d52-b1a2-c7c32cb2312a)
- [Skype for Business 活动报告](/SkypeForBusiness/skype-for-business-online-reporting/activity-report)
- [Skype for Business 对等活动报告](/SkypeForBusiness/skype-for-business-online-reporting/peer-to-peer-activity-report)
- [Skype for Business 会议组织者报告](/SkypeForBusiness/skype-for-business-online-reporting/conference-organizer-activity-report)
- [Skype for Business 会议参与者活动报告](/SkypeForBusiness/skype-for-business-online-reporting/conference-participant-activity-report)

有关详细信息，请参阅 [Microsoft 365 管理中心中的活动报表](https://support.office.com/article/activity-reports-in-the-office-365-admin-center-0d6dfb17-8582-4172-a9a9-aed798150263)。

## <a name="azure-ad-reports"></a>Azure AD 报告

Microsoft 365 使用 Azure AD 进行身份验证和身份管理。 Microsoft 365 管理员使用 Azure 生成的报告来识别异常活动和未经授权访问其数据。 可以使用 Azure AD 中的访问和使用情况报告查看组织的目录完整性和安全性。 通过此信息，您可以识别并缓解可能的安全风险。

Azure AD 报告可以导出到 Microsoft Excel，并与其他来自 Microsoft 365 的数据相关联。 例如，搜索审核日志可提供访问、身份验证和应用程序级活动的见解。 Azure AD Premium 提供了高级异常和资源使用情况报告。 这些高级报告通过应用有关设备访问和应用程序使用情况的分析来帮助你改进安全状况，并帮助你响应潜在威胁。 有关详细信息，请参阅 [Azure Active Directory 报告](/azure/active-directory/reports-monitoring/overview-reports/)。

## <a name="exchange-online-audit-reports"></a>Exchange Online 审核报告

Exchange Online 审核报告包括有关邮箱访问和管理员对 Exchange Online 租户所做的更改的详细信息。 通过邮箱审核，可以使用下表中的任务运行报告并导出 Exchange Online 审核日志。

> [!NOTE]
> 必须启用每个邮箱的邮箱审核日志记录，以便审核的事件保存在该审核日志邮箱的邮箱中。 如果未为邮箱启用邮箱审核日志记录，该邮箱的事件不会保存在 审核日志也不会显示在邮箱审核报告中。 有关详细信息，请参阅启用 [邮箱审核](https://support.office.com/article/Enable-mailbox-auditing-in-Office-365-aaca8987-5b62-458b-9882-c28476a66918)。

| 任务 | 说明 |
|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [运行非所有者邮箱访问报告](/exchange/security-and-compliance/exchange-auditing-reports/non-owner-mailbox-access-report) | 显示邮箱所有者外的其他用户访问的邮箱列表。 该报告包含有关谁访问邮箱、他们在邮箱中采取的操作以及操作是否成功的信息。 |
| [导出邮箱审核日志](/exchange/security-and-compliance/exchange-auditing-reports/export-mailbox-audit-logs) | 邮箱审核日志包含有关邮箱中除邮箱所有者外的用户的访问和操作的信息。 管理员可以指定邮箱以及生成报告的日期范围。 日志以 XML 格式导出、附加到邮件中，并发送给管理员确定的特定用户。 |
| [运行管理员角色组报告](/Office365/SecurityCompliance/eop/run-an-administrator-role-group-report-in-eop-eop) | 管理员角色组向用户分配管理权限。 这些权限允许用户执行管理任务，如重置密码、创建或修改邮箱，以及向其他用户分配管理员权限。 管理员角色组报告显示对角色组所做的更改，包括添加或删除成员。 |
| [查看管理员审核日志](/exchange/security-and-compliance/exchange-auditing-reports/view-administrator-audit-log) | 管理员审核日志列出了管理员在 Exchange Online 中执行的所有创建、更新和删除功能。 日志条目提供有关运行哪个 cmdlet、使用了哪些参数、运行该 cmdlet 的人以及受影响的对象的信息。 |
| [邮箱内容搜索和保留](/exchange/security-and-compliance/in-place-ediscovery/in-place-ediscovery) | 提供有关邮箱上对In-Place电子数据展示或In-Place保留设置的任何更改的详细信息。 |
| [导出管理员审核日志](/exchange/security-and-compliance/exchange-auditing-reports/search-role-group-changes) | 管理员审核日志特定管理操作，如在 Exchange Online 中创建、更新和删除。 日志的结果将导出到 XML，管理员可以选择将此日志发送给一组用户。 |
| [运行预邮箱诉讼保留报告](/exchange/security-and-compliance/exchange-auditing-reports/per-mailbox-litigation-hold-report) | 提供有关邮箱上诉讼保留设置的任何更改的详细信息。 |
| [查看和导出外部管理员审核日志](/exchange/security-and-compliance/exchange-auditing-reports/view-external-admin-audit-log) | 包含外部管理员执行的操作的详细信息。 这些条目提供有关运行哪个 cmdlet、使用了哪些参数以及创建、修改或删除 Exchange Online 中的对象的任何操作的信息。 |

## <a name="device-compliance-reports"></a>设备合规性报告

使用 Microsoft 365 的基本移动性和安全性管理和保护连接到订阅的移动设备。 用于访问工作电子邮件、日历、联系人和文档的移动设备在确保员工能够随时随地工作方面起到非常显著的作用。 保护组织的信息至关重要。 使用 Microsoft 365 的基本移动性和安全性设置设备安全策略和访问规则。 如果丢失或被盗，还可使用 Microsoft 365 的基本移动性和安全性擦除移动设备。

基本移动性和安全性合规性报告概述了组织为保护访问 Microsoft 365 数据的移动设备而设置的策略。 该报告允许按合规性状态、报告的违反、阻止的设备以及安全策略擦除多少设备来筛选设备。 有关详细信息，请参阅 Microsoft [365 的基本移动性和安全性概述](https://support.microsoft.com/office/overview-of-basic-mobility-and-security-for-microsoft-365-faa7d8e5-645d-4d59-839c-c8d4c1869e4a)。

## <a name="data-loss-prevention"></a>数据丢失防护

DLP 策略有助于管理组织的安全性和信息流。 您可以设置策略以阻止访问内容、加密数据，或者使用应用程序内 DLP 策略提示通知用户策略和策略违反情况。 DLP 报告可深入了解策略和规则匹配、替代和误报的数量。

使用 Microsoft 365 管理中心查看有关 DLP 策略检测到的邮件数的信息。 DLP 报告提供有关已发送和已接收邮件的策略和规则匹配项的见解。 您还可以使用 Exchange 管理中心查看过去 24 小时内每个策略的匹配数、替代数和误报数。 如果下载 Excel 报告，可以查看更多详细信息，如谁发送了哪个邮件、哪天以及触发了哪些策略匹配。 有关详细信息，请参阅 [查看有关 DLP 策略检测的报告](/previous-versions/exchange-server/exchange-150/jj889415(v=exchg.150))。

## <a name="auditing-in-yammer-enterprise"></a>Yammer Enterprise 中的审核

Yammer Enterprise 使管理员能够通过 Yammer 数据导出 API 或手动通过 Yammer 网络管理页从 [Yammer](https://support.office.com/article/export-data-from-yammer-enterprise-b303d8f3-007d-4ad4-81f8-54fb1ecfb3f2)网络导出用户活动数据。 导出日志的能力仅限于 Yammer 中的网络管理员。  (所有 Microsoft 365 全局管理员都是 Yammer Network Administrators.) 

可导出以下数据：

| Filename | 说明 |
|----------------------------|-------------------------------------------------------------------------|
| Users.csv | 网络中所有新的、挂起和挂起的用户 |
| Messages.csv | 网络内的所有消息 |
| Files.csv (元数据)  | 诸如文件名、文件 API URL、上传者 ID、上传位置等的元数据。 |
| Files.csv (原始文件)  | 用户上传到 Yammer 的原始文件的 Zip 文件 |
| Topics.csv | 网络上创建的主题 |
| Pages.csv | 网页 (记录) 由网络用户创建 |
| Admins.csv | 网络上所有已验证的管理员 |
| Networks.csv | 所有 Yammer 外部网络 |

Yammer 企业版数据也可通过 Microsoft 365 活动报告获得。 此外，Yammer 正积极致力于通过 Microsoft 365 管理活动 API 公开其他日志记录，以及使用 Power BI 对数据进行原因的能力。 有关 [这些功能详细信息，](https://fasttrack.microsoft.com/roadmap?filters=yammer) 请参阅 Office 路线图。
