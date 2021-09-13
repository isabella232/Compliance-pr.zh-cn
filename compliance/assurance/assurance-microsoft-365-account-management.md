---
title: 帐户管理中的Microsoft 365
description: 了解 Microsoft 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
ms.localizationpriority: medium
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: d525edfb9854df156f5b7b8571199b7a0102a0bf
ms.sourcegitcommit: 997dd3f66f65686c2e38b7e30e67add426dce5f3
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/12/2021
ms.locfileid: "59158248"
---
# <a name="account-management-in-microsoft-365"></a>帐户管理中的Microsoft 365

Microsoft 在自动执行大多数 Microsoft 365 运营的系统和控制方面投入大量资金，同时有意限制服务人员直接访问服务器和客户数据的要求。 人员管理服务，软件运营服务。 利用此结构，Microsoft Microsoft 365大规模管理威胁，并最大限度地降低内部和外部威胁的风险。 Microsoft 采用访问控制，假定每个人都是访问Microsoft 365客户数据的潜在威胁。 因此，"零长期访问 (ZSA) 原则为 Microsoft 365 使用的整个访问控制结构Microsoft 365。

默认情况下，Microsoft 人员对组织的任何Microsoft 365或客户数据具有零长期特权访问权限。 只有通过可靠的检查和审批系统，服务团队人员才能通过较窄的操作和时间范围获得特权访问。 通过此系统，Microsoft 可以显著减少服务Microsoft 365和攻击者获取未经授权的访问或对客户造成恶意或意外Microsoft 服务损害的可能性。

## <a name="account-types"></a>帐户类型

Microsoft 365三类帐户满足所有组织任务和业务功能：服务团队帐户、服务帐户和客户帐户。 管理这些帐户是 Microsoft 与客户共同的责任。 Microsoft 管理服务团队和服务帐户，它们用于运营和支持 Microsoft 产品和服务。 客户帐户由客户管理，并允许他们定制帐户访问权限以满足其内部访问控制要求。

![帐户的共同责任](../media/assurance-shared-responsibility-for-accounts.png)

## <a name="microsoft-managed-accounts"></a>Microsoft 托管的帐户

**服务团队帐户** 由Microsoft 365和维护服务的服务团队Microsoft 365使用。 这些帐户对服务没有长期特权Microsoft 365，而是可用于请求临时和受限的特权访问来执行指定的作业功能。 并非每个服务团队帐户都可以执行相同的操作，使用基于角色的访问控制和 RBAC (强制实施) 。 角色确保服务团队成员及其帐户仅具有执行特定工作职责所需的最低访问权限。 此外，服务团队帐户不能属于多个角色，他们可在其中充当其自己的操作审批者。

**服务帐户** 由服务Microsoft 365在通过自动化进程与其他服务通信时进行身份验证。 正如仅向服务团队帐户授予执行特定人员的工作职责所需的最低访问权限一样，服务帐户仅被授予预期目的所需的最低访问权限。 此外，还有多种旨在满足特定需求的服务帐户类型。 一Microsoft 365服务可能有多个服务帐户，每个帐户具有不同的角色要执行。

## <a name="customer-managed-accounts"></a>客户管理的帐户

**客户** 帐户用于访问Microsoft 365服务，并且是唯一由每个客户负责的帐户。 客户有责任在组织中创建和管理帐户，以维护安全的环境。 客户帐户的管理是通过 AAD Azure Active Directory (或) 本地 Active Directory (AD) 。 每个客户都有一组唯一的访问控制要求，客户帐户授予每个客户满足其个人需求的能力。 客户帐户无法访问其客户组织外部的任何数据。

## <a name="service-team-account-management"></a>服务团队帐户管理

Microsoft 365使用名为 Identity Management (IDM) 的帐户管理系统，管理服务团队帐户的整个生命周期。 IDM 结合使用自动验证流程和审批审批，强制执行与服务团队帐户访问相关的安全要求。

服务团队成员不会自动获取服务团队帐户，他们必须先满足资格要求并获取授权经理的批准。 若要有资格使用服务团队帐户，服务团队人员必须先通过聘用前人员筛选、[](assurance-pre-employment-screening.md)云背景检查，并完成所有[](assurance-cloud-background-check.md)标准和所需的基于角色的培训。 满足所有资格要求后，就可以提出服务团队帐户请求，并且必须由授权经理批准。

![人员筛选过程](../media/assurance-personnel-screening-process.png)

IDM 还负责跟踪维护服务团队帐户所需的定期重新检查和培训。 Microsoft 云背景检查必须每两年完成一次，并且每年必须审阅所有培训材料。 如果到期日期不满足上述任一要求，则撤消其资格，并自动禁用服务团队帐户。

此外，服务团队帐户资格通过人员转移和终止 [自动更新](assurance-employee-transfer-termination.md)。 在人力资源信息系统和 HRIS (更改) IDM 采取措施，具体取决于情况。 转移到另一个服务团队的人员将设置其资格的到期日期，并且维护资格的请求必须由服务团队成员提交并经其新经理批准。 已终止的人员将自动撤消所有资格，其服务团队帐户将在最后一天被禁用。 对于内部终止，可以提出帐户吊销的紧急请求。

默认情况下，服务团队帐户对用于常规疑难解答的广泛系统元数据具有有限的读取访问权限。 此外，基线服务团队帐户无法请求访问Microsoft 365或客户的特权访问权限。 必须对要添加到角色的服务团队帐户提出另一个请求，该角色允许服务团队成员请求提升的权限以执行特定任务和操作。
