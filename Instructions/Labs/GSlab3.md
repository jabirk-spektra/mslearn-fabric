# **Cloud Scale Analytics with Microsoft Fabric**

### Overall Estimated Duration: **120 minutes**  

## **Overview**  
In **Microsoft Fabric**, a data warehouse provides a relational database designed for large-scale analytics. Unlike the default read-only SQL endpoint for tables defined in a lakehouse, a data warehouse supports full SQL semantics, including the ability to insert, update, and delete data in tables.  

In this lab, you will dive into the world of data analysis within a data warehouse using **Power BI**.


## **Objective**  

**Analyze Data in a Data Warehouse:** Utilize Microsoft Fabric to build and analyze data in a data warehouse. In this lab, you will learn to create a data warehouse, define data models, query data using SQL, and generate insights. You will also create views and use Power BI to visualize data, enabling advanced reporting and interactive dashboards for data-driven decision-making.


## **Prerequisites**  

You should have:  
- **Basic Understanding of Relational Databases:** Familiarity with SQL and database concepts.  

- **Proficiency in Power BI:** Experience creating visualizations and analyzing data with Power BI.  
- **Basic knowledge of Microsoft Fabric:** Understanding of the components and structure of Microsoft Fabric.  
- **Basic data modeling skills:** Ability to define relationships and optimize data for analysis.  


## **Architecture**  

The architecture for this lab illustrates how Microsoft Fabric integrates with a data warehouse and Power BI to create a seamless data analysis experience. The data warehouse serves as the central repository for large-scale analytics, offering robust SQL capabilities. Using Microsoft Fabric, you can manage and scale the data warehouse while defining relationships and data models to ensure efficiency. Power BI acts as the visualization layer, providing an interactive interface to explore, analyze, and present data insights.

### **Architecture Diagram**  
   ![Navigate-To-AAD](./Images/Arch03.png)
---

## **Explanation of Components**  

The architecture for this lab involves the following key components:
-  **Create a Data Warehouse**
You will set up a data warehouse in Microsoft Fabric, learning the process of creating a scalable relational database designed for large-scale data analytics and reporting.

- **Create Tables and Insert Data**
You will create tables within the data warehouse, define their schema, and insert sample data to prepare for analysis, gaining hands-on experience in data organization.

- **Define a Data Model**
You will define relationships between tables to optimize the data for querying and analysis, using techniques like normalization to ensure data integrity and efficiency.

- **Query Data Warehouse Tables**
You will write and execute SQL queries to retrieve and manipulate data, using commands like SELECT, JOIN, and WHERE to filter and aggregate data for analysis.

- **Create a View and Visualize Your Data** 
You will create views to simplify querying and use Power BI to visualize data, building interactive dashboards and reports for insights and decision-making. 

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
