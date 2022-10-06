You can build the rest of your Power BI report either in Power BI Desktop or the Power BI app for Teams. The Power BI app for Teams is an embedded version of Power BI Service. Power BI Desktop contains the full range of report building capabilities. If you build the report in Teams, other users are able to collaborate with you. In this lab, you'll build out the rest of the report in Microsoft Teams.

## Task: Publish report to Teams

1.  In your Power BI Desktop file, select the **Home** tab in the ribbon, then select **Publish**. If prompted, select to save your changes.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the publish report button.](../media/publish.png)](../media/publish.png#lightbox)

1.  You can now select the workspace you wish to publish to. Select the name of the workspace you created earlier in this lab, that is, **Office - \<your name\>**, then select **Select**.

	> [!NOTE]
	> Publishing to a team requires Power BI Pro or Premium license, which should have been set up either by your lab facilitator or by yourself in the prerequisites. If you are unable to access the Pro or Premium license, you can choose to publish your report to the **My workspace** workspace.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the destination workspace.](../media/destination.png)](../media/destination.png#lightbox)

1.  You'll get this confirmation once the report has been published. Select **Got it**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the success message with got it button.](../media/success.png)](../media/success.png#lightbox)

1.  Navigate back to Microsoft Teams. If you need to open it again, you can access it by going to [Teams](https://teams.microsoft.com/?azure-portal=true) in your web browser and signing in with your lab credentials. In Teams, launch the Power BI app.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of launching Power BI Teams app.](../media/power-bi-app.png)](../media/power-bi-app.png#lightbox)

1.  Select Workspaces. If not selected already, select the team you've published the report to.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of workspaces menu selected.](../media/select-workspaces.png)](../media/select-workspaces.png#lightbox)

1.  Select **Contoso Coffee Swag Request Report**, of the Report type (don't select the dataset).

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Contoso Coffee Swag Request report selected.](../media/report.png)](../media/report.png#lightbox)

1.  On the ribbon at the top of the report, select **Edit**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the edit button.](../media/edit.png)](../media/edit.png#lightbox)

	> [!NOTE]
	> If you experience the same error below. Select the globe icon button to redirect to Power BI Service.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of Power BI extension missing credential error.](../media/error.png)](../media/error.png#lightbox)
 
	> [!div class="mx-imgBorder"]
	> [![Screenshot of the globe icon.](../media/globe.png)](../media/globe.png#lightbox)

1.  In Power BI Service, select the ... button then select **Settings** > **Settings**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the open settings menu.](../media/open-settings.png)](../media/open-settings.png#lightbox)

1.  Under **Datasets,** check the **Data source credentials.** Make sure it's signed in correctly. Then go back to Teams then refresh.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the datasets.](../media/datasets.png)](../media/datasets.png#lightbox)

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Power BI service sign in.](../media/sign-in.png)](../media/sign-in.png#lightbox)

1.  The space indicated below is the report canvas, where you'll be building your report. There are three panes at on the left side of the screen- Filters, Visualizations and Fields, which can be collapsed if you wish to zoom in on the canvas. Depending on the size of your screen, some buttons in the ribbon of the top may be hidden behind the **...** on the right side of the screen.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the report canvas.](../media/report-canvas.png)](../media/report-canvas.png#lightbox)

1. Select the **View** button to switch the toggle for Snap to grid to on. This will make formatting your report easier.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the snap to grid toggle.](../media/grid-snap.png)](../media/grid-snap.png#lightbox)

## Task: Create report title

We'll create the report title.

1.  In your report page, select **Text box**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the insert text box button.](../media/text-box.png)](../media/text-box.png#lightbox)

1.  Type the following text into the textbox: Contoso Coffee Swag Request Report

1.  Highlight the text, then change the text size to **24**, make the text **Bold**, and **Center** it.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the text formatted.](../media/format-text.png)](../media/format-text.png#lightbox)

1.  With the text box selected, go to the **Format** pane, expand the **Effects** section, and turn on **Background**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the background settings.](../media/background.png)](../media/background.png#lightbox)

1.  Change the background Color to **#015c55**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the text background color.](../media/background-color.png)](../media/background-color.png#lightbox)

1.  Change the textbox font color to **White**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the font color set to white.](../media/white.png)](../media/white.png#lightbox)

1.  Go the **Properties** section and change the **Height** of the textbox to **70** and the **Width** to **1270**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the height and width settings.](../media/size.png)](../media/size.png#lightbox)

## Task: Add a donut chart

In this task, you'll add a donut chart to the report. This chart will show the approval status of the requests.

1. Select to select the middle of the report and away from the textbox, go to the **Visualizations** pane, and select **Donut** **chart**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the donut chart.](../media/donut-chart.png)](../media/donut-chart.png#lightbox)

1. Expand the **Request** table, drag **Approval Status** to the **Legend** field, and drag the **Request Number** to the **Values** field.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the donut chart values.](../media/chart-values.png)](../media/chart-values.png#lightbox)

1. Move the donut chart to the top left of the report.

1. Save the report.

You should save your report regularly throughout the lab.

## Task: Create pie chart visual for number of requested assets

You'll create a pie chart visual to display the number of assets that have been requested based on asset category, which you can drill down to see the asset name. You'll use the Asset Category hierarchy created earlier in the lab to enable this drill down.

1.  From the Visualizations pane, select the **pie chart** visual to insert it into the report canvas. Before you insert it, make sure that no other visual on the screen is selected.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the pie chart.](../media/pie-chart.png)](../media/pie-chart.png#lightbox)

1.  Expand the **Asset** table, drag **Category Name Hierarchy** to Legend field.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the category name hierarchy added to legend field.](../media/legend.png)](../media/legend.png#lightbox)

1.  Drag **Request ID** from the **Asset** table and drop it in the Values field.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the request ID added to the values field.](../media/values-field.png)](../media/values-field.png#lightbox)

1.  Go to the format icon in the **Visualizations** pane, select the **General** tab, expand the **Title** section, and change the **Text** to **Requested Assets**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the title text changes to requested assets.](../media/requested-assets.png)](../media/requested-assets.png#lightbox)

1.  Move the pie chart next to the donut chart.

1.  Test out interacting with the pie chart visual. On the pie chart visual, select the down arrow icon to turn on drill-down.

1.  Select a segment within the pie chart visual, and the visual will be drilled down into the asset names of the selected asset category. To return to the top level of the hierarchy, select the up arrow icon.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the drill down button selected.](../media/drill-down.png)](../media/drill-down.png#lightbox)

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the drill up button selected.](../media/drill-up.png)](../media/drill-up.png#lightbox)

1.  Save the report.

## Task: Create multi-row card to display top requested assets 

You'll create a multi-row card visual to display the top three assets that are requested and the number of requests.

1.  Make sure nothing on the report is currently selected. From the Visualizations pane, select the multi-row card visual to insert it into the report canvas. Before you insert it, make sure that no other visual on the screen is selected.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the multi-row card.](../media/multi-row.png)](../media/multi-row.png#lightbox)

1.  From the Fields pane, drag the **Name** field of the Asset table and the **Request Number**. field of the Request table into the **Fields** well of the Visualizations pane.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the fields pane values.](../media/fields.png)](../media/fields.png#lightbox)

1.  From the Fields well, select the arrow next to **Request Number.** and set it to **Count**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the request number set to count.](../media/count.png)](../media/count.png#lightbox)

1.  Then, rename the Request Number filed to field to **Requested**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the field renamed to requested.](../media/requested.png)](../media/requested.png#lightbox)

1.  In the Filters pane, expand the **Name** **filter**, and set the Filter type to **Top N**. Set the filter to show the Top **3** items. From the Requests table, drag the **Request No.** field into the By value well.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the filter set to show top three requests.](../media/top-items.png)](../media/top-items.png#lightbox)

1.  Where the field says **First Request No.**, select the arrow next to it, and change it to **Count**. Then, select **Apply filter**. Your visual should now display the top three requested assets. *Your visual may display more than three assets if the same amount has been requested.*

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the value set to count.](../media/count-value.png)](../media/count-value.png#lightbox)

1.  Select **Apply filter**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the apply filter button.](../media/apply-filter.png)](../media/apply-filter.png#lightbox)

1.  Select the ... icon of the multi-row card visual. Choose **Sort by** > **Requested** and **Sort Descending**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the sort settings.](../media/sort.png)](../media/sort.png#lightbox)

1.  Go to the format tab, select the **General** tab, expand the **Title** section and enter **Top 3 Assets Requested** for **Text**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the title value changed.](../media/title.png)](../media/title.png#lightbox)

1.  Move and resize the multi-row card so that it's positioned on your report as shown below.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the current state of the report.](../media/current-report.png)](../media/current-report.png#lightbox)

1. Save your report.

## Task: Create column chart to display total amount spent based on asset categories

You'll create a clustered column chart visual to display the total cost of all the asset requests that have been approved, based on the asset category.

1.  From the Visualizations pane, select the **clustered column chart** visual to insert it into the report canvas. Before you insert it, make sure that no other visual on the screen is selected.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the clustered column chart.](../media/clustered-column-chart.png)](../media/clustered-column-chart.png#lightbox)

1.  From the Asset table, drag the **Category Name** field into the **Axis** well. From the Request table, drag the **Price** field into the **Values** well.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the category name and price added into the column chart.](../media/category-price.png)](../media/category-price.png#lightbox)

1.  Rename the field in the Axis well to **Asset Category**. Rename the field in the Values well to **Total Spent**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the renamed fields.](../media/rename-fields.png)](../media/rename-fields.png#lightbox)

1.  Go the format tab and turn on **Data labels**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the data labels turned on.](../media/data-labels.png)](../media/data-labels.png#lightbox)

1.  We'll add a filter to the visual so that it only displays the price based on the assets that have been approved. From the Requests table, drag the **Approval status** field and place it in the Filter pane for **Filters on this visual**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the approval status field added to the filter.](../media/approval-status-field.png)](../media/approval-status-field.png#lightbox)

1.  In the filter, tick the **Approved** checkbox.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the approved checkbox marked.](../media/approved.png)](../media/approved.png#lightbox)

1.  Move and resize the column chart visual so that it's positioned on your report as shown below.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the column chart visual repositioned.](../media/visual-position.png)](../media/visual-position.png#lightbox)

1.  Save your report.

## Task: Add table 

You'll add a table to the report. This table will show all requests.

1.  From the Visualizations pane, select the Table visual to insert it into the report canvas. Before you insert it, make sure that no other visual on the screen is selected.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the select table icon.](../media/select-table.png)](../media/select-table.png#lightbox)

1.  Select Request Name, Price Approval Status and Comment from the Request table.

	> [!div class="mx-imgBorder"]
	> [![Screenshot showing the selected columns.](../media/columns.png)](../media/columns.png#lightbox)

1.  Select **Name** from the **Asset** table.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the name from the asset table.](../media/name.png)](../media/name.png#lightbox)

1.  Rename the Name field to **Category**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the name field renamed to category.](../media/category.png)](../media/category.png#lightbox)

1.  Resize and reposition all the visuals until you're happy with the layout. The report should look like the image below.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the completed report.](../media/completed-report.png)](../media/completed-report.png#lightbox)
