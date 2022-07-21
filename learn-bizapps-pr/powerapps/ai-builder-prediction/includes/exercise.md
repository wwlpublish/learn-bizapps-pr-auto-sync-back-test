In this exercise, you'll build an AI Builder prediction model to help a Brazilian commerce predict the delivery timeliness of customer orders. The retailer has received complaints from customers about late shipments. This impacts the reviews and satisfaction surveys, which are high influence factors in competitive retail markets. By predicting the orders that have probability of late arrival, this retailer can implement rules to automatically upgrade shipping option to express service and have a higher probability of incurring no delay and receive positive feedback from its customers.

## Data preparation

As with all custom models, one of the initial important steps is to identify and prepare data that will be used to train the model. AI Builder prediction is no different and requires historical data to determine patterns that will help predict outcomes of new events.

To accelerate this exercise, follow the steps described at [Sample Dataset for prediction model](/ai-builder/prediction-data-prep?WT.mc_id=DX-MVP-5003600?azure-portal=true#sample-dataset-for-prediction-model).

For this exercise, you'll reference the three following tables that are part of the *Brazilian Commerce* (BC) Dataverse solution:

-   BC Customer: list of 5,000+ customers with the city and zip code their orders were delivered to

-   BC Order: list of 5,000+ orders processed for the customers with information about the product purchased, its price, estimated date of delivery, actual delivery date, and so on.

-   BC Product: list of 5,000+ products with category and shipment volume and weight information

> [!div class="mx-imgBorder"]
> [![Screenshot of the Brazilian Commerce solution in the Power Apps Studio displaying the list of tables imported.](../media/tables.png)](../media/tables.png#lightbox)

In the following video, you're walked through those data preparation steps.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/]

## Create a model

The prediction model determines potential outcomes after analyzing historical data. Providing records that have multiple potential influencers and a clear outcome, will support a model with high confidence level.

The tables imported during the data preparation steps will be used to create the prediction model.

1.  In the Power Apps Studio, in the left navigation menu, under **AI Builder**, select **Explore**, and then select the prediction model.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Power Apps Studio displaying the prediction model tile and AI Builder navigation menu.](../media/prediction-model-tile.png)](../media/prediction-model-tile.png#lightbox)

2.  Select **Get started**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the AI Builder prediction model with highlight on Get Started.](../media/get-started.png)](../media/get-started.png#lightbox)

1.  Select the **BC Order** table and **Delivery Timeliness** column. Confirm the four outcomes the model will study, and then select Next.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the AI Builder Prediction model with highlight on the table and column value selection and confirmation of the four possible outcomes.](../media/outcomes.png)](../media/outcomes.png#lightbox)

1.  Review and confirm the selected columns that may influence the outcome for the **BC Order** table. Notice that Delivery Delta and Delivery Date are not selected. These values are updated once the delivery has occurred and would bias the analysis, resulting in a model performance of type D. Other irrelevant columns, such as ID and Order Status, can also be removed for this model training. To move to the next step of this exercise, select **Next**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the AI Builder Prediction model with highlight on the selected table and column values.](../media/columns.png)](../media/columns.png#lightbox)

1. For this exercise, no filter is required; select **Skip this step**, and then select **Next**.

    > [!div class="mx-imgBorder"]
	> [![Screenshot of the AI Builder Prediction model with highlight on the skip and next button.](../media/skip.png)](../media/skip.png#lightbox)

1.  Review the model summary. Select **Train** to move to the next portion of this exercise.

    > [!div class="mx-imgBorder"]
	> [![Screenshot of the AI Builder Prediction model with highlight on the train button.](../media/train-2.png)](../media/train-2.png#lightbox)

1.	Select **Go to models**. The model will be in training for a few minutes. When training completes, the status will change to Trained.

1.	To view the performance details, select the trained model.

    > [!div class="mx-imgBorder"]
	> [![Screenshot of the AI Builder Prediction model with highlight on the prediction.](../media/prediction.png)](../media/prediction.png#lightbox)

1.  Review the performance details, in this **B** level is satisfactory. Most influential data provide information about the columns that have the highest impact on the determination of the outcome. Select **Publish** to move to the next step of this exercise.

    > [!div class="mx-imgBorder"]
	> [![Screenshot of the AI Builder Prediction model with highlight on the satisfactory level, data, and publish button.](../media/publish.png)](../media/publish.png#lightbox)

## Use the model to predict in real-time

When a prediction model is published, it will run automatically to refresh the outcome for newly created records, daily by default.
In scenarios where the prediction is required instantly, a Power Automate cloud flow is required to generate the outcome as rows are created.
Follow these steps to create a flow that will use the outcome of the custom model to predict the delivery timeliness potential for new orders:

1. In the Power Automate Studio, in the left navigation menu, select **Create**, and then select the **Automated cloud flow** tile.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Power Automate Studio with the create and automated cloud flow button selected.](../media/automated.png)](../media/automated.png#lightbox)

1.  Enter a name for the flow, then select the **When a row is added, modified or deleted** trigger for Dataverse. Then select **Create**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Power Automate Studio with the flow name and choose your flow trigger field selected.](../media/flow-trigger.png)](../media/flow-trigger.png#lightbox)

1.  In the Power Automate Studio, for the new cloud flow, select **Added** for the trigger type, select **BC Orders** as the table name, and select **Organization** as the scope. Then select **New Step** to create an action.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Power Automate Studio with add flow fields and next step selected.](../media/new-cloud.png)](../media/new-cloud.png#lightbox)

1.  For the AI Builder connector, select the Predict action.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Power Automate Studio with ai builder and predict selected.](../media/predict.png)](../media/predict.png#lightbox)

1. Select the prediction model created for this exercise. For each requested values by the model, select the appropriate column from the BC order table. Then select **New Step** to create an action.

    > [!div class="mx-imgBorder"]
	> [![Screenshot of the Power Automate Studio with predict fields completed.](../media/predict-complete.png)](../media/predict-complete.png#lightbox)

1. For the **Dataverse** connector, select the **Update a row** action.

    > [!div class="mx-imgBorder"]
	> [![Screenshot of the Power Automate Studio with dataverse and update a row selected.](../media/update-row.png)](../media/update-row.png#lightbox)

1.	Select **BC Order** as the Table name, the unique identifier from the trigger for the **Row ID**, the **Explanation**, **Prediction**, and **Likelihood** from the **Predict** action as the other values required. Then select **Save** to complete the creation of the flow.

    > [!div class="mx-imgBorder"]
	> [![Screenshot of the Power Automate Studio with update a row fields completed and save selected.](../media/update-row-complete.png)](../media/update-row-complete.png#lightbox)

1.	To test the prediction model and flow, add a new row to the table, refresh the data entry form, and the results are visible.

    > [!div class="mx-imgBorder"]
	> [![Screenshot of the Power Automate Studio with update a row fields completed and save selected.](../media/test-prediction.png)](../media/test-prediction.png#lightbox)

    You have now successfully create a prediction model and a Power Automate cloud flow that generates the outcome analysis when new rows are added to the BC Order table.