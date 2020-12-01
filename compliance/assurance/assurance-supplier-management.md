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
ms.openlocfilehash: e46a7d2121a3ed1f314a3126c51911248362ff59
ms.sourcegitcommit: 626b0076d133e588cd28598c149a7f272fc18bae
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/30/2020
ms.locfileid: "49506477"
---
# <a name="supplier-management-overview"></a>供应商管理概述

## <a name="how-does-microsoft-manage-risk-related-to-suppliers"></a>Microsoft 如何管理与供应商相关的风险？

Microsoft 合作伙伴与第三方公司合作，以帮助满足客户的需求。 这些第三方公司称为 "供应商" 或 "subprocessors"。 Microsoft 的供应商安全性和隐私由我们的 [供应商安全和隐私保证 (SSPA) 计划](https://www.microsoft.com/procurement/sspa?activetab=pivot1%3aprimaryr6)，针对与 Microsoft 合作的所有供应商提供的一组企业范围的要求，以提供我们的在线服务。 如果 SSPA 计划提供了我们的提供商基础的全面公司治理和管理，则各个业务单位（如 Microsoft 365）可能会保留对其供应商的其他要求。

## <a name="how-does-microsofts-supplier-security-and-privacy-assurance-sspa-program-protect-customer-data"></a>Microsoft 的供应商安全和隐私保证 (SSPA) 计划如何保护客户数据？

SSPA 是 Microsoft 采购、公司外部和法律事务以及公司安全性之间的合作关系，以确保供应商遵守 Microsoft 的隐私和安全原则。 SSPA 的范围涵盖处理个人数据或 Microsoft 机密数据的所有供应商。 SSPA 计划注册包括遵守 Microsoft 的数据保护要求 (DPR) 。 DPR 包含供应商在开始与 Microsoft 进行合同合作前必须实施的安全和隐私控制。 所有已注册的供应商自证明符合 DPR 年的要求。

DPR 要求的作用范围基于六个不同的数据处理类别供应商可在 SSPA 的注册过程中批准。 这些类别用于确定与供应商向 Microsoft 提供的服务相关联的风险。 供应商的数据处理配置文件确定哪些 DPR 控件被认为是范围内的，以提供适当的数据保护。 处理被认为是较高风险的数据的供应商必须符合所有 DPR 要求，并且可能还需要提供独立的合规性验证。 Microsoft 购买工具可验证所有供应商的 SSPA 状态，包括在允许采购该供应商之前与 DPR 的适用部分兼容。

## <a name="what-types-of-subprocessors-provide-services-for-microsoft"></a>哪些类型的 subprocessors 为 Microsoft 提供服务？

"Subprocessor" 是 Microsoft 参与的第三方，其职责包括处理 microsoft 为其处理器的 Microsoft 个人数据。 Microsoft 的 subprocessors 分为三个不同的类别。 每个用户必须先证明是否符合 SSPA，然后才能在代表 Microsoft 的客户数据上进行处理。

- **技术** subprocessors 提供用于提供特定 Microsoft online 服务的技术。 如果客户部署了其中的某项服务，则为该服务标识的 subprocessors 可能会处理、存储或以其他方式访问客户数据或个人数据，同时帮助提供该服务。
- **辅助** subprocessors 提供支持、操作和维护联机服务的服务。 如果客户部署了其中的某项服务，则标识的 subprocessors 可能会处理、存储或以其他方式访问有限的客户数据或个人数据，同时提供其辅助服务。
- **员工充实** subprocessors 采用两种不同的形式：在这两种情况下，个人数据仅驻留在 microsoft 设备中的 microsoft 系统上，并受 microsoft 策略和监督的制约。

    - 第一种形式的人员充实提供支持、操作和维护 Microsoft online services 的人员。 在履行其职责的同时，这些 subprocessors 可能会暴露给客户数据或个人数据。 例如，subprocessor 可能在 Microsoft 服务器上执行远程故障排除，而这样做可能会在服务器故障转储日志中向客户数据的代码段公开。
    - 第二种形式的员工充实涉及 subprocessors 谁与 Microsoft 全职员工一起工作，以支持、操作和维护 Microsoft online 服务。 在 Microsoft 全职员工的工作中，这些 subprocessors 可能会暴露给假名数据。

需要技术和辅助 subprocessors 来实施访问控制，以符合 Microsoft 的数据保护要求 (DPR) 。 这些要求达到或超过 Microsoft 在 (OST) 的联机服务条款中对其客户做出的合约承诺。 执行员工充实工作的供应商将受到 Microsoft 全职员工的相同访问控制。

## <a name="how-does-microsoft-onboard-suppliers"></a>Microsoft 板载供应商有何功能？

第三方供应商需要在加入过程中签署 Microsoft 主协议。 本协议控制 Microsoft 与其供应商之间的关系，并确保一致地管理供应商关系。 作为加入过程的一部分，供应商注册了 SSPA，并且必须先完成所有适用的要求，然后才能批准对任何数据处理类别。 如果预订的数据处理活动与供应商已获批准的数据处理类别相匹配，则 Microsoft 业务部门只能创建与供应商的预订。

## <a name="how-does-microsoft-notify-customers-of-changes-to-suppliers-who-process-their-data"></a>Microsoft 如何通知客户对处理其数据的供应商所做的更改？

根据 Microsoft 在线服务数据保护附录 (DPA) ，Microsoft 会对添加任何 subprocessor 的通知期做出额外的承诺。 注意时间帧取决于 subprocessor 将代表 Microsoft 处理的数据类型。 如 DPA 中所述，Microsoft 承诺向客户提供至少6个月的时间来处理客户数据的新 subprocessor。 对于任何其他个人数据，Microsoft 将至少提供30天的通知。 通知由 [Microsoft Online Services Subprocessor 列表](https://servicetrust.microsoft.com/ViewPage/TrustDocumentsV3?command=Download&downloadType=Document&downloadId=926b2cf5-6b6e-43ca-9bc3-f73e961aad5f&tab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913&docTab=7f51cb60-3d6c-11e9-b2af-7bb9f5d2d913_Subprocessor_List)的更新提供。

## <a name="related-external-regulations--certifications"></a>& 认证的相关外部法规

将定期审核 Microsoft 的在线服务，以遵守外部法规和认证。 请参阅下表，以验证与供应商管理相关的控制措施。

| **外部审核** | **Section** | **最新报告日期** |
|:--------------------|:------------|:-----------------------|  
| [FedRAMP (Office 365) ](https://compliance.microsoft.com/compliancemanager) | CA-3：系统互连 <br> IA-4：标识符管理 <br> PS-6：访问协议 <br> PS-7：第三方个人安全性 <br> SA-4：收购过程 <br> SA-9：外部信息系统服务 <br> SA-12：提供链保护 | 2020年9月24日 |
| [ISO 27001/27002 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 15.1：信息在供应商关系中的安全性 | 2020 年 2 月 22 日 |
| [ISO 27017 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | 15.1：信息在供应商关系中的安全性 | 2020 年 2 月 22 日 |
| [ISO 27018 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=43e89534-f48d-42ea-a7a7-3523ff516036&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) |  8.1：已转包 PII 处理的泄漏 | 2019 年 9 月 30 日 |
| [SOC 2 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=fa062990-e758-4ddc-ace3-7fb21a301d09&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Rep-11e9-b9e1-290b1eb4cdeb_SOC_/_SSAE_16_Reports) | CA-53：第三方监视 | 2019 年 9 月 30 日 |

## <a name="resources"></a>资源

- [供应商安全隐私和保证计划](https://www.microsoft.com/procurement/sspa?activetab=pivot1%3aprimaryr6)
