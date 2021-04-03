---
title: 标识和访问管理概述
description: 了解 Microsoft 365 中的标识和访问管理
ms.author: robmazz
author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: Admin
ms.topic: article
f1.keywords:
- NOCSH
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- MS-Compliance
search.appverid:
- MET150
- MOE150
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: d431a7f04b156b003f5f4e213aef9bb9792874fe
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "51497160"
---
# <a name="identity-and-access-management-overview"></a>标识和访问管理概述

## <a name="how-does-microsoft-365-protect-production-systems-from-unauthorized-or-malicious-access"></a>Microsoft 365 如何保护生产系统免受未经授权的或恶意访问？

Microsoft 365 旨在允许 Microsoft 工程师在不访问客户内容的情况下操作服务。 默认情况下，Microsoft 365 工程师具有零长期访问 (ZSA) 访问客户内容，并且没有对生产环境的特权访问。 Microsoft 365 使用实时 (JIT) 、Just-Enough-Access (JEA) 模型，在支持 Microsoft 365 时需要提供对生产环境的临时特权访问。 JIT 访问模型将传统的持久管理访问替换为工程师根据需要请求临时提升为特权角色的过程。

工程师被分配到服务团队以支持生产服务通过标识管理工具请求服务团队帐户的资格 (IDM) 。 资格申请触发了一系列人员检查，以确保工程师已通过所有云筛选要求、完成必要的培训，并获得了帐户创建前的适当管理批准。 只有在满足所有资格要求后，才能为请求的环境创建服务团队帐户。

服务团队帐户不会授予任何长期管理员权限或客户内容的访问权限。 当工程师需要其他访问权限来支持其 Microsoft 365 服务时，他们使用名为"密码箱"的访问管理工具请求临时提升的资源访问权限。 密码箱将提升的访问权限限制为完成分配的任务所需的最小特权、资源和时间。 如果授权审阅者批准 JIT 访问请求，则只会向工程师授予一个临时帐户，该帐户仅具有完成其分配的工作所需的权限。 此临时帐户需要多重身份验证，在批准期限到期后自动删除。

## <a name="how-does-microsoft-365-handle-remote-access-to-production-systems"></a>Microsoft 365 如何处理对生产系统的远程访问？

Microsoft 365 系统组件位于地理位置上与运营团队分开的数据中心。 数据中心人员对 Microsoft 365 系统没有逻辑访问权限。 因此，Microsoft 365 服务团队人员通过远程访问管理环境。 需要远程访问以支持 Microsoft 365 的服务团队人员只有在获得授权经理批准后，才被授予远程访问。 所有远程访问都使用 FIPS 140-2 兼容 TLS 进行安全远程连接。

Microsoft 365 使用安全管理工作站 (SAW) 服务团队远程访问，以帮助保护 Microsoft 365 环境免遭入侵。 这些工作站专门用于防止有意或无意丢失生产数据，包括锁定 USB 端口，以及将 SAW 上可用的软件限制到支持环境所需的操作。 SAW 受到密切跟踪和监视，以检测和防止 Microsoft 工程师恶意或无意泄露客户数据。

## <a name="how-does-customer-lockbox-add-additional-protection-for-customer-content"></a>客户密码箱如何为客户内容添加其他保护？

客户可以通过启用客户密码箱来向其内容添加其他级别的访问控制。 当密码箱提升请求涉及访问客户内容时，客户密码箱需要客户批准，这是审批工作流的最后一步。 这使组织可以选择批准或拒绝这些请求，并为客户提供直接访问控制。 如果客户拒绝客户密码箱请求，则对所请求内容的访问将被拒绝。 如果客户在特定时间内不拒绝或批准请求，那么请求将自动过期，Microsoft 不会获得客户内容的访问权限。 如果客户批准请求，Microsoft 对客户内容的临时访问将在分配完成疑难解答操作的时间到期后自动记录、审核和撤消。

## <a name="related-external-regulations--certifications"></a>认证的相关&法规

Microsoft 的在线服务会定期进行审核，以遵守外部法规和认证。 有关与标识和访问控制相关的控件的验证，请参阅下表。

| **外部审核** | **Section** | **最新报告日期** |
|:--------------------|:------------|:-----------------------|
| [FedRAMP (Office 365) ](https://compliance.microsoft.com/compliancemanager) | AC-2：帐户管理 <br> AC-3：实施访问 <br> AC-5：职责分离 <br> AC-6：最小特权 <br> AC-17：远程访问 | 2020 年 9 月 24 日 |
| [OFFICE 365 (ISO 27001/27002) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=1e84a14a-2468-45ac-9412-5e53250d57ec&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.1：访问控制的业务要求 <br> A.9.2：用户访问管理 <br> A.9.3：用户责任 <br> A.9.4：系统和应用程序访问控制 <br> A.15.1：供应商关系中的信息安全 | 2020 年 2 月 22 日 |
| [OFFICE 365 (ISO 27017) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=d7864d4f-e053-4cc4-a964-fa526d07c3be&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) <br><br> [适用性声明](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuide?command=Download&downloadType=Document&downloadId=8ee1e46b-2ada-4e7b-bb7d-4c55a8cb6fcd&docTab=4ce99610-c9c0-11e7-8c2c-f908a777fa4d_ISO_Reports) <br> [认证](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=70de0999-5451-43a3-9ef4-761e8fbfb1a3&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_ISO_Reports) | A.9.2：用户访问管理 <br> A.9.4：系统和应用程序访问控制 <br> A.15.1：供应商关系中的信息安全 | 2020 年 2 月 22 日 |
| [SOC 1 (Office 365)](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=90df3f9c-3aaf-4dbf-99d0-ca9f2991721b&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-33：帐户修改 <br> CA-34：用户身份验证 <br> CA-35：特权访问 <br> CA-36：远程访问 <br> CA-57：客户密码箱 Microsoft 管理审批 <br> CA-58：客户密码箱服务请求 <br> CA-59：客户密码箱通知 <br> CA-61：JIT 审阅和审批 | 2020 年 12 月 24 日 |
| [SOC 2 (Office 365) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=a73c1738-7892-42b7-acd3-87b6371c53f6&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CA-32：共享帐户策略 <br> CA-33：帐户修改 <br> CA-34：用户身份验证 <br> CA-35：特权访问 <br> CA-36：远程访问 <br> CA-53：第三方监控 <br> CA-56：客户密码箱客户批准 <br> CA-57：客户密码箱 Microsoft 管理审批 <br> CA-58：客户密码箱服务请求 <br> CA-59：客户密码箱通知 <br> CA-61：JIT 审阅和审批 | 2020 年 12 月 24 日 |
| [OFFICE 365 (SOC 3) ](https://servicetrust.microsoft.com/ViewPage/MSComplianceGuideV3?command=Download&downloadType=Document&downloadId=274054e5-4968-48d2-bf94-9a8eda5d7a93&tab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb&docTab=7027ead0-3d6b-11e9-b9e1-290b1eb4cdeb_SOC_%2F_SSAE_16_Reports) | CUEC-15：客户密码箱请求 | 2020 年 12 月 24 日 |