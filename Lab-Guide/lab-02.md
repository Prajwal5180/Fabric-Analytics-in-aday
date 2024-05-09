 目录
简介	3
Fabric 许可证	3
任务 1：启用Microsoft Fabric 试用许可证	3
Fabric 体验概述	6
任务 2：Data Factory 体验	6
任务 3：Data Activator 体验	7
任务 4：Industry Solutions 体验	8
任务 5：Synapse Data Engineering 体验	9
任务 6：Synapse Data Science 体验	10
任务 7：Synapse Data Warehouse 体验	11
任务 8：Real-Time Analytics 体验	12
Fabric 工作区	13
任务 9：创建Fabric 工作区	13
任务 10：创建 Lakehouse	15
参考	17

 
简介
今天，您将学习Microsoft Fabric 的多种主要功能。这是一个介绍性研讨会，旨在向您介绍Fabric 中提供的各种产品体验和项目。在本次研讨会结束时，您将学习如何使用 Lakehouse、数据流 Gen2、数据管道和 DirectLake 功能。
本实验结束后，您将学会：
•	如何创建 Fabric 工作区
•	如何创建 Lakehouse


Fabric 许可证
任务 1：启用Microsoft Fabric 试用许可证
1.	打开浏览器并导航到  https://app.powerbi.com/。您将导航到登录页。
注意：如果您未使用实验环境，并且已经有 Power BI 帐户，您可能希望在隐私/无痕模式下使用浏览器。
2.	输入用户名，其位于环境变量选项卡中（“实验指南”选项卡旁边），作为电子邮件地址，然后点击 Submit。
3.	您将导航到密码屏幕。输入讲师提供给您的密码，其位于环境变量选项卡中（“实验指南”选项卡旁边）。
4.	点击 Sign in 并按照提示登录Fabric。
 
 
5.	您将导航到熟悉的 Power BI 服务主页。
6.	我们相信您熟悉Power BI 服务的布局。如果您有任何问题，请随时询问讲师。

您当前位于我的工作区。要使用 Fabric 项目，您需要试用许可证和具有Fabric 许可证的工作区。让我们开始设置。

7.	在屏幕右上角，选择用户图标。
8.	选择 Start trial。

9.	“升级到 Microsoft Fabric 免费试用版”对话框随即打开。选择开始试用。
 

10.	选择 Just one last step 对话框右上角的“X”关闭对话框。这是一个实验环境，因此我们不会提供这些详细信息。
 
 

11.	“已成功升级到Microsoft Fabric”对话框随即打开。选择 Fabric Home Page。

12.	您将导航到 Microsoft Fabric 主页。
 
 
Fabric 体验概述
任务 2：Data Factory 体验
1.	选择屏幕左下角的 Microsoft Fabric（Fabric 体验选择器）图标。将打开一个包含Fabric 体验列表的对话框。请注意，Power BI、Data Factory、Data Activator 和Industry Solutions 是独立的体验。Data Engineering、Data Science、Data Warehouse 和Real-Time Analytics 是Synapse 体验，这四种体验均由Synapse 提供支持。我们来探索吧。
2.	选择 Data Factory。

3.	您将导航到 Data Factory 主页页面。该页面包含三个主要部分。
a.	New：这里列出了 Data Factory - Dataflow Gen2 和 Data pipeline 中的可用项目。
i.	Dataflow Gen2 是新一代数据流。
ii.	Data pipeline 用于数据编排。
b.	Recommended：这一部分可用于访问快速入门学习文档。
c.	Quick Access：这一部分列出了最近使用或收藏的项目。
 
 

任务 3：Data Activator 体验
1.	选择屏幕左下角的 Fabric 体验选择器图标（目前设为 Data Factory）。Fabric 体验对话框随即打开。

2.	从对话框选择 Data Activator。您将导航到 Data Activator 主页。Data Activator 是Microsoft Fabric 中的一种无代码体验，在数据变化中检测到模式或条件时自动采取操作。请注意， 这三个部分与 Data Factory 体验相似。在“新建”部分中，请注意以下项：
a.	Reflex：用于监视数据集、查询和事件流中的模式。
b.	Reflex 示例：示例解决方案。
 
 


任务 4：Industry Solutions 体验
1.	选择屏幕左下角的 Fabric 体验选择器图标（目前设置为 Data Activator）。Fabric 体验对话框随即打开。
2.	从对话框中选择 Industry Solutions。您将导航到 Industry Solutions 主页。Microsoft Fabric 提供特定于行业的数据解决方案，这些解决方案为数据管理、分析和决策提供强大的平 台。这些数据解决方案解决了不同行业面临的独特挑战，助力企业优化运营、整合来自不 同来源的数据并使用丰富的分析。请注意，这三个部分与之前的体验相似。在“新建”部 分中，请注意以下项：
a.	可持续性解决方案：支持引入、标准化和分析环境、社会和治理 (ESG)  数据。
b.	零售解决方案：有助于管理大量数据，整合来自各个来源的数据，并提供实时分析 以促进及时做出决策。零售商可以使用这些解决方案进行库存优化、客户细分、销 售预测、动态定价和欺诈检测。

 
任务 5：Synapse Data Engineering 体验
1.	选择屏幕左下角的 Fabric 体验选择器图标（目前设置为Industry Solutions）。Fabric 体验对话框随即打开。
2.	选择 Data Engineering。您将导航到 Data Engineering 主页。该页面也包含三个主要部分。在“New”部分中，请注意以下项：
a.	Lakehouse：用于存储大数据以供清理、查询、报告和共享。
b.	Notebook：使用 Python、R 和 Scala 等各种语言进行数据引入、准备、分析和其他与数据相关的任务。
c.	Environment：用于为笔记本和spark 作业定义设置共享库、spark 计算设置和资源。
d.	Spark Job Definition：用于定义、计划和管理 Apache 作业。
e.	Data pipeline：用于编排数据解决方案。
f.	Import notebook：用于从本地计算机导入笔记本。
g.	Use a sample：示例解决方案。

 
任务 6：Synapse Data Science 体验
1.	选择屏幕左下角的 Fabric 体验选择器图标（目前设置为 Data Engineering）。Fabric 体验对话框随即打开。
2.	选择 Data Science。您将导航到 Data Science 主页。这里也有三个部分。在“New”部分中，请注意以下项：
a.	ML model：用于创建机器学习模型。
b.	Experiment：用于创建、运行和跟踪多个模型的开发。
c.	Notebook：用于探索数据和构建机器学习解决方案。
d.	Environment：用于为笔记本和spark 作业定义设置共享库、spark 计算设置和资源。
e.	Import Notebook：用于从本地计算机导入笔记本。
f.	Use a sample：示例解决方案。
注意：笔记本、环境、数据管道等项目在多种体验中可用，因为它们与每种体验都相关。

 
任务 7：Synapse Data Warehouse 体验
1.	选择屏幕左下角的 Fabric 体验选择器图标（目前设置为 Data Science）。Fabric 体验对话框随即打开。
2.	选择 Data Warehouse。您将导航到 Data Warehouse 主页。这里也有三个部分。在“新建”部分中，请注意以下项：
a.	仓库：用于创建 Data Warehouse。
b.	数据管道：用于编排数据解决方案。

 
任务 8：Real-Time Analytics 体验
1.	选择屏幕左下角的 Fabric 体验选择器图标（目前设置为 Data Warehouse）。Fabric 体验对话框随即打开。
2.	选择 Real-Time Analytics。您将导航到 Real-Time Analytics 主页。这里也有三个部分。在“新建”部分中，请注意以下项：
a.	事件仓库：用于创建数据库的工作区，可跨项目共享。
b.	KQL 数据库：用于快速加载和存储结构化、非结构化和流式数据进行查询。
c.	KQL 查询集：用于对数据运行查询以生成可共享的表和视觉对象。
d.	Eventstream：用于捕获、转换和路由实时事件流。
e.	使用示例：示例解决方案。

 
Fabric 工作区
任务 9：创建Fabric 工作区
1.	现在我们创建一个具有Fabric 许可证的工作区。从左侧导航栏中选择工作区。对话框随即打开。
2.	选择新建工作区。
3.	浏览器右侧将打开创建工作区对话框。
4.	在名称字段中输入 FAIAD_<username>
注意：工作区名称必须唯一。但是，您必须使用不同的工作区名称。确保“名称”字段下方显 示带有“此名称可用”的绿色复选标记。
5.	您可以选择输入工作区的说明。这是选填字段。
6.	点击高级以展开此部分。
 
 
7.	在 License mode 下，确保选择 Trial。（这应该已默认选中。）
8.	选择 Apply 以创建新工作区。
这样就创建了新的工作区，且您将会导航到该工作区。我们将来自不同数据源的数据引入
Lakehouse，并使用 Lakehouse 中的数据来构建模型并生成报表。第一步是创建 Lakehouse。
 
任务 10：创建 Lakehouse
1.	选择屏幕左下角的 Fabric 体验选择器图标（目前设置为Real-Time Analytics）。Fabric 体验对话框随即打开。
2.	选择 Data Engineering 以导航到 Data Engineering 主页。

3.	选择湖屋。
 
4.	New lakehouse 对话框随即打开。在Name 文本框中输入 lh_FAIAD。
注意：这里的 lh 指的是 Lakehouse。我们添加 lh 前缀是为了便于识别和搜索。
5.	选择 Create。
 
 
Lakehouse 很快就会创建完毕，您将导航到 Lakehouse 界面。
在左侧面板中，请注意工作区下方有一个 Lakehouse  图标。您可以随时点击此图标轻松导航到
Lakehouse。

在 Lakehouse Explorer 中会显示表和文件。Lakehouse 的文件部分下可能会显示Azure Data Lake Storage Gen2 文件，或者数据流可能会将数据加载到 Lakehouse 表中。有各种选项可用。我们将在以下实验中向您展示其中一些选项。
在本实验中，我们探索了Fabric 界面，创建了Fabric 工作区和 Lakehouse。在下一个实验中， 我们将学习如何使用数据流 Gen2 连接到 ADLS Gen2 以提取、转换数据并将数据引入 Lakehouse。
 
参考
Fabric Analyst in a Day (FAIAD) 介绍了Microsoft Fabric 中提供的一些主要功能。在服务菜单中， “帮助 (?)”部分包含指向一些优质资源的链接。


以下更多参考资源可帮助您进行与Microsoft Fabric 相关的后续步骤。
•	请参阅博客文章以阅读完整的Microsof t Fabric GA 公告
•	通过引导式教程探索 Fabric
•	注册 Microsof t Fabric 免费试用版
•	访问 Microsof t Fabric 网站
•	通过探索 Fabric 学习模块学习新技能
•	探索 Fabric 技术文档
•	阅读有关Fabric 入门指南的免费电子书
•	加入 Fabric 社区发布问题、分享反馈并向他人学习
 
阅读更多深度Fabric 体验公告博客：
•	Fabric 中的Data Factory 体验博客
•	Fabric 中的Synapse Data Engineering 体验博客
•	Fabric 中的Synapse Data Science 体验博客
•	Fabric 中的Synapse Data Warehousing 体验博客
•	Fabric 中的Synapse Real-Time Analytics 体验博客
•	Power BI 公告博客
•	Fabric 中的Data Activator 体验博客
•	Fabric 中的管理和治理博客
•	Fabric 中的OneLake 博客
•	Dataverse 和Microsof t Fabric 集成博客


© 2023 Microsoft Corporation. 保留所有权利。使用此演示/实验即表示您已同意以下条款：
本演示/实验中的技术/功能由 Microsoft Corporation 出于获取反馈和提供学习体验的目的提供。只能将本演示/实验用于评估这些技术特性和功能以及向Microsoft 提供反馈。不得用于任何其他用途。不得对此演示/实验或其任何部分进行修改、复制、分发、传送、显示、 执行、复制、公布、许可、转让、销售或基于以上内容创建衍生作品。
严禁将本演示/实验（或其任何部分）复制到任何其他服务器或位置以便进一步复制或再 分发。
本演示/实验出于上述目的，在不涉及复杂设置或安装操作的模拟环境中提供特定软件技术
/产品特性和功能，包括潜在的新功能和概念。本演示/实验中展示的技术/概念可能不是完 整的功能，可能会以不同于最终版本的工作方式工作。我们也可能不会发布此类功能或概念的最终版本。在物理环境中使用此类特性和功能的体验可能也有所不同。
反馈。如您针对本演示/实验中所述的技术特性、功能和/或概念向 Microsoft 提供反馈，则意味着您向Microsoft  无偿提供以任何方式、出于任何目的使用和分享您的反馈并将其商业化的权利。您同样无偿为第三方提供其产品、技术和服务使用或配合使用包含此反馈的
Microsoft 软件或服务的任何特定部分所需的任何专利权。如果根据某项许可的规定，
Microsoft  由于在其软件或文档中包含了您的反馈需要向第三方授予该软件或文档的许可， 请不要提供这样的反馈。这些权利在本协议终止后继续有效。
 
对于本演示/实验，Microsoft Corporation 不提供任何明示、暗示或法定的保证和条件，包括有关适销性、针对特定目的的适用性、所有权和不侵权的所有保证和条件。对于使用本 演示/实验产生的结果或输出内容的准确性，或者出于任何目的包含本演示/实验中的信息的适用性，Microsoft 不做任何保证或陈述。
免责声明
本演示/实验仅包含 Microsoft Power BI 的部分新功能和增强功能。在产品的后续版本中， 部分功能可能有所更改。在本演示/实验中，可了解部分新功能，但并非全部新功能。
