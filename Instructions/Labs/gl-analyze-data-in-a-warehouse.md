# Exercise 4: Data Warehouse Analyze Data in a Warehouse with Fabric Copilot

### Estimated Duration: 60 minutes

## Overview

In this Exercise, you will analyze data in a warehouse using Fabric Copilot by connecting to your data source, running queries, and visualizing insights to drive informed decision-making.

## Lab objectives

You will be able to complete the following tasks:

- Task 1: Create a data warehouse
- Task 2: Create tables and insert data
- Task 3: Define a data model
- Task 4: Generate reports using Copilot

## Task 1: Create a data warehouse

In this task, you'll create a new data warehouse in the Data Warehouse experience of the Power BI portal.

Now that you already have a workspace, it's time to switch to the *Data Warehouse* experience in the portal and create a data warehouse.

1. Select **Workspaces (1)**, and then choose your workspace **fabric-<inject key="DeploymentID" enableCopy="false"/> (2)**.

    ![](./Images/cop-fab-apr-ex1-g8.png)

1. In your workspace, select **+ New item**.

    ![](./Images/cop-fab-apr-ex1-g1.png)

1. In the **New item** pane, enter **Warehouse (1)** in the search bar and then select **Warehouse (2)**.

    ![](./Images/cop-fab-apr-ex4-g2.png)

1. In the **Data Warehouse** home page, create a new **Warehouse** named **Data Warehouse-<inject key="DeploymentID" enableCopy="false"/> (1)** and click on **Create (2)**.

   ![01](./Images/cop-fab-apr-ex4-g3.png)   

> **Congratulations** on completing the task! Now, it's time to validate it. Here are the steps:

   - Hit the Validate button for the corresponding task. If you receive a success message, you can proceed to the next task. 
   - If not, carefully read the error message and retry the step, following the instructions in the lab guide.
   - If you need any assistance, please contact us at cloudlabs-support@spektrasystems.com. We are available 24/7 to help you out.

<validation step="0ef77b08-2998-4a99-ab87-d97b737e97d7" />

## Task 2: Create tables and insert data

In this task, you'll create and populate tables in your data warehouse using T-SQL, then verify that the tables have been created and data has been inserted successfully.

A warehouse is a relational database in which you can define tables and other objects.

1. In your new warehouse, select the Create tables with **T-SQL** tile.

   ![01](./Images/cop-fab-apr-ex4-g4.png)

1. Replace the default SQL code with the following **CREATE TABLE statement (1)** and use the **&#9655; Run (2)** button to run the SQL script.

   ```sql
   CREATE TABLE dbo.DimProduct
   (
       ProductKey INTEGER NOT NULL,
       ProductAltKey VARCHAR(25) NULL,
       ProductName VARCHAR(50) NOT NULL,
       Category VARCHAR(50) NULL,
       ListPrice DECIMAL(5,2) NULL
   );
   GO
   ```

   ![01](./Images/cop-fab-apr-ex4-g5.png)

1. Use the **Refresh** button on the toolbar, then in the **Explorer** pane, expand **Schemas (1)** > **dbo (2)** > **Tables (3)** and verify that the **DimProduct (4)** table is present.

    ![](./Images/cop-fab-apr-ex4-g6.png)

1. On the **Home** tab, select **New SQL query (2)** from the dropdown **(1)**.

    ![](./Images/cop-fab-apr-ex4-g7.png)

1. Enter the following **INSERT statement (1)** and click on **&#9655; Run (2)** button to insert three rows into the **DimProduct** table.

    ```sql
   INSERT INTO dbo.DimProduct
   VALUES
   (1, 'RING1', 'Bicycle bell', 'Accessories', 5.99),
   (2, 'BRITE1', 'Front light', 'Accessories', 15.49),
   (3, 'BRITE2', 'Rear light', 'Accessories', 15.49);
   GO
    ```

    ![01](./Images/cop-fab-apr-ex4-g8.png)

1. In the **Explorer** pane, select the **DimProduct (1)** table and verify that the data is displayed with three rows **(2)**.

    ![](./Images/cop-fab-apr-ex4-g10.png)

1. On the **Home** tab, select **New SQL query (2)** from the dropdown **(1)**.

    ![](./Images/cop-fab-apr-ex4-g9.png)

1. In the **LabVM** open the **File explorer** from the bottom menu.

   ![01](./Images/f-43.png)

1. Open **create-dw-01.txt** from **C:\LabFiles\Files**, copy the Transact-SQL code for the **DimProduct** table, and paste it into the query pane; then open **create-dw-02.txt** and **create-dw-03.txt**, copy the code for **DimCustomer**, **DimDate**, and **FactSalesOrder**, paste them sequentially into the same query pane.

   ![01](./Images/02/Pg4-T2-S7.png)

1. **Run** the query, which creates a simple data warehouse schema and loads some data. The script should take around 30 seconds to run.

   ![01](./Images/cop-fab-apr-ex4-g11.png)

1. Use the **Refresh** button on the toolbar to refresh the view. Then in the **Explorer** pane, verify that the **dbo** schema in the data warehouse now contains the following four tables:

    - **DimCustomer**
    - **DimDate**
    - **DimProduct**
    - **FactSalesOrder**

       ![01](./Images/cop-fab-apr-ex4-g13.png)  

       > **Tip**: If the schema takes a while to load, just refresh the browser page.

## Task 3: Define a data model

In this task, you'll define a data model in your data warehouse by creating relationships between fact and dimension tables. You'll establish many-to-one relationships between FactSalesOrder and DimProduct, DimCustomer, and DimDate using the Model tab.

A relational data warehouse typically consists of *fact* and *dimension* tables. The fact tables contain numeric measures you can aggregate to analyze business performance (for example, sales revenue), and the dimension tables contain attributes of the entities by which you can aggregate the data (for example, product, customer, or time). In a Microsoft Fabric data warehouse, you can use these keys to define a data model that encapsulates the relationships between the tables.

1. On the **Home** tab, select **New semantic model**.

    ![](./Images/cop-fab-apr-ex4-g14.png)

1. In the **New semantic model** pane, enter **sales-semantic-<inject key="DeploymentID" enableCopy="false"/> (1)** in **Direct Lake semantic model name**, select **Direct Lake on SQL (2)**, ensure **Select all (3)** is checked, and then select **Confirm (4)**.

    ![](./Images/cop-fab-apr-ex4-g15.png)

1. Select **Workspaces (1)**, and then choose your workspace **fabric-<inject key="DeploymentID" enableCopy="false"/> (2)**.

    ![](./Images/cop-fab-apr-ex1-g8.png)

1. In the workspace, selectt the **sales-semantic-<inject key="DeploymentID" enableCopy="false"/>** semantic model that has been created.

    ![](./Images/cop-fab-apr-ex4-g16.png)

1. Select **Open** to open the **sales-semantic-<inject key="DeploymentID" enableCopy="false"/>** semantic model.

    ![](./Images/cop-fab-apr-ex4-g17.png)

1. Arrange the tables in the model view by dragging them so they are laid out clearly as shown.

    ![](./Images/cop-fab-apr-ex4-g18.png)

1. Drag the **ProductKey** field from **FactSalesOrder** and drop it onto **ProductKey** in **DimProduct**.

    ![](./Images/cop-fab-apr-ex4-g19.png)

1. In the **New relationship** pane, confirm the following settings and then select **Save (8)**:

      - **From table (1)**: FactSalesOrder
      - **Column (2)**: ProductKey
      - **To table (3)**: DimProduct
      - **Column (4)**: ProductKey
      - **Cardinality (5)**: Many to one (*:1)
      - **Cross filter direction (6)**: Single
      - **Make this relationship active (7)**: Selected
      - **Assume referential integrity**: Unselected

        ![](./Images/cop-fab-apr-ex4-g20.png)

1. Drag the **CustomerKey** field from **FactSalesOrder** and drop it onto **CustomerKey** in **DimCustomer**.

      ![](./Images/cop-fab-apr-ex4-g21.png)

1. In the **New relationship** pane, confirm the following settings and then select **Save (8)**:

      - **From table (1)**: FactSalesOrder
      - **Column (2)**: CustomerKey
      - **To table (3)**: DimCustomer
      - **Column (4)**: CustomerKey
      - **Cardinality (5)**: Many to one (*:1)
      - **Cross filter direction (6)**: Single
      - **Make this relationship active (7)**: Selected
      - **Assume referential integrity**: Unselected

        ![](./Images/cop-fab-apr-ex4-g22.png)

1. Drag the **SalesOrderDateKey** field from the **FactSalesOrder** table and drop it on the **DateKey** field in the **DimDate** table.

      ![](./Images/cop-fab-apr-ex4-g23.png)

1. In the **New relationship** pane, configure the relationship as follows, and then select **Save (8)**:

   - **From table (1)**: FactSalesOrder  
   - **Column (2)**: SalesOrderDateKey  
   - **To table (3)**: DimDate  
   - **Column (4)**: DateKey  
   - **Cardinality (5)**: Many to one (*:1)  
   - **Cross filter direction (6)**: Single  
   - **Make this relationship active (7)**: Selected

        ![](./Images/cop-fab-apr-ex4-g24.png)

1. When all of the relationships have been defined, the model should look like this:

   ![.](./Images/cop-fab-apr-ex4-g25.png)

## Task 4: Generate reports using Copilot

In this task, you will utilize Microsoft Fabric's Copilot feature to generate comprehensive reports by leveraging natural language inputs. Copilot assists in transforming raw data into actionable insights, enabling you to create detailed reports efficiently. 

1. When you click on the relationship between **FactSalesOrder** and **DimCustomer** and access its properties, you're essentially examining how these two tables are linked together. This relationship defines how data from these tables can be combined or related when querying or visualizing in Power BI.

     ![](./Images/cop-fab-apr-ex4-g26.png)

    - This relationship indicates that each record in the "FactSalesOrder" table is associated with a specific customer represented in the "DimCustomer" table. For example, if we have a sales record in "FactSalesOrder" for a particular transaction, we can use this relationship to look up additional details about the corresponding customer from the "DimCustomer" table.

    - This linkage is crucial for defining the Semantic Model used by Power BI. The Semantic Model essentially acts as a blueprint that outlines how data elements are interconnected and how they should be interpreted within Power BI. By establishing and defining relationships between tables, we're instructing Power BI on how to navigate and analyze the data effectively.
 
1. From the **File (1)** menu, select **Create new report (2)** to create a report using the semantic model.
 
   ![](./Images/cop-fab-apr-ex4-g27.png)

1. The Semantic Model, as defined in the data warehouse, is reflected in the Power BI interface. This includes the tables and their respective fields visible in the Data Pane of Power BI, which you can use to build your reports.

1. On the report canvas, select **Copilot** from the top menu to open the Copilot pane.

   ![](./Images/cop-fab-apr-ex4-g28.png)

1. Explore the capabilities of Copilot further by **clicking on its logo** within the text box. This will allow you to access additional features and functionalities that Copilot offers, providing a deeper understanding of its capabilities.

   ![](./Images/cop-fab-apr-ex4-g29.png)

1. Recognize that Copilot offers functionalities such as providing suggestions, generating code snippets, and offering explanations. However, it's important to note its limitations, which may include the inability to create certain visualizations or directly modify page layouts.

1. Selecting **What's in my data** prompts Copilot to analyze the semantic model or dataset currently in use.

   ![](./Images/cop-fab-apr-ex4-g30.png)

1. Review the Copilot response, which summarizes the tables and fields in your data model.

   ![](./Images/cop-fab-apr-ex4-g31.png)

   > **Note:** The response format may vary since it is generated dynamically by Copilot.

1. Click **Create a page that shows**.

    ![](./Images/cop-fab-apr-ex4-g32.png)
   
1. At this time, you can only ask for a page or report to be created. You can't ask for specific visuals.
 
1. Type the following command into Copilot:
  
    ```
    Create a page that shows "Total Sales by Product Category"
    ```

    ![](./Images/cop-fab-apr-ex4-g33.png)
 
1. **Execute the command** and let Copilot generate the report. Note that AI-generated results may vary.

    ![](./Images/cop-fab-apr-ex4-g34.png)
   
1. Type the following command into Copilot

    ```
    Suggest Content for this Report
    ```

    ![](./Images/cop-fab-apr-ex4-g35.png)
 
1. **Expand each suggestion** to see the text of the prompt and what will be created. This helps illustrate the range of suggestions Copilot can provide.

    ![](./Images/cop-fab-apr-ex4-g36.png)

1. Click on **Create** on any suggestion **(1)**. You can see the report **(2)**.   

    ![](./Images/cop-fab-apr-ex4-g37.png)

1. Review the generated report page, which includes visuals for sales performance and trends such as total sales, average sales, category breakdown, and regional distribution.

    ![](./Images/cop-fab-apr-ex4-g38.png)

    > **Note:** The layout and visuals may vary as they are dynamically generated by Copilot.

1. In the **Copilot** pane, enter the followin **prompt (1)**, and then select **Send (2)**.

    ```
    Give me an executive summary
    ```

    ![](./Images/cop-fab-apr-ex4-g39.png)

1. Review the Copilot-generated executive summary, which highlights key insights such as total sales, average order value, and top-performing product categories.

    ![](./Images/cop-fab-apr-ex4-g40.png)

    > **Note:** The response content and format may vary since it is dynamically generated by Copilot.

1. From the **File (1)** menu, select **Save (2)** to save the report..

    ![](./Images/cop-fab-apr-ex4-g41.png)

1. In the **Save your report** pane, enter a name in the **Name (1)** field, and then select **Save (2)**.

    ![](./Images/cop-fab-apr-ex4-g42.png)

## Summary

In this Exercise, you connected to a data warehouse using Fabric Copilot and explored the available datasets. You ran queries to extract insights and created visualizations for effective analysis. Finally, you compiled your findings into reports and collaborated with team members on the results.

### Review
In this lab, you have completed:

- Task 1: Create a data warehouse
- Task 2: Create tables and insert data
- Task 3: Define a data model
- Task 4: Generate reports using Copilot

### You have successfully completed the lab.