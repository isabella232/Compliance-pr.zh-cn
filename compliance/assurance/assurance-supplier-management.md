---
title: 供应商管理概述
description: 了解 Microsoft 365 中的供应商管理
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH'
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
ms.openlocfilehash: 4da4775332989c4a40738777dfae7318e27086f0
ms.sourcegitcommit: 7a5b6bc58fc4613b38f3fda20aebee5cec6a5730
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/08/2021
ms.locfileid: "49787371"
---
# <a name="supplier-management-overview"></a>供应商管理概述

## <a name="how-does-microsoft-manage-risk-related-to-suppliers"></a>Microsoft 如何管理与供应商相关的风险？

Microsoft 与第三方公司合作，帮助满足客户的需求。 这些第三方公司称为供应商或下级处理者。 Microsoft 的供应商安全和隐私由我们的供应商安全和隐私保障 [ (SSPA) ](https://www.microsoft.com/procurement/sspa?activetab=pivot1%3aprimaryr6)计划管理，该计划是一套企业范围的要求，适用于与 Microsoft 合作以提供联机服务的所有供应商。 虽然 SSPA 计划提供对供应商基础的全面治理和管理，但各个业务部门（如 Microsoft 365）可能会维护其供应商的其他要求。

## <a name="how-does-microsofts-supplier-security-and-privacy-assurance-sspa-program-protect-customer-data"></a>Microsoft 供应商安全和隐私保障服务 (SSPA) 保护客户数据？

SSPA 是 Microsoft 采购、公司外部和法律事务与公司安全之间的合作关系，以确保供应商遵守 Microsoft 的隐私和安全原则。 SSPA 的范围涵盖处理个人数据或 Microsoft 机密数据的所有供应商。 SSPA 计划注册包括遵守 Microsoft 的数据保护要求 (或) 。 在开始与 Microsoft 签订合同之前，SUPPLIER 包括供应商必须实施的安全和隐私控制。 所有注册的供应商都自证明每年遵守了一次，即符合该计划。

根据 6 个不同的数据处理类别确定 2013 年 4 月 1 日要求的范围，可在 SSPA 中批准供应商作为其注册的一部分。 这些类别用于标识与供应商向 Microsoft 提供的服务相关联的风险。 供应商的数据处理配置文件确定哪些函数在范围内被视为在范围内，以提供适当的数据保护。 处理被视为高风险的数据的供应商必须遵守所有 2016 年 4 月 1 日要求，并且可能还需要提供独立的合规性验证。 Microsoft 购买工具在允许供应商进行采购之前验证所有供应商的 SSPA 状态，包括符合适用于该 SUPPLIER 的部分。

## <a name="what-types-of-subprocessors-provide-services-for-microsoft"></a>哪些类型的子处理器为 Microsoft 提供服务？

"子处理者"是 Microsoft 参与的第三方，其职责包括处理 Microsoft 作为处理者所负责的 Microsoft 个人数据。 Microsoft 的子处理者分为三个不同的类别。 每个用户都必须证明符合 SSPA，然后才能代表 Microsoft 处理客户数据。

- **技术** 子处理者提供用于提供特定 Microsoft 联机服务的技术。 如果客户部署这些服务之一，为该服务标识的子处理者可以处理、存储或以其他方式访问客户数据或个人数据，同时帮助提供该服务。
- **辅助** 子处理者提供支持、操作和维护联机服务的服务。 如果客户部署其中一项服务，则标识的子处理者可能在提供辅助服务的同时处理、存储或以其他方式访问有限的客户数据或个人数据。
- **员工扩充** 子处理者有两种不同的形式：在这两种方案中，个人数据仅驻留在 Microsoft 设施、Microsoft 系统上，并受 Microsoft 策略和监管。

    - 第一种员工扩充形式提供支持、运营和维护 Microsoft 联机服务的员工。 在履行他们的责任时，这些子处理者可能会向客户数据或个人数据公开。 例如，子处理器可能在 Microsoft 服务器上执行远程疑难解答，而这样做可能会向服务器故障转储日志中的客户数据的代码段公开。
    - 第二种员工扩充形式涉及与 Microsoft 全职员工一起合作以支持、运营和维护 Microsoft 联机服务的下级处理者。 在 Microsoft 全职员工的工作中，这些子处理者可能会向化名数据公开。

技术和辅助子处理者需要实现访问控制，以遵守 Microsoft 的数据保护要求 (或) 。 这些要求符合或超过 Microsoft 在 OST (联机服务条款中向) 。 执行员工扩充工作的供应商受针对 Microsoft 全职员工的相同访问控制。

## <a name="how-does-microsoft-onboard-suppliers"></a>Microsoft 如何载入供应商？

作为载入过程的一部分，需要第三方供应商签署 Microsoft 主协议。 本协议管理 Microsoft 及其供应商之间的关系，并确保对供应商关系的一致管理。 作为载入的一部分，供应商在 SSPA 中注册，并且必须先完成所有适用要求，然后才能批准任何数据处理类别。 只有当服务活动的数据处理活动与供应商批准的数据处理类别相匹配时，Microsoft 业务部门才能创建与供应商的服务活动。

## <a name="how-does-microsoft-notify-customers-of-changes-to-suppliers-who-process-their-data"></a>Microsoft 如何通知客户对处理其数据的供应商所做的更改？

根据 Microsoft Online Service 数据保护附录 (DPA) ，Microsoft 对添加任何子处理者的通知期做出其他承诺。 请注意，时间范围取决于子处理器将代表 Microsoft 处理的数据类型。 如 DPA 中说明，Microsoft 承诺在将处理客户数据的任何新子处理者之前至少提前六个月通知客户。 对于任何其他个人数据，Microsoft 将至少提供 30 天的通知。 通知由更新的子处理器 [Microsoft Online Services提供](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=926b2cf5-6b6e-43ca-9bc3-f73e961aad5f&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_Subprocessor_List)。

## <a name="related-external-regulations--certifications"></a>认证的相关&法规

Microsoft 的在线服务会定期进行审核，以遵守外部法规和认证。 请参阅下表，以验证与供应商管理相关的控制措施。

| **外部审核** | **Section** | **最新报告日期** |
|:--------------------|:------------|:-----------------------|  
| [Office 365 (FedRAMP) ](https://compliance.microsoft.com/compliancemanager) | CA-3：系统互连 <br> IA-4：标识符管理 <br> PS-6：访问协议 <br> PS-7：第三方人员安全 <br> SA-4：购置过程 <br> SA-9：外部信息系统服务 <br> SA-12：供应链保护 | 2020 年 9 月 24 日 |
| [ISO 27001/27002 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.15.1：供应商关系中的信息安全性 | 2020 年 2 月 22 日 |
| [Office 365 (ISO 27017) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.15.1：供应商关系中的信息安全性 | 2020 年 2 月 22 日 |
| [OFFICE 365 (ISO 27018) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) |  A.8.1：泄露已泄漏的 PII 处理 | 2020 年 12 月 24 日 |
| [SOC 2 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-53：第三方监控 | 2020 年 12 月 24 日 |

## <a name="resources"></a>资源

- [供应商安全隐私和保障计划](https://www.microsoft.com/procurement/sspa?activetab=pivot1%3aprimaryr6)
