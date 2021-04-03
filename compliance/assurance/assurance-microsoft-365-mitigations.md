---
title: Microsoft 365 企业版业务连续性管理缓解
description: Microsoft 365 服务事件情景的一些缓解措施示例。
author: robmazz
ms.author: robmazz
manager: laurawi
ms.reviewer: sosstah
audience: ITPro
ms.topic: article
f1.keywords:
- NOCSH
ms.service: o365-solutions
localization_priority: Normal
ms.collection:
- M365-subscription-management
- Strat_O365_Enterprise
- MS-Compliance
titleSuffix: Microsoft Service Assurance
hideEdit: true
ms.openlocfilehash: 34f6bc7e597d4dfc279e55b9b8a1434e3ada45fb
ms.sourcegitcommit: 024137a15ab23d26cac5ec14c36f3577fd8a0cc4
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/01/2021
ms.locfileid: "51496975"
---
# <a name="service-incident-mitigation-strategies"></a>服务事件缓解策略

下面的一些策略和情景说明了如何缓解 Microsoft 365 服务事件对业务流程产生的影响。

## <a name="service-incident-scenarios-and-potential-mitigations"></a>服务事件情景和可能的缓解措施

|Microsoft 365 依赖项|可能的缓解措施|
|---------|---------|
|事件管理系统需要通过 Exchange Online 联系待命的工程师和事件管理员。|确保事件管理系统支持多通道通信（如并行电子邮件、电话联络和短信通知）以及呼叫树层次结构（以便在主要的待命工程师未响应的情况下，由系统自动启用备用人员）。 还应在每条通知中包括备用人员联系方法，从而嵌入备用通信方法以方便参考。 如果事件管理服务不可用，则可使用其他通信方法（如 Yammer）进行紧急协作。|
|使用 Microsoft Teams 来存储通过客户端访问的文件。|Teams 将上传到客户端的文件存储在 SharePoint Online 文档库中。 仍可通过 SharePoint Online 访问文件。 告知用户 SharePoint Online 中的文件位置。|
|常规通信和事件管理会审过程需要使用 Microsoft Teams 电话会议。|使用第三方提供商建立备用的会议解决方案。|
|VoIP 电话用作辅助通信方式。|实现支持 PSTN 通话的非 VoIP 电话，尤其对于事件期间的网络和服务运营中心。 将员工移动电话号码添加到公司目录，以便通过移动数据网络联系关键人员。|
|文件存储和用户高效工作需要使用 OneDrive for Business。 配置[文件随选](https://techcommunity.microsoft.com/t5/Microsoft-OneDrive-Blog/OneDrive-Files-On-Demand-For-The-Enterprise/ba-p/117234)来释放本地用户驱动器上的空间。|OneDrive 同步功能提供了组策略，允许管理员要求在本地同步特定内容或在需要时释放空间。 若要缓解无法访问文档的风险，请配置此策略以便在本地同步重要文档。 告知用户对重要文档手动应用“始终在此设备上保留”设置。|
|使用 Exchange Online 与客户和供应商沟通业务中断情况。|公用的第三方社交网络可用作大量通信的替代方法。
|混合本地体系结构（如 ADFS 或直通身份验证）将失败，从而导致用户无法再对云服务进行身份验证。|将[密码哈希同步](/azure/active-directory/authentication/concept-resilient-controls#deploy-password-hash-sync-even-if-you-are-federated-or-use-pass-through-authentication)与混合身份验证服务一起配置为基于云的辅助身份验证服务，以避免在故障过程中出现登录中断。 有关构建弹性身份验证和访问控制体系结构的详细信息，请参阅[使用 Azure Active Directory 创建弹性访问控制管理策略](/azure/active-directory/authentication/concept-resilient-controls)。|  

## <a name="leveraging-mobile-app-access"></a>利用移动应用访问方法

随着移动应用的剧增，出现了全新的沟通方式，而 Microsoft 365 移动应用程序可作为复原策略的关键一环。 因为这些应用程序通过移动数据提供商网络连接到云服务，所以它们不依赖于组织内部的网络基础结构。

我们以 Outlook 为例。 根据所使用的电子邮件应用，用户可以通过不同的网络协议（https 或 MAPI）连接到其 Exchange Online 邮箱。 如果有一个服务事件涉及到其中一种协议，比如桌面客户端使用的 MAPI，那么你的用户仍可通过 Outlook Mobile 应用或 Outlook 网页版访问其邮箱。
  
如果你决定允许用户通过其移动设备连接到 Microsoft 365 服务，则可以使用 Microsoft Intune 安全地配置和管理这些设备。 在移动管理解决方案中注册用户帐户和设备后，请确保已下载并配置应用。
