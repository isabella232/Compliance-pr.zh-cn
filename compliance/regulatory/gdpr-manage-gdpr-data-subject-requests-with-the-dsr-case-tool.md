---
title: 在安全与合规中心内使用 DSR 案例工具管理 GDPR 数据主体请求。
description: 了解如何使用 DSR 案例工具管理《欧盟一般数据保护条例》(GDPR) 数据主体请求。
f1.keywords:
- NOCSH
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- SPO_Content
- MS-Compliance
ms.assetid: ce9eb942-3589-42cb-88fd-1576ecb09c5c
ms.custom: seo-marvel-apr2020
hideEdit: true
ms.openlocfilehash: 8448d9a77352491ce0066dbf74ed5aea0e8f7a29
ms.sourcegitcommit: fb379d1110a9a86c7f9bab8c484dc3f4b3dfd6f0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/23/2021
ms.locfileid: "53089575"
---
# <a name="manage-gdpr-data-subject-requests-with-the-dsr-case-tool-in-the-security--compliance-center"></a><span data-ttu-id="dc17d-103">在安全与合规中心内使用 DSR 案例工具管理 GDPR 数据主体请求。</span><span class="sxs-lookup"><span data-stu-id="dc17d-103">Manage GDPR data subject requests with the DSR case tool in the Security & Compliance Center</span></span>

<span data-ttu-id="dc17d-104">《欧盟一般数据保护条例》(GDPR) 旨在保护和授予欧盟境内的个人隐私权。</span><span class="sxs-lookup"><span data-stu-id="dc17d-104">The EU General Data Protection Regulation (GDPR) is about protecting and enabling individuals' privacy rights inside the European Union (EU).</span></span> <span data-ttu-id="dc17d-105">GDPR 使欧盟的个人（称为数据主体）有权访问、检索、更正、清除和限制其个人数据的处理。</span><span class="sxs-lookup"><span data-stu-id="dc17d-105">The GDPR gives individuals in the European Union (known as data subjects) the right to access, retrieve, correct, erase, and restrict processing of their personal data.</span></span> <span data-ttu-id="dc17d-106">按照 GDPR 的规定，个人数据是指已确定身份或可确定身份的自然人的任何相关信息。</span><span class="sxs-lookup"><span data-stu-id="dc17d-106">Under the GDPR, personal data means any information relating to an identified or identifiable natural person.</span></span> <span data-ttu-id="dc17d-107">个人向其组织发出的对其个人数据执行操作的正式请求，称为数据主体请求 (DSR)。</span><span class="sxs-lookup"><span data-stu-id="dc17d-107">A formal request by a person to their organization to take an action on their personal data is called a Data Subject Request or DSR.</span></span> <span data-ttu-id="dc17d-108">有关在 Office 365 中响应数据的 DSR 的详细信息，请参阅《[Office 365 数据主体请求指南](https://go.microsoft.com/fwlink/?linkid=871169 )》。</span><span class="sxs-lookup"><span data-stu-id="dc17d-108">For detailed information about responding to DSRs for data in Office 365, see [Office 365 Data Subject Request Guide](https://go.microsoft.com/fwlink/?linkid=871169 ).</span></span>
  
<span data-ttu-id="dc17d-109">若要管理调查以响应组织中人员提交的 DSR，可以使用安全与合规中心中的 DSR 案例工具查找存储在以下位置的内容：</span><span class="sxs-lookup"><span data-stu-id="dc17d-109">To manage investigations in response to a DSR submitted by a person in your organization, you can use the DSR case tool in the Security & Compliance Center to find content stored in:</span></span>
  
- <span data-ttu-id="dc17d-110">组织中的任何用户邮箱。</span><span class="sxs-lookup"><span data-stu-id="dc17d-110">Any user mailbox in your organization.</span></span> <span data-ttu-id="dc17d-111">这包括 Microsoft Teams 中的 Skype for Business 对话和一对一聊天</span><span class="sxs-lookup"><span data-stu-id="dc17d-111">This includes Skype for Business conversations and one-to-one chats in Microsoft Teams</span></span>
    
- <span data-ttu-id="dc17d-112">与 Microsoft 365 组关联的所有邮箱以及 Microsoft Teams 中的所有团队邮箱</span><span class="sxs-lookup"><span data-stu-id="dc17d-112">All mailboxes associated with an Microsoft 365 Group and all team mailboxes in Microsoft Teams</span></span>
    
- <span data-ttu-id="dc17d-113">组织中的所有 SharePoint Online 网站和 OneDrive for Business 帐户</span><span class="sxs-lookup"><span data-stu-id="dc17d-113">All SharePoint Online sites and OneDrive for Business accounts in your organization</span></span>
    
- <span data-ttu-id="dc17d-114">组织中的所有 Microsoft Teams 网站和 Microsoft 365 组网站</span><span class="sxs-lookup"><span data-stu-id="dc17d-114">All Teams sites and Microsoft 365 Group sites in your organization</span></span>
    
- <span data-ttu-id="dc17d-115">Exchange Online 中的所有公用文件夹</span><span class="sxs-lookup"><span data-stu-id="dc17d-115">All public folders in Exchange Online</span></span>
    
<span data-ttu-id="dc17d-116">你可以使用 DSR 案例工具：</span><span class="sxs-lookup"><span data-stu-id="dc17d-116">Using the DSR case tool you can:</span></span>
  
- <span data-ttu-id="dc17d-117">为每个 DSR 调查创建单独的案例。</span><span class="sxs-lookup"><span data-stu-id="dc17d-117">Create a separate case for each DSR investigation.</span></span>
    
- <span data-ttu-id="dc17d-118">通过将人员添加为例成员，控制有权访问案例的人员；只有成员才能访问 DSR 案例，并在安全与合规中心的“**DSR 案例**”页面上查看其在案例列表中的案例。</span><span class="sxs-lookup"><span data-stu-id="dc17d-118">Control who has access to the DSR case by adding people as members of the case; only members can access the case and can only see their cases in the list of cases on the **DSR cases** page in the Security & Compliance Center.</span></span> <span data-ttu-id="dc17d-119">此外，可为同一案例的不同成员分配不同的权限。</span><span class="sxs-lookup"><span data-stu-id="dc17d-119">Also, you can assign different permissions to different members of the same case.</span></span> <span data-ttu-id="dc17d-120">例如，可以只允许一些成员查看案例和搜索结果，而允许其他成员创建搜索和导出搜索结果。</span><span class="sxs-lookup"><span data-stu-id="dc17d-120">For example, you can allow some members to only view the case and search results and allow other members to create searches and export search results.</span></span> 
    
- <span data-ttu-id="dc17d-121">使用内置搜索查询搜索与特定数据主体创建或上传的所有内容。</span><span class="sxs-lookup"><span data-stu-id="dc17d-121">Use the built-in search to search for all content created or uploaded by a specific data subject.</span></span>
    
- <span data-ttu-id="dc17d-122">还可以修改内置搜索查询并重新运行搜索，以缩小搜索结果的范围。</span><span class="sxs-lookup"><span data-stu-id="dc17d-122">Optionally revise the built-in search query and rerun the search to narrow the search results.</span></span>
    
- <span data-ttu-id="dc17d-123">添加与 DSR 案例关联的其他内容搜索。</span><span class="sxs-lookup"><span data-stu-id="dc17d-123">Add other content searches associated with the DSR case.</span></span> <span data-ttu-id="dc17d-124">这包括创建从 Office 漫游服务返回部分索引项和系统生成的日志的搜索。</span><span class="sxs-lookup"><span data-stu-id="dc17d-124">This includes creating searches that return partially indexed items and system-generated logs from the Office Roaming Service.</span></span>
    
- <span data-ttu-id="dc17d-125">导出数据以响应 DSR 访问或导出请求。</span><span class="sxs-lookup"><span data-stu-id="dc17d-125">Export data in response to a DSR access or export request.</span></span>
    
- <span data-ttu-id="dc17d-p105">在 DSR 调查过程完成时删除案例集。这会删除所有搜索，并导出与案例集关联的作业。</span><span class="sxs-lookup"><span data-stu-id="dc17d-p105">Delete cases when the DSR investigation process is complete. This removes all searches and export jobs associated with the case.</span></span>
    
<span data-ttu-id="dc17d-128">以下是使用 DSR 案例工具管理 DSR 调查的高级流程：</span><span class="sxs-lookup"><span data-stu-id="dc17d-128">Here's the high-level process for using the DSR case tool to manage DSR investigations:</span></span>
  
[<span data-ttu-id="dc17d-129">步骤 1：向潜在案例成员分配电子数据展示权限</span><span class="sxs-lookup"><span data-stu-id="dc17d-129">Step 1: Assign eDiscovery permissions to potential case members</span></span>](#step-1-assign-ediscovery-permissions-to-potential-case-members)

[<span data-ttu-id="dc17d-130">步骤 2：创建 DSR 案例并添加成员</span><span class="sxs-lookup"><span data-stu-id="dc17d-130">Step 2: Create a DSR case and add members</span></span>](#step-2-create-a-dsr-case-and-add-members)

[<span data-ttu-id="dc17d-131">步骤 3：运行搜索查询</span><span class="sxs-lookup"><span data-stu-id="dc17d-131">Step 3: Run the search query</span></span>](#step-3-run-the-search-query)

[<span data-ttu-id="dc17d-132">步骤 4：导出数据</span><span class="sxs-lookup"><span data-stu-id="dc17d-132">Step 4: Export the data</span></span>](#step-4-export-the-data)

[<span data-ttu-id="dc17d-133">（可选）步骤 5：修改内置搜索查询</span><span class="sxs-lookup"><span data-stu-id="dc17d-133">(Optional) Step 5: Revise the built-in search query</span></span>](#optional-step-5-revise-the-built-in-search-query)

[<span data-ttu-id="dc17d-134">有关使用 DSR 案例工具的详细信息</span><span class="sxs-lookup"><span data-stu-id="dc17d-134">More information about using the DSR case tool</span></span>](#more-information-about-using-the-dsr-case-tool)
  
> [!IMPORTANT]
> <span data-ttu-id="dc17d-135">我们的工具允许管理员利用 DSR 案例工具中找到的内置搜索和导出功能，帮助他们执行 DSR 访问或导出请求。</span><span class="sxs-lookup"><span data-stu-id="dc17d-135">Our tools can help admins perform DSR access or export requests by enabling them to utilize the built-in search and export functionality found in the DSR case tool.</span></span> <span data-ttu-id="dc17d-136">该工具可助你尽最大努力地导出与数据主体提交的 DSR 请求相关的数据。</span><span class="sxs-lookup"><span data-stu-id="dc17d-136">The tool helps to facilitate a best-effort method to export data that's relevant to a DSR request submitted by a data subject.</span></span> <span data-ttu-id="dc17d-137">但是，请务必注意，搜索结果可能因数据主体或管理员操作而异，这些操作可能会影响项目是否被视为可供导出的“个人数据”。</span><span class="sxs-lookup"><span data-stu-id="dc17d-137">However, it's important to note that search results can vary based on the data subject or the admin actions taken that may impact whether or not an item would be deemed as "personal data" for export purposes.</span></span> <span data-ttu-id="dc17d-138">例如，如果数据主体是最后一个修改并非他们本人创建的文件的人员，则搜索结果中可能不会返回该文件。</span><span class="sxs-lookup"><span data-stu-id="dc17d-138">For example, if the data subject was the last person to modify a file they didn't create, the file might not be returned in the search results.</span></span> <span data-ttu-id="dc17d-139">同样，管理员可以导出数据，而不包含部分索引项或所有版本的 SharePoint 文档。</span><span class="sxs-lookup"><span data-stu-id="dc17d-139">Similarly, an admin could export data without including partially indexed items or all versions of SharePoint documents.</span></span> <span data-ttu-id="dc17d-140">因此，提供的工具有助于访问和导出数据请求；但是，结果受具体的管理员和数据主体使用方案的约束。</span><span class="sxs-lookup"><span data-stu-id="dc17d-140">Therefore, the tools provided can help facilitate accessing and exporting data requests; however, the results are subject to specific admin and data subject usage scenarios.</span></span> 
  
## <a name="step-1-assign-ediscovery-permissions-to-potential-case-members"></a><span data-ttu-id="dc17d-141">步骤 1：向潜在案例成员分配电子数据展示权限</span><span class="sxs-lookup"><span data-stu-id="dc17d-141">Step 1: Assign eDiscovery permissions to potential case members</span></span>

<span data-ttu-id="dc17d-142">默认情况下，全局管理员可以访问安全与合规中心中的 DSR 案例工具。</span><span class="sxs-lookup"><span data-stu-id="dc17d-142">By default, a global administrator can access the DSR case tool in the Security & Compliance Center.</span></span> <span data-ttu-id="dc17d-143">根据设计，其他用户（如数据隐私官、人力资源经理或参与 DSR 调查的其他人员）无权访问 DSR 案例工具，并且必须分配适当的权限才能访问该工具。</span><span class="sxs-lookup"><span data-stu-id="dc17d-143">By design, other users such as a data privacy officer, a human resources manager, or other people involved in DSR investigations don't have access to the DSR case tool and will have to be assigned the appropriate permissions to access the tool.</span></span> <span data-ttu-id="dc17d-144">最简单的方法是前往安全与合规中心的“**权限**”页面，并将用户添加到“电子数据展示管理器”角色组。</span><span class="sxs-lookup"><span data-stu-id="dc17d-144">The easiest way to do this is to go to the **Permissions** page in the Security & Compliance Center and add users to the eDiscovery Manager role group.</span></span> <span data-ttu-id="dc17d-145">你还必须分配这些权限，以便可以将其添加为在步骤 2 中创建的 DSR 案例的成员。</span><span class="sxs-lookup"><span data-stu-id="dc17d-145">You also have to assign these permissions so you can add them as members of the DSR case that you create in Step 2.</span></span> 
  
<span data-ttu-id="dc17d-146">如需了解分步说明，请参阅[分配 Office 365 安全与合规中心中的电子数据展示权限](/microsoft-365/compliance/assign-ediscovery-permissions)。</span><span class="sxs-lookup"><span data-stu-id="dc17d-146">For step-by-step instructions, see [Assign eDiscovery permissions in the Office‍ 365 Security & Compliance Center](/microsoft-365/compliance/assign-ediscovery-permissions).</span></span>
  
> [!NOTE]
> <span data-ttu-id="dc17d-147">默认情况下，全局管理员（或安全与合规中心中组织管理角色组的其他成员，没有导出内容搜索结果必需的权限（请参阅本文中的步骤 4）。</span><span class="sxs-lookup"><span data-stu-id="dc17d-147">By default, a global administrator (or other members of the Organization Management role group in the Security & Compliance Center don't have the necessary permissions to export Content Search results (see Step 4 in this article).</span></span> <span data-ttu-id="dc17d-148">若要解决此问题，管理员可以将自己添加为电子数据展示管理器角色组的成员。</span><span class="sxs-lookup"><span data-stu-id="dc17d-148">To address this, an admin can add themselves as a member of the eDiscovery Manager role group.</span></span> 
  
## <a name="step-2-create-a-dsr-case-and-add-members"></a><span data-ttu-id="dc17d-149">步骤 2：创建 DSR 案例并添加成员</span><span class="sxs-lookup"><span data-stu-id="dc17d-149">Step 2: Create a DSR case and add members</span></span>

<span data-ttu-id="dc17d-150">下一步是创建 DSR 案例。</span><span class="sxs-lookup"><span data-stu-id="dc17d-150">The next step is to create a DSR case.</span></span> <span data-ttu-id="dc17d-151">创建案例时，可以选择启动内置搜索，也可以在不启动搜索的情况下创建案例。</span><span class="sxs-lookup"><span data-stu-id="dc17d-151">When you create a case, you can choose to start the built-in search or you can create the case without starting the search.</span></span> <span data-ttu-id="dc17d-152">以下过程介绍了在不启动搜索的情况下创建案例，然后向你演示了如何向案例添加成员。</span><span class="sxs-lookup"><span data-stu-id="dc17d-152">The following procedure instructs you to create the case without starting the search and then show you how to add members to the case.</span></span>
  
1. <span data-ttu-id="dc17d-153">转到 [https://protection.office.com](https://protection.office.com)，使用工作或学校帐户登录。</span><span class="sxs-lookup"><span data-stu-id="dc17d-153">Go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account.</span></span> 
    
2. <span data-ttu-id="dc17d-154">在安全与合规中心中，点击“**数据隐私** \> **数据主体请求**”，然后点击![“添加”图标](../media/ITPro-EAC-AddIcon.gif) **新建 DSR 案例**。</span><span class="sxs-lookup"><span data-stu-id="dc17d-154">In the Security & Compliance Center, click **Data privacy** \> **Data subject requests**, and then click ![Add Icon](../media/ITPro-EAC-AddIcon.gif) **New DSR case**.</span></span>
    
3. <span data-ttu-id="dc17d-155">在“**新建 DSR 案例**”浮出页面上，指定案例名称，键入可选说明，然后点击“**下一步**”。</span><span class="sxs-lookup"><span data-stu-id="dc17d-155">On the **New DSR case** flyout page, give the case a name, type an optional description, and then click **Next**.</span></span> <span data-ttu-id="dc17d-156">案例名称在你的组织中必须保持唯一。</span><span class="sxs-lookup"><span data-stu-id="dc17d-156">The name of the case must be unique in your organization.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="dc17d-157">请考虑在新案例的名称和/或说明中添加提交你正在调查的 DSR 请求的人员的姓名。</span><span class="sxs-lookup"><span data-stu-id="dc17d-157">Consider adding the name of the person who submitted the DSR request that you're investigating in the name and/or description of the new case.</span></span> <span data-ttu-id="dc17d-158">请注意，只有本案例的成员（和电子数据展示管理员）才能在 **数据主体请求** 页面上的案例列表中看到此案例。</span><span class="sxs-lookup"><span data-stu-id="dc17d-158">Note that only members of this case (and eDiscovery Administrators) will be able to see the case in the list of cases on the **Data subject requests** page.</span></span> 
  
4. <span data-ttu-id="dc17d-159">在“**请求详细信息**”页面上，“**数据主题（提交此请求的人员）**”下方，选择要查找和导出其数据的人员，然后点击“**下一步**”。</span><span class="sxs-lookup"><span data-stu-id="dc17d-159">On the **Request details** page, under **Data subject (the person who filed this request)**, select the person that you want to find and export data for and then click **Next**.</span></span>
    
5. <span data-ttu-id="dc17d-160">在“**确认案例设置**”页面上，可以更改案例名称和说明，并选择其他数据主体。</span><span class="sxs-lookup"><span data-stu-id="dc17d-160">On the **Confirm your case settings** page, you can change the case name and description, and select a different data subject.</span></span> <span data-ttu-id="dc17d-161">如果不需要更改，请点击“**下一步**”。</span><span class="sxs-lookup"><span data-stu-id="dc17d-161">Otherwise, click **Save**.</span></span>
    
    <span data-ttu-id="dc17d-162">将会显示一个页面，确认已创建新的 DSR 案例。</span><span class="sxs-lookup"><span data-stu-id="dc17d-162">A page is displayed that confirms the new DSR case has been created.</span></span>
    
    ![开始搜索或关闭“新建 DSR 案例”页面](../media/b5e62c2c-cafe-4a8d-a38c-789ed9f9ccbd.png)
  
    <span data-ttu-id="dc17d-164">此时，你可以执行以下两项操作中的一项：</span><span class="sxs-lookup"><span data-stu-id="dc17d-164">At this point, you can do one of two things:</span></span>
    
    <span data-ttu-id="dc17d-165">a.</span><span class="sxs-lookup"><span data-stu-id="dc17d-165">a.</span></span> <span data-ttu-id="dc17d-166">点击“**显示搜索结果**”，启动搜索。</span><span class="sxs-lookup"><span data-stu-id="dc17d-166">Clicking **Show me search results** starts the search.</span></span> <span data-ttu-id="dc17d-167">此为默认选项。</span><span class="sxs-lookup"><span data-stu-id="dc17d-167">This is the default selection.</span></span> <span data-ttu-id="dc17d-168">步骤 3 中会介绍选择此选项时行的内置搜索，以及返回的结果。</span><span class="sxs-lookup"><span data-stu-id="dc17d-168">The built-in search that's run when you select this option and the results that are returned are discussed in Step 3.</span></span>
    
    <span data-ttu-id="dc17d-169">b.</span><span class="sxs-lookup"><span data-stu-id="dc17d-169">b.</span></span> <span data-ttu-id="dc17d-170">点击“**完成**”，在不启动内置搜索的情况下关闭新的 DSR 案例。</span><span class="sxs-lookup"><span data-stu-id="dc17d-170">Clicking **Finish** closes the new DSR case without starting the built-in search.</span></span> <span data-ttu-id="dc17d-171">选择此选项时，新的 DSR 案例将显示在“**数据主体请求**”页面上。</span><span class="sxs-lookup"><span data-stu-id="dc17d-171">When you select this option, the new DSR case is displayed on the **Data subject requests** page.</span></span>
    
6. <span data-ttu-id="dc17d-172">点击“**完成**”，以便可以转到新的 DSR 案例并向其添加成员。</span><span class="sxs-lookup"><span data-stu-id="dc17d-172">Click **Finish** so that you can go in to the new DSR case and add members to it.</span></span> 
    
7. <span data-ttu-id="dc17d-173">在“**数据主体请求** 页面上，点击创建的 DSR 案例的名称。</span><span class="sxs-lookup"><span data-stu-id="dc17d-173">On the **Data subject requests** page, click the name of the DSR case that you created.</span></span> 
    
8. <span data-ttu-id="dc17d-174">在”**管理此案例**“浮出页面上，“**管理成员**”下方，点击“**添加**”。</span><span class="sxs-lookup"><span data-stu-id="dc17d-174">On the **Manage this case** flyout page, under **Manage members**, click **Add**.</span></span> 
    
    <span data-ttu-id="dc17d-175">在“**用户**”下方，将显示分配了相应电子数据展示权限的人员列表。</span><span class="sxs-lookup"><span data-stu-id="dc17d-175">Under **Users**, a list of people that are assigned the appropriate eDiscovery permissions is displayed.</span></span> <span data-ttu-id="dc17d-176">在步骤 1 中分配了电子数据展示权限的人员，将会显示在此列表中。</span><span class="sxs-lookup"><span data-stu-id="dc17d-176">The people you assigned eDiscovery permissions to in Step 1 will be displayed in this list.</span></span> 
    
9. <span data-ttu-id="dc17d-177">选择要添加为 DSR 案例成员的人员，点击“**添加**”，然后保存更改。</span><span class="sxs-lookup"><span data-stu-id="dc17d-177">Select the people to add as members of the DSR case, click **Add**, and then save your changes.</span></span>
    
    <span data-ttu-id="dc17d-178">还可以将角色组添加为 DSR 案例成员，方法是点击“**管理角色组**”下的”**添加**”。</span><span class="sxs-lookup"><span data-stu-id="dc17d-178">You can also add role groups as members of DSR case by clicking **Add** under **Manage role groups**.</span></span> 
    
## <a name="step-3-run-the-search-query"></a><span data-ttu-id="dc17d-179">步骤 3：运行搜索查询</span><span class="sxs-lookup"><span data-stu-id="dc17d-179">Step 3: Run the search query</span></span>

<span data-ttu-id="dc17d-180">创建 DSR 案例并添加成员后，下一步是运行与案例关联的内置搜索。</span><span class="sxs-lookup"><span data-stu-id="dc17d-180">After you create a DSR case and add members, the next step is to run the built-in search that's associated with the case.</span></span> <span data-ttu-id="dc17d-181">此默认搜索查询会执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="dc17d-181">This default search query does the following things:</span></span>
  
- <span data-ttu-id="dc17d-182">在组织中的所有邮箱中，搜索数据主体发送或接收的所有电子邮件项目。</span><span class="sxs-lookup"><span data-stu-id="dc17d-182">Searches all mailboxes in your organization for all email items that were sent or received by the data subject.</span></span> <span data-ttu-id="dc17d-183">这是通过使用  *参与者*  电子邮件属性来实现的，该属性会搜索电子邮件消息中，所有人员字段中的数据主体。</span><span class="sxs-lookup"><span data-stu-id="dc17d-183">This is accomplished by using the  *Participants*  email property, which searches for the data subject in all the people fields in an email message.</span></span> <span data-ttu-id="dc17d-184">该属性会返回 **发件人**、**收件人**、**抄送** 和 **密件抄送** 字段中包含数据主体的项目。</span><span class="sxs-lookup"><span data-stu-id="dc17d-184">This property returns items in which the data subject is in the **From**, **To**, **CC**, and **BCC** fields.</span></span> <span data-ttu-id="dc17d-185">Exchange Online 中的公用文件夹也会搜索数据主体发送或接收的邮件。</span><span class="sxs-lookup"><span data-stu-id="dc17d-185">Public folders in Exchange Online are also searched for messages sent or received by the data subject.</span></span> 
    
- <span data-ttu-id="dc17d-186">在组织中的所有站点中，搜索数据主体创建或上传的文档和项目。</span><span class="sxs-lookup"><span data-stu-id="dc17d-186">Searches all sites in your organization for documents and items created or uploaded by the data subject.</span></span> <span data-ttu-id="dc17d-187">这是通过使用下列站点属性实现的：</span><span class="sxs-lookup"><span data-stu-id="dc17d-187">This is accomplished by using the following site properties:</span></span>
    
  - <span data-ttu-id="dc17d-188">“*作者*”属性返回数据主体在 Office 文档的作者字段中列出的项。</span><span class="sxs-lookup"><span data-stu-id="dc17d-188">The  *Author*  property returns items where the data subject is listed in the author field in Office documents.</span></span> <span data-ttu-id="dc17d-189">即使文档由其他人复制和上传，该值仍会保留。</span><span class="sxs-lookup"><span data-stu-id="dc17d-189">This value persists, even if the document is copied and uploaded by someone else.</span></span> 
    
  - <span data-ttu-id="dc17d-190">“*创建者*”属性返回数据主体创建或上传的项。</span><span class="sxs-lookup"><span data-stu-id="dc17d-190">The  *CreatedBy*  property returns items that were created or uploaded by the data subject.</span></span> 
    
<span data-ttu-id="dc17d-191">下面是创建 DSR 案例时自动创建的内置搜索的关键字查询。</span><span class="sxs-lookup"><span data-stu-id="dc17d-191">Here's what the keyword query looks like for the built-in search that gets automatically created when you create a DSR case.</span></span>
  
```powershell
participants:"<email address>" OR author:"<display name>" OR createdby:"<display name>"
```

<span data-ttu-id="dc17d-192">例如，如果数据主体的姓名是 Ina Leonte，则关键字查询如下所示：</span><span class="sxs-lookup"><span data-stu-id="dc17d-192">For example, if the name of the data subject is Ina Leonte, the keyword query would look like this:</span></span>
  
```powershell
participants:"ina@contoso.com" OR author:"Ina Leonte" OR createdby:"Ina Leonte"
```

 <span data-ttu-id="dc17d-193">**要运行 DSR 案例的内置搜索，请执行以下操作：**</span><span class="sxs-lookup"><span data-stu-id="dc17d-193">**To run the built-in search for a DSR case:**</span></span>
  
1. <span data-ttu-id="dc17d-194">在安全与合规中心中，点击“**数据隐私** \> **数据主体请求**”，然后点击在步骤 2 中创建的 DSR 案例旁边的“**打开**”。</span><span class="sxs-lookup"><span data-stu-id="dc17d-194">In the Security & Compliance Center, click **Data privacy** \> **Data subject requests**, and then click **Open** next to the DSR case that you created in Step 2.</span></span> 
    
    <span data-ttu-id="dc17d-195">点击页面顶部的“**搜索**”选项卡，然后点击创建 DSR 案例时创建的内置搜索旁边的复选框。</span><span class="sxs-lookup"><span data-stu-id="dc17d-195">Click the **Search** tab at the top of the page, and then click the checkbox next to the built-in search that was created when you created the DSR case.</span></span> <span data-ttu-id="dc17d-196">搜索的名称与 DSR 案例相同。</span><span class="sxs-lookup"><span data-stu-id="dc17d-196">The search has the same name as the DSR case.</span></span> 
    
2. <span data-ttu-id="dc17d-197">在搜索浮出页面上，点击“**打开查询**”。</span><span class="sxs-lookup"><span data-stu-id="dc17d-197">In the search flyout page, click **Open query**.</span></span>
    
    <span data-ttu-id="dc17d-198">打开查询后，便会开始搜索，并很快完成。</span><span class="sxs-lookup"><span data-stu-id="dc17d-198">When you open the query, the search is started and will complete in a few moments.</span></span> 
    
3. <span data-ttu-id="dc17d-199">搜索完成后，点击“**预览结果**”预览搜索结果。</span><span class="sxs-lookup"><span data-stu-id="dc17d-199">When the search is complete, click **Preview results** to preview the search results.</span></span> <span data-ttu-id="dc17d-200">有关详细信息，请参阅[预览搜索结果](/microsoft-365/compliance/content-search#preview-search-results)。</span><span class="sxs-lookup"><span data-stu-id="dc17d-200">For more information, see [Preview search results](/microsoft-365/compliance/content-search#preview-search-results).</span></span>
    
    > [!TIP]
    > <span data-ttu-id="dc17d-201">还可以查看搜索查询统计信息，以查看搜索返回的邮箱和网站项数量，以及包含与搜索查询匹配的项目的主要内容位置。</span><span class="sxs-lookup"><span data-stu-id="dc17d-201">You can also view the search query statistics to see the number of mailbox and site items that are returned by the search, and the top content locations that contain items that match the search query.</span></span> <span data-ttu-id="dc17d-202">有关详细信息，请参阅[查看与搜索相关的信息和统计信息](/microsoft-365/compliance/content-search#view-information-and-statistics-about-a-search)。</span><span class="sxs-lookup"><span data-stu-id="dc17d-202">For more information, see [View information and statistics about a search](/microsoft-365/compliance/content-search#view-information-and-statistics-about-a-search).</span></span> 
  
<span data-ttu-id="dc17d-203">可以编辑内置搜索查询，更改搜索的内容位置，然后重新运行搜索。</span><span class="sxs-lookup"><span data-stu-id="dc17d-203">You can edit the built-in search query, change the content locations that are searched, and then rerun the search.</span></span> <span data-ttu-id="dc17d-204">请参阅[步骤 5](#optional-step-5-revise-the-built-in-search-query) 以了解更多信息。</span><span class="sxs-lookup"><span data-stu-id="dc17d-204">See [Step 5](#optional-step-5-revise-the-built-in-search-query) for more information.</span></span> 
  
## <a name="step-4-export-the-data"></a><span data-ttu-id="dc17d-205">步骤 4：导出数据</span><span class="sxs-lookup"><span data-stu-id="dc17d-205">Step 4: Export the data</span></span>

<span data-ttu-id="dc17d-206">运行内置搜索后，可以导出搜索结果。</span><span class="sxs-lookup"><span data-stu-id="dc17d-206">After you run the built-in search, you can export the search results.</span></span> <span data-ttu-id="dc17d-207">或者，在导出数据之前，修改查询以减少搜索结果数量。</span><span class="sxs-lookup"><span data-stu-id="dc17d-207">Alternatively, before you export the data, you may want to revise the query to reduce the number of search results.</span></span> <span data-ttu-id="dc17d-208">有关缩小搜索结果范围的详细信息，请参阅步骤 5。</span><span class="sxs-lookup"><span data-stu-id="dc17d-208">See Step 5 for more information about narrowing the search results.</span></span>
  
<span data-ttu-id="dc17d-209">导出搜索结果时，可将邮箱项目下载为 PST 文件或单独的邮件。</span><span class="sxs-lookup"><span data-stu-id="dc17d-209">When you export search results, mailbox items can be downloaded in PST files or as individual messages.</span></span> <span data-ttu-id="dc17d-210">当你从 SharePoint 和 OneDrive 帐户导出内容时，将导出本地 Office 文档副本。</span><span class="sxs-lookup"><span data-stu-id="dc17d-210">When you export content from SharePoint and OneDrive accounts, copies of native Office documents and other documents are exported.</span></span> <span data-ttu-id="dc17d-211">搜索结果中包含一个包含与每个导出项有关信息的结果文件。</span><span class="sxs-lookup"><span data-stu-id="dc17d-211">A results file that contains information about every exported item is included with the search results.</span></span> <span data-ttu-id="dc17d-212">有关导出的更多详细信息，请参阅[导出内容搜索结果](/microsoft-365/compliance/export-search-results)。</span><span class="sxs-lookup"><span data-stu-id="dc17d-212">For more detailed information about exporting, see [Export Content Search results](/microsoft-365/compliance/export-search-results).</span></span>
  
> [!NOTE]
> <span data-ttu-id="dc17d-213">默认情况下，全局管理员（或安全与合规中心中组织管理角色组的其他成员）没有导出内容搜索结果必需的权限。</span><span class="sxs-lookup"><span data-stu-id="dc17d-213">By default, a global administrator (or other members of the Organization Management role group in the Security & Compliance Center) don't have the necessary permissions to export Content Search results.</span></span> <span data-ttu-id="dc17d-214">若要解决此问题，管理员可以将自己添加为电子数据展示管理器角色组的成员。</span><span class="sxs-lookup"><span data-stu-id="dc17d-214">To address this, an admin can add themselves as a member of the eDiscovery Manager role group.</span></span> 
  
<span data-ttu-id="dc17d-215">用于导出数据的计算机须满足下列系统要求：</span><span class="sxs-lookup"><span data-stu-id="dc17d-215">The computer you use to export data has to meet the following system requirements:</span></span>
  
- <span data-ttu-id="dc17d-216">32 位或 64 位版本的 Windows 7 和更高版本</span><span class="sxs-lookup"><span data-stu-id="dc17d-216">32-bit or 64-bit versions of Windows 7 and later versions</span></span>
    
- <span data-ttu-id="dc17d-217">Microsoft .NET Framework 4.7</span><span class="sxs-lookup"><span data-stu-id="dc17d-217">Microsoft .NET Framework 4.7</span></span>
    
- <span data-ttu-id="dc17d-218">支持的浏览器：</span><span class="sxs-lookup"><span data-stu-id="dc17d-218">A supported browser:</span></span>
    
  - <span data-ttu-id="dc17d-219">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="dc17d-219">Microsoft Edge</span></span>
    
    <span data-ttu-id="dc17d-220">或</span><span class="sxs-lookup"><span data-stu-id="dc17d-220">Or</span></span>
    
  - <span data-ttu-id="dc17d-221">Microsoft Internet Explorer 10 和更高版本</span><span class="sxs-lookup"><span data-stu-id="dc17d-221">Microsoft Internet Explorer 10 and later versions</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="dc17d-222">Microsoft 不开发面向 ClickOnce 应用程序的第三方扩展或加载项。</span><span class="sxs-lookup"><span data-stu-id="dc17d-222">Microsoft doesn't manufacture third-party extensions or add-ons for ClickOnce applications.</span></span> <span data-ttu-id="dc17d-223">不支持使用具有第三方扩展或加载项的浏览器导出数据。</span><span class="sxs-lookup"><span data-stu-id="dc17d-223">Exporting data using an unsupported browser with third-party extensions or add-ons isn't supported.</span></span> 
  
 <span data-ttu-id="dc17d-224">**若要从 DSR 案例中的内置搜索导出数据，请执行以下操作：**</span><span class="sxs-lookup"><span data-stu-id="dc17d-224">**To export data from the built-in search in a DSR case:**</span></span>
  
1. <span data-ttu-id="dc17d-225">在安全与合规中心中，点击“**数据隐私** \> **数据主体请求**”，然后点击想要从中导出数据的 DSR 案例旁边的“**打开**”。</span><span class="sxs-lookup"><span data-stu-id="dc17d-225">In the Security & Compliance Center, click **Data privacy** \> **Data subject requests**, and then click **Open** next to the DSR case that you want to export data from.</span></span> 
    
2. <span data-ttu-id="dc17d-226">点击页面顶部的“**搜索**”选项卡，然后点击创建 DSR 案例时创建的内置搜索旁边的复选框。</span><span class="sxs-lookup"><span data-stu-id="dc17d-226">Click the **Search** tab at the top of the page, and then click the checkbox next to the built-in search that was created when you created the DSR case.</span></span> <span data-ttu-id="dc17d-227">或者点击其他搜索，以从中导出数据。</span><span class="sxs-lookup"><span data-stu-id="dc17d-227">Or click another search to export data from that search.</span></span> 
    
3. <span data-ttu-id="dc17d-228">在搜索浮出页面上，单击“![导出搜索结果](../media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png)”图标“**更多**”，然后从下拉列表中选择“**导出结果**”。</span><span class="sxs-lookup"><span data-stu-id="dc17d-228">On the search flyout page, click ![Export search results icon](../media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **More**, and then select **Export results** from the drop-down list.</span></span> 
    
4. <span data-ttu-id="dc17d-229">在“**导出结果**”页面上，为 DSR 导出请求选择以下建议选项。</span><span class="sxs-lookup"><span data-stu-id="dc17d-229">On the **Export results** page, select the following recommended options for DSR export requests.</span></span> 
    
    ![配置导出设置](../media/25416b79-57da-46a1-ae07-e640602a8fa4.png)
  
    <span data-ttu-id="dc17d-231">a.</span><span class="sxs-lookup"><span data-stu-id="dc17d-231">a.</span></span> <span data-ttu-id="dc17d-232">在“**输出选项**”下方，选择第一个选项（**所有项（不包括具有无法识别格式的项）已加密，或由于其他原因未编制索引**）以仅导出已编制索引的项目。</span><span class="sxs-lookup"><span data-stu-id="dc17d-232">Under **Output options**, select the first option (**All items, excluding ones that have ones that have an unrecognized format, are encrypted, or weren't indexed for other reasons**) to export indexed items only.</span></span> <span data-ttu-id="dc17d-233">不建议从内置搜索中导出部分索引项的原因是，这样做会连同其他用户的已编入索引的部分项目一起导出。</span><span class="sxs-lookup"><span data-stu-id="dc17d-233">The reason you don't want to export partially indexed items from the built-in search is because partially indexed items from other users will also be exported.</span></span> <span data-ttu-id="dc17d-234">若要仅导出数据主体的部分索引项，建议创建单独的搜索。</span><span class="sxs-lookup"><span data-stu-id="dc17d-234">To export only the partially indexed items for the data subject, we recommend that you create a separate search.</span></span> <span data-ttu-id="dc17d-235">有关详细信息，请参阅“有关使用 DSR 案例工具的更多信息”部分的“[导出部分索引项](#exporting-partially-indexed-items)”。</span><span class="sxs-lookup"><span data-stu-id="dc17d-235">For more information, see [Exporting partially indexed items](#exporting-partially-indexed-items) in the "More information about using the DSR case tool" section.</span></span>
    
    <span data-ttu-id="dc17d-236">b.</span><span class="sxs-lookup"><span data-stu-id="dc17d-236">b.</span></span> <span data-ttu-id="dc17d-237">在“**将 Exchange 内容导出为** 下方，选择第三个选项，**包含单个文件夹中所有邮件的 One PST 文件**。</span><span class="sxs-lookup"><span data-stu-id="dc17d-237">Under **Export Exchange content as**, select the third option, **One PST file containing all messages in a single folder**.</span></span> <span data-ttu-id="dc17d-238">由于某些结果可能属于源自其他用户邮箱的项目，因此，此选项只列出单个文件夹中的项目，而不指示实际邮箱，并且是取消复制下一项中建议的结果时使用的最佳选项。</span><span class="sxs-lookup"><span data-stu-id="dc17d-238">Because some of the results may be for items that originated in another user's mailbox, this option just lists the item in a single folder without indicating the actual mailbox and is the best option to use when you de-duplicate the results as recommended in the next item.</span></span> <span data-ttu-id="dc17d-239">此选项还允许数据主体按时间顺序查看项目（按发送日期排序项目），而无需导航到每个项目的原始邮箱文件夹结构。</span><span class="sxs-lookup"><span data-stu-id="dc17d-239">This option also lets the data subject review items in chronological order (items are sorted by sent date) without having to navigate the original mailbox folder structure for each item.</span></span>
    
    <span data-ttu-id="dc17d-240">c.</span><span class="sxs-lookup"><span data-stu-id="dc17d-240">c.</span></span> <span data-ttu-id="dc17d-241">选择 **启用重复数据删除** 选项，以排除重复的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="dc17d-241">Select **Enable de-duplication** option to excludes duplicate email messages.</span></span> <span data-ttu-id="dc17d-242">我们建议使用此选项，因为内置搜索会搜索组织中的所有邮箱。</span><span class="sxs-lookup"><span data-stu-id="dc17d-242">We recommend this option because the built-in search searches all mailboxes in your organization.</span></span> <span data-ttu-id="dc17d-243">因此，如果在已搜索的邮箱中找到同一封邮件的多个副本，则此选项意味着将只导出邮件的一个副本。</span><span class="sxs-lookup"><span data-stu-id="dc17d-243">So if multiple copies of the same message are found in the mailboxes that were searched, this option means that only one copy of a message will be exported.</span></span> <span data-ttu-id="dc17d-244">此选项会一起导出单个文件夹中一个 PST 文件中的邮件，为 DSR 导出请求提供最佳用户体验。</span><span class="sxs-lookup"><span data-stu-id="dc17d-244">This option, together will exporting messages in one PST file in a single folder, results in the best user experience for DSR export requests.</span></span> <span data-ttu-id="dc17d-245">Results.csv 导出报表会列出发现重复邮件的所有位置。</span><span class="sxs-lookup"><span data-stu-id="dc17d-245">The Results.csv export report lists all locations where duplicate messages were found.</span></span>
    
    <span data-ttu-id="dc17d-246">也可以选择“**包含 SharePoint 文档的版本**”选项，以导出所有版本的 SharePoint 和 OneDrive 文档。</span><span class="sxs-lookup"><span data-stu-id="dc17d-246">Optionally, you can select **Include versions for SharePoint documents** option to export all versions of SharePoint and OneDrive documents.</span></span> <span data-ttu-id="dc17d-247">这要求为文档库启用版本控制。</span><span class="sxs-lookup"><span data-stu-id="dc17d-247">This requires that versioning is turned on for document libraries.</span></span> <span data-ttu-id="dc17d-248">此选项有助于确保导出所有相关数据。</span><span class="sxs-lookup"><span data-stu-id="dc17d-248">This option helps to ensure that all relevant data is exported.</span></span>
    
5. <span data-ttu-id="dc17d-249">选择导出设置后，点击“**导出**”。</span><span class="sxs-lookup"><span data-stu-id="dc17d-249">After you choose the export settings, click **Export**.</span></span>
    
    <span data-ttu-id="dc17d-250">搜索结果已准备下载是指它们被上传至 Microsoft 云中，你的组织的 Azure 存储区域。</span><span class="sxs-lookup"><span data-stu-id="dc17d-250">The search results are prepared for downloading, which means they're uploaded to the Azure Storage area for your organization in the Microsoft cloud.</span></span> <span data-ttu-id="dc17d-251">后续步骤将会介绍如何将此数据下载到本地计算机。</span><span class="sxs-lookup"><span data-stu-id="dc17d-251">The next steps show you how to download this data to your local computer.</span></span>
    
6. <span data-ttu-id="dc17d-252">点击“**导出**”选项卡以显示创建的导出作业。</span><span class="sxs-lookup"><span data-stu-id="dc17d-252">Click the **Export** tab to display the export job you created.</span></span> <span data-ttu-id="dc17d-253">导出作业的名称与搜索名称最后带有“**_Export**”的相应搜索相同。</span><span class="sxs-lookup"><span data-stu-id="dc17d-253">Export jobs have the same name as the corresponding search with **_Export** appended to the end of search name.</span></span> 
    
7. <span data-ttu-id="dc17d-254">点击刚刚创建的导出作业，以显示导出浮出页面。</span><span class="sxs-lookup"><span data-stu-id="dc17d-254">Click the export job that you just created to display the export flyout page.</span></span> <span data-ttu-id="dc17d-255">此页显示有关搜索的信息，例如要导出的项的大小和总数，以及已传输到 Azure 存储区域的项的百分比。</span><span class="sxs-lookup"><span data-stu-id="dc17d-255">This page shows information about the search, such as the size and total number of items to be exported, and the percentage of the items that have been transferred to an Azure storage area.</span></span> <span data-ttu-id="dc17d-256">点击“**刷新**”，更新上传状态信息。</span><span class="sxs-lookup"><span data-stu-id="dc17d-256">Click **Refresh** to update the upload status information.</span></span> 
    
8. <span data-ttu-id="dc17d-257">在“**导出密钥**”下，点击“**复制到剪贴板**”。</span><span class="sxs-lookup"><span data-stu-id="dc17d-257">Under **Export key**, click **Copy to clipboard**.</span></span> <span data-ttu-id="dc17d-258">在步骤 11 中，将使用此密钥下载搜索结果。</span><span class="sxs-lookup"><span data-stu-id="dc17d-258">You use this key in step 11 to download the search results.</span></span>
    
9. <span data-ttu-id="dc17d-259">点击导出浮出页面顶部的![导出搜索结果图标](../media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **下载结果**。</span><span class="sxs-lookup"><span data-stu-id="dc17d-259">Click ![Export search results icon](../media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **Download results** at the top of the export flyout page.</span></span> 
    
10. <span data-ttu-id="dc17d-260">在页面底部的弹出窗口中，点击“**打开**”以打开“**电子数据展示导出工具**”。</span><span class="sxs-lookup"><span data-stu-id="dc17d-260">In the pop-up window at the bottom of the page, click **Open** to open the **eDiscovery Export Tool**.</span></span> <span data-ttu-id="dc17d-261">如果是首次下载搜索结果，则会安装 **电子数据展示导出工具**。</span><span class="sxs-lookup"><span data-stu-id="dc17d-261">The **eDiscovery Export Tool** will be installed the first time you download search results.</span></span> 
    
11. <span data-ttu-id="dc17d-262">在“**电子数据展示导出工具**”中，将在步骤 8 中复制的导出密钥粘贴在相应的框中。</span><span class="sxs-lookup"><span data-stu-id="dc17d-262">In the **eDiscovery Export Tool**, paste the export key that you copied in step 8 in the appropriate box.</span></span>
    
12. <span data-ttu-id="dc17d-263">单击“**浏览**”指定要下载搜索结果文件的位置。</span><span class="sxs-lookup"><span data-stu-id="dc17d-263">Click **Browse** to specify the location where you want to download the search result files.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="dc17d-264">由于磁盘活动量很大（读取和写入），应将搜索结果下载到本地磁盘驱动器；勿将其载到映射的网络驱动器或其他网络位置。</span><span class="sxs-lookup"><span data-stu-id="dc17d-264">Due to the high amount of disk activity (reads and writes), you should download search results to a local disk drive; don't download them to a mapped network drive or other network location.</span></span> 
  
13. <span data-ttu-id="dc17d-265">单击“启动”将搜索结果下载到计算机。</span><span class="sxs-lookup"><span data-stu-id="dc17d-265">Click **Start** to download the search results to your computer.</span></span> 
    
    <span data-ttu-id="dc17d-266">**电子数据展示工具** 显示有关导出过程的状态信息，包括要下载的剩余项的估计数量（和大小）。</span><span class="sxs-lookup"><span data-stu-id="dc17d-266">The **eDiscovery Export Tool** displays status information about the export process, including an estimate of the number (and size) of the remaining items to be downloaded.</span></span> <span data-ttu-id="dc17d-267">导出过程完成后，你可以在文件下载的位置访问它们。</span><span class="sxs-lookup"><span data-stu-id="dc17d-267">When the export process is complete, you can access the files in the location where they were downloaded.</span></span> <span data-ttu-id="dc17d-268">有关下载内容搜索结果时包含的报告的详细信息，请参阅“导出内容搜索结果”中的“[更多信息](/microsoft-365/compliance/export-search-results#more-information)”。</span><span class="sxs-lookup"><span data-stu-id="dc17d-268">For more information about the reports that included when you download Content Search results, see the [More information](/microsoft-365/compliance/export-search-results#more-information) section in "Export Content Search results".</span></span> 
    
<span data-ttu-id="dc17d-269">导出数据后，搜索结果和导出报告位于与 DSR 案例同名的文件夹中。</span><span class="sxs-lookup"><span data-stu-id="dc17d-269">After the data is exported, the search results and export reports are located in a folder that has the same name as the DSR case.</span></span> <span data-ttu-id="dc17d-270">包含邮箱项的 PST 文件位于名为“**Exchange**”的子文件夹中。</span><span class="sxs-lookup"><span data-stu-id="dc17d-270">The PST files that contain mailbox items are located in a subfolder named **Exchange**.</span></span> <span data-ttu-id="dc17d-271">网站中的文档和其他项目位于名为“**SharePoint**”的子文件夹中。</span><span class="sxs-lookup"><span data-stu-id="dc17d-271">Documents and other items from sites are located in a subfolder named **SharePoint**.</span></span> 
  
## <a name="optional-step-5-revise-the-built-in-search-query"></a><span data-ttu-id="dc17d-272">（可选）步骤 5：修改内置搜索查询</span><span class="sxs-lookup"><span data-stu-id="dc17d-272">(Optional) Step 5: Revise the built-in search query</span></span>

<span data-ttu-id="dc17d-273">运行内置搜索后，可以对其进行修改以缩小范围，返回更少的搜索结果。</span><span class="sxs-lookup"><span data-stu-id="dc17d-273">After you run the built-in search, you can revise it to narrow the scope to return fewer search results.</span></span> <span data-ttu-id="dc17d-274">你可以添加向查询添加条件来实现。</span><span class="sxs-lookup"><span data-stu-id="dc17d-274">You can do this by adding conditions to the query.</span></span> <span data-ttu-id="dc17d-275">条件将通过 **AND** 运算符在逻辑上连接至关键字查询。</span><span class="sxs-lookup"><span data-stu-id="dc17d-275">A condition is logically connected to the keyword query by the **AND** operator.</span></span> <span data-ttu-id="dc17d-276">这意味着，项必须同时满足关键字查询和添加的所有条件，才能在搜索结果中返回。</span><span class="sxs-lookup"><span data-stu-id="dc17d-276">That means to be returned in the search results, items must satisfy both the keyword query and any conditions you add.</span></span> <span data-ttu-id="dc17d-277">这就是条件如何帮助缩小结果范围的原理。</span><span class="sxs-lookup"><span data-stu-id="dc17d-277">This is how conditions help to narrow the results.</span></span> <span data-ttu-id="dc17d-278">如果将两个或多个唯一性条件（指定不同属性的条件）添加到搜索查询中，这些条件将在逻辑上使用 **AND** 运算符来连接。</span><span class="sxs-lookup"><span data-stu-id="dc17d-278">If you add two or more unique conditions to a search query (conditions that specify different properties), those conditions are logically connected by the **AND** operator.</span></span> <span data-ttu-id="dc17d-279">这意味着仅返回满足所有条件（除了关键字查询以外）的项目。</span><span class="sxs-lookup"><span data-stu-id="dc17d-279">That means only items that satisfy all the conditions (in addition to the keyword query) are returned.</span></span> <span data-ttu-id="dc17d-280">如果向单个条件中添加多个值（用逗号或分号分隔），这些值将通过 **OR** 运算符来连接。</span><span class="sxs-lookup"><span data-stu-id="dc17d-280">If you add multiple values (separated by commas or semi-colons) to a single condition, those values are connected by the **OR** operator.</span></span> <span data-ttu-id="dc17d-281">这意味着如果这些项包含条件中指定的任何属性值，则返回这些项。</span><span class="sxs-lookup"><span data-stu-id="dc17d-281">That means items are returned if they contain any of the specified values for the property in the condition.</span></span> 
  
<span data-ttu-id="dc17d-282">以下是可添加到 DSR 案例内置搜索查询中的一些示例条件。</span><span class="sxs-lookup"><span data-stu-id="dc17d-282">Here are some examples of the conditions that you can add to the built-in search query of a DSR case.</span></span> <span data-ttu-id="dc17d-283">搜索查询中使用的实际属性的名称显示为括号。</span><span class="sxs-lookup"><span data-stu-id="dc17d-283">The name of the actual property used in a search query is shown parentheses.</span></span>
  
- <span data-ttu-id="dc17d-284">**文件类型 (`filetype`)** – 文档或文件的扩展名。</span><span class="sxs-lookup"><span data-stu-id="dc17d-284">**File type ( `filetype`)** – Specifies the extension of a document or file.</span></span> <span data-ttu-id="dc17d-285">使用此条件搜索由特定 Office 应用程序（如 Word、Excel 和 OneNote）创建的文档和文件。</span><span class="sxs-lookup"><span data-stu-id="dc17d-285">Use this condition to search for documents and files created by specific Office applications, such as Word, Excel, and OneNote.</span></span> 
    
- <span data-ttu-id="dc17d-286">**邮件类型 (`kind`)** – 指定要搜索的电子邮件项的类型。</span><span class="sxs-lookup"><span data-stu-id="dc17d-286">**Message type ( `kind`)** – Specifies the type of email item to search for.</span></span> <span data-ttu-id="dc17d-287">例如，可以使用语法  `kind:email OR kind:im` 仅返回电子邮件和 Skype for Business 对话，或 Microsoft Teams 中的一对一聊天。</span><span class="sxs-lookup"><span data-stu-id="dc17d-287">For example, you can use the syntax  `kind:email OR kind:im` to return only email messages and Skype for Business conversations or one-to-one chats in Microsoft Teams.</span></span> 
    
- <span data-ttu-id="dc17d-288">**合规性标记 (`compliancetag`)** – 指定分配给电子邮件或文档的标签。</span><span class="sxs-lookup"><span data-stu-id="dc17d-288">**Compliance tag (`compliancetag`)** – Specifies a label assigned to an email message or a document.</span></span> <span data-ttu-id="dc17d-289">此条件会返回使用特定标签分类的项。</span><span class="sxs-lookup"><span data-stu-id="dc17d-289">This condition returns items that are classified with a specific label.</span></span> <span data-ttu-id="dc17d-290">标签用于对电子邮件和文档进行分类，以实现数据治理，并根据标签定义的分类加强实施保留规则。</span><span class="sxs-lookup"><span data-stu-id="dc17d-290">Labels are used to classify email and documents for data governance and enforce retention rules based on the classification defined by the label.</span></span> <span data-ttu-id="dc17d-291">此条件对于 DSR 调查非常有用，因为组织可能使用了标签对数据隐私相关内容或者包含个人数据或敏感信息的内容进行了分类。</span><span class="sxs-lookup"><span data-stu-id="dc17d-291">This is a useful condition for DSR investigations because your organization may be using labels to classify content related to data privacy or that contains personal data or sensitive information.</span></span> <span data-ttu-id="dc17d-292">对于此条件的值，请使用完整的标签名称或带有通配符的标签名称的第一部分。</span><span class="sxs-lookup"><span data-stu-id="dc17d-292">For the value of this condition, use the complete label name or the first part of the label name with a wildcard.</span></span> <span data-ttu-id="dc17d-293">有关详细信息，请参阅[了解 Office 365 中的保留策略和保留标签](/microsoft-365/compliance/retention)。</span><span class="sxs-lookup"><span data-stu-id="dc17d-293">For more information, see [Learn about retention policies and retention labels in Office 365](/microsoft-365/compliance/retention).</span></span>
    
<span data-ttu-id="dc17d-294">有关可以在 DSR 案例工具中使用的条件的列表和描述，请参阅“内容搜索的关键词查询和搜索条件”文章中的“[搜索条件](/microsoft-365/compliance/keyword-queries-and-search-conditions#search-conditions)”。</span><span class="sxs-lookup"><span data-stu-id="dc17d-294">For a list and description of all the conditions available in the DSR case tool, see [Search conditions](/microsoft-365/compliance/keyword-queries-and-search-conditions#search-conditions) in the "Keyword queries and search conditions for Content Search" article.</span></span> 
  
### <a name="changing-the-content-locations-that-are-searched"></a><span data-ttu-id="dc17d-295">更改搜索的内容位置</span><span class="sxs-lookup"><span data-stu-id="dc17d-295">Changing the content locations that are searched</span></span>

<span data-ttu-id="dc17d-296">除了修改 DSR 案例的内置搜索之外，还可以更改搜索的内容位置。</span><span class="sxs-lookup"><span data-stu-id="dc17d-296">In addition to revising the built-in search for a DSR case, you can also change the content locations that are searched.</span></span> <span data-ttu-id="dc17d-297">如前所述，内置搜索会搜索组织中的每个邮箱和网站，以及任何 Exchange Online 公用文件夹。</span><span class="sxs-lookup"><span data-stu-id="dc17d-297">As previously explained, the built-in search searches every mailbox and site in the organization, and any Exchange Online public folders.</span></span> <span data-ttu-id="dc17d-298">例如，可以将搜索范围缩小为仅搜索数据主体的邮箱、OneDrive 帐户和所选 SharePoint 网站。</span><span class="sxs-lookup"><span data-stu-id="dc17d-298">For example, you could narrow the search to only search the data subject's mailbox and OneDrive account and selected SharePoint sites.</span></span> <span data-ttu-id="dc17d-299">如果选择搜索特定网站，则必须添加要搜索的每个网站。</span><span class="sxs-lookup"><span data-stu-id="dc17d-299">If you choose to search specific sites, you have to add each site that you want to search.</span></span>
  
<span data-ttu-id="dc17d-300">要修改要搜索的内容位置：请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="dc17d-300">To modify the content locations to search:</span></span>
  
1. <span data-ttu-id="dc17d-301">打开要更改内容位置的内置搜索。</span><span class="sxs-lookup"><span data-stu-id="dc17d-301">Open the built-in search that you want to change the content locations for.</span></span>
    
2. <span data-ttu-id="dc17d-302">在搜索查询的“**位置**”下方，点击“**特定位置**”选项旁边的“**修改**”。</span><span class="sxs-lookup"><span data-stu-id="dc17d-302">In the search query, under **Locations**, click **Modify** next to the **Specific locations** option.</span></span> 
    
    ![点击“修改”，更改内置搜索查询的内容位置](../media/d66f7ba7-b71f-4ff5-a030-460ff02e3123.png)
  
    <span data-ttu-id="dc17d-304">将显示“**修改位置**”浮出页面。</span><span class="sxs-lookup"><span data-stu-id="dc17d-304">The **Modify locations** flyout page is displayed.</span></span> <span data-ttu-id="dc17d-305">页面中会显示内置搜索中内容位置的说明，以及有关修改所搜索位置的一些信息。</span><span class="sxs-lookup"><span data-stu-id="dc17d-305">Here's a description of the content locations in the built-in search and some information about modifying the locations that are searched.</span></span> 
    
    ![修改位置浮出页面。](../media/56c033f6-6735-46ba-abb2-a263a2b79836.png)
  
    <span data-ttu-id="dc17d-307">a.</span><span class="sxs-lookup"><span data-stu-id="dc17d-307">a.</span></span> <span data-ttu-id="dc17d-308">浮出页面顶部，邮箱部分“**全选**”下方的切换键处于选中状态，这表示搜索所有邮箱。</span><span class="sxs-lookup"><span data-stu-id="dc17d-308">The toggle under **Select all** in mailbox section at the top of the flyout page is selected, which indicates that all mailboxes are searched.</span></span> <span data-ttu-id="dc17d-309">若要缩小搜索范围，请点击切换键取消选中，然后点击 **选择用户、组或团队**”，并选择要搜索的具体邮箱。</span><span class="sxs-lookup"><span data-stu-id="dc17d-309">To narrow the scope of the search, click the toggle to unselect it, and then click **Choose users, groups, or teams** and choose specific mailboxes to search.</span></span>
    
    <span data-ttu-id="dc17d-310">b.</span><span class="sxs-lookup"><span data-stu-id="dc17d-310">b.</span></span> <span data-ttu-id="dc17d-311">浮出页面中部，网站部分“**全选**”下方的切换键处于选中状态，这表示搜索所有网站。</span><span class="sxs-lookup"><span data-stu-id="dc17d-311">The toggle under **Select all** in the sites section in the middle of the flyout page is selected, which indicates that all sites are searched.</span></span> <span data-ttu-id="dc17d-312">若要将搜索范围缩小到所选网站，请取消选择切换键，然后点击“**选择网站**”。</span><span class="sxs-lookup"><span data-stu-id="dc17d-312">To narrow the search to selected sites, you would unselect the toggle and then click **Choose sites**.</span></span> <span data-ttu-id="dc17d-313">必须添加要搜索的每个具体网站，包括数据主体的 OneDrive 帐户。</span><span class="sxs-lookup"><span data-stu-id="dc17d-313">You have to add each specific site that you want to search, including the data subject's OneDrive account.</span></span>
    
    <span data-ttu-id="dc17d-314">c.</span><span class="sxs-lookup"><span data-stu-id="dc17d-314">c.</span></span> <span data-ttu-id="dc17d-315">“Exchange 公用文件夹”部分中的切换键处于选中状态，这意味着搜索所有 Exchange 公用文件夹。</span><span class="sxs-lookup"><span data-stu-id="dc17d-315">The toggle in the Exchange public folders section is selected, which means all Exchange public folders are searched.</span></span> <span data-ttu-id="dc17d-316">你只能要么仅搜索所有 Exchange 公用文件夹，要么完全不搜索。</span><span class="sxs-lookup"><span data-stu-id="dc17d-316">You can only search all Exchange public folders or none of them.</span></span> <span data-ttu-id="dc17d-317">无法选择具体的 Exchange 公用文件夹进行搜索。</span><span class="sxs-lookup"><span data-stu-id="dc17d-317">You can't choose specific ones to search.</span></span>
    
3. <span data-ttu-id="dc17d-318">如果修改内置搜索中的内容位置，请点击“**保存&amp;运行**“以重新启动搜索。</span><span class="sxs-lookup"><span data-stu-id="dc17d-318">If you modify the content locations in the built-in search, click **Save &amp; run** to restart the search.</span></span> 

> [!NOTE]
> <span data-ttu-id="dc17d-319">搜索所有邮箱位置或仅特定邮箱，导出搜索结果时，保存至用户邮箱的其他 Office 365 应用程序数据将包括在内。</span><span class="sxs-lookup"><span data-stu-id="dc17d-319">When you search all mailbox locations or just specific mailboxes, data from other Office 365 applications that's saved to user mailboxes is included when you export the results of the search.</span></span> <span data-ttu-id="dc17d-320">此数据将不会包括在估计的搜索结果中，并且也不可用于预览。</span><span class="sxs-lookup"><span data-stu-id="dc17d-320">This data won't be included in the estimated search results and isn't available for preview.</span></span> <span data-ttu-id="dc17d-321">但在导入和下载搜索结果时，此数据将包括在内。</span><span class="sxs-lookup"><span data-stu-id="dc17d-321">But it's included when you export and download the search results.</span></span> <span data-ttu-id="dc17d-322">有关在用户邮箱中存储数据的应用程序的详细信息，请参阅[存储在 Exchange Online 邮箱中的内容](/microsoft-365/compliance/what-is-stored-in-exo-mailbox)。</span><span class="sxs-lookup"><span data-stu-id="dc17d-322">For more information the applications that store data in a user's mailbox, see [Content stored in Exchange Online mailboxes](/microsoft-365/compliance/what-is-stored-in-exo-mailbox).</span></span>
  
## <a name="more-information-about-using-the-dsr-case-tool"></a><span data-ttu-id="dc17d-323">有关使用 DSR 案例工具的详细信息</span><span class="sxs-lookup"><span data-stu-id="dc17d-323">More information about using the DSR case tool</span></span>

<span data-ttu-id="dc17d-324">以下部分包含有关使用 DSR 案例工具响应 DSR 导出请求的详细信息。</span><span class="sxs-lookup"><span data-stu-id="dc17d-324">The following sections contain more information about using the DSR case tool to respond to DSR export requests.</span></span>
  
[<span data-ttu-id="dc17d-325">从 Office 漫游服务导出数据</span><span class="sxs-lookup"><span data-stu-id="dc17d-325">Exporting data from the Office Roaming Service</span></span>](#exporting-data-from-the-office-roaming-service)

[<span data-ttu-id="dc17d-326">导出部分索引项</span><span class="sxs-lookup"><span data-stu-id="dc17d-326">Exporting partially indexed items</span></span>](#exporting-partially-indexed-items)

[<span data-ttu-id="dc17d-327">搜索并从 Microsoft Teams 和 Microsoft 365 组中导出数据</span><span class="sxs-lookup"><span data-stu-id="dc17d-327">Searching and exporting data from Microsoft Teams and Microsoft 365 Groups</span></span>](#searching-and-exporting-data-from-microsoft-teams-and-microsoft-365-groups)

[<span data-ttu-id="dc17d-328">搜索 Exchange 公用文件夹</span><span class="sxs-lookup"><span data-stu-id="dc17d-328">Searching Exchange public folders</span></span>](#searching-exchange-public-folders)
  
### <a name="exporting-data-from-the-office-roaming-service"></a><span data-ttu-id="dc17d-329">从 Office 漫游服务导出数据</span><span class="sxs-lookup"><span data-stu-id="dc17d-329">Exporting data from the Office Roaming Service</span></span>

<span data-ttu-id="dc17d-330">可以使用 DSR 案例工具搜索并导出由 Office 漫游服务生成的使用情况数据。</span><span class="sxs-lookup"><span data-stu-id="dc17d-330">You can use the DSR case tool to search for and export usage data that's generated by the Office Roaming Service.</span></span> <span data-ttu-id="dc17d-331">漫游是一种可以存储 Office 相关设置，如 Office 主题、自定义词典、语言设置、开发者模式和自动更正的服务。</span><span class="sxs-lookup"><span data-stu-id="dc17d-331">Roaming is a service that stores Office-related settings, such as Office theme, custom dictionary, language settings, developer mode, and auto correct.</span></span> 
    
<span data-ttu-id="dc17d-332">来自 Office 漫游服务的数据存储在数据主体邮箱中的隐藏文件夹中，该文件夹位于 Exchange Online 邮箱的非人际邮件（非 IPM）子树中。</span><span class="sxs-lookup"><span data-stu-id="dc17d-332">The data from the Office Roaming service is stored in a data subject's mailbox in a hidden folder located in a non-interpersonal message (non-IPM) subtree of Exchange Online mailboxes.</span></span> <span data-ttu-id="dc17d-333">这意味着当用户使用 Outlook 或其他邮件客户端访问其邮箱时，用户的视图中不会显示此类数据。</span><span class="sxs-lookup"><span data-stu-id="dc17d-333">This means that the data is hidden from the user's view when they use Outlook or other mail clients to access their mailbox.</span></span> <span data-ttu-id="dc17d-334">有关隐藏文件夹的详细信息，请参阅 [MAPI 隐藏文件夹](https://go.microsoft.com/fwlink/?linkid=872758)。</span><span class="sxs-lookup"><span data-stu-id="dc17d-334">For more information about hidden folders, see [MAPI Hidden Folders](https://go.microsoft.com/fwlink/?linkid=872758).</span></span>
  
<span data-ttu-id="dc17d-335">可以创建单独的内容搜索（并将其与 DSR 事例相关联），以返回数据主体邮箱中的 Office 漫游服务使用情况数据。</span><span class="sxs-lookup"><span data-stu-id="dc17d-335">You can create a separate content search (and associate it with a DSR case) that returns the Office Roaming Service usage data in the data subject's mailbox.</span></span> <span data-ttu-id="dc17d-336">此数据不包含在搜索统计信息中，并且不可预览。</span><span class="sxs-lookup"><span data-stu-id="dc17d-336">This data isn't included in the search statistics and it won't be available for preview.</span></span> <span data-ttu-id="dc17d-337">但可以将其导出，然后提供给数据主体以响应 DSR 导出请求。</span><span class="sxs-lookup"><span data-stu-id="dc17d-337">But you can export it and then give it to the data subject in response to a DSR export request.</span></span>
  
<span data-ttu-id="dc17d-338">从 Office 漫游服务导出数据时，数据将保存到位于 **ApplicationDataRoot** 文件夹中的单独文件夹中，该文件夹位于以数据主体电子邮件地址命名的文件夹下。</span><span class="sxs-lookup"><span data-stu-id="dc17d-338">When you export data from the Office Roaming Service, the data is saved to a separate folder that's located in the **ApplicationDataRoot** folder, which is under a folder that is name with the data subject's email address.</span></span> <span data-ttu-id="dc17d-339">此数据导出为附加到电子邮件的 JSON 文件（与 XML 或 TXT 文件类似，可供人工读取的文本文件）。</span><span class="sxs-lookup"><span data-stu-id="dc17d-339">This data is exported as JSON files, which are human-readable text files similar to XML or TXT files, that are attached to email messages.</span></span> <span data-ttu-id="dc17d-340">目前，此文件夹采用全局唯一标识符 (GUID) 命名：**1caee58f-eb14-4a6b-9339-1fe2ddf6692b**。</span><span class="sxs-lookup"><span data-stu-id="dc17d-340">Currently, this folder is named with the globally unique identifier (GUID): **1caee58f-eb14-4a6b-9339-1fe2ddf6692b**.</span></span> <span data-ttu-id="dc17d-341">在 DSR 案例工具的未来版本中，GUID 将替换为实际应用程序的名称。</span><span class="sxs-lookup"><span data-stu-id="dc17d-341">In future versions of the DSR case tool, the GUID will be replaced with the name of the actual application.</span></span> 

   
 <span data-ttu-id="dc17d-342">**若要搜索并导出 Office 漫游服务数据，请执行以下操作：**</span><span class="sxs-lookup"><span data-stu-id="dc17d-342">**To search for and export Office Roaming Service data:**</span></span>
  
1. <span data-ttu-id="dc17d-343">在安全与合规中心中，点击“**数据隐私** \> **数据主体请求**”，然后点击要导出使用情况数据的数据主体的 DSR 案例旁边的“**打开**”。</span><span class="sxs-lookup"><span data-stu-id="dc17d-343">In the Security & Compliance Center, click **Data privacy** \> **Data subject requests**, and then click **Open** next to the DSR case for the data subject that you want to export usage data for.</span></span> 
    
2. <span data-ttu-id="dc17d-344">单击页面顶部的“**搜索**”选项卡，然后点击![添加图标](../media/ITPro-EAC-AddIcon.gif) **引导式搜索**。</span><span class="sxs-lookup"><span data-stu-id="dc17d-344">Click the **Search** tab at the top of the page, and then click ![Add Icon](../media/ITPro-EAC-AddIcon.gif) **Guided search**.</span></span>
    
3. <span data-ttu-id="dc17d-345">在 **命名搜索 **页面上，点击“** 取消**”。</span><span class="sxs-lookup"><span data-stu-id="dc17d-345">Click **Cancel** on the **Name your search** page.</span></span> 
    
4. <span data-ttu-id="dc17d-346">在“**搜索查询**”下，“**类型**”条件中，选中“**Office 漫游服务**”旁边的复选框。</span><span class="sxs-lookup"><span data-stu-id="dc17d-346">Under **Search query**, in the **Type** condition, select the check box next to **Office Roaming Service**.</span></span> 
    
    ![选中 Office 漫游服务复选框以导出使用情况数据](../media/O365_DSRCase_SDSDataExport1.png)
  
    <span data-ttu-id="dc17d-348">“**类型**”条件（即电子邮件类）应是搜索查询中的唯一项。</span><span class="sxs-lookup"><span data-stu-id="dc17d-348">The **Type** condition (which are email message classes) should be the only item in the search query.</span></span> <span data-ttu-id="dc17d-349">可以删除 **关键字** 框或留空。</span><span class="sxs-lookup"><span data-stu-id="dc17d-349">You can delete the **Keywords** box or leave it blank.</span></span> 
    
5. <span data-ttu-id="dc17d-350">在“**位置**”下，确保选中“**特定位置**”，然后点击“**修改**”。</span><span class="sxs-lookup"><span data-stu-id="dc17d-350">Under **Locations**, make sure that **Specific locations** is selected, and then click **Modify**.</span></span>
    
6. <span data-ttu-id="dc17d-351">在“**修改位置**”浮出页面（邮箱部分）顶部，点击“**选择用户、组或团队**”。</span><span class="sxs-lookup"><span data-stu-id="dc17d-351">On top part of the **Modify locations** flyout page (the mailbox section), click **Choose users, groups, or teams**.</span></span>
    
7. <span data-ttu-id="dc17d-352">在“**编辑位置**”页面上，点击“**选择用户、组或团队**”，选择数据主体的邮箱，然后保存所选内容。</span><span class="sxs-lookup"><span data-stu-id="dc17d-352">On the **Edit locations** page, click **Choose users, groups, or teams**, choose the data subject's mailbox, and then save your selection.</span></span> 
    
8. <span data-ttu-id="dc17d-353">点击“**保存并运行**”，然后命名搜索并保存。</span><span class="sxs-lookup"><span data-stu-id="dc17d-353">Click **Save & run**, and then name the search and save it.</span></span>
    
    <span data-ttu-id="dc17d-354">搜索即启动。</span><span class="sxs-lookup"><span data-stu-id="dc17d-354">The search is started.</span></span>
    
 <span data-ttu-id="dc17d-355">**若要导出 Office 漫游服务数据，请执行以下操作：**</span><span class="sxs-lookup"><span data-stu-id="dc17d-355">**To export Office Roaming Service data:**</span></span>
  
1. <span data-ttu-id="dc17d-356">当上个步骤中创建的搜索完成后，点击页面顶部的“**搜索**”选项卡，然后点击搜索旁边的复选框。</span><span class="sxs-lookup"><span data-stu-id="dc17d-356">When the search that you created in the previous step is complete, click the **Search** tab at the top of the page, and then click the checkbox next to the search.</span></span> <span data-ttu-id="dc17d-357">可能必须点击“![刷新](../media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png) **刷新**”才能显示搜索。</span><span class="sxs-lookup"><span data-stu-id="dc17d-357">You may have to click ![Refresh](../media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png) **Refresh** to display the search.</span></span> 
    
2. <span data-ttu-id="dc17d-358">在搜索浮出页面上，单击“![导出搜索结果](../media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png)”图标“**更多**”，然后从下拉列表中选择“**导出结果**”。</span><span class="sxs-lookup"><span data-stu-id="dc17d-358">On the search flyout page, click ![Export search results icon](../media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **More**, and then select **Export results** from the drop-down list.</span></span> 
    
3. <span data-ttu-id="dc17d-359">在“**导出结果**”页面上，选择建议的选项以导出使用情况数据。</span><span class="sxs-lookup"><span data-stu-id="dc17d-359">On the **Export results** page, select the recommended options to export usage data.</span></span> 
    
    ![导出 Office 漫游服务使用情况数据时的导出选项](../media/470a7d1e-eeae-4b42-95aa-15cb82ce2f68.png)
  
    <span data-ttu-id="dc17d-361">a.</span><span class="sxs-lookup"><span data-stu-id="dc17d-361">a.</span></span> <span data-ttu-id="dc17d-362">在“**输出选项**”下方，选择第一个选项（**所有项（不包括具有无法识别格式的项）已加密，或由于其他原因未编制索引**）以仅导出已编制索引的项目。</span><span class="sxs-lookup"><span data-stu-id="dc17d-362">Under **Output options**, select the first option (**All items, excluding ones that have ones that have an unrecognized format, are encrypted, or weren't indexed for other reasons**) to export indexed items only.</span></span>
    
    <span data-ttu-id="dc17d-363">b.</span><span class="sxs-lookup"><span data-stu-id="dc17d-363">b.</span></span> <span data-ttu-id="dc17d-364">在“**将 Exchange 内容导出为** 下方，选择第二个选项，**一个 PST 文件包含所有邮件**。</span><span class="sxs-lookup"><span data-stu-id="dc17d-364">Under **Export Exchange content as**, select the second option, **One PST file containing all messages**.</span></span>
    
    <span data-ttu-id="dc17d-365">c.</span><span class="sxs-lookup"><span data-stu-id="dc17d-365">c.</span></span> <span data-ttu-id="dc17d-366">剩余的导出选项保持未选中状态。</span><span class="sxs-lookup"><span data-stu-id="dc17d-366">Leave the remaining export options unselected.</span></span>
    
4. <span data-ttu-id="dc17d-367">选择导出设置后，点击“**导出**”。</span><span class="sxs-lookup"><span data-stu-id="dc17d-367">After you choose the export settings, click **Export**.</span></span>
    
    <span data-ttu-id="dc17d-368">搜索结果已准备下载是指它们被上传至 Microsoft 云中的 WindowsAzure 存储区域。</span><span class="sxs-lookup"><span data-stu-id="dc17d-368">The search results are prepared for downloading, which means they're uploaded to the Azure storage area for your organization in the Microsoft cloud.</span></span> <span data-ttu-id="dc17d-369">后续步骤将会介绍如何将此数据下载到本地计算机。</span><span class="sxs-lookup"><span data-stu-id="dc17d-369">The next steps show you how to download this data to your local computer.</span></span>
    
5. <span data-ttu-id="dc17d-370">点击“**导出**”选项卡以显示创建的导出作业。</span><span class="sxs-lookup"><span data-stu-id="dc17d-370">Click the **Export** tab to display the export job you created.</span></span> <span data-ttu-id="dc17d-371">导出作业的名称与搜索名称最后带有“**_Export**”的相应搜索相同。</span><span class="sxs-lookup"><span data-stu-id="dc17d-371">The export jobs have the same name as the corresponding search with **_Export** appended to the end of search name.</span></span> 
    
6. <span data-ttu-id="dc17d-372">点击刚刚创建的导出作业，以显示导出浮出页面。</span><span class="sxs-lookup"><span data-stu-id="dc17d-372">Click the export job that you just created to display the export flyout page.</span></span> 
    
7. <span data-ttu-id="dc17d-373">在“**导出密钥**”下，点击“**复制到剪贴板**”。</span><span class="sxs-lookup"><span data-stu-id="dc17d-373">Under **Export key**, click **Copy to clipboard**.</span></span> <span data-ttu-id="dc17d-374">在步骤 10 中，将使用此密钥下载搜索结果。</span><span class="sxs-lookup"><span data-stu-id="dc17d-374">You use this key in step 10 to download the search results.</span></span>
    
8. <span data-ttu-id="dc17d-375">点击导出浮出页面顶部的![导出搜索结果图标](../media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **下载结果**。</span><span class="sxs-lookup"><span data-stu-id="dc17d-375">Click ![Export search results icon](../media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) **Download results** at the top of the export flyout page.</span></span> 
    
9. <span data-ttu-id="dc17d-376">在页面底部的弹出窗口中，点击“**打开**”以打开“**电子数据展示导出工具**”。</span><span class="sxs-lookup"><span data-stu-id="dc17d-376">In the pop-up window at the bottom of the page, click **Open** to open the **eDiscovery Export Tool**.</span></span> <span data-ttu-id="dc17d-377">如果是首次下载搜索结果，则会安装 **电子数据展示导出工具**。</span><span class="sxs-lookup"><span data-stu-id="dc17d-377">The **eDiscovery Export Tool** will be installed the first time you download search results.</span></span> 
    
10. <span data-ttu-id="dc17d-378">在“**电子数据展示导出工具**”中，将在步骤 7 中复制的导出密钥粘贴在相应的框中。</span><span class="sxs-lookup"><span data-stu-id="dc17d-378">In the **eDiscovery Export Tool**, paste the export key that you copied in step 7 in the appropriate box.</span></span>
    
11. <span data-ttu-id="dc17d-379">单击“**浏览**”指定要下载搜索结果文件的位置。</span><span class="sxs-lookup"><span data-stu-id="dc17d-379">Click **Browse** to specify the location where you want to download the search result files.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="dc17d-380">由于磁盘活动量很大（读取和写入），应将搜索结果下载到本地磁盘驱动器；勿将其载到映射的网络驱动器或其他网络位置。</span><span class="sxs-lookup"><span data-stu-id="dc17d-380">Due to the high amount of disk activity (reads and writes), you should download search results to a local disk drive; don't download them to a mapped network drive or other network location.</span></span> 
  
12. <span data-ttu-id="dc17d-381">单击“启动”将搜索结果下载到计算机。</span><span class="sxs-lookup"><span data-stu-id="dc17d-381">Click **Start** to download the search results to your computer.</span></span> 
    
    <span data-ttu-id="dc17d-382">**电子数据展示工具** 显示有关导出过程的状态信息，包括要下载的剩余项的估计数量（和大小）。</span><span class="sxs-lookup"><span data-stu-id="dc17d-382">The **eDiscovery Export Tool** displays status information about the export process, including an estimate of the number (and size) of the remaining items to be downloaded.</span></span> <span data-ttu-id="dc17d-383">导出过程完成后，可以在 Outlook 中打开 Exchange PST 文件，然后转到 **ApplicationDataRoot** 文件夹以访问漫游服务的子文件夹。</span><span class="sxs-lookup"><span data-stu-id="dc17d-383">When the export process is complete, you can open the Exchange PST file in Outlook and then go to the **ApplicationDataRoot** folder to access the subfolder for the Roaming service.</span></span> 
    
    <span data-ttu-id="dc17d-384">如前所述，包含使用情况数据的 JSON 文件会附加到邮件中。</span><span class="sxs-lookup"><span data-stu-id="dc17d-384">As previously explained, the JSON files that contain usage data are attached to messages.</span></span> <span data-ttu-id="dc17d-385">若要查看 JSON 文件，点击一封邮件，然后打开附件中的 JSON 文件。</span><span class="sxs-lookup"><span data-stu-id="dc17d-385">To view a JSON file, click a message and then open the attached JSON file.</span></span> 
  
### <a name="exporting-partially-indexed-items"></a><span data-ttu-id="dc17d-386">导出部分索引项</span><span class="sxs-lookup"><span data-stu-id="dc17d-386">Exporting partially indexed items</span></span>

<span data-ttu-id="dc17d-387">建议不要从创建 DSR 案例时创建的内置搜索中导出部分索引项（也称为未编制索引的项目）。</span><span class="sxs-lookup"><span data-stu-id="dc17d-387">We recommend that you don't export partially indexed items (also called unindexed items) from the built-in search that's created when you create a DSR case.</span></span> <span data-ttu-id="dc17d-388">这是因为搜索结果很可能包含组织中其他用户的部分索引项，而不仅仅是数据主体的部分索引项。</span><span class="sxs-lookup"><span data-stu-id="dc17d-388">That's because the search results will more than likely include partially indexed items for other users in your organization, and not just partially indexed items for the data subject).</span></span> <span data-ttu-id="dc17d-389">我们建议创建一个单独的内容搜索，该搜索与 DSR 案例相关联，旨在仅导出与数据主体相关的部分索引项。</span><span class="sxs-lookup"><span data-stu-id="dc17d-389">Instead, we recommend that you create a separate Content Search that's associated with the DSR case that's designed to export only the partially indexed items related to the data subject.</span></span> 
  
<span data-ttu-id="dc17d-390">下面是导出部分索引项的高级流程。</span><span class="sxs-lookup"><span data-stu-id="dc17d-390">Here's a high-level process to export partially indexed items.</span></span> <span data-ttu-id="dc17d-391">导出后，可以查看它们，以确定项目是否响应 DSR 访问或导出请求。</span><span class="sxs-lookup"><span data-stu-id="dc17d-391">After they're export, you can review them to determine if an item is responsive to a DSR access or export request.</span></span>
  
1. <span data-ttu-id="dc17d-392">打开 DSR 案例并在“**搜索**”页面上创建搜索。</span><span class="sxs-lookup"><span data-stu-id="dc17d-392">Open the DSR case and create a search on the **Search** page.</span></span> 
    
2. <span data-ttu-id="dc17d-393">使用以下条件配置搜索查询，以及要搜索的内容位置：</span><span class="sxs-lookup"><span data-stu-id="dc17d-393">Use the following criteria for configuring the search query and the content locations to search:</span></span>
    
    - <span data-ttu-id="dc17d-394">使用空的关键字查询。</span><span class="sxs-lookup"><span data-stu-id="dc17d-394">Use an empty/blank keyword query.</span></span> <span data-ttu-id="dc17d-395">这样做会返回搜索的内容位置中的所有项。</span><span class="sxs-lookup"><span data-stu-id="dc17d-395">This returns all items in the content locations that are searched.</span></span>
    
    - <span data-ttu-id="dc17d-396">仅搜索数据主体的 Exchange Online 邮箱及其 OneDrive 帐户。</span><span class="sxs-lookup"><span data-stu-id="dc17d-396">Search only the data subject's Exchange Online mailbox and their OneDrive account.</span></span>
    
3. <span data-ttu-id="dc17d-397">运行搜索并完成后，可以导出并下载搜索结果（如[步骤 4](#step-4-export-the-data) 中所述）。</span><span class="sxs-lookup"><span data-stu-id="dc17d-397">After you run the search and it completes, you can export and download the search results (as described in [Step 4](#step-4-export-the-data)).</span></span> <span data-ttu-id="dc17d-398">使用以下设置导出部分索引项。</span><span class="sxs-lookup"><span data-stu-id="dc17d-398">Use the following settings to export partially indexed items.</span></span> 
    
    - <span data-ttu-id="dc17d-399">在“**输出选项**”下方，选择第三个选项（**仅具有无法识别格式、已加密，或由于其他原因未编制索引的项**）以仅导出部分索引项。</span><span class="sxs-lookup"><span data-stu-id="dc17d-399">Under **Output options**, select the third option (**Only items that have an unrecognized format, are encrypted, or weren't indexed for other reasons**) to export partially indexed items only.</span></span>
    
    - <span data-ttu-id="dc17d-400">在“**将 Exchange 内容导出为**”下，你可以根据偏好选择任何选项。</span><span class="sxs-lookup"><span data-stu-id="dc17d-400">Under **Export Exchange content as**, you can select any option based on your preferences.</span></span> 
    
    - <span data-ttu-id="dc17d-401">选择“**包含 SharePoint 文档的版本**”选项导出文档的版本（如果某个版本已部分编制索引）。</span><span class="sxs-lookup"><span data-stu-id="dc17d-401">Selecting the **Include versions for SharePoint documents** option exports versions of documents if a version is partially indexed.</span></span> 
    
<span data-ttu-id="dc17d-402">有关详细信息，请参阅：</span><span class="sxs-lookup"><span data-stu-id="dc17d-402">For more information about partially indexed items, see:</span></span> 
  
- [<span data-ttu-id="dc17d-403">处理 Office 365 内容搜索中的部分索引项</span><span class="sxs-lookup"><span data-stu-id="dc17d-403">Partially indexed items in Content Search in Office 365</span></span>](/microsoft-365/compliance/partially-indexed-items-in-content-search)

- [<span data-ttu-id="dc17d-404">导出部分索引项</span><span class="sxs-lookup"><span data-stu-id="dc17d-404">Exporting partially indexed items</span></span>](/microsoft-365/compliance/export-search-results#exporting-partially-indexed-items)

### <a name="searching-and-exporting-data-from-microsoft-teams-and-microsoft-365-groups"></a><span data-ttu-id="dc17d-405">搜索并从 Microsoft Teams 和 Microsoft 365 组中导出数据</span><span class="sxs-lookup"><span data-stu-id="dc17d-405">Searching and exporting data from Microsoft Teams and Microsoft 365 Groups</span></span>

<span data-ttu-id="dc17d-406">属于 Microsoft Teams 中聊天列表的对话（称为“团队聊天”或“一对一聊天”）将存储在参与该聊天的用户的 Exchange Online 邮箱中。</span><span class="sxs-lookup"><span data-stu-id="dc17d-406">Conversations that are part of the Chat list in Microsoft Teams (called Team chats or one-to-one chats) are stored in the Exchange Online mailbox of the users who participate in the chats.</span></span> <span data-ttu-id="dc17d-407">此外，用户在一对一聊天中共享的文件存储在该用户的 OneDrive 帐户中。</span><span class="sxs-lookup"><span data-stu-id="dc17d-407">Also, the files a person shares in a one-to-one chat are stored in the OneDrive account of the person who shares the file.</span></span> <span data-ttu-id="dc17d-408">由于内置搜索会搜索组织中的所有邮箱和 OneDrive 帐户，因此在 DSR 案例中内置搜索会返回聊天会话中共享的团队聊天和文档（由数据主体创建或上传的）。</span><span class="sxs-lookup"><span data-stu-id="dc17d-408">Because the built-in search searches all mailboxes and OneDrive accounts in the organization, team chats and documents shared in a chat session (that the data subject created or uploaded) are returned by built-in search in a DSR case.</span></span>
  
<span data-ttu-id="dc17d-409">此外，Teams 频道中的对话（也称为“频道消息”）存储在与某个团队关联的邮箱中。</span><span class="sxs-lookup"><span data-stu-id="dc17d-409">Alternatively, conversations that are part of a Teams channel (also called channel messages) are stored in the mailbox that's associated with a team.</span></span> <span data-ttu-id="dc17d-410">数据主体参与的这些类型的对话也由内置搜索返回，因为会搜索与 Teams 关联的所有邮箱。</span><span class="sxs-lookup"><span data-stu-id="dc17d-410">These types of conversations that the data subject participated in are also returned by the built-in search because all mailboxes associated with Teams are searched.</span></span> <span data-ttu-id="dc17d-411">此外，数据主体在 Teams 频道中共享的文件存储在团队的 SharePoint 网站上。</span><span class="sxs-lookup"><span data-stu-id="dc17d-411">Additionally, files that a data subject shares in a Teams channel are stored on the team's SharePoint site.</span></span> <span data-ttu-id="dc17d-412">数据主体创建或上传的文件由 DSR 案例中的内置搜索返回，因为搜索中包含与 Teams 关联的网站。</span><span class="sxs-lookup"><span data-stu-id="dc17d-412">Files created or uploaded by the data subject are returned by the built-in search in a DSR case because the sites associated with Teams are included in the search.</span></span>
  
<span data-ttu-id="dc17d-413">同样，与 Microsoft 365 组对应的邮箱和 SharePoint 网站也包含在内置搜索中。</span><span class="sxs-lookup"><span data-stu-id="dc17d-413">Similarly, mailboxes and SharePoint sites that correspond to an Microsoft 365 Group are also included in the built-in search.</span></span> <span data-ttu-id="dc17d-414">这意味着将返回数据主体发送或接收的电子邮件，以及数据主体创建或上传的文件。</span><span class="sxs-lookup"><span data-stu-id="dc17d-414">This means that email messages sent or received by the data subject and files created or uploaded by the data subject are returned.</span></span> 
  
<span data-ttu-id="dc17d-415">有关使用内容搜索在 Microsoft Teams 和 Microsoft 365 组中搜索项目，或查看如何获取成员列表的详细信息，请参阅“[Microsoft 365 中的内容搜索](/microsoft-365/compliance/content-search#searching-microsoft-teams-and-microsoft-365-groups)”中的“搜索 Microsoft Teams 和 Microsoft 365 组”部分。</span><span class="sxs-lookup"><span data-stu-id="dc17d-415">For more information about using Content Search to search for items in Microsoft Teams and Microsoft 365 Groups or to see how to get a list of members, see the "Searching Microsoft Teams and Microsoft 365 Groups" section in [Content Search in Microsoft 365](/microsoft-365/compliance/content-search#searching-microsoft-teams-and-microsoft-365-groups).</span></span> 
  
### <a name="searching-exchange-public-folders"></a><span data-ttu-id="dc17d-416">Exchange 公用文件夹</span><span class="sxs-lookup"><span data-stu-id="dc17d-416">Searching Exchange public folders</span></span>

<span data-ttu-id="dc17d-417">DSR 案例中的内置搜索将仅返回数据主体发送到启用邮件的公用文件夹，或其他人发送到公用文件夹并抄送给数据主体的电子邮件。</span><span class="sxs-lookup"><span data-stu-id="dc17d-417">The built-in search in a DSR case will only return email messages that the data subject sent to a mail-enabled public folder or messages that someone else sent to a public folder and also copied the data subject.</span></span> <span data-ttu-id="dc17d-418">不会返回数据主体发布到公用文件夹的邮件。</span><span class="sxs-lookup"><span data-stu-id="dc17d-418">It doesn't return messages that the data subject posted to a public folder.</span></span> <span data-ttu-id="dc17d-419">若要搜索数据主体发布到公用文件夹的项目，可以单独创建一个内容搜索，用于搜索数据主体发布到公用文件夹的任何项目。</span><span class="sxs-lookup"><span data-stu-id="dc17d-419">To search for items that the data subject posted to a public folder, you can create a separate create a separate Content Search that searches for any item posted to a public folder by the data subject.</span></span>
  
<span data-ttu-id="dc17d-420">以下是搜索数据主体发布到公用文件夹的项目的高级流程。</span><span class="sxs-lookup"><span data-stu-id="dc17d-420">Here's a high-level process to search for items that the data subject posted to a public folder.</span></span> 
  
1. <span data-ttu-id="dc17d-421">打开 DSR 案例并在“**搜索**”页面上创建搜索。</span><span class="sxs-lookup"><span data-stu-id="dc17d-421">Open the DSR case and create a search on the **Search** page.</span></span> 
    
2. <span data-ttu-id="dc17d-422">使用以下条件配置搜索查询，以及要搜索的内容位置：</span><span class="sxs-lookup"><span data-stu-id="dc17d-422">Use the following criteria for configuring the search query and the content locations to search:</span></span>
    
  - <span data-ttu-id="dc17d-423">在“**关键字**”框中，使用以下搜索查询：</span><span class="sxs-lookup"><span data-stu-id="dc17d-423">In the **Keywords** box, use the following search query:</span></span> 
    
    ```powershell
    itemclass:ipm.post AND "<email address of the data subject>"
    ```

  - <span data-ttu-id="dc17d-424">搜索所有 Exchange 公用文件夹</span><span class="sxs-lookup"><span data-stu-id="dc17d-424">Search all Exchange public folders</span></span>
    
  - <span data-ttu-id="dc17d-425">运行搜索并完成后，可以导出并下载搜索结果（如[步骤 4](#step-4-export-the-data) 中所述）。</span><span class="sxs-lookup"><span data-stu-id="dc17d-425">After you run the search and it completes, you can export and download the search results (as described in [Step 4](#step-4-export-the-data)).</span></span> <span data-ttu-id="dc17d-426">使用以下设置导出部分索引项。</span><span class="sxs-lookup"><span data-stu-id="dc17d-426">Use the following settings to export partially indexed items.</span></span> 
