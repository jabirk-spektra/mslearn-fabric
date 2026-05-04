# Cloud Scale Analytics with Microsoft Fabric

### Overall Estimated Duration : **30 Minutes**

## Overview

Microsoft Fabric is a unified data platform that combines data engineering, data warehousing, and business intelligence tools into a cohesive environment. By leveraging Microsoft Fabric, you can effectively manage, analyze, and visualize large datasets, analyze, and visualize large datasets, enabling powerful data-driven decision-making processes.

In this lab, you will create dedicated workspaces and work with Lakehouse storage to upload and organize data files. Microsoft Fabric serves as a comprehensive analytics platform, streamlining workflows by integrating data engineering, data warehousing, and business intelligence capabilities. Here, you can create dedicated workspaces and work with Lakehouse storage to upload and organize data files.

## Objective

In this lab, you will:

- Create and configure a Microsoft Fabric workspace
- Assign the Fabric Administrator role
- Create a Lakehouse for structured data storage
- Upload files for analysis

## Prerequisites

Participants should have:

- **Basic Knowledge of Microsoft Azure**: Familiarity with the Azure portal and the process of role assignments within Azure Active Directory (Entra ID).
- **Understanding of Workspace creation**: Familiarity with the concept of workspaces in cloud platforms and how to create and configure them.
- **Basic Knowledge of cloud data storage**: Understanding the concept of Lakehouses for organizing and storing data in cloud environments.
- **Basic file management skills**: Ability to upload files into a cloud-based data platform like Microsoft Fabric for further analysis.

## Architecture

The lab architecture involves a structured flow where a Fabric Administrator Role is assigned to manage the Fabric environment, ensuring that all resources and permissions are properly handled. A Fabric Workspace is established to provide a dedicated area for organizing and managing resources, enhancing workflow efficiency. Data is centralized in a Lakehouse, designed to handle large-scale data storage, making it easy to store and access for analysis. The File Upload Process is implemented to streamline the uploading and organizing of data within the Lakehouse, ensuring that data is easily accessible and ready for efficient processing and analysis. This integrated flow supports effective resource management, data storage, and analysis.   

## Architecture Diagram 

![Navigate-To-AAD](./Images/Arch1.png)

## Explanation of Components

The architecture for this lab involves the following key components:

- **Fabric Administrator Role:** Ensures that the necessary permissions are granted to manage the workspace effectively, enabling access control and administrative capabilities.

- **Workspace:** A central environment where data and resources are managed. The workspace acts as the foundation for organizing and collaborating on data storage and analysis tasks.

- **Lakehouse:** A data storage solution designed for structured and unstructured data. The Lakehouse enables efficient data organization and facilitates analysis tasks.

- **Data Ingestion Tools:** Enables the uploading of files into the Lakehouse to populate datasets required for analysis and querying.

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
