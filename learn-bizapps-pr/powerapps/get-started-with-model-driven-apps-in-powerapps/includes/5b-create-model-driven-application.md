## Scenario

In the [exercise](/training/modules/get-started-with-powerapps-common-data-service/4a-use-data-cds-exercise/?azure-portal=true) from the previous module of this learning path, you created the Prospects table in Microsoft Dataverse and imported the existing leads. In this exercise, you'll use that data to create a model-driven app.
If you don't have the Prospects table, then refer to the previous [exercise](/training/modules/get-started-with-powerapps-common-data-service/4a-use-data-cds-exercise/?azure-portal=true),
keep the managers up to date on the current leads and forecasted revenue.

### Create the model-driven app for the prospects table

After you've created the *Prospects* table from the previous [exercise](/training/modules/get-started-with-powerapps-common-data-service/4a-use-data-cds-exercise/?azure-portal=true), you'll need the *Prospects* table from the previous [exercise](/training/modules/get-started-with-powerapps-common-data-service/4a-use-data-cds-exercise/?azure-portal=true) to complete this exercise.

1. Sign in to [Power Apps](https://make.powerapps.com/?azure-portal=true) by using your organizational account.

1. Select the environment you want, or go to the [Power Apps admin center](https://admin.powerplatform.microsoft.com/?azure-portal=true) to create a new one.

1. On the **Home** page, select the **Blank app** and then **Create** under **Blank app based on Dataverse**.

1. Enter the following for the Name and Select **Create**.

   - Name: Prospect Entry

1. Select **+ Add page**.

1. Select **Table based view and form** and then **Next**.

1. Select **Prospects** and then **Add**.

1. Select **Save**.

1. Select **Publish**.

### Creating a chart

1. Start at [https://make.powerapps.com](https://make.powerapps.com)

1. Select **Dataverse**, **Tables** and then find **Prospects**.

1. Select **Charts** under **Data experiences**.

1. Select **New chart**.

1. For the Chart Name, enter **Forecasted Revenue by Stage**.

1. For Legend Entries (Series), check the box, and select the **Forecasted Revenue** column.

1. For Horizontal (Category) Axis Labels, select the **Stage** column.

1. Select **Save and Close**.

1. Back on the App Designer, select the checkbox next to **Forecasted Revenue by Stage**.

1. Select **Save**.

1. Select **Publish**.

### Creating the form

You can follow the steps below to create a new main
form.

1. Go to the Power Apps Home Page, and on the left, Select **Dataverse**.

1. Select **Tables**.

1. Locate and select the **Prospects** table.

1. Select **Forms** under **Data experiences**.

1. Select the drop-down arrow next to New form, and then select **Main Form**.

1. Drag the **Stage** column from the left and place it below the **Owner** column in the center.

1. Drag the **Contract Amount** column and place it below the **Stage** column.

1. Drag the **Probability** column and place it below the **Contract Amount** column.

1. Drag the **Forecasted Revenue** column and place it below the **Probability** column.

1. Now select **Forecasted Revenue** and then select **Change Properties** on the ribbon.

1. Select the checkbox for **Read-only column**.

1. Select **Save**.

1. Select **Publish**.

1. Close the window.

1. Select **Done**.
