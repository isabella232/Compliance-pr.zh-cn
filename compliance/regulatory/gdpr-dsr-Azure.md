---
title: 针对 GDPR 和 CCPA 的 Azure 数据主体请求
description: 了解如何使用 Azure 产品、服务和管理工具来查找和处理个人数据以响应 DSR。
keywords: Microsoft 365, Microsoft 365 教育版, Microsoft 365 文档, GDPR, CCPA
localization_priority: Priority
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
ms.openlocfilehash: 48c8df230e3497c6176898226bb5b76de5d3b1e0
ms.sourcegitcommit: 5d8e670e9d9968458047b51b6b2930f7bd14a011
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/25/2021
ms.locfileid: "53141533"
---
# <a name="azure-data-subject-requests-for-the-gdpr-and-ccpa"></a><span data-ttu-id="fb6a4-104">针对 GDPR 和 CCPA 的 Azure 数据主体请求</span><span class="sxs-lookup"><span data-stu-id="fb6a4-104">Azure Data Subject Requests for the GDPR and CCPA</span></span>

## <a name="introduction-to-data-subject-requests-dsrs"></a><span data-ttu-id="fb6a4-105">数据主体请求 (DSR) 简介</span><span class="sxs-lookup"><span data-stu-id="fb6a4-105">Introduction to Data Subject Requests (DSRs)</span></span>

<span data-ttu-id="fb6a4-p101">根据欧盟 [一般数据保护条例 (GDPR)](https://ec.europa.eu/justice/data-protection/reform/index_en.htm)，用户（在条例中称为“*数据主体*”）有权管理由雇主或其他类型机构或组织（称为“*数据控制者*”或简称为“*控制者*”）收集的个人数据。根据 GDPR，个人数据的定义非常广泛，包括与身份已识别或可识别的自然人相关的任何数据。根据 GDPR，数据主体有权对自己的个人数据执行以下操作：获取个人数据副本、请求更正个人数据、限制个人数据处理、删除个人数据或接收电子格式的个人数据（以便于转移给其他控制者）。数据主体为了对自己的个人数据执行操作而向控制者发出的正式请求，称为“*数据主体请求*”或“DSR”。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p101">The European Union [General Data Protection Regulation (GDPR)](https://ec.europa.eu/justice/data-protection/reform/index_en.htm) gives rights to people (known in the regulation as *data subjects*) to manage the personal data that has been collected by an employer or other type of agency or organization (known as the *data controller* or just *controller*). Personal data is defined very broadly under the GDPR as any data that relates to an identified or identifiable natural person. The GDPR gives data subjects specific rights to their personal data; these rights include obtaining copies of personal data, requesting corrections to it, restricting the processing of it, deleting it, or receiving it in an electronic format so it can be moved to another controller. A formal request by a data subject to a controller to take an action on their personal data is called a *Data Subject Request* or DSR.</span></span>

<span data-ttu-id="fb6a4-110">同样，加州消费者隐私法案 (CCPA) 规定了加州消费者的隐私权和义务，包括与 GDPR 的数据主体权利类似的权利，例如删除、访问和接收（可移植性）其个人信息的权利。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-110">Similarly, the California Consumer Privacy Act (CCPA), provides privacy rights and obligations to California consumers, including rights similar to GDPR's Data Subject Rights, such as the right to delete, access and receive (portability) their personal information.</span></span> <span data-ttu-id="fb6a4-111">CCPA 还就某些披露规定了在选择行使权限时防止歧视的保障措施，并就分类为“销售”的特定数据传输提出了“选择退出/选择加入”要求。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-111">The CCPA also provides for certain disclosures, protections against discrimination when electing exercise rights, and "opt-out/ opt-in" requirements for certain data transfers classified as "sales".</span></span> <span data-ttu-id="fb6a4-112">“出售”广义定义为包含共享数据来换取有值对价的行为。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-112">Sales are broadly defined to include the sharing of data for a valuable consideration.</span></span> <span data-ttu-id="fb6a4-113">有关 CCPA 的详细信息，请参阅[加州消费者隐私法案](offering-ccpa.md)和[加州消费者隐私法案常见问题解答](ccpa-faq.yml)。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-113">For more information about the CCPA, see the [California Consumer Privacy Act](offering-ccpa.md) and the [California Consumer Privacy Act FAQ](ccpa-faq.yml).</span></span>

<span data-ttu-id="fb6a4-p103">本指南讨论了如何使用 Microsoft 产品、服务和管理工具帮助我们的控制者客户查找和操作个人数据以响应 DSR。具体而言，这包括如何查找、访问和操作驻留在 Microsoft 云中的个人数据。下面是本指南中所列流程的快速概述：</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p103">The guide discusses how to use Microsoft products, services and administrative tools to help our controller customers find and act on personal data to respond to DSRs. Specifically, this includes how to find, access, and act on personal data that reside in the Microsoft cloud. Here's a quick overview of the processes outlined in this guide:</span></span>

- <span data-ttu-id="fb6a4-p104">**发现：** 使用搜索和发现工具更轻松地查找可能是 DSR 主体的客户数据。一旦收集了潜在响应文档，则可以执行一个或多个下列步骤中所述的 DSR 操作。或者，你可能会确定请求不符合组织有关响应 DSR 的指导原则。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p104">**Discover:** Use search and discovery tools to more easily find customer data that may be the subject of a DSR. Once potentially responsive documents are collected, you can perform one or more of the DSR actions described in the following steps to respond to the request. Alternatively, you may determine that the request doesn't meet your organization's guidelines for responding to DSRs.</span></span>
- <span data-ttu-id="fb6a4-120">**访问：** 检索驻留在 Microsoft 云中的个人数据，如果提出请求，还制作可供数据主体使用的个人数据副本。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-120">**Access:** Retrieve personal data that resides in the Microsoft cloud and, if requested, make a copy of it that can be available to the data subject.</span></span>
- <span data-ttu-id="fb6a4-121">**纠正：** 进行更改或者对个人数据实施其他请求的操作（如果适用）。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-121">**Rectify:** Make changes or implement other requested actions on the personal data, where applicable.</span></span>
- <span data-ttu-id="fb6a4-p105">**限制：** 通过移除各种 Azure 服务的许可证或者在可能的情况下关闭所需服务，限制个人数据的处理。你也可以从 Microsoft 云中移除数据并仍将其保留在內部或其他位置。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p105">**Restrict:** Restrict the processing of personal data, either by removing licenses for various Azure services or turning off the desired services where possible. You can also remove data from the Microsoft cloud and retain it on-premises or at another location.</span></span>
- <span data-ttu-id="fb6a4-124">**删除：** 永久删除保存在 Microsoft 云中的个人数据。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-124">**Delete:** Permanently remove personal data that resided in the Microsoft cloud.</span></span>
- <span data-ttu-id="fb6a4-125">**导出/接收（可移植性）：** 向数据主体提供个人数据或个人信息的电子副本（采用机器可读格式）。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-125">**Export/Receive (Portability):** Provide an electronic copy (in a machine-readable format) of personal data or personal information to the data subject.</span></span> <span data-ttu-id="fb6a4-126">根据 CCPA 的定义，个人信息是指与已识别或可识别人员相关的任何信息。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-126">Personal information under the CCPA is any information relating to an identified or identifiable person.</span></span> <span data-ttu-id="fb6a4-127">个人的私人、公共或工作角色之间没有任何区别。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-127">There is no distinction between a person's private, public, or work roles.</span></span> <span data-ttu-id="fb6a4-128">所定义的“个人信息”术语与 GDPR 下的“个人信息”大致相同。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-128">The defined term "personal information" roughly lines up with "personal data" under GDPR.</span></span> <span data-ttu-id="fb6a4-129">但是，CCPA 还包括家人和家庭数据。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-129">However, the CCPA also includes family and household data.</span></span> <span data-ttu-id="fb6a4-130">有关 CCPA 的详细信息，请参阅[加州消费者隐私法案](offering-ccpa.md)和[加州消费者隐私法案常见问题解答](ccpa-faq.yml)。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-130">For more information about the CCPA, see the [California Consumer Privacy Act](offering-ccpa.md) and the [California Consumer Privacy Act FAQ](ccpa-faq.yml).</span></span>

<span data-ttu-id="fb6a4-131">本指南中的每个部分概述了数据控制者组织为响应对 Microsoft 云中个人数据的 DSR 而采取的技术过程。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-131">Each section in this guide outlines the technical procedures that a data controller organization can take to respond to a DSR for personal data in the Microsoft cloud.</span></span>

## <a name="terminology"></a><span data-ttu-id="fb6a4-132">术语</span><span class="sxs-lookup"><span data-stu-id="fb6a4-132">Terminology</span></span>

<span data-ttu-id="fb6a4-133">下面提供了与本指南相关的术语定义。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-133">The following provides definitions of terms that are relevant to this guide.</span></span>

- <span data-ttu-id="fb6a4-134">**控制者：** 单独或与其他人一起确定个人数据处理的用途和途径的自然人或法人、公共机构、机关或其他实体；如果欧盟或成员国法律确定了此类处理的用途和途径，欧盟或成员国法律可能会规定控制者或具体提名条件。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-134">**Controller:** The natural or legal person, public authority, agency or other body which, alone or jointly with others, determines the purposes and means of the processing of personal data; where the purposes and means of such processing are determined by Union or Member State law, the controller, or the specific criteria for its nomination may be provided for by Union or Member State law.</span></span>
- <span data-ttu-id="fb6a4-135">**个人数据和数据主体：** 身份已识别或可识别的自然人（“数据主体”）的任何相关信息；身份可识别的自然人是指可被直接或间接识别的自然人，尤其是通过参考姓名、证件号码、位置数据、联机标识符等标识，或通过参考特定于该自然人的身体、生理、基因、精神、经济、文化或社会标识的一个或多个因素进行识别。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-135">**Personal data and data subject:** Any information relating to an identified or identifiable natural person ('data subject'); an identifiable natural person is one who can be identified, directly or indirectly, in particular by reference to an identifier such as a name, an identification number, location data, an online identifier or to one or more factors specific to the physical, physiological, genetic, mental, economic, cultural, or social identity of that natural person.</span></span>
- <span data-ttu-id="fb6a4-136">**处理者：** 代表控制者处理个人数据的自然人或法人、公共机构、机关或其他主体。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-136">**Processor:** A natural or legal person, public authority, agency, or other body, which processes personal data on behalf of the controller.</span></span>
- <span data-ttu-id="fb6a4-p107">**客户数据：** 客户或代表客户通过使用企业服务提供给 Microsoft 的所有数据，包括所有文本、声音、视频或图像文件以及软件。客户数据包括（1）最终用户的身份信息（例如，Azure Active Directory 中的用户名和联系信息）和客户上传到特定服务或者在特定服务中创建的客户内容（例如，Azure 存储帐户中的客户内容，Azure SQL 数据库的客户内容，或 Azure 虚拟机中的客户虚拟机映像）。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p107">**Customer Data:** All data, including all text, sound, video, or image files, and software, that are provided to Microsoft by, or on behalf of, a customer through use of the enterprise service. Customer Data includes both (1) identifiable information of end users (for example, user names and contact information in Azure Active Directory) and Customer Content that a customer uploads into or creates in specific services (for example, customer content in an Azure Storage account, customer content of an Azure SQL Database, or a customer's virtual machine image in Azure Virtual Machines).</span></span>
- <span data-ttu-id="fb6a4-p108">**系统生成日志：** Microsoft 生成的日志和相关数据，可帮助 Microsoft 向用户提供企业服务。系统生成日志主要包括化名数据，例如唯一标识符，这通常是系统生成的无法单独识别个人但用于向用户提供企业服务的一个数字。系统生成日志还可能包含有关最终用户的身份信息，例如用户名。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p108">**System-Generated Logs:** Logs and related data generated by Microsoft that help Microsoft provide enterprise services to users. System-generated logs contain primarily pseudonymized data, such as unique identifiers — typically a number generated by the system that cannot on its own identify an individual person but is used to deliver the enterprise services to users. System-generated logs may also contain identifiable information about end users, such as a user name.</span></span>

## <a name="how-to-use-this-guide"></a><span data-ttu-id="fb6a4-142">如何使用本指南</span><span class="sxs-lookup"><span data-stu-id="fb6a4-142">How to use this guide</span></span>

<span data-ttu-id="fb6a4-143">本指南由两部分组成：</span><span class="sxs-lookup"><span data-stu-id="fb6a4-143">This guide consists of two parts:</span></span>

- <span data-ttu-id="fb6a4-p109">**第 1 部分：响应对客户数据的数据主体请求：** 本指南第 1 部分讨论了如何访问、纠正、限制、删除数据和将数据从你创建数据的应用程序中导出。本节详细介绍了如何针对客户内容以及最终用户的身份信息执行 DSR。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p109">**Part 1: Responding to Data Subject Requests for Customer Data:** Part 1 of this guide discusses how to access, rectify, restrict, delete, and export data from applications in which you have authored data. This section details how to execute DSRs against both Customer Content and also identifiable information of end users.</span></span>
- <span data-ttu-id="fb6a4-p110">**第 2 部分：响应对系统生成日志的数据主体请求：** 在你使用 Microsoft 的企业服务时，Microsoft 会生成一些信息（称为系统生成日志）以提供服务。本指南第 2 部分讨论了如何访问、删除和导出 Azure 的此类信息。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p110">**Part 2: Responding to Data Subject Requests for System-Generated Logs:** When you use Microsoft's enterprise services, Microsoft generates some information, known as System-Generated Logs, in order to provide the service. Part 2 of this guide discusses how to access, delete, and export such information for Azure.</span></span>

## <a name="understanding-dsrs-for-azure-active-directory-and-microsoft-service-accounts"></a><span data-ttu-id="fb6a4-148">了解 Azure Active Directory 和 Microsoft 服务帐户的 DSR</span><span class="sxs-lookup"><span data-stu-id="fb6a4-148">Understanding DSRs for Azure Active Directory and Microsoft service accounts</span></span>

<span data-ttu-id="fb6a4-p111">在考虑提供给企业客户的服务时，必须始终在特定 Azure Active Directory (AAD) 租户环境中执行 DSR。需要注意的是，始终在给定的 AAD 租户内执行 DSR。如果用户参与了多个租户，则务必注意 *仅* 在收到请求的特定租户内执行给定的 DSR。必须知道的是，这意味着一个企业客户执行 DSR **不会** 影响相邻企业客户的数据。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p111">When considering services provided to enterprise customers, execution of DSRs must always be understood within the context of a specific Azure Active Directory (AAD) tenant. Notably, DSRs are always executed within a given AAD tenant. If a user is participating in multiple tenants, it is important to emphasize that a given DSR is *only* executed within the context of the specific tenant the request was received within. This is critical to understand as it means the execution of a DSR by one enterprise customer **will not** impact the data of an adjacent enterprise customer.</span></span>

<span data-ttu-id="fb6a4-p112">这同样也适用于提供给企业客户的服务环境中的 Microsoft 服务帐户 (MSA)：针对 *与 AAD 租户关联* 的 MSA 帐户执行 DSR **将仅** 与租户内的数据相关。此外，在处理租户内的 MSA 帐户时，务必了解以下内容：</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p112">The same also applies for Microsoft Service Accounts (MSA) within the context of services provided to an enterprise customer: execution of a DSR against an MSA account *associated with an AAD tenant* **will only** pertain to data within the tenant. In addition, it is important to understand the following when handling MSA accounts within a tenant:</span></span>

- <span data-ttu-id="fb6a4-p113">如果 MSA 用户创建了 Azure 订阅，订阅将视为 AAD 租户。因此，如上文所述，DSR 的范围仅限于租户。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p113">If an MSA user creates an Azure subscription, the subscription will be handled as if it were an AAD tenant. Consequently, DSRs are scoped within the tenant as described above.</span></span>
- <span data-ttu-id="fb6a4-p114">如果删除通过 MSA 帐户创建的 Azure 订阅，**不会影响** 实际 MSA 帐户。同样，如上所述，Azure 订阅中执行的 DSR 仅限于租户本身的范围。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p114">If an Azure subscription created via an MSA account is deleted, **it will not affect** the actual MSA account. Again, as noted above, DSRs executing within the Azure subscription are limited to the scope of the tenant itself.</span></span>

<span data-ttu-id="fb6a4-p115">在 **给定租户外** 针对 MSA 帐户本身的 DSR 将通过消费者隐私面板执行。请参考《Windows 数据主体请求指南》了解更多详细信息。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p115">DSRs against an MSA account itself, **outside a given tenant**, are executed via the Consumer Privacy Dashboard. Please refer to the Windows Data Subject Request Guide for further details.</span></span>

## <a name="part-1-dsr-guide-for-customer-data"></a><span data-ttu-id="fb6a4-161">第 1 部分：客户数据的 DSR 指南</span><span class="sxs-lookup"><span data-stu-id="fb6a4-161">Part 1: DSR Guide for customer data</span></span>

### <a name="executing-dsrs-against-customer-data"></a><span data-ttu-id="fb6a4-162">针对客户数据执行 DSR</span><span class="sxs-lookup"><span data-stu-id="fb6a4-162">Executing DSRs against customer data</span></span>

<span data-ttu-id="fb6a4-p116">Microsoft 让你能够通过 Azure 门户访问、删除和导出某些客户数据，也可直接通过特定服务的预先存在的应用程序编程接口 (API) 或用户界面 (UI)（也称为 *产品内体验*）。有关此类产品内体验的详细信息，在各个服务的参考文档中进行了介绍。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p116">Microsoft provides the ability to access, delete, and export certain Customer Data through the Azure Portal and also directly via pre-existing application programming interfaces (APIs) or user interfaces (UIs) for specific services (also referred to as *in-product experiences*). Details regarding such in-product experiences are described in the respective services' reference documentation.</span></span>

>[!IMPORTANT]  
> <span data-ttu-id="fb6a4-p117">支持产品内 DSR 的服务要求直接使用服务的应用程序编程接口 (API) 或用户界面 (UI)，描述适用的 CRUD（创建、读取、更新、删除）操作。因此，除了在 Azure 门户中内执行 DSR 之外，还必须在给定服务内执行 DSR，以便完成针对给定数据主体的完整请求。请参考特定服务的参考文档以了解更多详细信息。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p117">Services supporting in-product DSRs require direct usage of the service's application programming interface (API) or user interface (UI), describing applicable CRUD (create, read, update, delete) operations. Consequently, execution of DSRs within a given service must be done in addition to execution of a DSR within the Azure Portal in order to complete a full request for a given data subject. Please refer to specific services' reference documentation for further details.</span></span>

### <a name="step-1-discover"></a><span data-ttu-id="fb6a4-168">步骤 1：发现</span><span class="sxs-lookup"><span data-stu-id="fb6a4-168">Step 1: Discover</span></span>

<span data-ttu-id="fb6a4-p118">响应 DSR 的第一步是查找作为请求主体的个人数据。这第一步（查找和审查所涉及的个人数据）将帮助你确定 DSR 是否符合组织有关接受或拒绝 DSR 的要求。例如，在查找并审查所涉及的个人数据后，你可以确定请求不符合组织的要求，因为这样做可能会对他人的权利和自由产生负面影响。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p118">The first step in responding to a DSR is to find the personal data that is the subject of the request. This first step — finding and reviewing the personal data at issue — will help you determine whether a DSR meets your organization's requirements for honoring or declining a DSR. For example, after finding and reviewing the personal data at issue, you may determine the request doesn't meet your organization's requirements because doing so may adversely affect the rights and freedoms of others.</span></span>

<span data-ttu-id="fb6a4-172">找到数据后，可执行特定操作以满足数据主体的请求。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-172">After you find the data, you can then perform the specific action to satisfy the request by the data subject.</span></span>

<span data-ttu-id="fb6a4-p119">[Azure Active Directory](https://azure.microsoft.com/services/active-directory/) 是 Microsoft 的基于云的、多租户目录和标识管理服务。你可以使用 [Azure 门户](https://portal.azure.com/)找到最终用户的身份信息，例如在 [Azure Active Directory](https://azure.microsoft.com/services/active-directory/) (AAD) 环境中包含个人数据的客户和员工的用户配置文件和用户工作信息。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p119">[Azure Active Directory](https://azure.microsoft.com/services/active-directory/) is Microsoft's cloud-based, multi-tenant directory and identity management service. You can locate identifiable information of end users, such as customer and employee user profiles and user work information that contain personal data in your [Azure Active Directory](https://azure.microsoft.com/services/active-directory/) (AAD) environment by using the [Azure portal](https://portal.azure.com/).</span></span>

<span data-ttu-id="fb6a4-p120">这在你想要查找或更改特定用户的个人数据时尤其有用。还可以添加或更改用户配置文件和工作信息。必须使用作为该目录的全局管理员的帐户进行登录。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p120">This is particularly helpful if you want to find or change personal data for a specific user. You can also add or change user profile and work information. You must sign in with an account that's a global admin for the directory.</span></span>

#### <a name="how-do-i-locate-or-view-user-profile-and-work-information"></a><span data-ttu-id="fb6a4-178">如何查找或查看用户配置文件和工作信息？</span><span class="sxs-lookup"><span data-stu-id="fb6a4-178">How do I locate or view user profile and work information?</span></span>

1. <span data-ttu-id="fb6a4-179">使用作为该目录的全局管理员的帐户登录到 [Azure 门户](https://portal.azure.com/)。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-179">Sign in to the [Azure portal](https://portal.azure.com/) with an account that's a global admin for the directory.</span></span>

2. <span data-ttu-id="fb6a4-180">选择“**Azure Active Directory**”。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-180">Select **Azure Active Directory**.</span></span>

     ![选择“所有服务”](../media/gdpr-azure-dsr-azure-portal.png)

3. <span data-ttu-id="fb6a4-182">选择“**用户**”。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-182">Select **Users**.</span></span>

     ![选择用户](../media/gdpr-azure-dsr-azure-all-users.png)

4. <span data-ttu-id="fb6a4-184">在“**所有用户**”边栏选项卡上，从列表中选择用户，然后在所选用户的边栏选项卡上，选择“**配置文件**”以查看可能包含个人数据的用户配置文件信息。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-184">On the **All users** blade, select a user from the list, and then, on the blade for the selected user, select **Profile** to view user profile information that might contain personal data.</span></span>

    ![选择配置文件](../media/gdpr-azure-dsr-azure-user-profile.png)

5. <span data-ttu-id="fb6a4-186">如果需要添加或更改用户配置文件信息，可以在命令栏中选择“**编辑**”，然后在做出更改后选择“**保存**”。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-186">If you need to add or change user profile information, you can do so by selecting **Edit** in the command bar, then select **Save** after making changes.</span></span>

#### <a name="service-specific-interfaces"></a><span data-ttu-id="fb6a4-187">特定于服务的界面</span><span class="sxs-lookup"><span data-stu-id="fb6a4-187">Service-specific interfaces</span></span>

<span data-ttu-id="fb6a4-p121">Microsoft 让你能够直接通过特定服务的预先存在的应用程序编程接口 (API) 或用户界面 (UI) 发现客户数据。详细信息在各个服务的参考文档中进行了介绍，描述了适用的（创建、读取、更新、删除）操作。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p121">Microsoft provides the ability to discover Customer Data directly via pre-existing application programming interfaces (APIs) or user interfaces (UIs) for specific services. Details are described in the respective services' reference documentation, describing applicable CRUD (create, read, update, delete) operations.</span></span>

### <a name="step-2-access"></a><span data-ttu-id="fb6a4-190">步骤 2：访问</span><span class="sxs-lookup"><span data-stu-id="fb6a4-190">Step 2: Access</span></span>

<span data-ttu-id="fb6a4-p122">在找到包含潜在响应 DSR 的个人数据的客户数据后，应该由你和你的组织决定将哪些数据提供给数据主体。可以通过实际文档副本、经过适当编校的版本或者你认为适合共享的部分的屏幕截图来提供。对于访问请求的每个响应，需要检索包含响应数据的文档或其他项目的副本。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p122">After you've found Customer Data containing personal data that is potentially responsive to a DSR, it is up to you and your organization to decide which data to provide to the data subject. You can provide them with a copy of the actual document, an appropriately redacted version, or a screenshot of the portions you have deemed appropriate to share. For each of these responses to an access request, you will have to retrieve a copy of the document or other item that contains the responsive data.</span></span>

<span data-ttu-id="fb6a4-194">将副本提供给数据主体时，可能需要删除或修订有关其他数据主体和任何机密信息的个人信息。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-194">When providing a copy to the data subject, you may have to remove or redact personal information about other data subjects and any confidential information.</span></span>

#### <a name="azure-active-directory"></a><span data-ttu-id="fb6a4-195">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="fb6a4-195">Azure Active Directory</span></span>

<span data-ttu-id="fb6a4-p123">Microsoft 提供了门户和产品内体验，让企业客户的租户管理员能够管理 DSR 访问请求。DSR 访问请求允许访问用户的个人数据，包括：(a) 最终用户的身份信息，以及 (b) 系统生成日志。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p123">Microsoft offers both a portal and in-product experiences providing the enterprise customer's tenant administrator the capability to manage DSR access requests. DSR Access requests allow for access of the personal data of the user, including: (a) identifiable information about an end-user and (b) system-generated logs.</span></span>

#### <a name="service-specific-interfaces"></a><span data-ttu-id="fb6a4-198">特定于服务的界面</span><span class="sxs-lookup"><span data-stu-id="fb6a4-198">Service-specific interfaces</span></span>

<span data-ttu-id="fb6a4-p124">Microsoft 让你能够直接通过特定服务的预先存在的应用程序编程接口 (API) 或用户界面 (UI) 发现客户数据。详细信息在各个服务的参考文档中进行了介绍，描述了适用的（创建、读取、更新、删除）操作。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p124">Microsoft provides the ability to discover Customer Data directly via pre-existing application programming interfaces (APIs) or user interfaces (UIs) for specific services. Details are described in the respective services' reference documentation, describing applicable CRUD (create, read, update, delete) operations.</span></span>

### <a name="step-3-rectify"></a><span data-ttu-id="fb6a4-201">步骤 3：纠正</span><span class="sxs-lookup"><span data-stu-id="fb6a4-201">Step 3: Rectify</span></span>

<span data-ttu-id="fb6a4-p125">如果数据主体要求你纠正驻留在你组织的数据中的个人数据，你和你的组织需要确定是否接受请求。纠正数据可能包括以下操作：编辑、修订个人数据或从文档或其他项目类型中移除个人数据。下面提供了对 Microsoft 支持和 FastTrack 数据执行此操作的最便利的方法。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p125">If a data subject has asked you to rectify the personal data that resides in your organization's data, you and your organization will have to determine whether it's appropriate to honor the request. Rectifying the data may include taking actions such as editing, redacting, or removing personal data from a document or other type or item. The most expedient way to do this for Microsoft Support and FastTrack data is provided below.</span></span>

#### <a name="azure-active-directory"></a><span data-ttu-id="fb6a4-205">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="fb6a4-205">Azure Active Directory</span></span>

<span data-ttu-id="fb6a4-p126">企业客户能够管理 DSR 纠正请求，包括根据给定 Microsoft 服务的特性的有限编辑功能。作为数据处理者，Microsoft 不提供更正系统生成日志的功能，因为这些日志反映真实活动，包含 Microsoft 服务内的事件历史记录。关于 Azure Active Directory，存在有限编辑功能，可纠正有关最终用户的身份信息，如下文所述。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p126">Enterprise customers have the ability to manage DSR rectify requests, including limited editing features per the nature of a given Microsoft service. As a data processor, Microsoft does not offer the ability to correct system-generated logs as it reflects factual activities and constitutes a historical record of events within Microsoft services. With respect to Azure Active Directory, limited editing features exist to rectify identifiable information about an end-user, as described further below.</span></span>

##### <a name="azure-active-directory-rectifycorrect-inaccurate-or-incomplete-personal-data"></a><span data-ttu-id="fb6a4-209">Azure Active Directory：纠正/更正不准确或不完整的个人数据</span><span class="sxs-lookup"><span data-stu-id="fb6a4-209">Azure Active Directory: rectify/correct inaccurate or incomplete personal data</span></span>

<span data-ttu-id="fb6a4-p127">你可以使用 [Azure 门户](https://portal.azure.com/)在 [Azure Active Directory](https://azure.microsoft.com/services/active-directory/) (AAD) 环境中更正、更新或删除有关最终用户的身份信息，例如包含个人数据的客户和员工用户配置文件，如用户的姓名、工作职务、地址或电话号码。必须使用作为该目录的全局管理员的帐户进行登录。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p127">You can correct, update, or delete identifiable information about end users, such as customer and employee user profiles and user work information that contain personal data, such as a user's name, work title, address, or phone number, in your [Azure Active Directory](https://azure.microsoft.com/services/active-directory/) (AAD) environment by using the [Azure portal](https://portal.azure.com/). You must sign in with an account that's a global admin for the directory.</span></span>

###### <a name="how-do-i-correct-or-update-user-profile-and-work-information-in-azure-active-directory"></a><span data-ttu-id="fb6a4-212">如何在 Azure Active Directory 中更正或更新用户配置文件和工作信息？</span><span class="sxs-lookup"><span data-stu-id="fb6a4-212">How do I correct or update user profile and work information in Azure Active Directory?</span></span>

1. <span data-ttu-id="fb6a4-213">使用作为该目录的全局管理员的帐户登录到 [Azure 门户](https://portal.azure.com/)。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-213">Sign in to the [Azure portal](https://portal.azure.com/) with an account that's a global admin for the directory.</span></span>

2. <span data-ttu-id="fb6a4-214">选择“**Azure Active Directory**”。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-214">Select **Azure Active Directory**.</span></span>

    ![选择“所有服务”](../media/gdpr-azure-dsr-azure-portal.png)

3. <span data-ttu-id="fb6a4-216">选择“**用户**”。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-216">Select **Users**.</span></span>

    ![选择用户](../media/gdpr-azure-dsr-azure-all-users.png)

4. <span data-ttu-id="fb6a4-218">在“**所有用户**”边栏选项卡上，从列表中选择用户，然后在所选用户的边栏选项卡上，选择“**配置文件**”以查看需要更正或更新的用户配置文件信息。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-218">On the **All users** blade, select a user from the list, and then, on the blade for the selected user, select **Profile** to view the user profile information that needs to be corrected or updated.</span></span>

    ![选择用户配置文件](../media/gdpr-azure-dsr-azure-user-profile.png)

5. <span data-ttu-id="fb6a4-220">通过在命令栏中选择“**编辑**”，然后在做出更改后选择“ **保存**”，可更正或更新包括工作信息在内的用户配置文件信息。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-220">Correct or update the user profile information including work information by selecting **Edit** in the command bar, then select **Save** after making changes.</span></span>

    ![选择"编辑"](../media/gdpr-azure-dsr-azure-edit-user-profile.png)

#### <a name="service-specific-interfaces"></a><span data-ttu-id="fb6a4-222">特定于服务的界面</span><span class="sxs-lookup"><span data-stu-id="fb6a4-222">Service-Specific Interfaces</span></span>

<span data-ttu-id="fb6a4-p128">Microsoft 让你能够直接通过特定服务的预先存在的应用程序编程接口 (API) 或用户界面 (UI) 发现客户数据。详细信息在各个服务的参考文档中进行了介绍，描述了适用的（创建、读取、更新、删除）操作。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p128">Microsoft provides the ability to discover Customer Data directly via pre-existing application programming interfaces (APIs) or user interfaces (UIs) for specific services. Details are described in the respective services' reference documentation, describing applicable CRUD (create, read, update, delete) operations.</span></span>

### <a name="step-4-restrict"></a><span data-ttu-id="fb6a4-225">步骤 4：限制</span><span class="sxs-lookup"><span data-stu-id="fb6a4-225">Step 4: Restrict</span></span>

<span data-ttu-id="fb6a4-p129">数据主体可能会请求限制其个人数据的处理。我们提供 Azure 门户和预先存在的应用程序编程接口 (API) 或用户界面 (UI)。这些体验让企业客户的租户管理员能够通过数据导出和数据删除组合来管理此类 DSR。客户可 (1) 导出用户个人数据的电子副本，包括 (a) 帐户，(b) 系统生成日志，和 (c) 关联日志，然后 (2) 删除帐户以及驻留在 Microsoft 系统中的关联数据。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p129">Data subjects may request that you restrict processing of their personal data. We provide both the Azure Portal and pre-existing application programming interfaces (APIs) or user interfaces (UIs). These experiences provide the enterprise customer's tenant administrator the capability to manage such DSRs through a combination of data export and data deletion. A customer may (1) export an electronic copy of the personal data of the user, including (a) account(s), (b) system-generated logs, and (c) associated logs, followed with (2) deletion of the account and associated data residing within Microsoft systems.</span></span>

### <a name="step-5-delete"></a><span data-ttu-id="fb6a4-230">步骤 5：删除</span><span class="sxs-lookup"><span data-stu-id="fb6a4-230">Step 5: Delete</span></span>

<span data-ttu-id="fb6a4-p130">将个人数据从组织的客户数据移除的“擦除权限”是 GDPR 中的一项关键保护措施。移除个人数据包括移除审核日志信息之外的所有个人数据和系统生成日志。在 **软删除** 用户（请参阅下文的详细信息）后，帐户将禁用 30 天。如果在这 30 天期间不执行任何进一步操作，则将 **永久删除** 用户（同样请参阅下文的详细信息）。在 **永久删除** 后，将在下一个 30 天内擦除用户的帐户、个人数据和系统生成日志。如果租户管理员立即发出 **永久删除**，将在发出后 30 天內擦除用户的帐户、个人数据和系统生成日志。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p130">The "right to erasure" by the removal of personal data from an organization's Customer Data is a key protection in the GDPR. Removing personal data includes removing all personal data and system-generated logs, except audit log information. When a user is **soft deleted** (see details below), the account is disabled for 30 days. If no further action is taken during this 30-day period, the user is **permanently deleted** (again, see details below). Upon a **permanent delete**, the user's account, personal data, and system-generated logs are expunged within an additional 30 days. If a tenant admin immediately issues a **permanent delete**, the user's account, personal data, and system-generated logs are expunged within 30 days of issuance.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fb6a4-237">你必须是租户管理员才能从租户中删除用户。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-237">You must be a tenant administrator to delete a user from the tenant.</span></span>

#### <a name="delete-a-user-and-associated-data-through-the-azure-portal"></a><span data-ttu-id="fb6a4-238">通过 Azure 门户删除用户和关联数据</span><span class="sxs-lookup"><span data-stu-id="fb6a4-238">Delete a user and associated data through the Azure portal</span></span>

<span data-ttu-id="fb6a4-239">你在收到对数据主体的删除请求后，可以使用 Azure 门户删除用户和关联的个人信息，以及系统生成日志。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-239">After you receive a delete request for a data subject, you can use the Azure portal to delete both a user and the associated personal information as well as system-generated logs.</span></span>

<span data-ttu-id="fb6a4-p131">删除此数据也意味着从租户删除用户。用户最初会被软删除，这是指帐户可在标记为软删除后的 30 天內由租户管理员恢复。30 天后，帐户将自动从租户中永久删除。在这 30 天期限之前，你可手动将软删除的用户从回收站删除。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p131">Deleting this data also means deleting the user from the tenant. Users are initially soft-deleted, which means the account can be recovered by a tenant admin within 30 days of being marked for soft-delete. After 30 days, the account is automatically, and permanently, deleted from the tenant. Prior to that 30 days, you can manually delete a soft-deleted user from the recycle bin.</span></span>

<span data-ttu-id="fb6a4-244">下面是从租户删除用户的高级流程。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-244">Here's the high-level process for deleting users from your tenant.</span></span>

1. <span data-ttu-id="fb6a4-245">转到 Azure 门户并找到用户。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-245">Go to the Azure portal and locate the user.</span></span>

2. <span data-ttu-id="fb6a4-p132">删除用户。你最初删除用户时，用户的帐户将发送到回收站。**此时，用户已软删除，这表示帐户已禁用，但并未从 Azure Active Directory 擦除。**</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p132">Delete the user. When you initially delete the user, the user's account is sent to the Recycle Bin. **At this point, the user is soft deleted, meaning the account is disabled, but not expunged from Azure Active Directory.**</span></span>

3. <span data-ttu-id="fb6a4-p133">转到“最近已删除的用户”列表并永久删除用户。**此时，该用户将永久删除（也称为硬删除），这表示帐户已从 Azure Active Directory 擦除。**</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p133">Go to the Recently deleted users list and permanently delete the user. **At this point the user is permanently deleted (also known as hard deleted), meaning the account has been expunged from Azure Active Directory**</span></span>

###### <a name="to-delete-a-user-from-an-azure-tenant"></a><span data-ttu-id="fb6a4-251">从 Azure 租户删除用户</span><span class="sxs-lookup"><span data-stu-id="fb6a4-251">To delete a user from an Azure tenant</span></span>

1. <span data-ttu-id="fb6a4-252">使用作为该目录的全局管理员的帐户登录到 [Azure 门户](https://portal.azure.com/)。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-252">Sign in to the [Azure portal](https://portal.azure.com/) with an account that's a global admin for the directory.</span></span>

2. <span data-ttu-id="fb6a4-253">选择“**Azure Active Directory**”。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-253">Select **Azure Active Directory**.</span></span>

    ![选择“所有服务”](../media/gdpr-azure-dsr-azure-portal.png)

3. <span data-ttu-id="fb6a4-255">选择“**用户**”。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-255">Select **Users**.</span></span>

    ![选择用户](../media/gdpr-azure-dsr-azure-all-users.png)

4. <span data-ttu-id="fb6a4-257">选中想要删除的用户旁边的框，选择“删除用户”，然后在询问你是否要删除用户时在框中选择“是”。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-257">Check the box next to the user you want to delete, select **Delete user**, and then select **Yes** in the box asking if you want to delete the user.</span></span>

    ![用户管理](../media/gdpr-azure-dsr-azure-selected-user.png)

5. <span data-ttu-id="fb6a4-259">在“ **所有用户**” 边栏选项卡上，选择“ **已删除的用户**”。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-259">On the **All users** blade, select **Deleted users**.</span></span>

    ![查看用户配置文件](../media/gdpr-azure-dsr-azure-deleted-user.png)

4. <span data-ttu-id="fb6a4-261">再次选择同一用户，在命令栏中选择“ **永久删除**”，然后在询问你是否确定时在框中选择“ **是**” 。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-261">Select the same user again, select **Delete permanently** in the command bar, and then select **Yes** in the box asking if you're sure.</span></span>

>[!IMPORTANT]  
><span data-ttu-id="fb6a4-p134">请注意，单击 **“是”** 将永久且不可挽回地删除用户和所有关联的数据及系统生成日志。如果错误地执行了该操作，必须手动将用户添加回租户。关联的数据和系统生成日志是不可恢复的。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p134">Be aware that by clicking **Yes** you are permanently, and irrevocably, deleting the user and all associated data and system-generated logs. If you do this by mistake, you'll have to manually add the user back to the tenant. The associated data and system-generated logs are non-recoverable.</span></span>

   ![查看用户工作信息](../media/gdpr-azure-dsr-azure-permanently-deleted-user.png)

#### <a name="service-specific-interfaces"></a><span data-ttu-id="fb6a4-266">特定于服务的界面</span><span class="sxs-lookup"><span data-stu-id="fb6a4-266">Service-specific interfaces</span></span>

<span data-ttu-id="fb6a4-p135">Microsoft 让你能够直接通过特定服务的预先存在的应用程序编程接口 (API) 或用户界面 (UI) 发现客户数据。详细信息在各个服务的参考文档中进行了介绍，描述了适用的（创建、读取、更新、删除）操作。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p135">Microsoft provides the ability to discover Customer Data directly via pre-existing application programming interfaces (APIs) or user interfaces (UIs) for specific services. Details are described in the respective services' reference documentation, describing applicable CRUD (create, read, update, delete) operations.</span></span>

## <a name="step-6-export"></a><span data-ttu-id="fb6a4-269">步骤 6：导出</span><span class="sxs-lookup"><span data-stu-id="fb6a4-269">Step 6: Export</span></span>

<span data-ttu-id="fb6a4-p136">“数据移植权限”允许数据主体以电子格式请求个人数据副本（这是一种“结构化、常用、机器可读、可互操作的格式”），该副本可传输到另一个数据控制者。Azure 支持此操作，让你的组织可通过本机 JSON 格式将数据导出到指定 Azure 存储容器。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p136">The "right of data portability" allows a data subject to request a copy of their personal data in an electronic format (that's a "structured, commonly used, machine read-able, and interoperable format") that may be transmitted to another data controller. Azure supports this by enabling your organization to export the data in the native JSON format, to your specified Azure Storage Container.</span></span>

>[!IMPORTANT]
><span data-ttu-id="fb6a4-272">你必须是租户管理员才能从租户中导出用户数据。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-272">You must be a tenant administrator to export user data from the tenant.</span></span>

### <a name="azure-active-directory"></a><span data-ttu-id="fb6a4-273">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="fb6a4-273">Azure Active Directory</span></span>

<span data-ttu-id="fb6a4-274">关于客户数据，Microsoft 提供了门户和产品内体验，让企业客户的租户管理员能够管理对一个最终用户的身份信息的导出请求。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-274">With respect to Customer Data, Microsoft offers both a portal and in-product experiences providing the enterprise customer's tenant administrator the capability to manage export requests for identifiable information about an end user.</span></span>

### <a name="service-specific-interfaces"></a><span data-ttu-id="fb6a4-275">特定于服务的界面</span><span class="sxs-lookup"><span data-stu-id="fb6a4-275">Service-specific interfaces</span></span>

<span data-ttu-id="fb6a4-p137">Microsoft 让你能够直接通过特定服务的预先存在的应用程序编程接口 (API) 或用户界面 (UI) 发现客户数据。详细信息在各个服务的参考文档中进行了介绍，描述了适用的（创建、读取、更新、删除）操作。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p137">Microsoft provides the ability to discover Customer Data directly via pre-existing application programming interfaces (APIs) or user interfaces (UIs) for specific services. Details are described in the respective services' reference documentation, describing applicable CRUD (create, read, update, delete) operations.</span></span>

## <a name="part-2-system-generated-logs"></a><span data-ttu-id="fb6a4-278">第 2 部分：系统生成的日志</span><span class="sxs-lookup"><span data-stu-id="fb6a4-278">Part 2: System-Generated Logs</span></span>

<span data-ttu-id="fb6a4-279">Microsoft 还让你能够访问、删除和导出有关 Azure 用户使用情况的某些系统生成日志。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-279">Microsoft also provides you with the ability to access, delete, and export certain system-generated logs associated with a user's use of Azure.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="fb6a4-p138">不支持限制或纠正系统生成日志的功能。系统生成日志包括 Microsoft 云内执行的实际操作和诊断数据，修改此类数据可能会损坏操作历史记录，这会增加诈骗和安全风险。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p138">The ability to restrict or rectify system-generated logs is not supported. System-generated logs constitute factual actions conducted within the Microsoft cloud and diagnostic data, and modifications to such data would compromise the historical record of actions, increasing fraud and security risks.</span></span>

### <a name="executing-dsrs-against-system-generated-logs"></a><span data-ttu-id="fb6a4-282">针对系统生成日志执行 DSR</span><span class="sxs-lookup"><span data-stu-id="fb6a4-282">Executing DSRs against System-Generated Logs</span></span>

<span data-ttu-id="fb6a4-p139">Microsoft 让你能够通过 Azure 门户访问、删除和导出某些系统生成日志，也可以直接通过特定服务的编程接口或用户界面进行。详细信息在各个服务的参考文档中进行了介绍。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p139">Microsoft provides the ability to access, delete, and export certain system-generated logs through the Azure Portal and also directly via programmatic interfaces or user interfaces for specific services. Details are described in the respective services' reference documentation.</span></span>

>[!IMPORTANT]  
> <span data-ttu-id="fb6a4-p140">支持产品内 DSR 的服务要求直接使用服务的应用程序编程接口 (API) 或用户界面 (UI)。因此，**除了在 Azure 门户内执行 DSR 之外，还必须执行产品内 DSR，以便完成针对给定数据主体的完整请求。请参考特定服务的参考文档以了解更多详细信息。**</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p140">Services supporting in-product DSRs require direct usage of the service's application programming interface (API) or user interface (UI). Consequently, execution of an in-product DSRs **must be done in addition to execution of a DSR within the Azure Portal in order to complete a full request for a given data subject. Please refer to specific services' reference documentation for further details.**</span></span>

### <a name="step-1-access"></a><span data-ttu-id="fb6a4-287">步骤 1：访问</span><span class="sxs-lookup"><span data-stu-id="fb6a4-287">Step 1: Access</span></span>

<span data-ttu-id="fb6a4-p141">租户管理员是组织内唯一可以访问与 Azure 的特定用户使用情况相关联的系统生成日志的人员。为访问请求检索到的数据将以机器可读格式提供，并在允许用户知道数据与哪些服务关联的文件中提供。如上所述，检索到的数据不包括可能会危及服务安全性的数据。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p141">The tenant admin is the only person within your organization who can access system-generated logs associated with a particular user's use of Azure. The data retrieved for an access request will be provided in a machine-readable format and will be provided in files that will allow the user to know which services the data is associated with. As noted above, the data retrieved will not include data that may compromise the security of the service.</span></span>

#### <a name="azure-active-directory"></a><span data-ttu-id="fb6a4-291">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="fb6a4-291">Azure Active Directory</span></span>

<span data-ttu-id="fb6a4-p142">Microsoft 提供了门户和产品内体验，让企业客户的租户管理员能够管理访问请求。访问请求允许访问用户的个人数据，包括：(a) 最终用户的身份信息，以及 (b) 系统生成日志。该流程与第 1 部分“步骤 2：访问”的“Azure Active Directory”部分中所述的流程相同。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p142">Microsoft offers both a portal and in-product experiences providing the enterprise customer's tenant administrator the capability to manage access requests. Access requests will allow for access of the personal data of the user, including: (a) identifiable information about an end user and (b) service-generated logs. The process is identical to that described in the Azure Active Directory section of Part 1, Step 2: Access.</span></span>

#### <a name="service-specific-interfaces"></a><span data-ttu-id="fb6a4-295">特定于服务的界面</span><span class="sxs-lookup"><span data-stu-id="fb6a4-295">Service-specific interfaces</span></span>

<span data-ttu-id="fb6a4-p143">Microsoft 让你能够直接通过特定服务的预先存在的应用程序编程接口 (API) 或用户界面 (UI) 发现客户数据。详细信息在各个服务的参考文档中进行了介绍，描述了适用的（创建、读取、更新、删除）操作。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p143">Microsoft provides the ability to discover Customer Data directly via pre-existing application programming interfaces (APIs) or user interfaces (UIs) for specific services. Details are described in the respective services' reference documentation, describing applicable CRUD (create, read, update, delete) operations.</span></span>

### <a name="step-2-delete"></a><span data-ttu-id="fb6a4-298">步骤 2：删除</span><span class="sxs-lookup"><span data-stu-id="fb6a4-298">Step 2: Delete</span></span>

<span data-ttu-id="fb6a4-299">租户管理员是组织内唯一可以对 Azure 租户内的特定用户执行 DSR 删除请求的人员。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-299">The tenant admin is the only person within your organization who can execute a DSR delete request for a particular user within an Azure tenant.</span></span>

#### <a name="azure-active-directory"></a><span data-ttu-id="fb6a4-300">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="fb6a4-300">Azure Active Directory</span></span>

<span data-ttu-id="fb6a4-p144">Microsoft 提供了门户和产品内体验，让企业客户的租户管理员能够管理 DSR 删除请求。DSR 删除请求遵循第 1 部分“步骤 5：删除”中的“Azure 门户”部分中所述的流程。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p144">Microsoft offers both a portal and in-product experiences providing the enterprise customer's tenant administrator the capability to manage DSR delete requests. DSR delete requests follow the same as described in the Delete a user and associated data through the Azure portal section of Part 1, Step 5: Delete.</span></span>

#### <a name="service-specific-interfaces"></a><span data-ttu-id="fb6a4-303">特定于服务的界面</span><span class="sxs-lookup"><span data-stu-id="fb6a4-303">Service-specific interfaces</span></span>

<span data-ttu-id="fb6a4-p145">Microsoft 让你能够直接通过特定服务的预先存在的应用程序编程接口 (API) 或用户界面 (UI) 发现客户数据。详细信息在各个服务的参考文档中进行了介绍，描述了适用的（创建、读取、更新、删除）操作。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p145">Microsoft provides the ability to discover Customer Data directly via pre-existing application programming interfaces (APIs) or user interfaces (UIs) for specific services. Details are described in the respective services' reference documentation, describing applicable CRUD (create, read, update, delete) operations.</span></span>

### <a name="step-3-export"></a><span data-ttu-id="fb6a4-306">步骤 3：导出</span><span class="sxs-lookup"><span data-stu-id="fb6a4-306">Step 3: Export</span></span>

<span data-ttu-id="fb6a4-p146">租户管理员是组织内唯一可以访问与 Azure 的特定用户使用情况相关联的系统生成日志的人员。为导出请求检索到的数据将以机器可读格式提供，并在允许用户知道数据与哪些服务关联的文件中提供。如上所述，检索到的数据不包括可能会危及服务安全性或稳定性的数据。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p146">The tenant admin is the only person within your organization who can access system-generated logs associated with a particular user's use of Azure. The data retrieved for an export request will be provided in a machine-readable format and will be provided in files that will allow the user to know which services the data is associated with. As noted above, the data retrieved will not include data that may compromise the security or stability of the service.</span></span>

#### <a name="export-system-generated-logs-using-the-azure-portal"></a><span data-ttu-id="fb6a4-310">使用 Azure 门户导出系统生成日志</span><span class="sxs-lookup"><span data-stu-id="fb6a4-310">Export system-generated logs using the Azure portal</span></span>

<span data-ttu-id="fb6a4-311">你收到对数据主体的导出请求后，可使用 Azure 门户导出与给定用户相关联的系统生成日志。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-311">After you receive an export request for a data subject, you can use the Azure portal to export system-generated logs associated with a given user.</span></span>

<span data-ttu-id="fb6a4-312">下面是从租户导出用户数据的高级流程。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-312">Here's the high-level process for exporting data from your tenant.</span></span>

1. <span data-ttu-id="fb6a4-313">转到 Azure 门户并代表用户创建导出请求。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-313">Go to the Azure portal and create an export request on behalf of the user.</span></span>
2. <span data-ttu-id="fb6a4-314">导出数据并将文件发送给用户。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-314">Export the data and send file to user.</span></span>

###### <a name="to-export-a-users-info-from-an-azure-tenant"></a><span data-ttu-id="fb6a4-315">从 Azure 租户导出用户信息</span><span class="sxs-lookup"><span data-stu-id="fb6a4-315">To export a user's info from an Azure tenant</span></span>

1. <span data-ttu-id="fb6a4-316">打开 Azure 门户，选择“所有服务”，在筛选器中键入“策略”，然后选择“策略”。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-316">Open the Azure portal, select **All services**, type *policy* into the filter, and then select **Policy**.</span></span>

     ![<span data-ttu-id="fb6a4-317">“所有服务”筛选器</span><span class="sxs-lookup"><span data-stu-id="fb6a4-317">All services filter</span></span> ](../media/gdpr-azure-dsr-azure-policy.png)

2. <span data-ttu-id="fb6a4-318">在“策略”边栏选项卡中，依次选择“用户策略”、“管理用户请求”和“添加导出请求”。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-318">In the **Policy** blade, select **User privacy**, select **Manage User Requests**, and then select **Add export request**.</span></span>

    ![<span data-ttu-id="fb6a4-319">添加导出请求</span><span class="sxs-lookup"><span data-stu-id="fb6a4-319">Add export request</span></span> ](../media/gdpr-azure-dsr-azure-add-export-request.png)

3. <span data-ttu-id="fb6a4-320">完成“导出数据请求”：</span><span class="sxs-lookup"><span data-stu-id="fb6a4-320">Complete the **Export data request**:</span></span>

    ![新建导出数据请求](../media/gdpr-azure-dsr-azure-export-data-request.png)

- <span data-ttu-id="fb6a4-p147">**用户。** 键入请求导出的 Azure Active Directory 用户的电子邮件地址。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p147">**User.** Type the email address of the Azure Active Directory user that requested the export.</span></span>
- <span data-ttu-id="fb6a4-p148">**订阅。** 选择要用于报告资源使用情况和为服务开具帐单的帐户。这也是 Azure 存储帐户所在的位置。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p148">**Subscription.** Select the account you use to report resource usage and to bill for services. This is also the location of your Azure storage account.</span></span>
- <span data-ttu-id="fb6a4-p149">**存储帐户。** 选择 Azure 存储 (Blob) 的位置。有关详细信息，请参阅 [《Microsoft Azure 存储简介 — Blob 存储》](/azure/storage/common/storage-introduction#blob-storage)一文。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p149">**Storage account.** Select the location of your Azure Storage (Blob). For more info, see the [Introduction to Microsoft Azure Storage — Blob storage](/azure/storage/common/storage-introduction#blob-storage) article.</span></span>
- <span data-ttu-id="fb6a4-p150">**容器。** 创建新的（或选择现有的）容器作为存放用户导出的隐私数据的存储位置。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p150">**Container.** Create a new (or select an existing) container as the storage location for the user's exported privacy data.</span></span>

4. <span data-ttu-id="fb6a4-332">选择 **创建**。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-332">Select **Create**.</span></span>

<span data-ttu-id="fb6a4-p151">导出请求将进入“**待定**”状态。可在“**用户隐私 — 概述**”边栏选项卡上查看报告状态。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p151">The export request goes into **Pending** status. You can view the report status on the **User privacy — Overview** blade.</span></span>

>[!IMPORTANT]  
><span data-ttu-id="fb6a4-335">由于个人数据可能来自多个系统，因此导出过程可能需要一个月才能完成。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-335">Because personal data can come from multiple systems, it's possible that the export process might take up to one month to complete.</span></span>

#### <a name="service-specific-interfaces"></a><span data-ttu-id="fb6a4-336">特定于服务的界面</span><span class="sxs-lookup"><span data-stu-id="fb6a4-336">Service-Specific Interfaces</span></span>

<span data-ttu-id="fb6a4-p152">Microsoft 让你能够直接通过特定服务的预先存在的应用程序编程接口 (API) 或用户界面 (UI) 发现客户数据。详细信息在各个服务的参考文档中进行了介绍，描述了适用的（创建、读取、更新、删除）操作。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-p152">Microsoft provides the ability to discover Customer Data directly via pre-existing application programming interfaces (APIs) or user interfaces (UIs) for specific services. Details are described in the respective services' reference documentation, describing applicable CRUD (create, read, update, delete) operations.</span></span>

### <a name="notify-about-exporting-or-deleting-issues"></a><span data-ttu-id="fb6a4-339">通知导出或删除问题</span><span class="sxs-lookup"><span data-stu-id="fb6a4-339">Notify about exporting or deleting issues</span></span>

<span data-ttu-id="fb6a4-340">如果在从 Azure 门户导出或删除数据时遇到问题，请转到 Azure 门户“**帮助 + 支持**”边栏选项卡，并在“**订阅管理”>“订阅的隐私与合规请求”>“隐私边栏选项卡和 GDPR 请求**”下提交新票证。</span><span class="sxs-lookup"><span data-stu-id="fb6a4-340">If you run into issues while exporting or deleting data from the Azure portal, go to the Azure portal **Help + Support** blade and submit a new ticket under **Subscription Management > Privacy and compliance requests for Subscriptions > Privacy Blade and GDPR Requests**.</span></span>

## <a name="learn-more"></a><span data-ttu-id="fb6a4-341">了解详细信息</span><span class="sxs-lookup"><span data-stu-id="fb6a4-341">Learn more</span></span>

- [<span data-ttu-id="fb6a4-342">Microsoft 信任中心</span><span class="sxs-lookup"><span data-stu-id="fb6a4-342">Microsoft Trust Center</span></span>](https://www.microsoft.com/trust-center/privacy/gdpr-overview)
