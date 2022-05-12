## Overview

The estimated time to complete this exercise is 30 minutes.

In this exercise, you will complete the following tasks:

1.  Use Excel to create a pivot table from a Dataset published in the Power BI service

1.  Add Sparkline Charts

> [!NOTE]
> This exercise has been created based on the sales activities of the *fictitious* Wi-Fi company called SureWi which has been provided by [P3 Adaptive](https://p3adaptive.com/). The data is property of P3 Adaptive and has been shared with the purpose of demonstrating Excel and Power BI functionality with industry sample data. Any use of this data must include this attribution to P3 Adaptive. If you have not already, download and extract the lab files from https://aka.ms/modern-analytics-labs into your **C:\ANALYST-LABS** folder. 

## Exercise 1: Use Excel to create a Pivot Table from a Data Set in the Power BI service

In this exercise, you will use Excel to connect to a published Data Set in the Power BI service.

### Task 1: Launch Excel

In this task, you will launch a new blank worksheet to get started.

1.  Launch Excel.

	> [!NOTE]
	> If you have not already signed in to your O365 account, you may be prompted to sign in, use your work email address and password to sign into your account.

1.  Create a new blank workbook.

### Task 2: Use Insert new Pivot Table from Power BI

In this task, you will create a new Pivot Table workspace connected to a published data set in the Power BI service.

1.  Select the **Insert** tab on the Main Excel main ribbon menu.

1.  Choose **PivotTable** > **From Power BI**.

	> 
	> [![Screenshot of Insert tab with PivotTable button and From Power BI displayed.](../media/pivot-table-button.png)](../media/pivot-table-button.png#lightbox)

1.  If you have many published Data Sets, you can use the **Search** option to type in "Lab", then select the **MAIAD Lab 03 - Power BI Model** data set from the available data set options.

	> 
	> [![Screenshot of Power BI Datasets window.](../media/datasets-window.png)](../media/datasets-window.png#lightbox)

1.  Notice you have a new Pivot Table workspace and the PivotTable Fields with Measure and Field tables.

	> [!NOTE]
	> Measure tables are identified by the summation icon. This behaviour occurs when Excel connects to a Power BI data set. All Measures that can ONLY go into the Values of the PivotTable Fields will be in located in the summation icon table name. And any of the columns or calculated columns that are used for Filters, Columns, or Rows are located in a table icon of the same name.

	> 
	> [![Screenshot of New Excel workbook connected to MAIAD Lab 03 in the Power BI service displaying new Pivot Table workspace and PivotTable Fields.](../media/workbook-connected.png)](../media/workbook-connected.png#lightbox)

	> [!NOTE]
	> On the right-hand side of the PivotTable Fields window, notice the icons that allow you to toggle the window between Power BI Datasets or PivotTable Fields.

	> 
	> [![Screenshot of PivotTable Fields close-up showing the Power BI Datasets and PivotTable Fields icons.](../media/pivot-table-fields-icon.png)](../media/pivot-table-fields-icon.png#lightbox)

### Task 3: Add Measures to the PivotTable Fields Values

In this task, you will populate the PivotTable with Measure fields from the Power BI Dataset connection.

1.  From the **Contracts** measure table, drag the [Raw MRR per Office] measure to the **Values** section in the PivotTable Fields List.

	> 
	> [![Screenshot of PivotTable Fields with measure in the Values.](../media/measure-values.png)](../media/measure-values.png#lightbox)

### Task 4: Add Fields to the PivotTable Fields Rows

In this task, you will populate the PivotTable with Lookup fields from the Power BI Dataset connection.

1.  From the **Offices** field table, drag the [Region]and [District] fields to the **Rows** section in the PivotTable Fields List.

	> [!NOTE]
	> Lookup field tables are identified by the table with fields icon.

	> 
	> [![Screenshot of PivotTable Fields window displaying the fields in the Rows.](../media/fields-rows.png)](../media/fields-rows.png#lightbox)

1.  From the **Dates** field table, drag the [Year] field to the **Columns** section in the PivotTable Fields List.

	> 
	> [![Screenshot of Excel workbook showing the Year in Columns and Pivot Table results.](../media/year-results.png)](../media/year-results.png#lightbox)

### Task 5: Add Slicers

In this task, you will Add Slicers connected to the Pivot Table.

1. If the PivotTable Fields list does not display, click on the Pivot Table to make it *active* and then use a right click and choose **Show Field List**.

1. In the PivotTable Fields, locate the **Customers** Lookup fields table, right-click on the [Company Size] field.

1. Select the **Add as Slicer** option.

	> [!NOTE]
	> The Slicer will just appear in a random location the worksheet, we will reposition the Slicer in the next task.

1. You can also add a Slicer from the Main ribbon menu. Click on the Pivot Table to make it active and then click on the **PivotTable Analyze** tab in the Main ribbon menu.

1. Click the **Insert Slicer** button.

1. From the **Customers** Lookup fields table, click the checkbox next to the [Segment] field.

### Task 6: Move & Format Slicers

In this task, you will insert blank Rows and Columns to make space for the Slicers to create a mindful report design for the end users.

1. Right-click on Column A and **Insert 1 blank column** to the left of the Pivot Table.

1. Right-click on Column A to resize the Column Width to 1.

	> 
	> [![Screenshot of Worksheet displaying column width of A to 1.](../media/column-width.png)](../media/column-width.png#lightbox)

1. Right-click in Row 1 and **Insert 1 blank row** above the Pivot Table.

1. Use **CTRL+Y** to repeat the insert **five times** to create a total of 6 blank rows above the Pivot Table. This will provide space for our Slicers above the Pivot Table.

1. Drag the **Company Size slicer** above the Pivot Table.

1. With the Company Size slicer selected, choose the **Slicer** tab on the Main ribbon menu.

1. Change the Slicer Buttons number of Columns to 3.

	> 
	> [![Screenshot of Slicer tab options and Buttons options.](../media/slicer.png)](../media/slicer.png#lightbox)

1. Change the Slicer Style color to **Dark Blue**.

	> 
	> [![Screenshot of Slicer tab options and Slicer Styles.](../media/slicer-options.png)](../media/slicer-options.png#lightbox)

1. Drag the **Segment slicer** above the Pivot Table and to the right of the Company Size slicer.

1. With the Segment slicer selected, choose the **Slicer** tab in the Main ribbon menu.

1. Change the Slicer Buttons number of Columns to 5.

1. Change the Color to **Dark Blue**.

	> 
	> [![Screenshot of Worksheet displaying re-positioning of Slicers.](../media/reposition.png)](../media/reposition.png#lightbox)

### Task 7: Add Report Title & Format Pivot Table

In this task, you will add a title for the Report and apply final formatting to the Pivot Table.

1. In cell B2, enter the Report title **MAIAD - Lab 03B - Excel & Power BI service - better together** and use **CTRL + B** to make the font bold.

1. In cell B8, enter the Pivot Table row title **By Region & District**.

1. In cell C7, enter the Pivot Table column title **By Year**.

	> 
	> [![Screenshot of Worksheet with Report Title and Pivot Table Rows and Column Headings.](../media/title-rows-headings.png)](../media/title-rows-headings.png#lightbox)

1. Click in the Pivot Table to make it active.

1. Select **Design** from the Main ribbon menu > **Subtotals** button > **Subtotals at Top of Group** option. This will create Subtotals for each Region in the Pivot Table.

1. Highlight Columns C to J and with a right-click, change the Column Width to 12.

1. With the Columns C to J still highlighted, select the **Center** Alignment from the Home tab on the Main ribbon menu.

	> 
	> [![Screenshot of Home tab with Center Alignment.](../media/center.png)](../media/center.png#lightbox)

1. Expand the Segment Slicer so that each of the values is fully visible to the end user.

1. Right-click on the Pivot Table and select **PivotTable Options...**

1. From the Layout & Format tab, de-select the **Autofit column widths on update** checkbox.

	> 
	> [![Screenshot of Autofit column widths on update check-box.](../media/autofit.png)](../media/autofit.png#lightbox)

## Exercise 2: Add Sparklines 

In this exercise, you will create Sparkline charts to display the Year trend next to the Pivot Table.

### Task 1: Create Sparkline chart

In this task, you will create a Sparkline chart, combining features in Excel with a Data Model published to the Power BI service.

1. Position your cursor in cell **K9** then choose **Insert** from the main ribbon menu and select the **Line** button.

	> 
	> [![Screenshot of Insert menu options with Line button in Sparklines.](../media/sparklines.png)](../media/sparklines.png#lightbox)

1. Enter the Data Range for the **Central Region** and the Years 2013 to 2017 (D9:H9). Then select the **OK** button.

1. From the Sparkline menu options, select the **Sparkline Color drop down** and change to **Green, Accent 6**.

	> 
	> [![Screenshot of Sparkline menu with Sparkline Color palette displayed.](../media/sparkline-color.png)](../media/sparkline-color.png#lightbox)

1. From the Sparkline menu options, select the **Marker Color drop down** and add a **Green, Accent 6** High Point. Then add a **Dark Red** Low Point.

	> 
	> [![Screenshot of Marker Color Low Point set to Dark Red.](../media/dark-red.png)](../media/dark-red.png#lightbox)

1. In Column K, copy/paste the Sparkline for each of the Region rows.

1. In cell K8, enter the title **Completed Year Trend**.

	> 
	> [![Screenshot of Column K with Sparkline Charts.](../media/charts.png)](../media/charts.png#lightbox)

1. Hold the **CTRL** key and highlight each of the Region rows (9, 13, 16, 19, and 23) and then with a right-click, select the **Row Height**... and change to 20.

	> 
	> [![Screenshot of Pivot Table with Region Rows highlighted and Row Height changed to 20.](../media/row-height.png)](../media/row-height.png#lightbox)

### Task 2: Final Formatting

In this task, you will create a final polished report by removing the Excel Headings and Gridlines.

1. From the main ribbon menu, select the **View** tab.

1. De-select the **Formula Bar**, **Headings**, and **Gridlines** check boxes.

	> 
	> [![Screenshot of View menu with Formula Bar, Gridlines and Headings options de-selected.](../media/view-menu.png)](../media/view-menu.png#lightbox)

1. Select the Pivot Table and use a **right-click** to display the **PivotTable Options** and de-select the **Autofit column widths on update check box**. This will keep the Pivot Table column widths when slicers are selected.

	> 
	> [![Screenshot of PivotTable Options window.](../media/pivot-table-options-window.png)](../media/pivot-table-options-window.png#lightbox)

### Task 3: Save the Excel file

In this task, you will save the Excel file.

1. From the main ribbon menu, select **File** > **Save**.

1. Navigate to the **C:\ANALYST-LABS\Lab 03B** folder.

1. Save the file as **MAIAD Lab 03B - Solution.xlsx**.

In this exercise, you started in the Excel application and connected to a published data set in the Power BI service to create a Pivot Table with Slicers and Sparkline charts, demonstrating how Excel + Power BI is used better together!

> 
> [![Screenshot of Completed Lab 04 solution.](../media/completed-lab.png)](../media/completed-lab.png#lightbox)

