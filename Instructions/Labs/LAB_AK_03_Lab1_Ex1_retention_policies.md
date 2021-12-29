# 实验室 3 - 练习 1 - 配置保留策略

在本练习中，假设你是 Joni Sherman，Contoso Ltd. 的系统管理员，你的组织位于德克萨斯州，并且想要实现保留策略以遵守州法律，该法律规定，记录可以在三年后删除，而不会构成违法。 

为了遵守该法，你的组织制定了一个保留计划，打算将组织内的所有项都保留三年。


### 任务 1 - 创建公司范围内的保留策略

在本练习中，你将创建公司范围内的保留策略，应用保留期，并设置策略应用位置。

1. 使用 **“lon-cl1\admin”** 帐户登录到客户端 1 VM (LON-CL1)。

2. 在 **Microsoft Edge** 中，导航到 **https://compliance.microsoft.com** ， 并以 **Joni Sherman** 身份 JoniS@WWLxZZZZZZ.onmicrosoft.com（其中 ZZZZZZ 是实验室托管提供程序提供的唯一租户 ID）登录到 Microsoft 365 合规性门户。  Joni 的密码应由实验室托管提供程序提供。

3. 在 **Microsoft 365 合规性**门户的左侧导航窗格中，选择“**策略**”，然后在“**数据**”下选择“**保留**”。

4. 在 **“信息治理”** 页上的 **“保留”** 选项卡中，选择 **“+ 新建保留策略”**。

5. 在 **“为保留策略命名”** 页上的 **“名称”** 和 **“说明”** 中输入以下信息：

	- 名称：公司范围
	- 说明：所有位置（Teams 除外）

6. 选择 **“下一步”** 按钮。  

7. 在“**选择要创建的保留策略类型**”区域中，选择“**静态**”，然后选择”**下一步**”。

8. 在“**选择应用策略的位置”区域中，确保选择了**“Exchange 电子邮件”、“SharePoint 网站”、“OneDrive 帐户”和“Microsoft 365 组”，然后选择“**下一步**”。

9. 在“**确定是想要保留内容还是删除内容或两者兼而有之**”页上的“**将项保留特定时间段**”部分中，输入以下信息：

	- 将项保留特定时间段：从下拉列表中选择“**自定义**”
	- 将年字段更改为“**3**”
	- **保留期开始依据**：上次修改项的时间

10. 选择“**下一步**”按钮。

11. 在“**查看并完成**”页面上，选择“**提交**”按钮。

12. 创建策略后，选择“**完成**”按钮。

你已成功为 Exchange 电子邮件、Microsoft 365 组、OneDrive 和 SharePoint 网站位置创建了保留策略。此保留策略将自上次修改日期起将这些项保留在这些位置 3 年。此策略可能需要长达 24 小时才能应用于你的租户，但你可以继续执行下一步。

### 任务 2 - 使用筛选器创建基于位置的保留策略

你现在将为 Teams 位置创建保留策略。由于 Teams 频道可以包含文档，因此它们将全部保留。你的组织决定要求部分用户进行 Team 聊天时需要保留期。

1. 你仍应使用 **lon-cl1\admin** 帐户登录到客户端 1 VM (LON-CL1)，并且应该以 **Joni Sherman** 的身份登录到 Microsoft 365。 

2. 在 **Microsoft Edge** 中，Microsoft 365 合规性门户标签页应该仍处于打开状态。如果是这样，请选择该标签页并继续进行下一步。如果该标签页已关闭，则在新的标签页中，导航到 **https://compliance.microsoft.com** 。

3. 在 **Microsoft 365 合规性**门户的左侧导航窗格中，选择“**策略**”，然后在“**数据**”下选择“**保留**”。

4. 在 **“信息治理”** 页上的 **“保留策略”** 选项卡中，选择 **“+ 新建保留策略”**。

5. 在 **“为保留策略命名”** 页上的 **“名称”** 和 **“说明”** 中输入以下信息：

	- **名称**：Teams 保留
	- **说明**：针对 Teams 的保留位置

6. 选择 **“下一步”** 按钮。

7. 在“**选择要创建的保留策略类型**”区域中，选择“**静态**”，然后选择“**下一步**”。

8. 在“”选择应用策略的位置””页面上，输入以下设置：

	- “**Teams 频道消息**”位置 -“**状态**”：开 
	- “**Teams 聊天位置**” -“**状态**”：开
	- **关闭**所有其他位置。

9. 对于 Teams 聊天位置，在“**所有用户**”中选择“**编辑**”文本链接

10. 在“**Teams 聊天**”窗格中，添加用户： 
    - Adele Vance
    - Pradeep Gupta

    备注：通过添加这两名用户，Teams 聊天中的包括设置从“所有团队”更改为了仅添加的这两名用户。

11. 选择“**完成**”按钮

12. 在位置页面上，将显示一条通知：已添加 **2 位用户**

13. 选择“**下一步**”按钮。

14. 在“**确定是想要保留内容还是删除内容或两者兼而有之**”页上的“**将项保留特定时间段**”部分中，输入以下信息：

	- 将项保留特定时间段：从下拉列表中选择“**自定义**”
	- 将年字段更改为“**3**”
	- **保留期开始依据**：上次修改项的时间


15. 选择“**下一步**”按钮。

16. 在“**查看并完成**”页面上，选择“**提交**”按钮。

17. 成功创建策略后，选择“**完成**”。

你已成功为 Teams 位置创建了保留策略。你为所有 Teams 频道位置设置了 3 年保留期。你已为“Teams 聊天”位置设置了一个筛选器，以便仅应用于特定用户。

### 任务 3 - 通过 PowerShell 创建保留策略

你将使用 PowerShell 创建相同的保留策略

1. 使用 **“lon-cl1\admin”** 帐户登录到客户端 1 VM (LON-CL1)。

2. 通过使用鼠标右键来选择 Windows 按钮，然后选择 **“Windows PowerShell(管理员)”** 来打开提升的 PowerShell 窗口，如果遇到“用户帐户控制”窗口，则选择 **“是”**。

3. 使用以下 cmdlet 连接到租户中的“安全与合规中心”：

    `Connect-IPPSSession`

4. 如果出现登录对话框提示，请以 **MOD 管理员**身份 admin@WWLxZZZZZZ.onmicrosoft.com（其中 ZZZZZZ 是实验室托管服务提供程序提供的唯一租户 ID）登录。  管理员的密码应由实验室托管提供程序提供。

5. 运行以下 cmdlet 为所有位置（Teams 除外）创建第一个保留策略：

    `New-RetentionCompliancePolicy -Name "Company Wide PS" -ExchangeLocation All -ModernGroupLocation All -PublicFolderLocation All -SharePointLocation All -OneDriveLocation All`

6. 运行以下 cmdlet 以基于修改日期设置保留期（以天为单位）：
	
    `New-RetentionComplianceRule -Name "Company Wide PS Rule" -Policy "Company Wide PS" -RetentionDuration 1095 -ExpirationDateOption ModificationAgeInDays -RetentionComplianceAction Keep`

7. 运行以下 cmdlet，为 Teams 位置创建第二个保留策略：

    `New-RetentionCompliancePolicy -Name "Teams Retention PS" -TeamsChannelLocation All -TeamsChatLocation "Adele Vance", "Pradeep Gupta"`

8. 运行以下 cmdlet，以天为单位设置保留期：

    `New-RetentionComplianceRule -Name "Teams Retention PS Rule" -Policy "Teams Retention PS" -RetentionDuration 1095 -RetentionComplianceAction Keep`

你已通过 PowerShell 成功创建了保留策略，其保留期为 3 年。

# 继续进行实验室 3 - 练习 2
