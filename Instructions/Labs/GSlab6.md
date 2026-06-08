# Cloud Scale Analytics with Microsoft Fabric

### Overall Estimated Duration : **120 Minutes**

## Overview

Microsoft Fabric is a unified data platform that combines data engineering, data warehousing, and business intelligence tools into a cohesive environment. By leveraging Microsoft Fabric, you can effectively manage, analyze, and visualize large datasets, enabling powerful data-driven decision-making.

In this hands-on lab, you will explore and set up Microsoft Fabric by creating a workspace and assigning the Fabric Administrator role. You will then create a Lakehouse to centralize and manage data, followed by uploading files for analysis. Additionally, you will leverage Apache Spark within Microsoft Fabric to load, explore, and transform data, performing operations such as filtering, aggregating, and summarizing. You will also save the transformed data in Parquet format, partition it, and visualize insights through Spark, gaining practical experience in data analysis and visualization within the platform.

## Objective

Learn how to leverage Microsoft Fabric for workspace management, use Apache Spark to analyze and transform large datasets, and perform advanced data manipulation.

- **Getting Started with Microsoft Fabric:** Learn how to create and manage a workspace in Microsoft Fabric by assigning the Fabric Administrator role, setting up a new workspace for data and analytics projects, and organizing your work effectively. Additionally, gain hands-on experience in setting up a Lakehouse within the workspace and uploading data files (e.g., CSV) to the Lakehouse, laying the foundation for future data analysis and processing.

- **Analyze Data with Apache Spark:** Use Apache Spark to analyze large datasets and perform data transformations. You will learn how to process and analyze large volumes of data efficiently, apply data transformations, clean and structure data, and perform aggregations using Spark. The lab will also cover creating and querying a Delta table for advanced data manipulation.

## Prerequisites

You should have:

- **Basic Knowledge of Microsoft Azure**: Familiarity with the Azure portal and the process of role assignments within Azure Active Directory (Entra ID).
- **Understanding of Workspace Creation**: Familiarity with the concept of workspaces in cloud platforms and how to create and configure them.
- **Basic Knowledge of Cloud Data Storage**: Understanding the concept of Lakehouses for organizing and storing data in cloud environments.
- **Basic File Management Skills**: Ability to upload files into a cloud-based data platform like Microsoft Fabric for further analysis.
- **Basic Knowledge of Apache Spark**: Familiarity with the fundamentals of Apache Spark, including its data processing capabilities and how to use it for large-scale data analysis.
- **Experience with Microsoft Fabric**: Understanding the Microsoft Fabric environment, including navigating the interface and using its notebooks for data analysis.
- **Basic Python Programming Skills**: Ability to write and modify Python code, particularly for using PySpark within notebooks.
- **Familiarity with DataFrame Operations in Spark**: Knowledge of DataFrame operations in Spark, including loading data, filtering, transforming, and performing aggregations.
- **Experience with Data File Formats**: Familiarity with data file formats such as CSV and Parquet, and how to load, save, and partition data using Spark.
- **Basic SQL Knowledge**: Understanding SQL queries for data manipulation and querying within Spark SQL, including grouping and aggregating data.

## Architecture

The architecture leverages Microsoft Fabric to streamline data management and analysis, integrating workspaces, lakehouses, notebooks, and reporting tools. The first lab focuses on the foundational setup, starting with assigning the Fabric Administrator Role to ensure proper permissions and access control. The workspace is then created, acting as the central environment for organizing and collaborating on data tasks. Following this, a lakehouse is established for data storage, and files are uploaded, populating the lakehouse with datasets for analysis. The second lab builds upon this setup by introducing a notebook for data exploration, where data is loaded into a dataframe, explored for insights, and transformed using Spark. The lab culminates with visualizations created using Spark to help communicate the results. This flow ensures a smooth progression from workspace and data storage setup to hands-on data exploration and reporting, empowering users with efficient tools for actionable insights.

## Architecture Diagram 

![Navigate-To-AAD](./Images/Arch5.png)

## Explanation of Components

The architecture for this lab involves the following key components:

### Lab 01 Components:

- **Fabric Administrator Role:** Ensures that the necessary permissions are granted to manage the workspace effectively, enabling access control and administrative capabilities.

- **Workspace:** A central environment where data and resources are managed. The workspace acts as the foundation for organizing and collaborating on data storage and analysis tasks.

- **Lakehouse:** A data storage solution designed for structured and unstructured data. The Lakehouse enables efficient data organization and facilitates analysis tasks.

- **Data Ingestion Tools:** Enables you to upload files into the Lakehouse to populate datasets required for analysis and querying.

### Lab 02 Components:

- **Notebook Environment:** The Notebook Environment serves as an interactive workspace for writing and executing code, providing a user-friendly interface for developing, running, and debugging data workflows efficiently.  

- **DataFrame for Data Loading:** Data is imported from various sources, such as CSV files, databases, or JSON, and structured into a DataFrame, enabling efficient storage, manipulation, and analysis of the data.  

- **Data Exploration:** Data exploration allows for in-depth analysis and visualization within the DataFrame, supporting operations such as querying, filtering, and summarizing data to uncover insights and patterns.  

- **Apache Spark for Data Transformation:** Apache Spark leverages its distributed processing capabilities to handle large datasets effectively, facilitating complex operations like filtering, joining, and aggregating data at scale.  

- **Data Visualization with Spark:** Data visualization with Spark utilizes built-in libraries or third-party tools to represent insights through intuitive charts, graphs, and dashboards, ensuring clear communication of data findings.  

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
