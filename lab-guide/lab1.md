Microsoft Fabric

Fabric Analyst in a Day

Lab 0

Microsoft Fabric

Fabric Analyst in a Day

Lab 1

Lab 0
# ![](Aspose.Words.75ea6829-7998-4d6f-8e60-59d82c1678ac.001.png)

# Contents
[Introduction	3]()

[Fabric Workspace	3]()

[How** to create trial Fabric workspace:	3]()

[Overview of Fabric Experiences:	5]()

[How** to create a New workspace:	11]()

[How** to create a Lakehouse:	12]()

[References	14]()


#
#
#
#
#
#
#
#
#
#
#
#
# <a name="_toc150852461"></a>**Introduction** 
Today you will learn about various key features of Fabric. This is an introductory course intended to expose you to the various artifacts product experiences and items available in Fabric.  By the end of this course workshop you will learn how to use Lakehouse, Dataflow Gen 2, Data Pipeline and use DirectLake feature.

By the end of this lab, you will have learned: 

- How to create a Fabric workspace
- How create a Lakehouse  

# <a name="_toc150852462"></a>**Fabric Workspace**
### <a name="_toc150852463"></a>How** to create trial Fabric workspace:

1. Open the **browser** and navigate to <https://app.powerbi.com/>. You will be navigated to the login page.
1. Note: If you have an existing Power BI account, you may want to use the browser in private/incognito mode.
1. Enter the **Email** provided by the instructor and click **Submit.**

![A screenshot of create account page](Aspose.Words.75ea6829-7998-4d6f-8e60-59d82c1678ac.002.png)

1. You will be navigated to the **password** screen. Enter the password shared with you by the instructor. 
1. Click **Sign in** and follow the prompts to sign in to Fabric.

![A sceenshot of the enter password page](Aspose.Words.75ea6829-7998-4d6f-8e60-59d82c1678ac.003.png)

1. You will be navigated to the familiar **Power BI Service landing page**.
1. We assume you are familiar with the layout of Power BI Service. If you have any questions, please do not hesitate to ask the instructor.

Currently, you are in **My Workspace**. To work with the Fabric artifactsitems, you will need a trial license and a workspace that has Fabric license. Let’s do this.

1. On the top right corner of the screen, select the **user** **icon**.
1. Select **Start trial**.

![A screenshot of start trial]

1. Upgrade to a free Microsoft Fabric trial dialog opens. Select **Start trial**.

![A screenshot of upgrade to free trial]

1. Once successful, select **Stay in current workspace**.
1. Once successful, select Stay in current workspace.
1. On the **bottom** left of the screen, select **Power BI**. A dialog opens with all the options available in Fabric. In this course we will be learning how to create and work with some of these artifacts.


![A screenshot of Fabric experiences options](Aspose.Words.75ea6829-7998-4d6f-8e60-59d82c1678ac.006.png)

Currently, you are in **My Workspace**. To work with the Fabric artifacts, you will need a trial license and a workspace that has Fabric license. Let’s do this.

1. On the top right corner of the screen, select the **user** **icon**.
1. Select **Start trial**.

![A screenshot of a computer

Description automatically generated]

1. Upgrade to a free Microsoft Fabric trial dialog opens. Select **Start trial**.

![A screenshot of a computer

Description automatically generated]

1. Once successful, select **Stay in current workspace**.
1. Select **Workspaces** from the left navigation bar. A dialog opens.
1. Select **New workspace**.

![A screenshot of a computer

Description automatically generated]

1. **Create a workspace** dialog opens on the right side of the browser.
1. In the **Name** field enter **FAIAD\_<yourusername>**. Note: Workspace name must be unique. We are using FAIAD as the workspace name for this document. However, your workspace name will be different. Make sure a green check mark with “**This name is available**” is displayed below the Name field.
1. If you choose to, you can enter a **Description** for the workspace. This is an optional field.
1. Click on **Advanced** to expand the section.

![A screenshot of a computer

Description automatically generated]

1. Under **License mode**, make sure **Trial** is selected. (It should be selected by default)
1. Select **Apply** to create a new workspace.

![A screenshot of a computer

Description automatically generated]

A new workspace is created, and you will be navigated into this workspace. We will bring data from the different data sources into Lakehouse and use the data from the Lakehouse to build our model and report on it. The first step is to create a Lakehouse.

### How** to create a Lakehouse:<a name="_toc150852464"></a>Overview of Fabric Experiences:

1. Select **Power BI** on the bottom left of your screen. A dialog with the list of Fabric experiences will open. Let’s explore these.
1. Select Data Factory.
1. ![A screenshot of a dialog to select Data Factory experience](Aspose.Words.75ea6829-7998-4d6f-8e60-59d82c1678ac.012.png)
1. You are navigated to Data Factory Home page. The page contains 3 main sections. 
   1. New: This lists the items available in Data Factory – Dataflow Gen2 and Data pipeline.
      1. Dataflow Gen2 is the next generation of Dataflow.
      1. Data pipeline is used for data orchestration.
   1. Recommended: This section provides access to quick start learning documentation.
   1. Quick Access: This section lists the recently used or favorite items.
   1. ![A screenshot of Data Factory Home page](Aspose.Words.75ea6829-7998-4d6f-8e60-59d82c1678ac.013.png)
1. Select **Data Factory** on the bottom left of your screen. Fabric experience dialog opens.
1. ![A screenshot of dialog to select Data Activator](Aspose.Words.75ea6829-7998-4d6f-8e60-59d82c1678ac.014.png)
1. Select **Data Activator** from the dialog. You will be navigated to Data Activator Home. Data Activator is a no-code experience in Microsoft Fabric for automatically taking actions when patterns or conditions are detected in changing data. Notice the 3 sections are like Data Factory experience. In the New section notice the items.
   1. **Reflex:** Used to monitor datasets, queries and event streams for patterns.
   1. **Reflex sample:** Sample solution.
1. ![A screenshot of Data Activator Home page](Aspose.Words.75ea6829-7998-4d6f-8e60-59d82c1678ac.015.png)
1. Select **Data Activator** on the bottom left of your screen. Fabric experience dialog opens.
1. Select **Data Engineering**. In the New section notice the items. 
   1. **Lakehouse:** Used to store big data for cleaning, querying, reporting, sharing.
   1. **Notebook:** Used to run queries on the data to produce shareable tables and visuals.
   1. **Spark Job Definition:** Used to define, schedule and manage apache jobs.
   1. **Data pipeline:** Used to orchestrate data solution.
   1. **Import notebook:** Used to import notebooks from local machine.
   1. **Use a sample:** Used to create a sample.
   1. ![A screenshot of Data Engineering Home page](Aspose.Words.75ea6829-7998-4d6f-8e60-59d82c1678ac.016.png)
   1. Select **Data Engineering** on the bottom left of your screen. Fabric experience dialog opens.
1. Select Data Science. You will be navigated to Data Science Home. Again, there are 3 sections. In the New section notice the items.
   1. Model:** Used to create machine learning models.
   1. Experiment:** Used to create, run and track development of multiple models.
   1. Notebook:** Used to explore data and build machine learning solutions.
   1. Import Notebook:** Used to import notebooks from local machine.
   1. Sample:** S**ample solution.**
   1. ![A screenshot of Data Science Home page](Aspose.Words.75ea6829-7998-4d6f-8e60-59d82c1678ac.017.png)
1. Select **Data Science** on the bottom left of your screen. Fabric experience dialog opens.
1. Select **Data Warehouse**. You will be navigated to Data Warehouse Home. Again, there are 3 sections. In the New section notice the items. Notice Data pipeline and Dataflow Gen2 are available here as well.
   1. **Warehouse: Used to provide strategic insights from multiple sources.**
   1. **Sample warehouse:** Sample warehouse solution.
   1. **Data pipeline:** Used to orchestrate data solution.
   1. **Dataflow Gen2:** Next generation of Dataflow.
   1. ![A screenshot of Data Warehouse Home page](Aspose.Words.75ea6829-7998-4d6f-8e60-59d82c1678ac.018.png)
1. Select **Data Warehouse** on the bottom left of your screen. Fabric experience dialog opens.
1. Select **Real-Time Analytics**. You will be navigated to Real-Time Analytics Home. Again, there are 3 sections. In the New section notice the items. 
   1. **KQL Database:** Used to rapidly load structured, unstructured, and streaming data for querying.
   1. **KQL Queryset:** Used to run queries on the data to produce shareable tables and visuals.
   1. **Eventstream:** Used to capture, transform and route real time event stream.
   1. **Use a sample:** Used to create a sample.
1. ![A screenshot of Real Time Analytics Home page](Aspose.Words.75ea6829-7998-4d6f-8e60-59d82c1678ac.019.png)Select **Data Engineering**. (Lakehouse is a Data Engineering artifact).

![A screenshot of a computer

Description automatically generated](Aspose.Words.75ea6829-7998-4d6f-8e60-59d82c1678ac.020.png) <a name="_toc150852465"></a>How** to create a New workspace:

1. Now let’s create a workspace with Fabric license. Select **Workspaces** from the left navigation bar. A dialog opens.
1. Select **New workspace**.

   ![A screenshot of New workspace dialog]

1. **Create a workspace** dialog opens on the right side of the browser.
1. In the **Name** field enter **FAIAD\_<yourusername>**. Note: Workspace name must be unique. We are using FAIAD as the workspace name for this document. However, your workspace name will be different. Make sure a green check mark with “**This name is available**” is displayed below the Name field.
1. If you choose to, you can enter a **Description** for the workspace. This is an optional field.
1. Click on **Advanced** to expand the section.

![A screenshot of Create a workspace dialog]

1. Under **License mode**, make sure **Trial** is selected. (It should be selected by default)
1. Select **Apply** to create a new workspace.

![A screenshot to select trial license]

A new workspace is created, and you will be navigated into this workspace. We will bring data from the different data sources into Lakehouse and use the data from the Lakehouse to build our model and report on it. The first step is to create a Lakehouse.
### <a name="_toc150852466"></a>How** to create a Lakehouse:

1. Select **Real-Time Analytics** on the bottom left of your screen. Fabric experience dialog opens.
1. Select Data **Engineering** to be navigated to Data Engineering experience.
1. ![A screenshot of dialog to select Data Engineering](Aspose.Words.75ea6829-7998-4d6f-8e60-59d82c1678ac.024.png)
1. Under New, you will find various options like Lakehouse, Notebook, Data Pipeline, etc. Select **Lakehouse (Preview)**.

![A screenshot of Data Engineering home page](Aspose.Words.75ea6829-7998-4d6f-8e60-59d82c1678ac.025.png)

1. A dialog requesting **Lakehouse Name** opens. Enter **lh\_FAIAD** (lh here refers to Lakehouse.).
1. Note: lh here refers to Lakehouse. We are prefixing lh so that it is easy to identify and search.
1. Select **Create**.

![A screenshot of dialog to name the Lakehouse](Aspose.Words.75ea6829-7998-4d6f-8e60-59d82c1678ac.026.png)

Within a few moments, a Lakehouse is created, and you will be navigated to the Lakehouse interface.

On the **left panel**, notice that below your workspace, you will have the Lakehouse icon. You can easily navigate to the Lakehouse by clicking on this icon at any time.

Within the Lakehouse explorer you will notice **Tables** and **Files**. Lakehouse could expose Azure Data Lake Gen2 files under the files section, or a dataflow could load data to Lakehouse tables. There are various options available. We are going to show you some of the options as in the following labs.


![A screenshot of LakeHouse](Aspose.Words.75ea6829-7998-4d6f-8e60-59d82c1678ac.027.png)

In this lab, we explored the Fabric interface, created a Fabric workspace and a Lakehouse. In the next lab, we will learn how to use Dataflow Gen2 to connect to ADLS Gen2 to extract, transform and ingest data into the Lakehouse.

# <a name="_toc150777627"></a><a name="_toc150852467"></a>**References**
Fabric Analyst in a Day introduces you to some of the key functions available in Microsoft Fabric. In the menu of the service, the Help section has links to some great resources.

![A screenshot of help options](Aspose.Words.75ea6829-7998-4d6f-8e60-59d82c1678ac.028.png)

Here are a few more resources that will help you with your next steps with Microsoft Fabric.

- See blog post to read the full [Microsoft Fabric GA announcement](https://aka.ms/Fabric-Hero-Blog-Ignite23)
- Explore Fabric through the [Guided Tour](https://aka.ms/Fabric-GuidedTour)
- Sign up for the [Microsoft Fabric free trial](https://aka.ms/try-fabric)
- Visit the [Microsoft Fabric website](https://aka.ms/microsoft-fabric)
- Learn new skills by exploring the [Fabric Learning modules](https://aka.ms/learn-fabric)
- Explore the [Fabric technical documentation](https://aka.ms/fabric-docs)
- Read the [free e-book on getting started with Fabric](https://aka.ms/fabric-get-started-ebook)

Read the more in-depth Fabric experience announcement blogs:

- [Data Factory experience in Fabric blog](https://aka.ms/Fabric-Data-Factory-Blog) 
- [Synapse Data Engineering experience in Fabric blog](https://aka.ms/Fabric-DE-Blog) 
- [Synapse Data Science experience in Fabric blog](https://aka.ms/Fabric-DS-Blog) 
- [Synapse Data Warehousing experience in Fabric blog](https://aka.ms/Fabric-DW-Blog) 
- [Synapse Real-Time Analytics experience in Fabric blog](https://aka.ms/Fabric-RTA-Blog)
- [Power BI announcement blog](https://aka.ms/Fabric-PBI-Blog)
- [Data Activator experience in Fabric blog](https://aka.ms/Fabric-DA-Blog) 
- [Administration and governance in Fabric blog](https://aka.ms/Fabric-Admin-Gov-Blog)
- [OneLake](https://aka.ms/Fabric-OneLake-Blog)[ in Fabric blog](https://aka.ms/Fabric-OneLake-Blog)
- [Dataverse and Microsoft Fabric integration blog](https://aka.ms/Dataverse-Fabric-Blog)

Here are a few more resources that will help you with your next steps with Microsoft Fabric.

- See blog post to read the full [Microsoft Fabric preview announcement](https://aka.ms/build2023-fabricblog)
- [Sign up for the Microsoft Fabric free trial](https://aka.ms/try-fabric)
- [Visit the Microsoft Fabric website](https://aka.ms/microsoft-fabric)
- Learning path: [Get started with Microsoft Fabric - Training | Microsoft Learn](https://learn.microsoft.com/en-us/training/paths/get-started-fabric/)
- Webinar series: [Microsoft Fabric Webinar Series](https://info.microsoft.com/ww-landing-introduction-to-microsoft-fabric-webinar-series.html?lcid=en-us)

Read the more in-depth Fabric experience announcement blogs:

- [Data Factory experience in Fabric blog](https://aka.ms/Fabric-Data-Factory-Blog) 
- [Synapse Data Engineering experience in Fabric blog](https://aka.ms/Fabric-DE-Blog) 
- [Synapse Data Science experience in Fabric blog](https://aka.ms/Fabric-DS-Blog) 
- [Synapse Data Warehousing experience in Fabric blog](https://aka.ms/Fabric-DW-Blog) 
- [Synapse Real-Time Analytics experience in Fabric blog](https://aka.ms/Fabric-RTA-Blog)
- [Power BI announcement blog](https://aka.ms/Fabric-PBI-Blog)
- [Data Activator experience in Fabric blog](https://aka.ms/Fabric-DA-Blog) 
- [Administration and governance in Fabric blog](https://aka.ms/Fabric-Admin-Gov-Blog)
- [OneLake](https://aka.ms/Fabric-OneLake-Blog)[ in Fabric blog](https://aka.ms/Fabric-OneLake-Blog)
- [Microsoft 365 data integration in Fabric blog](https://aka.ms/buil2023-m365-fabric-blog)
- [Dataverse and Microsoft Fabric integration blog](https://aka.ms/Dataverse-Fabric-Blog)
- Explore the [Fabric technical documentation](https://aka.ms/fabric-docs)
- Read the [free e-book on getting started with Fabric](https://aka.ms/fabric-get-started-ebook)
- Watch the [free Fabric webinar series](https://aka.ms/fabric-webinar-series)
- Explore Fabric through the [Guided Tour](https://aka.ms/Fabric-GuidedTour)

© 2023 Microsoft Corporation. All rights reserved.

By using this demo/lab, you agree to the following terms:

The technology/functionality described in this demo/lab is provided by Microsoft Corporation for purposes of obtaining your feedback and to provide you with a learning experience. You may only use the demo/lab to evaluate such technology features and functionality and provide feedback to Microsoft. You may not use it for any other purpose. You may not modify, copy, distribute, transmit, display, perform, reproduce, publish, license, create derivative works from, transfer, or sell this demo/lab or any portion thereof.

COPYING OR REPRODUCTION OF THE DEMO/LAB (OR ANY PORTION OF IT) TO ANY OTHER SERVER OR LOCATION FOR FURTHER REPRODUCTION OR REDISTRIBUTION IS EXPRESSLY PROHIBITED.

THIS DEMO/LAB PROVIDES CERTAIN SOFTWARE TECHNOLOGY/PRODUCT FEATURES AND FUNCTIONALITY, INCLUDING POTENTIAL NEW FEATURES AND CONCEPTS, IN A SIMULATED ENVIRONMENT WITHOUT COMPLEX SET-UP OR INSTALLATION FOR THE PURPOSE DESCRIBED ABOVE. THE TECHNOLOGY/CONCEPTS REPRESENTED IN THIS DEMO/LAB MAY NOT REPRESENT FULL FEATURE FUNCTIONALITY AND MAY NOT WORK THE WAY A FINAL VERSION MAY WORK. WE ALSO MAY NOT RELEASE A FINAL VERSION OF SUCH FEATURES OR CONCEPTS. YOUR EXPERIENCE WITH USING SUCH FEATURES AND FUNCITONALITY IN A PHYSICAL ENVIRONMENT MAY ALSO BE DIFFERENT.

**FEEDBACK**. If you give feedback about the technology features, functionality and/or concepts described in this demo/lab to Microsoft, you give to Microsoft, without charge, the right to use, share and commercialize your feedback in any way and for any purpose. You also give to third parties, without charge, any patent rights needed for their products, technologies and services to use or interface with any specific parts of a Microsoft software or service that includes the feedback. You will not give feedback that is subject to a license that requires Microsoft to license its software or documentation to third parties because we include your feedback in them. These rights survive this agreement.

MICROSOFT CORPORATION HEREBY DISCLAIMS ALL WARRANTIES AND CONDITIONS WITH REGARD TO THE DEMO/LAB, INCLUDING ALL WARRANTIES AND CONDITIONS OF MERCHANTABILITY, WHETHER EXPRESS, IMPLIED OR STATUTORY, FITNESS FOR A PARTICULAR PURPOSE, TITLE AND NON-INFRINGEMENT. MICROSOFT DOES NOT MAKE ANY ASSURANCES OR REPRESENTATIONS WITH REGARD TO THE ACCURACY OF THE RESULTS, OUTPUT THAT DERIVES FROM USE OF DEMO/ LAB, OR SUITABILITY OF THE INFORMATION CONTAINED IN THE DEMO/LAB FOR ANY PURPOSE.

**DISCLAIMER**

This demo/lab contains only a portion of new features and enhancements in Microsoft Power BI. Some of the features might change in future releases of the product. In this demo/lab, you will learn about some, but not all, new features.
Version: 11.15.2023                                Copyright 2023 Microsoft   	                                                         19|Page 

Maintained by:  Microsoft Corporation 

[A screenshot of start trial]: Aspose.Words.75ea6829-7998-4d6f-8e60-59d82c1678ac.004.png
[A screenshot of upgrade to free trial]: Aspose.Words.75ea6829-7998-4d6f-8e60-59d82c1678ac.005.png
[A screenshot of a computer

Description automatically generated]: Aspose.Words.75ea6829-7998-4d6f-8e60-59d82c1678ac.007.png
[A screenshot of a computer

Description automatically generated]: Aspose.Words.75ea6829-7998-4d6f-8e60-59d82c1678ac.008.png
[A screenshot of a computer

Description automatically generated]: Aspose.Words.75ea6829-7998-4d6f-8e60-59d82c1678ac.009.png
[A screenshot of a computer

Description automatically generated]: Aspose.Words.75ea6829-7998-4d6f-8e60-59d82c1678ac.010.png
[A screenshot of a computer Description automatically generated]: Aspose.Words.75ea6829-7998-4d6f-8e60-59d82c1678ac.011.png
[A screenshot of New workspace dialog]: Aspose.Words.75ea6829-7998-4d6f-8e60-59d82c1678ac.021.png
[A screenshot of Create a workspace dialog]: Aspose.Words.75ea6829-7998-4d6f-8e60-59d82c1678ac.022.png
[A screenshot to select trial license]: Aspose.Words.75ea6829-7998-4d6f-8e60-59d82c1678ac.023.png