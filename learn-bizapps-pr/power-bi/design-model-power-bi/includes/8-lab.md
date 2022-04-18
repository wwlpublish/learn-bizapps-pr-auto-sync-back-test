**The estimated time to complete the lab is 45 minutes**

In this lab you will commence developing the data model. It will involve creating relationships between tables, and then configuring table and column properties to improve the friendliness and usability of the data model. You will also create hierarchies and create quick measures.

In this lab you learn how to:

- Create model relationships

- Configure table and column properties

- Create hierarchies

- Create quick measures

### **Lab story**

This lab is one of many in a series of labs that was designed as a complete story from data preparation to publication as reports and dashboards. You can complete the labs in any order. However, if you intend to work through multiple labs, for the first 10 labs, we suggest you do them in the following order:

1. [Prepare data in Power BI Desktop](https://docs.microsoft.com/learn/modules/get-data/lab-prepare/?azure-portal=true)

1. [Load data in Power BI Desktop](https://docs.microsoft.com/learn/modules/clean-data-power-bi/8-lab/?azure-portal=true)

1. **Model data in Power BI Desktop, Part 1** << You are here. This is the lab for the current module.

1. [Model data in Power BI Desktop, part 2](https://docs.microsoft.com/learn/modules/design-model-power-bi/9-lab/?azure-portal=true)

1. [Create DAX calculations in Power BI Desktop, part 1](https://docs.microsoft.com/learn/modules/create-measures-dax-power-bi/6-lab/?azure-portal=true)

1. [Create DAX calculations in Power BI Desktop, part 2](https://docs.microsoft.com/learn/modules/create-measures-dax-power-bi/8-lab/?azure-portal=true)

1. [Design a report in Power BI Desktop, part 1](https://docs.microsoft.com/learn/modules/visuals-power-bi/8-lab/?azure-portal=true)

1. [Design a report in Power BI Desktop, part 2](https://docs.microsoft.com/learn/modules/data-driven-story-power-bi/13-lab/?azure-portal=true)

1. [Create a Power BI dashboard](https://docs.microsoft.com/learn/modules/create-dashboards-power-bi/9-lab/?azure-portal=true)

1. [Perform data analysis in Power BI Desktop](https://docs.microsoft.com/learn/modules/ai-visuals-power-bi/5-lab/?azure-portal=true)

1. [Create a Power BI paginated report](https://docs.microsoft.com/learn/modules/create-paginated-reports-power-bi/6-lab/?azure-portal=true)

> [!NOTE]
> Each lab starts with a PBIX file that has all of the previous lab work completed. If you should lose your work for any reason, you can open the PBIX file that includes the progress up to that point from the folder indicated at the beginning of the next lab.

## Exercise 1: Create Model Relationships

In this exercise you will create model relationships.

### Task 1: Get started

In this task you will set up the environment for the lab.

> [!IMPORTANT]
> If you are continuing on from the previous lab (and you completed that lab successfully), do not complete this task; instead, continue from the next task.

1. To open the Power BI Desktop, on the taskbar, select the Microsoft Power BI Desktop shortcut.

1. To close the getting started window, at the top-left of the window, select **X**.

1. To open the starter Power BI Desktop file, select the **File** ribbon tab to open the backstage view.

1. Select **Open Report**.

1. Select **Browse Reports**.

1. In the **Open** window, navigate to the **D:\DA100\Labs\03-configure-data-model-in-power-bi-desktop\Starter** folder.

1. Select the **Sales Analysis** file.

1. Select **Open**.

1. Close any informational windows that may open.

1. To create a copy of the file, select the **File** ribbon tab to open the backstage view.

1. Select **Save As**.

1. If prompted to apply changes, select **Apply**.

1. In the **Save As** window, navigate to the **D:\DA100\MySolution** folder.

1. Select **Save**.

## Task 2: Create model relationships

In this task, you'll create model relationships.

1. In Power BI Desktop, at the left, select the **Model** view icon.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Power B I Desktop Model view icon.](../media/lab-1-ssm.png)](../media/lab-1-ssm.png#lightbox)

1. If you do not see all seven tables, scroll horizontally to the right, and then drag and arrange the tables more closely together so they can all be seen at the same time.

    > [!TIP]
    > You can also use the zoom control located at the bottom of the window.
    >
    > In Model view, you can view each table and any relationships (connectors between tables). Presently, there are no relationships because in the **Prepare data in Power BI Desktop** lab, you disabled the data load relationship options.

1. To return to Report view, at the left, select the **Report view** icon.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Power B I Desktop Report view icon.](../media/lab-2-ssm.png)](../media/lab-2-ssm.png#lightbox)

1. To view all table fields, in the **Fields** pane, right-click an empty area, and then select **Expand All**.

1. To create a table visual, in the **Fields** pane, from inside the **Product** table, select the **Category** field.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Power B I Desktop Fields pane.](../media/lab-3-ssm.png)](../media/lab-3-ssm.png#lightbox)

    > [!NOTE]
    > The labs use a shorthand notation to reference a field. It looks like this: **Product | Category**. In this example, **Product** is the table name and **Category** is the field name.

1. To add a column to the table, in the **Fields** pane, select the **Sales | Sales** field.

1. Notice that the table visual lists four product categories, and that the sales value is the same for each, and the same for the total.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the problem where every category lists the same sales amount.](../media/lab-4-ss.png)](../media/lab-4-ss.png#lightbox)

    The issue is that the table is based on fields from different tables. The expectation is that each product category displays the sales for that category. However, because there isn't a model relationship between these tables, the **Sales** table is not filtered. You'll now add a relationship to propagate filters between the tables.

1. On the **Modeling** ribbon tab, from inside the **Relationships** group, select **Manage Relationships**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Manage Relationships button.](../media/lab-5-ssm.png)](../media/lab-5-ssm.png#lightbox)

1. In the **Manage Relationships** window, notice that no relationships are yet defined.

1. To create a relationship, select **New**.

1. In the **Create Relationship** window, in the first dropdown list, select the **Product** table.

1. In the second dropdown list (beneath the **Product** table grid), select the **Sales** table.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Create Relationship window.](../media/lab-6-ssm.png)](../media/lab-6-ssm.png#lightbox)

1. Notice the **ProductKey** columns in each table have been selected.

    The columns were automatically selected because they share the same name and data type.

1. In the **Cardinality** dropdown list, notice that **One To Many (1:*)** is selected.

    The cardinality was automatically detected, because Power BI understands that the **ProductKey** column from the **Product** table contains unique values. One-to-many relationships are the most common cardinality, and all relationships you create in this lab will be of this type. You'll work with a many-to-many cardinality in the **Model data in Power BI Desktop, Part 2** lab.

1. In the **Cross Filter Direction** dropdown list, notice that **Single** is selected.

    Single filter direction means that filters propagate from the "one side" to the "many side". In this case, it means filters applied to the **Product** table will propagate to the **Sales** table, but not in the other direction. You’ll work with a bi-directional relationship in the **Model data in Power BI Desktop, Part 2** lab.

1. Notice that the **Make This Relationship Active** is selected.

    Active relationships will propagate filters. It's possible to mark a relationship as inactive so filters don't propagate. Inactive relationships can exist when there are multiple relationship paths between tables. In which case, model calculations can use special functions to activate them. You’ll work with an inactive relationship in the **Model data in Power BI Desktop, Part 2** lab.

1. Select **OK**.

1. In the **Manage Relationships** window, notice that the new relationship is listed, and then select **Close**.

1. In the report, notice that the table visual has updated to display different values for each product category.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the corrected table with different sales amounts listed.](../media/lab-7-ss.png)](../media/lab-7-ss.png#lightbox)

   Filters applied to the **Product** table now propagate to the **Sales** table.

1. Switch to Model view, and then notice there is now a connector between the two tables. (It does not matter whether the tables are positioned next to each other.)

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the visual connection between two tables.](../media/lab-8-ss.png)](../media/lab-8-ss.png#lightbox)

1. In the diagram, notice that you can interpret the cardinality, which is represented by the **1** and **\*** indicators.

    > [!NOTE]
    > Filter direction is represented by the arrow head. A solid line represents an active relationship. A dashed line represents an inactive relationship.

1. Hover the cursor over the relationship to reveal the related columns.

    There's an easier way to create a relationship. In the model diagram, you can drag and drop columns to create a new relationship.

1. To create a new relationship, from the **Reseller** table, drag the **ResellerKey** column on to the **ResellerKey** column of the **Sales** table.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the ResellerKey in the Reseller table dragged to the ResellerKey in the Sales table.](../media/lab-10-ssm.png)](../media/lab-10-ssm.png#lightbox)

    > [!TIP]
    > Sometimes a column doesn't want to be dragged. If this situation arises, select a different column and then try again.

1. Create the following two model relationships:

    - **Region | SalesTerritoryKey** to **Sales | SalesTerritoryKey**

    - **Salesperson | EmployeeKey** to **Sales | EmployeeKey**

    In this lab, the **SalespersonRegion** and **Targets** tables will remain disconnected. There's a many-to-many relationship between salesperson and region. You'll work with this advanced scenario in the **Model data in Power BI Desktop, Part 2** lab.

1. In the diagram, place the **Sales** table in the center and arrange the related tables around it. Place the disconnected tables to the side.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the relationships between different tables.](../media/lab-10-ss.png)](../media/lab-10-ss.png#lightbox)

1. Save the Power BI Desktop file.

## Exercise 2: Configure tables

In this exercise, you will configure each table by creating hierarchies, and hiding, formatting, and categorizing columns.

### Task 1: Configure the Product table

In this task, you will configure the **Product** table.

1. In Model view, in the **Fields** pane, if necessary, expand the **Product** table.

1. To create a hierarchy, in the **Fields** pane, right-click the **Category** column, and then select **Create Hierarchy**.

1. In the **Properties** pane (to the left of the **Fields** pane), in the **Name** box, replace the text with **Products**.

1. To add the second level to the hierarchy, in the **Properties** pane, in the **Hierarchy** dropdown list, scroll down and select **Subcategory**.

1. To add the third level to the hierarchy, in the **Hierarchy** dropdown list, select **Product**.

1. To complete the hierarchy design, select **Apply Level Changes**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Hierarchy drop-down list with Apply Level Changes highlighted.](../media/lab-11-a-ssm.png)](../media/lab-11-a-ssm.png#lightbox)

    > [!TIP]
    > Don't forget to select **Apply Level Changes**. It's a common mistake to overlook this step.

1. In the **Fields** pane, notice the **Products** hierarchy.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Fields pane with the Products folder collapsed.](../media/lab-11-b-ssm.png)](../media/lab-11-b-ssm.png#lightbox)

1. To reveal the hierarchy levels, expand the **Products** hierarchy.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Fields pane with the Products folder expanded to show Category, Subcategory, and Product fields.](../media/lab-11-c-ssm.png)](../media/lab-11-c-ssm.png#lightbox)

1. To organize columns into a display folder, in the **Fields** pane, first select the **Background Color Format** column.

1. While pressing the **Ctrl** key, select the **Font Color Format** column.

1. In the **Properties** pane, in the **Display Folder** box, enter **Formatting**.

1. In the **Fields** pane, notice that the two columns are now inside a folder.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Fields pane with the Formatting folder expanded to show Background Color Format and Font Color Format.](../media/lab-11-ssm.png)](../media/lab-11-ssm.png#lightbox)

    > [!NOTE]
    > Display folders are a great way to declutter tables, especially those that contain many fields.

### Task 2: Configure the Region table

In this task, you will configure the **Region** table.

1. In the **Region** table, create a hierarchy named **Regions**, with the following three levels:

    - Group

    - Country

    - Region

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Regions hierarchy in the Fields pane.](../media/lab-12-a-ssm.png)](../media/lab-12-a-ssm.png#lightbox)

1. Select the **Country** column (not the **Country** hierarchy level).

1. In the **Properties** pane, expand the **Advanced** section at the bottom of the pane, and then in the **Data Category** dropdown list, select **Country/Region**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Properties pane and the Data category field.](../media/lab-12-ssm.png)](../media/lab-12-ssm.png#lightbox)

    > [!NOTE]
    > Data categorization can provide hints to the report designer. In this case, categorizing the column as country or region provides more accurate information when rendering a map visualization.

### Task 3: Configure the Reseller table

In this task, you will configure the **Reseller** table.

1. In the **Reseller** table, create a hierarchy named **Resellers**, with the following two levels:

    - Business Type

    - Reseller

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Resellers hierarchy in the Fields pane.](../media/lab-13-a-ssm.png)](../media/lab-13-a-ssm.png#lightbox)

1. Create a second hierarchy named **Geography**, with the following four levels:

    - Country-Region

    - State-Province

    - City

    - Reseller

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Geography hierarchy in the Fields pane.](../media/lab-13-b-ssm.png)](../media/lab-13-b-ssm.png#lightbox)

1. Categorize the following three columns:

    - **Country-Region** as **Country/Region**

    - **State-Province** as **State or Province**

    - **City** as **City**

### Task 4: Configure the Sales table

In this task, you will configure the **Sales** table.

1. In the **Sales** table, select the **Cost** column.

1. In the **Properties** pane, in the **Description** box, enter: **Based on standard cost**

    Descriptions can be applied to table, columns, hierarchies, or measures. In the **Fields** pane, description text is revealed in a tooltip when a report author hovers their cursor over the field.

1. Select the **Quantity** column.

1. In the **Properties** pane, from inside the **Formatting** section, slide the **Thousands Separator** property to **Yes**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Properties pane and the Thousands separator toggle.](../media/lab-13-ssm.png)](../media/lab-13-ssm.png#lightbox)

1. Select the **Unit Price** column.

1. In the **Properties** pane, from inside the **Formatting** section, slide the **Decimal Places** property to **2**.

1. In the **Advanced** group (you may need to scroll down to locate it), in the **Summarize By** dropdown list, select **Average**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Advanced group and the Summarize by property set to Average.](../media/lab-14-a-ssm.png)](../media/lab-14-a-ssm.png#lightbox)

    By default, numeric columns will summarize by summing values together. This default behavior is not suitable for a column like **Unit Price**, which represents a rate. Setting the default summarization to average will produce a useful and accurate result.

### Task 5: Bulk update properties

In this task, you will update multiple columns in a single bulk update. You will use this approach to hide columns, and format column values.

1. While pressing the **Ctrl** key, select the following 14 columns (spanning multiple tables):

    - Product | ProductKey

    - Region | SalesTerritoryKey

    - Reseller | ResellerKey

    - Sales | EmployeeKey

    - Sales | ProductKey	

    - Sales | ResellerKey

    - Sales | SalesOrderNumber

    - Sales | SalesTerritoryKey

    - Salesperson | EmployeeID

    - Salesperson | EmployeeKey

    - Salesperson | UPN

    - SalespersonRegion | EmployeeKey

    - SalespersonRegion | SalesTerritoryKey

    - Targets | EmployeeID

1. In the **Properties** pane, toggle the **Is Hidden** property to **On**.

    The columns were hidden because they are either used by relationships or calculation logic.

    You’ll define row-level security in the **Model data in Power BI Desktop, Part 2** lab using the **UPN** column. You’ll use the **SalesOrderNumber** in a calculation in the **Create DAX calculations in Power BI Desktop, Part 1** lab.

1. Multi-select the following three columns:

    - Product | Standard Cost

    - Sales | Cost

    - Sales | Sales

1. In the **Properties** pane, from inside the **Formatting** section, set the **Decimal Places** property to **0** (zero).

## Exercise 3: Review the model interface

In this exercise, you will switch to Report view, and review the model interface.

### Task 1: Review the model interface

In this task, you will switch to Report view, and review the model interface.

1. Switch to Report view.

1. In the **Fields** pane, notice the following:

    - Columns, hierarchies, and their levels are fields, which you can use to configure report visuals

    - Only fields relevant to report authoring are visible

    - The **SalespersonRegion** table is not visible because all of its fields are hidden

    - Spatial fields in the **Region** and **Reseller** table are adorned with a spatial icon

    - Fields adorned with the sigma symbol (Ʃ) will summarize by default

    - A tooltip appears when hovering the cursor over the **Sales | Cost** field

1. Expand the **Sales | OrderDate** field, and then notice that it reveals a date hierarchy.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Power B I Desktop Fields pane with OrderDate expanded to show a Date Hierarchy.](../media/lab-14-b-ssm.png)](../media/lab-14-b-ssm.png#lightbox)

    The **Targets | TargetMonth** field presents a similar hierarchy. These hierarchies were not created by you. They are created automatically. There is a problem, however. The Adventure Works financial year commences on July 1 of each year. But, the automatically created date hierarchy year commences on January 1 of each year.

    You'll now turn this automatic behavior off. In the **Create DAX calculations in Power BI Desktop, Part 1** lab, you’ll use DAX to create a date table and configure it to define the Adventure Works calendar.

1. To turn off auto/date time, select the **File** ribbon tab to open the backstage view.

1. At the left, select **Options and Settings**, and then select **Options**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Power B I Desktop Options and settings page with an arrow to Options.](../media/lab-14-c-ssm.png)](../media/lab-14-c-ssm.png#lightbox)

1. In the **Options** window, at the left, in the **Current File** group, select **Data Load**.

1. In the **Time Intelligence** section, clear the **Auto Date/Time** option.

1. Select **OK**.

1. In the **Fields** pane, notice that the date hierarchies are no longer available.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Power B I Desktop Fields pane with OrderDate highlighted.](../media/lab-14-ssm.png)](../media/lab-14-ssm.png#lightbox)

## Exercise 4: Create quick measures

In this exercise you will create two quick measures.

### Task 1: Create quick measures

In this task, you will create two quick measures to calculate profit and profit margin.

1. In the **Fields** pane, right-click the **Sales** table, and then select **New Quick Measure**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Fields pane with the New quick measure option highlighted.](../media/lab-15-a-ssm.png)](../media/lab-15-a-ssm.png#lightbox)

1. In the **Quick Measures** window, in the **Calculation** dropdown list, from inside the **Mathematical Operations** group, select **Subtraction**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Quick measures dialog with the Subtraction option highlighted.](../media/lab-15-b-ssm.png)](../media/lab-15-b-ssm.png#lightbox)

1. In the **Quick measures** window **Fields** pane, expand the **Sales** table.

1. Drag the **Sales** field into the **Base Value** box.

1. Drag the **Cost** field into the **Value to Subtract** box.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the completed Quick Measures dialog.](../media/lab-15-ssm.png)](../media/lab-15-ssm.png#lightbox)

1. Select **OK**.

    A quick measure creates the calculation for you. They're easy and fast to create for simple and common calculations. You’ll create measures without using this tool in the **Create DAX calculations in Power BI Desktop, Part 1** lab.

1. In the **Fields** pane, inside the **Sales** table, notice the new measure.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Fields pane with the new Sales minus Cost measure highlighted.](../media/lab-16-a-ssm.png)](../media/lab-16-a-ssm.png#lightbox)

    Measures are adorned with the calculator icon.

1. To rename the measure, right-click it, and then select **Rename**.

    > [!TIP]
    > To rename a field, you can also double-click it, or select it and press **F2**.

1. Rename the measure to **Profit**, and then press **Enter**.

1. In the **Sales** table, add a second quick measure, based on the following requirements:

    - Use the **Division** mathematical operation

    - Set the **Numerator** to the **Sales | Profit** field

    - Set the **Denominator** to **Sales | Sales** field

    - Rename the measure as **Profit Margin**

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Quick measures dialog with Profit and Sum of Sales highlighted.](../media/lab-16-b-ssm.png)](../media/lab-16-b-ssm.png#lightbox)

1. Ensure the **Profit Margin** measure is selected, and then on the **Measure Tools** contextual ribbon, set the format to **Percentage**, with two decimal places.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Measure Tools ribbon with Percentage and 2 highlighted.](../media/lab-16-ssm.png)](../media/lab-16-ssm.png#lightbox)

1. To test the two measures, first select the table visual on the report page.

1. In the **Fields** pane, select the two measures.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Profit and Profit Margin measured selected.](../media/lab-17-ssm.png)](../media/lab-17-ssm.png#lightbox)

1. Select and drag the right guide to widen the table visual.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the table visual and how to expand its width.](../media/lab-18-ssm.png)](../media/lab-18-ssm.png#lightbox)

1. Verify that the measures produce reasonable result that is correctly formatted.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the properly formatted table.](../media/lab-19-ss.png)](../media/lab-19-ss.png#lightbox)

## Task 2: Finish up

In this task, you will complete the lab.

1. To remove the table, select the table (by clicking it), and then press the **Delete** key.

1. Save the Power BI Desktop file.

1. If prompted to apply queries, click **Apply Later**.

1. If you intend to start the next lab, you can opt to leave Power BI Desktop open.

    > [!WARNING]
    > If you leave the lab open, it will time out after one to four hours. Your work in the *current* module's lab will be lost, but each lab after the first one includes a PBIX file with the work from all previous labs completed so that you don't need to start over.

You’ll enhance the data model by configuring a many-to-many relationship and row-level security in the **Model data in Power BI Desktop, Part 2** lab.

[!INCLUDE [](../../../includes/power-bi-lab-end.md)]
