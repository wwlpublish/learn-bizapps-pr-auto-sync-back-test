## Overview

The estimated time to complete this exercise is 30 minutes.

In this exercise, you will complete the following tasks:

1.  Publish a Power BI Desktop Dataset & Report to the Power BI service
1.  Download, Install, and Use Analyze in Excel
1.  Build an Excel Report using a Power BI Dataset

> [!NOTE]
> This exercise has been created based on the sales activities of the *fictitious* Wi-Fi company called SureWi which has been provided by [P3 Adaptive](https://p3adaptive.com/). The data is property of P3 Adaptive and has been shared with the purpose of demonstrating Excel and Power BI functionality with industry sample data. Any use of this data must include this attribution to P3 Adaptive. If you have not already, download and extract the lab files from https://aka.ms/modern-analytics-labs into your **C:\ANALYST-LABS** folder. 

## Exercise 1: Publish a Power BI Desktop Dataset & Report to the Power BI service

In this exercise, you will use Power BI Desktop to publish your Dataset and Report to My workspace in the Power BI service.

### Task 1: Launch Power BI Desktop

In this task, you will launch Power BI Desktop and open a PBIX file.

1.  Launch Power BI Desktop.
1.  If applicable, use the "x" in the upper right-hand corner to close the Welcome window.

### Task 2: Open the PBIX file

In this task, you will navigate and open the starting PBIX file with the Dataset and Report created from Lab 02.

1.  Select **File** > **Open report** > **Browse reports**.

	
	[![Screenshot of open report window with the Browse reports button.](../media/browse-reports.png)](../media/browse-reports.png#lightbox)

1.  Navigate to the **C:\ANALYST-LABS\Lab 03A**  folder.
1.  Select the file **MAIAD Lab 03A - Power BI Model.pbix** and choose **Open**.

### Task 3: Publish the PBIX file to the Service

In this task, you will publish the Dataset and Report from the Power BI Desktop file to the Power BI service.

1.  First, you will need to sign in to Power BI. Click on **Sign in** located in the upper right-hand corner of Power BI Desktop.

	
	[![Screenshot of sign in located in the upper right-hand corner of Power B I Desktop.](../media/sign-in.png)](../media/sign-in.png#lightbox)

1.  Next, you will need to enter your Power BI **username** and **password**. Once signed in, you will notice the Sign-in changes to become your name.

	
	[![Screenshot of sign in window.](../media/sign-in-window.png)](../media/sign-in-window.png#lightbox)

1.  From the **Home** tab in the main menu, select the **Publish** button.

	
	[![Screenshot of Power B I main menu Home tab and Publish button.](../media/home-tab.png)](../media/home-tab.png#lightbox)

1.  Select My workspace.

	
	[![Screenshot of publish to Power B I window with My workspace.](../media/workspace.png)](../media/workspace.png#lightbox)

1. Choose the Select button to publish the data model and report page to the Power BI service.

	> [!NOTE]
	> All users have My workspace in Power BI service. This is your *personal* sandbox. Every organization has different Workspaces. Workspaces can be created, and users can be added to Workspaces to share Datasets and Reports across the organization.

1. Once the publish is successful, you will see the **Success!** message with a link that you can click to open the report in the Power BI service.

1. Click on the Open **MAIAD Lab 03A - Power BI Model.pbix** in Power BI link.

	
	[![Screenshot of publishing to Power B I window with success message.](../media/success.png)](../media/success.png#lightbox)

    After clicking on the link, you will be navigated to your browser where you will see your report published to Power BI service in your My workspace location.

	> [!NOTE]
	> To navigate directly to Power BI service enter the URL: [https://app.powerbi.com](https://app.powerbi.com/groups/me/reports/0a9c5249-218c-41d0-b48f-9d66c93f5e52/ReportSection) in your browser.

	
	[![Screenshot of Power B I Service with M A I A D - Power B I Report displayed.](../media/report-displayed.png)](../media/report-displayed.png#lightbox)

	> [!NOTE]
	> Selected report page, slicers and filters are captured as default settings when published to the Power BI service.

## Exercise 2: Download, install, and use Analyze in Excel 

In this exercise, you will download the Analyze in Excel libraries and use Analyze in Excel to connect to the published **MAIAD Lab 03A - Power BI Model** in Power BI from within the Excel application.

### Task 1: Download Analyze in Excel updates

In this task, you will download a one-time download of Excel libraries that enables Excel to connect to Power BI Datasets.

1. From within the Power BI service, select **Analyze in Excel updates** from the Downloads menu, which is in the upper right corner.

1. Select the **Download** button.

	
	[![Animated screenshot of a demonstration how to download Analyze in Excel updates from the Power B I Service.](/media/download-install-analyze-in-excel.gif)](../media/download-install-analyze-in-excel.gif)

### Task 2: Install Analyze in Excel

In this task, you will install the Excel libraries that enable Excel to connect to Power BI Datasets.

1. Once the download completes, the installation file will be in your default Downloads folder. Navigate to your downloaded file and **Double-Click** the file to launch the (.msi) installer wizard.

	
	[![Screenshot of My Downloads folder and the downloaded M S I file.](../media/open.png)](../media/open.png#lightbox)
	> [!NOTE]
	> You can open this file directly from your browser's Downloads section. For Firefox this is in the top right corner. For Internet Explorer this is the bottom left. Download location varies by browser.

1. Follow the wizard steps to install the Analyze in Excel libraries.

	
	[![Screenshot of Analyze in Excel install wizard window.](../media/next.png)](../media/next.png#lightbox)

### Task 3: Launch Analyze in Excel from Datasets + dataflows

In this task, you will navigate to the Datasets + dataflows location in the Power BI service to launch Analyze in Excel using the "MAIAD Lab 03A - Power BI Model" Dataset.

1. From the left-hand pane navigation, select **My workspace**.

1. Select the **Datasets + dataflows** navigation option.

	
	[![Screenshot of Power B I Service with M A I A D - Lab 03 - Power B I Model displayed in Data sets from My workspace.](../media/datasets-dataflows.png)](../media/datasets-dataflows.png#lightbox)

	> [!NOTE]
	> When you publish your PBIX file to the service, there are two Power BI artifacts created: the Data Model will be in **Datasets + dataflows** and Report Pages will be in **Reports**.

1. From the **MAIAD Lab 03A - Power BI Model** Dataset select **More options** and then choose the **Analyze in Excel** menu option.

	
	[![Screenshot of Power B I Service Dataset More menu showing the Analyze in Excel option.](../media/analyze-excel.png)](../media/analyze-excel.png#lightbox)

### Task 4: Launch the Analyze in Excel file

In this task, you will launch the Excel file that has been connected to the **MAIAD Lab 03A - Power BI Model** Data Model.

1. Navigate to your Downloads folder, find the downloaded Excel file and **Double Click** the file to open.

	
	[![Screenshot of My Downloads folder with the Excel file selected in Windows Explorer.](../media/excel-open.png)](../media/excel-open.png#lightbox)
	> [!NOTE]
	> You can open this file directly from your browser's Downloads section. For Firefox this is in the top right corner. For Internet Explorer this is the bottom left. Download location varies by browser.

1. Once Excel launches, you may need to click the buttons to **Enable Editing** and **Enable Content**. This allows Excel to connect to the data model published to the Power BI service, which is an external data connection to Microsoft's Azure storage in the cloud.

	
	[![Screenshot of Enable Editing and Enable Content message and buttons.](../media/enable-message.png)](../media/enable-message.png#lightbox)

	> [!NOTE]
	> If you are not prompted with both the Enable Editing and Enable Content messages, you may need to check your Options > Trust Center > Trust Center Settings... to ensure your Message Bar Settings are turned on.

## Exercise 3: Build an Excel report using a Power BI Dataset

In this exercise, you will create a report in Excel using the Power BI Dataset connected to "MAIAD Lab 03A - Power BI Model" created using Analyze in Excel. The Excel report will contain a Pivot Table, a Pivot Chart, and CUBE formulas.

### Task 1: Add Measures to the Pivot Table Fields Values

In this task, you will populate the Pivot Table with Measure fields from the Power BI Dataset connection.

1. From the **Pivot Table Fields** window, select the Gear icon and change to the Fields Section and Areas Section Side-By-Side option.

	
	[![Screenshot of Pivot Table Fields highlighting the Gear icon.](../media/gear.png)](../media/gear.png#lightbox)

	> [!NOTE]
	> By default, the Pivot Table Fields are displayed with the **Fields Section and Areas Section Stacked**. The instructions that follow have the Pivot Table Fields displayed as **Fields Section and Areas Section Side-By-Side**.

1. From the **Offices** measure table, drag the [# of Offices] measure to the **Values** section in the Pivot Table Fields List.

1. From the **Contracts** measure table, click the **checkbox** for the [Total Contracts] & [MRR Won - Contracts] measures to the **Values** section in the Pivot Table Fields List.

	
	[![Screenshot of Pivot Table Fields List window with the measures in the Values section.](../media/measures.png)](../media/measures.png#lightbox)

	> [!NOTE]
	> When selecting fields from the measure tables, the checkbox will move the field into the Values section by default. This is because only measures can go into the Values section of a Pivot Table Field List when connecting Excel to a Power BI service Dataset.

1. Right click on the Pivot Table, select the **Pivot Table Options**...

	
	[![Screenshot of Pivot Table menu displaying the Pivot Table Options menu item.](../media/options.png)](../media/options.png#lightbox)

1. Select Display and then de-select the checkbox to **Show the Values row**.

	
	[![Screenshot of Pivot Table Options window with the Show the Values row check box de-selected.](../media/values-row.png)](../media/values-row.png#lightbox)

	> [!NOTE]
	> This is done for aesthetics purposes to remove the row with **Values** in the heading that happens by default when adding more than one measure into the Values section of the Pivot Table Fields.

### Task 2: Add Fields to the Pivot Table Fields Rows

In this task, you will populate the Pivot Table with Lookup fields from the Power BI Dataset connection.

1. From the **Offices** field table, drag the [Region] and [District] columns to the **Rows** section in the Pivot Table Fields List.

	
	[![Screenshot of Pivot Table Fields List window with the fields from the Offices table in the Rows section.](../media/fields.png)](../media/fields.png#lightbox)

1. Use the mouse to place the cursor in **Cell A1** and type the name **Region & District** into the cell to change the default heading name.

	
	[![Screenshot of close up of the Pivot Table header to show the label in column A row 1.](../media/label.png)](../media/label.png#lightbox)

### Task 3: Insert a Pivot Chart

In this task, you will insert a Pivot Chart workspace into the Excel worksheet to the right of the Pivot Table. Then you will add fields to the Axis and Values sections.

1. Use your mouse to select **Cell E1** on the worksheet. This is the selects the location for the Pivot Chart.

	
	[![Screenshot of Worksheet with column E row 1 selected for location of new Pivot Chart.](../media/location.png)](../media/location.png#lightbox)

1. Select the **Insert** tab on the main menu and select the **Pivot Chart** option from the **Pivot Chart** button drop-down.

	
	[![Screenshot of Insert tab on main menu with Pivot Chart button drop down selected and Pivot Chart option.](../media/pivotchart.png)](../media/pivotchart.png#lightbox)

1. On the Create Pivot Chart window, select the **Use an external data source** radio button.

1. Select the **Choose Connection**... button.

	
	[![Screenshot of Create Pivot Chart window showing the Use an external data source radio button selected and the Choose Connection button.](../media/connection.png)](../media/connection.png#lightbox)

1. Then from the **Connections** tab and the **Connections in this Workbook** section, select the `pbiazure//api.powerbi.com` connection string path name to connect the Pivot Chart to the Power BI Dataset external data source.

	
	[![Screenshot of Existing Connections window with the Connections tab selected, Connections in this Workbook section with the Power B I Service Azure connection path.](../media/workbook-connections.png)](../media/workbook-connections.png#lightbox)

   > [!NOTE]
   > The exact name of your pbiazure://api.powerbi.com connection string will be different than the one shown in the above image. This is the unique connection location identifier for a published Power BI dataset artifact.

1. Click **OK**.

1. From the **Quotes** measure table, click the **checkbox** next to the [Won vs Potential MRR] measure to move the measure into the **Values** section in the Pivot Table Fields List.

1. From the **Offices** field table, drag the [Region] to the **Axis (Categories)** section in the Pivot Table Fields List.

	
	[![Screenshot of Pivot Table Fields with measure from the Quotes table in the Values.](../media/pivot-table-fields.png)](../media/pivot-table-fields.png#lightbox)

### Task 4: Format Pivot Chart

In this task, you will format the Pivot Chart using some of the familiar formatting options in Excel.

1. From the **Design** tab in the main menu, select **Style 4**.

	
	[![Screenshot of Design tab on the main menu with Style 4 selected.](../media/design.png)](../media/design.png#lightbox)

1. Double-click into the Chart Title and change the default Title text to **MMR Won % by Region**.

1. Use the mouse to hover over the upper right-hand side of the Pivot Chart to display the Chart Elements options and **de-select the Legend checkbox** to remove the Legend.

	
	[![Screenshot of Pivot Chart Chart Elements with the Legend checkbox de-selected.](../media/legend.png)](../media/legend.png#lightbox)

### Task 5: Add KPIs using CUBEVALUE

In this task, you will use CUBE formulas to create high-level KPIs for the report.


1. Rename the **data connection** with a friendly name. Click on Data -> Queries & Connections to open the **Queries & Connections** along the right-hand side.
	 

	 [![Screenshot of Excel Data Tab Queries and Connections button with visual of Connections selected in pane.](../media/queries-connections-pane.png)](../media/queries-connections-pane.png#lightbox)

	> [!NOTE]

	> The exact name of your `pbiazure://api.powerbi.com` connection string will be different than the one shown in the above image. This is the unique connection location identifier for a published Power BI dataset artifact.

1. Select **Connections**, right-click, choose **Properties**, change the connection name to **Power BI - MAIAD Lab 03A – Power BI Model**, and then press ok.

	
	[![Screenshot of Excel Data Connection Properties with new name in Connection name box alongside image of Properties button.](../media/rename-data-connection.png)](../media/rename-data-connection.png#lightbox)
	> [!NOTE]
	> Best practice when referencing data models within Excel is to provide user friendly names for reference and to provide a detailed description about the data connection.

1. Use a **right-click on row 1** to **Insert** a row above the Pivot Table and Pivot Chart.

1. Use **CTRL+Y** to repeat the last step and add another row above the Pivot Table and Pivot Chart.

1. Use a **right-click on column A** to **Insert** a column before the Pivot Table.

	> [!NOTE]
	> This provides a row and column buffer for aesthetics purposes. And provides a row for a report heading and the KPIs using CUBEVALUE formulas.

1. Right-click **column A and set the column with to 1**.

1. Use **Fill Color = Black** from the **Home** tab on the main menu to create a report heading in row 2.

1. Use **Font Color = Gold, Accent 4** for row 2.

1. Select **Cell I2** and enter the text **"Potential MRR:"** - this will serve as the KPI description.

1. In **Cell J2** enter the following CUBEVALUE formula and hit Enter:

    =CUBEVALUE("Power BI - MAIAD Lab 03A – Power BI Model","[Measures].[Potential MRR]")

	
	[![Screenshot of Formula bar with measure access.](../media/measure-access.png)](../media/measure-access.png#lightbox)

	> [!TIP]
	> As you type the CUBEVALUE formula, you will notice that Intellisense displays to guide you as to the syntax needed to complete the formula. A CUBEVALUE formula can be combined for use with Slicers.

1. Select **Cell K2** and enter the text **"Won MRR:"** - this will serve as the KPI description.

1. In **Cell L2** enter the following CUBEVALUE formula and hit Enter:

    =CUBEVALUE("Power BI - MAIAD Lab 03A – Power BI Model","[Measures].[MRR Won - Contracts]")

	
	[![Screenshot of Formula bar with cubevalue function for calculating using a measure from the data model.](../media/cube-value.png)](../media/cube-value.png#lightbox)

    Select **Cell M2** and enter the text **"% Won:"** - this will serve as the KPI description.

1. In **Cell N2** enter the following Excel formula and hit Enter:

    =L2/J2

	
	[![Screenshot of Formula bar with an Excel cell division formula.](../media/formula-bar.png)](../media/formula-bar.png#lightbox)

	> [!TIP]
	> You can combine the familiarity and features of Excel with Dataset published to Power BI!

1. Using a **right-click**, select **Format Cells**... to **percentage**.

1. Select **File** from the Main Excel Ribbon Menu, then **Save As**.

1. Navigate to the **C:\ANALYST-LABS\Lab 03A**  folder.

1. Save the file as **MAIAD Lab 03A - Power BI Model - My Solution.xlsx**.

In this exercise, you published a Power BI Desktop Dataset and Report to the Power BI service. Then you created a report in Excel with a Pivot Table, Pivot Chart, and CUBE functions connected to a Power BI Dataset. This final exercise illustrates what is possible when you use Power BI together with Excel.

> 
> [![Screenshot of the final Excel report with Pivot Table, Pivot Chart, and Cube Value formulas.](../media/final-report.png)](../media/final-report.png#lightbox)

> [!IMPORTANT]
> Now that you have your report created, you will want to keep it updated. But do not worry, it takes just two button clicks: **Data** > **Refresh All**.

> 
> [![Screenshot of data tab on main menu with Refresh All button displayed.](../media/refresh.png)](../media/refresh.png#lightbox)
