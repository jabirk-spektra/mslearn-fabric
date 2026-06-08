# Cloud Scale Analytics with Microsoft Fabric

### Overall Estimated Duration : **90 Minutes**

## Overview

Microsoft Fabric is a unified data platform that combines data engineering, data warehousing, and business intelligence tools into a cohesive environment. By leveraging Microsoft Fabric, you can effectively manage, analyze, and visualize large datasets, enabling data-driven decision-making.

In this hands-on experience, you will explore how to use Microsoft Fabric to set up a centralized data workspace, ingest and transform data, and utilize Power BI for reporting and analysis. You will begin by configuring your Fabric workspace and Lakehouse to store data efficiently, then move on to ingesting and transforming data using notebooks. With SQL queries, you’ll analyze the data and create compelling, interactive reports in Power BI to uncover valuable insights.

## Objective

In this lab, you will learn to leverage Microsoft Fabric and Power BI to manage, transform, and analyze data within a unified data platform. This experience will guide you through the process of setting up a centralized data workspace, ingesting and transforming data, and creating interactive reports for actionable insights.

- **Getting Started with Microsoft Fabric:** Learn how to create and manage a workspace in Microsoft Fabric by assigning the Fabric Administrator role, setting up a new workspace for data and analytics projects, and organizing your work effectively. Additionally, gain hands-on experience in setting up a Lakehouse within the workspace and uploading data files (e.g., CSV) to the Lakehouse, laying the foundation for future data analysis and processing.

- **Ingest Data with a Microsoft Fabric Lakehouse:** Learn how to ingest data into a Microsoft Fabric Lakehouse using notebooks and SQL, process and transform the data with PySpark, and save the results as managed tables. Additionally, use SQL queries and visual queries in Power BI to analyze and visualize the data, creating comprehensive reports that provide meaningful insights and enhance data accessibility for further analysis.

## Prerequisites

Participants should have:

- **Basic Knowledge of Microsoft Azure**: Familiarity with the Azure portal and the process of role assignments within Azure Active Directory (Entra ID).
- **Understanding of Workspace Creation**: Familiarity with the concept of workspaces in cloud platforms and how to create and configure them.
- **Basic Knowledge of Cloud Data Storage**: Understanding the concept of Lakehouses for organizing and storing data in cloud environments.
- **Basic File Management Skills**: Ability to upload files into a cloud-based data platform like Microsoft Fabric for further analysis.
- **Proficiency in Python and SQL:** Experience with Python for data processing (using PySpark) and SQL for querying databases.
- **Familiarity with Data Transformation Tools:** Understanding of tools like notebooks in Microsoft Fabric to process and transform data.
- **Experience with Power BI:** Knowledge of using Power BI for creating visualizations and reports from ingested data.
- **Basic Understanding of Data Warehousing Concepts:** Familiarity with Lakehouse architecture and managed tables within cloud-based environments like Microsoft Fabric.


## Architecture

The architecture leverages Microsoft Fabric to create and manage a streamlined data environment involving workspaces, lakehouses, notebooks, and reporting tools. The first lab focuses on foundational setup, starting with assigning the Fabric administrator role, creating a workspace, setting up a lakehouse for data storage, and uploading files for analysis. The second lab builds on this by creating a notebook for data exploration, querying data using SQL, generating visual queries, and creating reports to summarize insights. This flow ensures a seamless transition from data ingestion to analysis and reporting, enabling efficient data management and actionable insights.


## Architecture Diagram

![Architecture Diagram](./Images/Arch2.png)

## Explanation of Components

### Lab 01 Components:

- **Fabric Administrator Role:** Ensures that the necessary permissions are granted to manage the workspace effectively, enabling access control and administrative capabilities.

- **Workspace:** A central environment where data and resources are managed. The workspace acts as the foundation for organizing and collaborating on data storage and analysis tasks.

- **Lakehouse:** A data storage solution designed for structured and unstructured data. The Lakehouse enables efficient data organization and facilitates analysis tasks.

- **Data Ingestion Tools:** Enables uploading of files into the Lakehouse to populate datasets required for analysis and querying.

### Lab 02 Components:

- **Notebook:** A collaborative environment for writing and executing code. Notebooks are used to explore and analyze data interactively.

- **SQL Query Engine:** Facilitates structured querying of stored data, extracting insights directly from tables for analysis.

- **Visual Query Tools:** Translates SQL results into visual representations, making data trends and patterns easier to understand.

- **Report Builder:** Compiles data insights into a structured and shareable format, providing a comprehensive view of the analyzed information.

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
