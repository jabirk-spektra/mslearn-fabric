# **Cloud Scale Analytics with Microsoft Fabric**

### Overall Estimated Duration: **60 minutes**  

## **Overview**  
**Microsoft Fabric** offers a robust runtime designed for storing and querying data using Kusto Query Language (KQL), which is particularly optimized for time series data, such as real-time logs and IoT device streams. This lab provides an engaging introduction to the capabilities of **KQL**, guiding you through the process of creating a KQL database, performing **data queries**, and **visualizing insights** with **Power BI reports**. By exploring the exciting realm of real-time analytics, you will gain hands-on experience with Microsoft Fabric's powerful tools and learn how to harness KQL for dynamic data analysis and reporting.


## **Objective**  

**Get Started with Real-Time Analytics in Microsoft Fabric:** In this lab, you will learn how to use Microsoft Fabric and Kusto Query Language (KQL) for real-time analytics. You will learn how to create a KQL database, query time-series data efficiently, and develop compelling Power BI reports. By the end of this lab, you will have hands-on experience leveraging Microsoft Fabric to analyze real-time data, such as log files and IoT device streams, and transform insights into actionable visualizations.


## **Prerequisites**  

You should have:  
- **Basic Understanding of KQL:** Familiarity with Kusto Query Language and querying structured data.  

- **Experience with Microsoft Fabric:** General understanding of the Microsoft Fabric environment and its components. 

- **Proficiency in Power BI:** Basic experience in creating and customizing visualizations using Power BI.  

- **Knowledge of Real-Time Data Concepts:** Understanding of time-series data and its applications, such as log files and IoT streams.

## **Architecture**  

The architecture illustrates the workflow for Exercise 1 of the lab, showcasing a three-step process. The first step involves creating a KQL database in Microsoft Fabric, which acts as the foundational storage for time-series or structured data. Once the database is set up, the next step is to use Kusto Query Language (KQL) to query the "Sales" table, retrieving and analyzing data based on specific criteria. Finally, the results of the KQL query are used to create a dynamic Power BI report, enabling visualization and actionable insights. This flow demonstrates the seamless integration of Microsoft Fabric, KQL, and Power BI to perform real-time analytics effectively.

### **Architecture Diagram**  
   ![Navigate-To-AAD](./Images/Arch4.png)
---

## **Explanation of Components**  

The architecture for this lab involves the following key components:
-  **Create a KQL Database:**
In this step, you created a KQL database to store and manage your data. This database serves as the foundation for querying and analyzing data using Kusto Query Language (KQL). The database structure was designed to efficiently organize sales data for further analysis.

- **Use KQL to Query the Sales Table:**
With KQL, you wrote queries to interact with the sales table, filtering and aggregating data to derive meaningful insights. By using various operators and functions, you calculated key metrics, such as total revenue and product-wise sales, enabling more precise data analysis.

- **Create a Power BI Report from a KQL Queryset:**
Using the results from your KQL query, you created a Power BI report that visualizes the data. The report was customized with charts and tables to display the insights clearly, allowing stakeholders to easily interpret and make data-driven decisions based on the sales information.


## Getting Started with the Lab Environment

## Accessing Your Lab Environment

Once you're ready to begin, your virtual machine and lab guide will be available directly within your web browser.

![](./Images/vm00100.png)

## Virtual Machine & Lab Guide

The virtual machine provides access to the Azure Portal and Microsoft security portals.  
The lab guide remains visible throughout the lab exercises.

## Exploring Your Lab Resources

Navigate to the **Environment** tab to review lab resources and credentials.

![](./Images/env01.png)

## Utilizing the Split Window Feature

Use the **Split Window** button in the top-right corner to open the lab guide in a separate window for easier navigation.

![](./Images/splitwin01.png)

## Managing Your Virtual Machine

Start, stop, or restart your virtual machine as needed from the **Resources** tab.

![](./Images/RT1.png)

## Lab Guide Zoom In / Zoom Out

Adjust the zoom level using the **A↕ : 100%** icon located next to the timer.

![](./Images/zoominout1.png)

## Let's Get Started with Azure Portal

1. On the virtual machine, click the **Azure Portal** icon:

    ![](./Images/vm101.png)

1. On the **Sign in to Microsoft Azure** page, enter:

   - **Email/Username:** <inject key="AzureAdUserEmail" enableCopy="true"/>

       ![](./Images/sign1.png)

1. Enter the password:

   - **Password:** <inject key="AzureAdUserPassword" enableCopy="true"/>

      ![](./Images/tpwrd.png)

1. Select **No** when prompted to stay signed in.

   ![](./Images/sign001.png)

## Support Contact

CloudLabs support is available 24/7 to assist learners and instructors.

- **Email:** cloudlabs-support@spektrasystems.com  
- **Live Chat:** https://cloudlabs.ai/labs-support  

Now, click on **Next** from the lower right corner to move on to the next page. 

![](./Images/next.png)

### Happy Learning!!
