In this lab, you will create the **Sales Monitoring** dashboard.

In this lab, you learn how to:

-   Pin visuals to a dashboard

-   Use Q&A to create dashboard tiles

-   Configure a dashboard tile alert

## Create a sales monitoring dashboard

In this exercise, you will create the **Sales Monitoring** dashboard. The completed dashboard will look like the following:

> [!div class="mx-imgBorder"]
> [![Screenshot of the Sales Monitoring dashboard.](../media/lab-1-ss.png)](../media/lab-1-ss.png#lightbox)

> [!NOTE]
> The exercise will require you to login to Power BI service, you will use your existing account or create a trial account before starting this part of the lab.

### Create a dashboard

In this task, you will create the **Sales Monitoring** dashboard.

1.	In Edge, in the Power BI service, open the Sales Report file you created in earlier lab, you will find the file in My Workspace. 

1.	If you are prompted to login to Power BI, please use your Power BI account credentials to login. 

1.	If you get “Unable to connect” error when opening the report, click Edit to select Sale Analysis dataset and click Create to re-create Sales Report.  You will save the file, and then republish the report. 

1.	After logging in, select Overview page from the report. 

1.	To create a dashboard and pin the logo image, hover the cursor over the Adventure Works logo.

1.	At the top-right corner, click the pushpin.


	> [!div class="mx-imgBorder"]
	> [![Screenshot of the pushpin.](../media/lab-2-ssm.png)](../media/lab-2-ssm.png#lightbox)

1.  In the **Pin to Dashboard** window, in the **Dashboard Name** box, enter **Sales Monitoring**.

1.  Click **Pin**.

1.  Set the **Year** slicer to **FY2020**.

1.  Set the **Region** slicer to **Select All**.

	> *When pinning visuals to a dashboard, they will use the current filter context. Once pinned, the filter context cannot be changed. For time-based filters, it's a better idea to use a relative date slicer (or, Q&A using a relative time-based question).*

1.  Pin the **Sales and Profit Margin by Month** (column/line) visual to the **Sales Monitoring** dashboard.

1.  Open the **Navigation** pane, and then open the **Sales Monitoring** dashboard.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Sales Monitoring dashboard in the Navigation pane.](../media/lab-3-ssm.png)](../media/lab-3-ssm.png#lightbox)

1. Notice that the dashboard has two tiles.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the two tiles on the Sales Monitoring dashboard.](../media/lab-4-ss.png)](../media/lab-4-ss.png#lightbox)

1. To resize the logo tile, drag the bottom-right corner, and resize the tile to become one unit wide, and two units high.

	Tile sizes are constrained into a rectangular shape. It's only possible to resize into multiples of the rectangular shape.

1. To add a tile based on a question, at the top-left of the dashboard, click **Ask a Question About Your Data**.

1. You can use the Q&A feature to ask a question, and Power BI will respond with a visual.

1. Click any one of the suggested questions beneath the Q&A box, in gray boxes.

1. Review the response.

1. Remove all text from the Q&A box.

1. In the Q&A box, enter the following: **Sales YTD**

1. Notice the response of **(Blank)**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Sales YTD showing the word Blank.](../media/lab-5-ss.png)](../media/lab-5-ss.png#lightbox)

	This measure is a Time Intelligence expression and it requires a filter on the **Date** table to produce a result.

1. Extend the question with: **in year FY2020**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Q&A field with the text Sales YTD in year FY2020.](../media/lab-6-ssm.png)](../media/lab-6-ssm.png#lightbox)

1. Notice the response is now **$33M**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of Blank replaced with $33M.](../media/lab-7-ss.png)](../media/lab-7-ss.png#lightbox)

1. To pin the response to the dashboard, at the top-right corner, click **Pin Visual**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Pin Visual option.](../media/lab-8-ssm.png)](../media/lab-8-ssm.png#lightbox)

1. When prompted to pin the tile to the dashboard, click **Pin**.

	> [!div class="mx-imgBorder"]
	> [![ Screenshot of the Pin to dashboard window.](../media/lab-9-ssm.png)](../media/lab-9-ssm.png#lightbox)

	There's a possible bug that will only allow you to pin to a new dashboard. It's because your Power BI session has reverted to your "My Workspace". If this happens, do not pin to a new dashboard. Return to your **Sales Analysis** workspace, open the dashboard again, and recreate the Q&A question.

1. To return to the dashboard, at the top-left corner, click **Exit Q&A**.

### Edit tile details

In this task, you will edit the details of two tiles.

1. Hover the cursor over the **Sales YTD** tile, and then at the top-right of the tile, click the ellipsis, and then select **Edit Details**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the drop-down menu showing Edit details.](../media/lab-10-ssm.png)](../media/lab-10-ssm.png#lightbox)

1. In the **Tile Details** pane (located at the right), in the **Subtitle** box, enter **FY2020**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Tile details window with the Subtitle field highlighted and containing FY2020.](../media/lab-11-ssm.png)](../media/lab-11-ssm.png#lightbox)

1. At the bottom of the pane, click **Apply**.

1. Notice that the **Sales YTD** tile displays a subtitle.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of FY2020 text displayed as a subtitle under Sales YTD on the tile.](../media/lab-12-ssm.png)](../media/lab-12-ssm.png#lightbox)

1. Edit the tile details for the **Sales, Profit Margin** tile.

1. In the **Tile Details** pane, in the **Functionality** section, check **Display Last Refresh Time**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Funtionality section with Display last refresh time checked.](../media/lab-13-ssm.png)](../media/lab-13-ssm.png#lightbox)

1. Click **Apply**.

1. Notice that the tile describes the last refresh time (which you did when refreshing the data model in Power BI Desktop).

	> *Later in this lab, you'll simulate a data refresh, and notice that the refresh time updates.*

### Configure an alert

In this task, you will configure a data alert.

1. Hover the cursor over the **Sales YTD** tile, click the ellipsis, and then select **Manage Alerts**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the ellipsis drop-down menu with Manage alerts highlighted.](../media/lab-14-ssm.png)](../media/lab-14-ssm.png#lightbox)

1. In the **Manage Alerts** pane (located at the right), click **Add Alert Rule**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Manage alerts pane.](../media/lab-15-ssm.png)](../media/lab-15-ssm.png#lightbox) 

1. In the **Threshold** box, replace the value with **35000000** (35 million).

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Threshold box with the Threshold field containing 35000000.](../media/lab-16-ssm.png)](../media/lab-16-ssm.png#lightbox)

	> *This configuration will ensure you're notified whenever the tile updates to a value above 35 million.*

1. At the bottom of the pane, click **Save and Close**.

In the next exercise, you'll refresh the dataset. Typically, this should be done by using scheduled refresh, and Power BI could use a gateway to connect to the SQL Server database. However, due to constraints in the classroom setup, there is no gateway. So, you'll opening Power BI Desktop, perform a manual data refresh, and the upload the file.

## Refresh the dataset

In this exercise, you will first load sales order data for June 2020 into the **AdventureWorksDW2020** database. You will then open your Power BI Desktop file, perform a data refresh, and then upload the file to your **Sales Analysis** workspace.

### Update the lab database

In this task, you will run a PowerShell script to update data in the **AdventureWorksDW2020** database.

1. In File Explorer, inside the **D:\DA100\Setup** folder, right-click the **UpdateDatabase-2-AddSales.ps1** file, and then select **Run with PowerShell**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Run with PowerShell option.](../media/lab-17-ssm.png)](../media/lab-17-ssm.png#lightbox)

1. When prompted to press any key to continue, press **Enter** again.

	*The **AdventureWorksDW2020** database now includes sales orders June 2020.*

### Refresh the Power BI Desktop file

In this task, you will open the Sales Analysis Power BI Desktop file, perform a data refresh, and then upload the file to your **Sales Analysis** workspace.

1. Open your **Sales Analysis** Power BI Desktop file, stored in the **D:\DA100\Lab10A\Starter** folder.

1. On the **Home** ribbon, from inside the **Queries** group, click **Refresh**.

1. When the refresh completes, save the Power BI Desktop file.

1. Publish the file to your workspace.

1. When prompted to replace the dataset, click **Replace**.

	> *The dataset in the Power BI service now has June 2020 sales data.*

1. Close Power BI Desktop.

1. In Edge, in the Power BI service, in your **Sales Analysis** workspace, notice that the **Sales Analysis** report was also published.

## Review the dashboard for updated sales

In this exercise, you will review the dashboard to notice updated sales, and that the alert was triggered.

### Review the dashboard

In this task, you will review the dashboard to notice updated sales, and that the alert was triggered.

1. In Edge, in the Power BI service, open the **Sales Monitoring** dashboard.

1. In the **Sales, Profit Margin** tile, in the subtitle, notice that the data was refreshed **NOW**.

1. Notice also that there is now a column for **2020 Jun**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Sales, Profit Margin tile. ](../media/lab-18-ssm.png)](../media/lab-18-ssm.png#lightbox)

	The alert on the **Sales YTD** tile should have triggered also. After a short while, the alert should notify you that sales now exceeds the configured threshold value.

1. Notice that the **Sales YTD** tile has updated to **$37M**.

1. Verify that the **Sales YTD** tile displays an alert notification icon.

	If you don't see the notification, you might need to press **F5** to reload the browser. If you still don't see the notification, wait some minutes longer.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the notification icon on the Sales YTD tile.](../media/lab-19-ssm.png)](../media/lab-19-ssm.png#lightbox)

Alert notifications appear on the dashboard tile, and can be delivered by email, and push notifications to mobile apps including the Apple Watch.
