# Microsoft Fabric - Fabric Analyst in a Day - Lab 1

# ![](../media/new1.png)

# Contents
- Document Structure
- Scenario / Problem Statement
- Overview of Power BI Desktop Report
   - Task 1: Set up Power BI Desktop in lab environment
   - Task 2: Analyze Power BI Desktop Report
   - Task 3: Review Power Queries
- References

# Document Structure
The lab includes steps for the user to follow along with associated screenshots that provide visual aid. In each screenshot, sections are highlighted with orange boxes to indicate the area(s) the user should focus on.

# Scenario / Problem Statement
Fabrikam, Inc. is a wholesale novelty goods distributor. As a wholesaler, Fabrikam’s customers are mostly companies that resell to individuals. Fabrikam sells to retail customers across the United States including specialty stores, supermarkets, computing stores, and tourist attraction shops. Fabrikam also sells to other wholesalers via a network of agents who promote the products on Fabrikam’s behalf. While all of Fabrikam's customers are currently based in the United States, the company intends to push for expansion into other countries/regions.

You are a Data Analyst in the Sales team. You collect, clean, and interpret data sets to solve business problems. You also put together visualizations like charts and graphs, write reports, and present them to the decision-makers in the organization.

In order to draw valuable insights from the data, you pull data from multiple systems, clean it and mash it up together. You pull data from the following sources:

- **Sales Data:** comes from the ERP system and data is stored in an ADLS Gen2 database or             Databricks. It gets updated at noon / 12 PM every day.
- **Supplier Data:** comes from different suppliers and data is stored in a Snowflake database.        It gets updated at midnight / 12 AM every day.
- **Customer Data:** comes from Customer Insights and data is stored in Dataverse. The data is         always up to date.
- **Employee Data:** comes from the HR system; it is stored as an export file in a SharePoint         folder. It gets updated every morning at 9 AM.

     ![Picture1FAID](https://github.com/CloudLabsAI-Azure/Fabric-Analytics-in-aday/assets/121504071/e236d8ac-890d-4f7b-93f5-e8d163e3b878)
  
You are currently building a dataset on Power BI Premium that pulls the data from the above source systems in order to satisfy your reporting needs as well as provide end users with the ability to self-serve. You use Power Query to update your model. 

**You are facing the following challenges:**
   - You need to refresh your dataset at least three times a day to accommodate the different         update times for the different data sources.
   - Your refreshes take a long time as you need to do a full refresh every time to capture any       updates that happened to the source systems.
   - Any errors in any of the data sources that you are pulling from will result in your dataset      refresh breaking. A lot of times the employee file does not upload on time resulting in          your dataset refresh breaking.
   - It takes a very long time to make any changes to your data model as Power Query takes a          long time to refresh your previews, given the large data sizes and complex transformations.
   - You need a Windows PC to use Power BI Desktop even though the corporate standard is Mac.

You heard about Microsoft Fabric and decided to try it to see if it will address your challenges.

# Overview of Power BI Desktop Report
Before we start with Fabric, let’s look at the current Report in Power BI Desktop to understand the transformations and the model.
### Task 1: Set up Power BI Desktop in lab environment
1. Open the **FAIAD.pbix** located in the **Report** folder on the **Desktop** of your lab environment. The file will open in Power BI Desktop.

      ![Picture2FAID](https://github.com/CloudLabsAI-Azure/Fabric-Analytics-in-aday/assets/121504071/ce64a7c3-6bb5-45d0-8ced-fc923145805c)

3. Enter your email address dialog opens. Navigate to the **Environment Details** tab on the right panel in the lab environment.
4. Copy the **Username Credentials** and paste it into the Email textbox of the dialog.
5. Select **Continue**.
 
      ![Picture3FAID](https://github.com/CloudLabsAI-Azure/Fabric-Analytics-in-aday/assets/121504071/ab7ccb1c-d41b-41c3-86e6-baccf6506361)
   
7. Let’s get you signed in dialog opens. Select **Work or school account**.
8. Select **Continue**.

      ![Picture4FAID](https://github.com/CloudLabsAI-Azure/Fabric-Analytics-in-aday/assets/121504071/d1908a37-3197-4c08-9fe6-73dfcb91f997)
   
10. Sign-in dialog opens. Reenter the **Username Credentials** by copying it from the **Environment Details** tab.
11. Select **Next**.
    
       ![Picture5FAID](https://github.com/CloudLabsAI-Azure/Fabric-Analytics-in-aday/assets/121504071/a3931a21-f2a9-48bd-8807-306f300a4c45)

12. In the next dialog, reenter the **Password Credentials** by copying it from the **Environment Details** tab.
13. Select **Sign in**.
14. Action Required dialog opens requesting to set up multifactor authentication. We do not need to set this up, since this is a lab environment. Select **Ask Later**.
    
     ![Picture6FAID](https://github.com/CloudLabsAI-Azure/Fabric-Analytics-in-aday/assets/121504071/999ecb8b-4854-4a3a-84f3-bd85e3daa77b)
    
15. Select **No, sign in the app** only in the next dialog. Power BI Desktop will now open.

### Task 2: Analyze Power BI Desktop Report
   The report below analyzes Sales for Fabrikam. KPIs are listed on the left top of the page. The remaining visuals highlight Sales over time, by Territory, Product Group, and Reseller Company. 
   
   ![Picture7FAID](https://github.com/CloudLabsAI-Azure/Fabric-Analytics-in-aday/assets/121504071/1ad8a0d4-5f3b-4dd4-ab15-9b6212a92de8)
     
   **Note:** In this training, we are focusing on data acquisition, transformation, and modeling using tools available in Fabric. We will not be focusing on report development or navigation. Let’s spend a couple of minutes understanding the report and move to the next steps.

1. Let’s analyze data by Sales Territory. Select **New England from the Sales Territory** (Scatter plot) visual.
Notice from the Sales over time, Reseller Tailspin Toys has more sales compared to Wingtip Toys in New England. If you look at the Sales YoY% column chart you will notice that Wingtip Toys sales growth has been low and declining quarter over quarter during the past year. After a small rebound in Q3, it went down again in Q4. 

    ![Picture8FAID](https://github.com/CloudLabsAI-Azure/Fabric-Analytics-in-aday/assets/121504071/b3f38036-16cb-4896-a851-7ff0aefc7c0d)
   
3. Let’s compare this to the Rocky Mountain territory. Select **Rocky Mountain from Sales Territory** (Scatter plot) visual.
Notice in the Sales YoY% column chart, that sales for Wingtip Toys have increased dramatically in 2022 Q4 after being low for the previous two quarters.

      ![Picture9FAID](https://github.com/CloudLabsAI-Azure/Fabric-Analytics-in-aday/assets/121504071/ac85d3d3-3aff-4229-aaf3-302c0dc07506)
   
4. Select **Rocky Mountain from Sales Territory** to remove the filter.
5. From the Scatter plot visual on the bottom center of the screen (Sales Orders by Sales) select the outlier on the top right (4th quadrant).
Notice the margin % is 52%, which is above the average of 50%. Also, the Sales YoY% has gone up in the last two quarters of 2022.

      ![Picture10FAID](https://github.com/CloudLabsAI-Azure/Fabric-Analytics-in-aday/assets/121504071/f0fc3e03-dcd3-47c6-9a34-a5bbd5d196b8)

5. Select the outlier Reseller in the scatter plot visual to **remove the filter**.
6. Let’s get the Product details by Product Group and Reseller. From the Sales by Product Group and Reseller Company bar chart visual, **right click on the Packaging Materials bar for Tailspin Toys** and from the dialog select **Drill through -> Product Detail**.

      ![Picture11FAID](https://github.com/CloudLabsAI-Azure/Fabric-Analytics-in-aday/assets/121504071/6b27ccc9-bc40-43b1-a447-0ded3660642c)

   You will be navigated to the page which provides the Product Details. Notice there are some future orders in place as well.
7. Once you are done reviewing this page, select the **Ctrl+back arrow** on the top right of the page to be navigated back to the Sales Report.
      
    ![Picture12FAID](https://github.com/CloudLabsAI-Azure/Fabric-Analytics-in-aday/assets/121504071/6ff10b89-9d8f-4b2b-bf76-be3d2c1608ab)

8. Feel free to further analyze the report. Once ready let’s look at the model view. From the left panel, select **Model view icon**. Notice there are two fact tables, Sales and PO.

      1. Granularity of Sales data is by Date, Reseller, Product, and People. Date, Reseller, Product, and People connect to Sales.
      2. Granularity of PO data is by Date, Product, and People. Date, Product, and People connect to PO.
      3. We have Supplier data by Product. Supplier connects to Product.
      4. We have Reseller’s location data by Geo. Geo connects to the Reseller.
      5. We have Customer information by Reseller. The customer connects to the Reseller.

### Task 3: Review Power Queries
1. Let’s look at Power Query to understand the data sources. From the ribbon select **Home -> Transform data**.

      ![Picture13FAID](https://github.com/CloudLabsAI-Azure/Fabric-Analytics-in-aday/assets/121504071/fbfb74a2-d328-4a18-bb6a-7e6fec6d2f82)

2. The Power Query window opens. From the ribbon, select **Home -> Data source settings**. The data source settings dialog opens. As you scroll through the list you will notice there are four main sources as mentioned in the problem statement:

      1. Snowflake
      2. SharePoint
      3. ADLS Gen2
      4. Dataverse

4. Select **Close** to close the Data source settings dialog.

    ![](../media/new12.png)

5. In the left Queries panel, notice the queries are grouped by data source. 
6. Notice **DataverseData** folder has Customer data available in four different queries: BabyBoomer, GenX, GenY, and GenZ. These four queries are appended to create a Customer query.

    ![Picture15](https://github.com/CloudLabsAI-Azure/Fabric-Analytics-in-aday/assets/121504071/7b261b69-164a-4ed1-9cba-bf0839969f77)

1. You can enter the credentials for the Dataverse data source by entering the **Username** and **Password** available in the **Environment Variables** tab (next to the Lab Guide). Please select the Microsoft account option.

      ![](../media/new2.png)

1. For ADLS data source, use the **Account Key** option and enter the **Adls storage account Access key** that is available in the **Environment Variables** tab (next to the Lab Guide).

1. Notice **ADLSData** folder has multiple dimensions: Geo, Product, Reseller, and Date. It also has Sales facts.
   
   1. **Geo dimension** is created by merging data from the Cities, Countries, and States query.
   2. **Product dimension** is created by merging data from Product Groups and Product Item Group query.
   3. **Reseller dimension** is filtered using the BuyingGroup query.
   4. **Sales fact** is created by merging InvoiceLineItems with Invoice query.

1. For ADLS data source, use the **Account Key** option and enter the **Adls storage account Access key** that is available in the **Environment Variables** tab (next to the Lab Guide).

1. Notice **SnowflakeData** folder has a Supplier dimension and PO (Order / Spend) fact.

   1. **Supplier dimension** is created by merging the Suppliers query with the SupplierCategories query.
   2. **PO fact** is created by merging PO with PO Line Items query.

1. For the SharePoint data source, enter the **Username** and **Password** available in **Environment Variables** tab (next to Lab guide). Please select the Microsoft account option.

1. Notice **SharepointData** folder has People dimension.

   ![](../media/new3.png)

Now we know what we are dealing with. In the following labs, we will create a similar Power Query using Dataflow Gen2 and a model using Lakehouse.

# References
Fabric Analyst in a Day (FAIAD) introduces you to some of the key functions available in Microsoft Fabric. In the menu of the service, the Help (?) section has links to some great resources.

   ![Picture16](https://github.com/CloudLabsAI-Azure/Fabric-Analytics-in-aday/assets/121504071/13178b86-b21e-4cd1-b34f-4ce4682d1de8)

Here are a few more resources that will help you with your next steps with Microsoft Fabric.

- See the blog post to read the full [Microsoft Fabric GA announcement](https://aka.ms/Fabric-Hero-Blog-Ignite23)
- Explore Fabric through the [Guided Tour](https://aka.ms/Fabric-GuidedTour)
- Sign up for the [Microsoft Fabric free trial](https://aka.ms/try-fabric)
- Visit the [Microsoft Fabric website](https://aka.ms/microsoft-fabric)
- Learn new skills by exploring the [Fabric Learning modules](https://aka.ms/learn-fabric)
- Explore the [Fabric technical documentation](https://aka.ms/fabric-docs)
- Read the [free e-book on getting started with Fabric](https://aka.ms/fabric-get-started-ebook)
- Join the [Fabric community ](https://aka.ms/fabric-community) to post your questions, share      your feedback, and learn from others

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

© 2023 Microsoft Corporation. All rights reserved.

By using this demo/lab, you agree to the following terms:

The technology/functionality described in this demo/lab is provided by Microsoft Corporation for the purposes of obtaining your feedback and providing you with a learning experience. You may only use the demo/lab to evaluate such technology features and functionality and provide feedback to Microsoft. You may not use it for any other purpose. You may not modify, copy, distribute, transmit, display, perform, reproduce, publish, license, create derivative works from, transfer, or sell this demo/lab or any portion thereof.

COPYING OR REPRODUCTION OF THE DEMO/LAB (OR ANY PORTION OF IT) TO ANY OTHER SERVER OR LOCATION FOR FURTHER REPRODUCTION OR REDISTRIBUTION IS EXPRESSLY PROHIBITED.

THIS DEMO/LAB PROVIDES CERTAIN SOFTWARE TECHNOLOGY/PRODUCT FEATURES AND FUNCTIONALITY, INCLUDING POTENTIAL NEW FEATURES AND CONCEPTS, IN A SIMULATED ENVIRONMENT WITHOUT COMPLEX SET-UP OR INSTALLATION FOR THE PURPOSE DESCRIBED ABOVE. THE TECHNOLOGY/CONCEPTS REPRESENTED IN THIS DEMO/LAB MAY NOT REPRESENT FULL FEATURE FUNCTIONALITY AND MAY NOT WORK THE WAY A FINAL VERSION MAY WORK. WE ALSO MAY NOT RELEASE A FINAL VERSION OF SUCH FEATURES OR CONCEPTS. YOUR EXPERIENCE WITH USING SUCH FEATURES AND FUNCTIONALITY IN A PHYSICAL ENVIRONMENT MAY ALSO BE DIFFERENT.

**FEEDBACK**. If you give feedback about the technology features, functionality and/or concepts described in this demo/lab to Microsoft, you give to Microsoft, without charge, the right to use, share and commercialize your feedback in any way and for any purpose. You also give to third parties, without charge, any patent rights needed for their products, technologies and services to use or interface with any specific parts of a Microsoft software or service that includes the feedback. You will not give feedback that is subject to a license that requires Microsoft to license its software or documentation to third parties because we include your feedback in them. These rights survive this agreement.

MICROSOFT CORPORATION HEREBY DISCLAIMS ALL WARRANTIES AND CONDITIONS WITH REGARD TO THE DEMO/LAB, INCLUDING ALL WARRANTIES AND CONDITIONS OF MERCHANTABILITY, WHETHER EXPRESS, IMPLIED OR STATUTORY, FITNESS FOR A PARTICULAR PURPOSE, TITLE AND NON-INFRINGEMENT. MICROSOFT DOES NOT MAKE ANY ASSURANCES OR REPRESENTATIONS WITH REGARD TO THE ACCURACY OF THE RESULTS, OUTPUT THAT DERIVES FROM USE OF DEMO/ LAB, OR SUITABILITY OF THE INFORMATION CONTAINED IN THE DEMO/LAB FOR ANY PURPOSE.

**DISCLAIMER**

This demo/lab contains only a portion of new features and enhancements in Microsoft Power BI. Some of the features might change in future releases of the product. In this demo/lab, you will learn about some, but not all, new features.

