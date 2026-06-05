# Lab 07: Create a Dataflow (Gen2) in Microsoft Fabric

### Estimated Duration: 40 minutes

In Microsoft Fabric, Dataflows (Gen2) connect to various data sources and perform transformations in Power Query Online. They can then be used in Data Pipelines to ingest data into a lakehouse or other analytical store or to define a dataset for a Power BI report.

This lab introduces the core elements of Dataflows (Gen2) and focuses on understanding the fundamentals rather than building a complex enterprise-level solution.

## Lab objectives

You will be able to complete the following tasks:

- Task 1: Create a Dataflow (Gen2) to ingest data
- Task 2: Add data destination for Dataflow
- Task 3: Add a dataflow to a pipeline

### Task 1: Create a Dataflow (Gen2) to ingest data

In this task, you will create a Dataflow (Gen2) to efficiently ingest and transform data from multiple sources for analysis. This process streamlines data preparation, enabling you to prepare the data for further processing and insights.

1. In the left pane, navigate to your **Workspace (1)** and click on **fabric-<inject key="DeploymentID" enableCopy="false"/> (1)**, then click on **+ New item (3)** to create a new **Data Flow Gen 2**.

    ![](./Images/fabricnav.png)

    ![](./Images/fabricnav2.png)

1. Search for **Dataflow Gen2 (1)** and select **Dataflow Gen2 (2)**. Leave the name as default, and then click on **Create (4)**.

   ![New dataflow.](./Images/E5T1S2.png)

   ![New dataflow.](./Images/dfsrcr.png)

1. From the **Get data** pane, select **Import from a Text/CSV file**.

   ![](./Images/Flow3.png)

1. Create a new data source with the following settings:

    - **Link to file: (1)** Selected
    - **File path or URL: (2)** `https://raw.githubusercontent.com/MicrosoftLearning/dp-data/main/orders.csv`
    - **Connection: (3)** Create new connection
    - **Connection Name: (4)** Connection
    - **Data gateway: (5)** (none)
    - **Authentication kind: (6)** Anonymous
    - **Privacy level: (7)** None
    - Click **Next (8)**

      ![](./Images/e8t1p2.png)

1. Preview the file data, and then click **Create** the data source. The Power Query editor shows the data source and an initial set of query steps to format the data, as shown below:

   ![Query in the Power Query editor.](./Images/e8t1p3.png)

1. Select the **Add column  (1)** tab on the toolbar ribbon. Then, choose **Custom column (2)** and create a new column with Name **MonthNo (3)** and enter the formula **Date.Month([OrderDate]) (4)** in the **Custom column formula** box and then click **OK (5)**.

   ![](./Images/e8t1p4.png)

   ![](./Images/e8t1p5.png)

1. The step to add the custom column is added to the query, and the resulting column is displayed in the data pane:

   ![](./Images/e8t1p6.png)

### Task 2: Add data destination for Dataflow

In this task, you’ll add a data destination for the Dataflow to determine where the ingested and transformed data will be stored for future use.

1. Switch to your Dataflow window. In the **Query settings** in the right pane, click on **+ (1)** for Data Destination, then choose **Lakehouse (2)** from the menu.

   ![Empty data pipeline.](./Images/Flow6.png)

   >**Note:** If the Query settings pane isn't visible, go to the top ribbon, select **Query (1)**, then click **Add data destination (2)** and choose **Lakehouse (3)**.

   ![Empty data pipeline.](./Images/lakedest.png)

   >**Note:** If this option is greyed out, you may already have a data destination set. Check the data destination at the bottom of the Query settings pane on the right side of the Power Query editor. If a destination is already set, you can change it using the gear.

1. In the **Connect to data destination** dialog box, make sure **Create a new connection (1)** is selected and the **<inject key="AzureAdUserEmail"></inject> (2)** account is signed in and then click on **Next (3)**.

   ![](./Images/E8T2S2.png)

1. In the **Choose destination target** window, select the **fabric-<inject key="DeploymentID" enableCopy="false"/>** Workspace. Select the **Lakehouse_<inject key="DeploymentID" enableCopy="false"/> (1)** then specify the new table name as **orders (2)**, then click **Next (3)**.

   ![Data destination configuration page.](./Images/img-05.png)

1. On the Destination settings page, observe that **MonthNo** is not selected in the Column mapping, and an informational message is displayed.
 
1. On the Destination settings page, toggle **off (1)** the **Use Automatic Settings** option. Then, for the **MonthNo** column header, change the **Source Type** to **Whole number (2)**. Now, click on **Save settings (3)**.
   
   ![Data destination settings page.](./Images/e8t2p2.png)

1. Click on the **Dataflow 2 (1)** on the top left, and rename the dataflow as **Transform Orders Dataflow (2)**.

   ![](./Images/E8T2S6.png)

1. Select **Home** tab, and click on **Save and Run**.

> **Congratulations** on completing the task! Now, it's time to validate it. Here are the steps:
> - Hit the Validate button for the corresponding task. If you receive a success message, you can proceed to the next task. 
> - If not, carefully read the error message and retry the step, following the instructions in the lab guide.
> - If you need any assistance, please contact us at cloudlabs-support@spektrasystems.com. We are available 24/7 to help you out.

<validation step="8a7b316c-9513-4f0e-a48a-2e84f7b12eb2" />

### Task 3: Add a dataflow to a pipeline

In this task, you’ll add a dataflow to a pipeline to streamline the data processing workflow and enable automated data transformations.

1. In the left pane, navigate to your **Workspace (1)** and click on **fabric-<inject key="DeploymentID" enableCopy="false"/> (1)**, then click on **+ New item (3)**.

    ![](./Images/fabricnav.png)

    ![](./Images/fabricnav2.png)

1. In the Search box, search for **Pipeline (1)**, and select **Pipeline (2)**.

   ![](./Images/E1T4S2.png)

1. Set the Name as **Load Orders pipeline (1)** and click on **Create (3)**. This will open the pipeline editor.

   ![](./Images/img-06.png)

   > **Note:** If the Copy Data wizard opens automatically, close it!

1. In the **Build a data pipeline to organize and move your data** window, click on **Pipeline activity (1)**, and select **Dataflow (2)** activity to the pipeline.

   ![Empty data pipeline.](./Images/E8t3S4.png)

1. With the new **Dataflow1** activity selected, go to the **Settings (1)** tab in the bottom. In the **Workspace** drop-down list, choose **fabric-<inject key="DeploymentID" enableCopy="false"/> (2)** and in the **Dataflow** drop-down list, select **Transform Orders Dataflow (3)** (the data flow you created previously).

   ![Empty data pipeline.](./Images/e8t3p2.png)
   
1. Select **Save** from the top-left corner to save the pipeline.

   ![](./Images/Flow11.png)

1. Use the **Run** button to run the pipeline then click on **Save and Run**, and wait for it to complete. It may take a few minutes.

   ![](./Images/Flow12.png)
   
   ![09](./Images/fab-ric-ex1-g15.png)
   
   ![](./Images/prun.png)

1. Navigate to your **Lakehouse_<inject key="DeploymentID" enableCopy="false"/>** Lakehouse.

1. Expand the **Tables** section and select the **orders** table created by your dataflow.

   ![Table loaded by a dataflow.](./Images/pop.png)

   >**Note:** You might have to refresh the browser to get the expected output.

> **Congratulations** on completing the task! Now, it's time to validate it. Here are the steps:
> - Hit the Validate button for the corresponding task. If you receive a success message, you can proceed to the next task. 
> - If not, carefully read the error message and retry the step, following the instructions in the lab guide.
> - If you need any assistance, please contact us at cloudlabs-support@spektrasystems.com. We are available 24/7 to help you out.

<validation step="8e4e892b-1a8b-4031-ae89-edc2622f0aae" />

### Summary

In this exercise, you have created a Dataflow (Gen2) to ingest data , added data destination for Dataflow and a dataflow to a pipeline.

### You have successfully completed the lab

