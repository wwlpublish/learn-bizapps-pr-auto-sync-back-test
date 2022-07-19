This exercise builds off the exercises found in Create an immersive business process flow in Power Automate.
It’s recommended that you complete that module before following the below exercises. However, if you’re already familiar with the steps in building out basic business process flows, feel free to take the concepts in the exercise below.

In this exercise, you'll enhance the business process flow by adding
a logical branch to determine what test to perform and
what information needs to be collected in order to complete a smog check on a
vehicle based on the vehicle's manufacture year. You’ll add
logic that will provide a different set of instructions for vehicles
that were manufactured before or during 1971, versus vehicles that were manufactured after 1971.

1. Sign in to [Power Automate](https://preview.flow.microsoft.com/?azure-portal=true). Make sure that you are in the same environment that you used to create the process flow in the previous module.

1. Select **My flows** and then select **Business process flows**.

1. Select the **Edit** button (pencil icon) and open the **Customer Check In** business process flow in the **Business process flow** editor.

    ![Screenshot of Power Automate on the My flows tab with Customer Check In highlighted and its Run button called out.](../media/6-edit-customer-check.png)

1. Double-click the first stage and rename it to **Customer
Info**. Double-click the second stage and rename it to **Automobile Info**, as
shown in the following figure. Select the **Update** button in the ribbon so all
the changes are saved and ready to use.

    > [!div class="mx-imgBorder"]
    > [![Screenshot showing the stages properly named.](../media/44-name-stages.png)

    Before you create the conditions, you need to set up the data that you want to collect in each stage you add. Select the **Customer Check In** stage and add the following fields by using the **Click to add field and forms** hyperlink on the right side of the page.

    > [!NOTE]
    > The entity window may open in an older UI. Alternatively, you can open
    > Power Apps, select your environment, expand **Data** and select **Tables**
    > to see the modern UI.

1. In **Schema**, select **Columns**

    ![Screenshot of Power Apps Solutions > Default Solution > Customer Check In page with the Add field button highlighted.](../media/14-add-field-customer-check-entity.png)

1. Select the **+ New column** button in the ribbon above the fields, as shown in the following figure, and then add the following
  fields.

    ![Screenshot of the new column button in the tables view.](../media/new-column.png)

    - Smog Pump Intact - Yes/No - Set Yes as default

    - PVC Valve Intact - Yes/No - Set Yes as default

    - Aftermarket Exhaust Headers - Yes/No - Set No as default

    - Comments Pre 1972 - Multiline Text

    - Exhaust Test Performed with Passing Score - Yes/No - Set Yes as default

    - HC Reading at 2000 RPM - Decimal Number

    - O2 Reading 2000 RPM - Decimal Number

    - CO Reading 2000 RPM - Decimal Number

    - Original Equipment - Yes/No - Set Yes as default

    - Comments Post 1972 - Multiline Text

    - Amount - Currency

    - Certificate Number - Whole Number

    - Payment Method - Choose **Choice** as the column type and under choice, choose **New choice** and enter the following options:

      - Cash

      - Mastercard

      - Visa

      - Discover

      - Debit Card

      - Bitcoin


1. Select the **Condition** flow control under the **Components** tab and then drag
it to the right of the **Customer Check In** stage, as shown in the following image.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of Power Apps on the Customer Check In design page with the Components tab highlighted and the Data Step Composition highlighted.](../media/7-add-condition.png)](../media/7-add-condition.png#lightbox)

    > [!div class="mx-imgBorder"]
    > [![Screenshot showing how to add values to a condition by selecting the condition and setting its values in the pane to the right.](../media/8-adding-arguments-condition.png)](../media/8-adding-arguments-condition.png#lightbox)

1. Select the **Condition** component within the editor and enter the following information:

    - **Display Name** - Manufacture Year Pre or Post 1971

    - **Field** - Automobile Year

    - **Operator** - Is greater than

    - **Type** - Value

    - **Value** - 1971

    The entries should resemble the following screenshot. When finished, select
  the **Apply** button.

    ![Screenshot of the filled-in properties listed above. The text view of the Condition Expression reads (Automobile Year Is greater than [1971]).](../media/9-detail-condition-entries.png)

1. Select the **Components** tab and then drag a new stage to the plus
(**+**) sign on the right of the page and another to the plus (**+**) sign under the **Condition** stage, as shown in the following figure.
Name each of the new stages by selecting each new stage and entering the new name. Be sure to save the name by clicking apply after each change.

    ![Two additional stages added in business process flow designer.](../media/10-two-additional-stages-added.png)

1. Drag another stage to the right of the **Customer Check In Post 1971 Smog Check** stage. Rename this last stage **Collect Payment**.

    > [!div class="mx-imgBorder"]
    > [![Final stage added in business process flow designer.](../media/11-add-final-stage.png)](../media/11-add-final-stage.png#lightbox)

1. Connect the **Customer Check In 1971 or Older Smog Check** stage to the **Collect Payment Stage** by following these steps:

    1. Select the **Customer Check In 1971 or Older Smog Check** stage.

    1. Select **Connector** in the ribbon and then select the **Connect** option.

    1. Select the **Customer Check In Collect Payment** stage.

    > [!div class="mx-imgBorder"]
    > [![Connect stages using the connector tool.](../media/12-connect-stages.png)](../media/12-connect-stages.png#lightbox)

Now, you’ll add the fields that you created to each stage. Select the following stages and add the fields that are noted by selecting the details link drop-down menu
and then adding data steps.

Add a data step for each field within each stage. When you’re done, you
should have a data step under each of the following stages.

- Stage - Customer Check In Post 1971 - add the following fields under the data step:

  - Smog Pump Intact

  - PVC Valve Intact

  - Aftermarket Exhaust Headers

  - Comments Pre 1972

- Stage - Customer Check In 1971 or Older - add the following fields:

  - Exhaust Test Performed with Passing Score

  - HC Reading at 2000 RPM

  - O2 Reading 2000 RPM

  - CO Reading 2000 RPM

  - Original Equipment

  - Comments Post 1972

- Stage - Customer Check In Collect Payment - add the following fields:

  - Amount

  - Certificate Number

  - Payment Method

When you're done, select the **Update** button in the top ribbon.
Your business process flow should look like the following image:

> [!div class="mx-imgBorder"]
> [![Completed flow with branching logic prior to the Customer Check In actions.](../media/17-completed-flow-branching-logic.png)](../media/17-completed-flow-branching-logic.png#lightbox)

Now, you'll test the enhanced business process flow.

1. Navigate to [Power Automate](https://preview.flow.microsoft.com/?azure-portal=true).

1. Select **My flows** and then **Business process flows**.

1. Run the Customer Check In flow by selecting the **run**
button (the play button next to the name of the flow).

You can enter a vehicle with a manufactured date of 1971 or before
and another after 1971. Notice that the smog check information in Stage 3
changes based on the year of vehicle manufacture. Additionally, notice that both
potential flows reconnect again at the last stage called **Collect Payment**.
