In this exercise, you'll configure the Retail Churn Model in the Dynamics 365 Customer Insights environment you created in the previous exercise.

## Task 1: Add a data source

In this task, you'll add a data source for your Retail Churn model.

1.  Navigate to your newly created Customer Insights environment, expand **Data,** and go to **Data sources**. Select **Add data source**.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the Customer Insights environment with add data source button.](../media/add-data-source.png)

1.  Select **Microsoft Power Query** save the data source as "RetailGroceryChurn", and then select **Next**.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of Microsoft Power Query selected and the data source set.](../media/power-query-data-source.png)

1.  Choose the **Azure Blobs** connector.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of Azure blobs set as the connector.](../media/azure-blobs.png)

	Follow the below steps to retrieve the **Storage Account name** and **Access Key** from the storage account created in exercise 2 under task 1 and then update them in the **Azure blob** connection settings in Customer Insights.

1.  Open a new internet browser tab and go to [Azure portal](https://ms.portal.azure.com/?azure-portal=true).

1.  Under Azure services navigate to Storage accounts.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the Azure services list.](../media/azure-services.png)

1.  Search for "retailchurn" and open the Storage Account.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the storage accounts with search results.](../media/storage-accounts.png)

1.  Go to the Access keys and copy the Storage account name. Paste that in the Account name under the Connection settings in Customer Insights.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the access keys with storage account name displayed.](../media/access-keys-storage-account-name.png)
	
	> [!div class="mx-imgBorder"]
	> ![Screenshot of the connection settings with account name field populated.](../media/connection-account-name.png)

1.  Back in **Azure portal**, select Show keys, and then copy **key 1**.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of show keys with key1 copied.](../media/key.png)

1.  Paste the access key on the field **Account Key** and storage name in the **Account name or URL** fields in the connection settings in D365 Customer insights environment.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the account key added.](../media/account-key.png)

1.  Select **retailgrocery** and select **Transform data**.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the data selected and transform data button.](../media/transform-data.png)

1.  Select the **\[Binary\]** link in the first cell of the first row for the **Grocery\_contact.csv** file.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the binary link in the first cell.](../media/binary.png)

1.  Go to the **Transform** ribbon and then select the **Use first row as headers** option.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the use first row as headers option.](../media/first-row.png)

1.  Right click the **birthdate** column, go to **Change type**, and select **Date**.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the birthdate column with change type menu and date selected.](../media/date.png)

1.  Select the following columns by holding down the **Ctrl key** on your keyboard: annualincome, msrc\_creditscore, msrc\_customerrelationshipduration, and msrc\_distancetoneareststore. Once highlighted, right click one of them, go to **Change type**, and select **Decimal number**.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the change type set to decimal number.](../media/decimal-number.png)

1. Finally, under Properties on the right side, change the **Name** to "contact" and hit the **Enter** key on your keyboard. Don't save.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of name changed to contact.](../media/contact.png)

1. Right-click the contact query and select Duplicate.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the contact query menu with duplicate selected.](../media/duplicate.png)

1. Right-click the duplicated query and rename it to "transactions".

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the duplicated query renamed to transactions.](../media/transactions.png)

1. With the **transactions** query selected, delete all the **Applied steps** on the right up to the Navigation step.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the applied steps deleted.](../media/delete-steps.png)

1. Select the **\[Binary\]** link in the first cell of the third row for the **Grocery\_msrc\_transaction.crv** file.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the third row binary link.](../media/third-binary.png)

1. As before, go to **Transform** and select **Use first row as headers**.

1. Scroll over to and select the **msrc\_transactiontimestamp** column. Right-click and **Change type** to **Date/Time**.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the type changed to date/time.](../media/date-time.png)

1. Press and hold the **Ctrl key** on your keyboard to select both the **msrc\_transactionamount** and **msrc\_discountappliedamount** columns. Right-click one of the columns, go to **Change type**, and select **Decimal number**.

1. Right-click the **transactions query** and select **duplicate**.

1. Rename the query to "**session**" and delete all the **Applied steps** up to Navigation like you did before.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the query renamed session and applied steps deleted.](../media/session.png)

1. Select the **\[Binary\]** link in the first cell of the second row for the **Grocery\_msrc\_session.csv** file.

1. Go to **Transform** and select **Use first row as headers**.

1. Right-click **msrc\_sessiontimestamp**, go to **Change type** and select **Date/Time**.

1. Right-click the **msrc\_sessionduration** column, go to **Change type**, and select **Decimal number**.

1. Finally, right-click the **msrc\_sessioncustomersatisfaction** column, go to **Change type**, and select **Whole number**.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the type changed to whole number.](../media/whole-number.png)

1. Select **Save** and monitor the Data source as it refreshes. This step should take a few minutes.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the save button with the data source refresh.](../media/save.png)

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the validating queries message.](../media/validating-queries.png)

## Task 2: Unify your data

1.  In Customer Insights, expand **Data** and go to **Unify**. Under **Map**, select **+ Select entities**.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of unify selected with map view and select entities button.](../media/select-entities.png)

1.  Select all **three** entities and select **Apply**.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the three entities selected and apply button.](../media/apply-entities.png)

1.  Select the **contact** entity, then select **contactid** as the primary key.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the primary key set as contactid.](../media/primary-key.png)

1.  Select the **session** entity, then select **msrc\_sessionid** as the primary key.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the session entity primary key set.](../media/session-primary-key.png)

1.  Select the **transactions** entity, then select **msrc\_transactionid** as the primary key. Select **Save**.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the transactions entity primary key set.](../media/transactions-primary-key.png)

1.  While still under Unify, select **Match**, and then select **+ Set order**.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the match view with set order button.](../media/set-order.png)

1.  In the pop-out, select + Add at the bottom to add a third entity.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of add button to add a third entity.](../media/add.png)

1.  Select the entities in the following order: **contact**, **transactions**, **session**. Ensure **Include all** is checked for all entities and select **Done**.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of entities selected with include all checkbox.](../media/include-all.png)

1.  Select **+ Add rule** next to the **transactions** entity.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the add rule button next to the transactions entity.](../media/add-rule.png)

1. Select **contactid** and **msrc\_customerid**, then name the rule "contacttransactions". Select **Done**.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the rule details.](../media/rule-details.png)

1. Scroll down and select + Add rule next to the session entity.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the add rule button next to the session entity.](../media/session-add-rule.png)

1. Choose the **transactions** entity and then select the **msrc\_transactionid** and **msrc\_sessionid** fields. Name the rule "transactionssession" and select **Done**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the create rule view for the transactions entity.](../media/transactions-entity-rule.png)

1. Select **Save**.

1. Select **Run**. This step will take several minutes to complete. Once it's done, we'll then merge the data.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the completed process with success results.](../media/success-message.png)

1. Under **Unify**, select **Merge** and then select **Save**.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of Merge view with save button.](../media/merge.png)

1. Once saved, select **Run** and select **Run only Merge**. This will take several minutes to complete.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the run menu with run only merge selected.](../media/run-only-merge.png)

**Congratulations!** The model should be visible and ready to train, follow the next steps to train the model.

## Task 3: Train the model

1.  Navigate to **Predictions** on the left menu, select Create and then select the **Retail channel churn (preview)** **Use model** button.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the use model button for retail channel churn.](../media/use-model.png)

1.  When the pane pops out, select the **Get started** button.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the get started button.](../media/get-started.png)

1.  Name the model and output entity "RetailChurnModel".

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the model name and output entity details.](../media/model-name.png)

1.  Adjust the Model preferences as needed and select **Next**.

1.  Select the **+ Add data** button below the Customer session on the middle pane. It will open a right pane to let you add the required customer data from the customer entity. Select **Save** when done to return to the middle pane.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the add data button under customer session.](../media/add-data.png)

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the customer data details displayed.](../media/customer-data-details.png)

1.  Repeat the process with the Transaction data by clicking the second **+ Add data** button below the Transaction section on the middle pane. Fill out the transaction entity information on the right pane and lick on **Save**. Select **Next** on the middle pane.

1.  Once both required data entities are complete, select **Next** to go to Additional data.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of both data entities completed.](../media/complete-data-entities.png)

1.  Select **+ Add data** to enter the Session information, **save** it and select **Next**.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the add customer data window.](../media/add-customer-data.png)

1.  Set the data update schedule as **Weekly** and select **Next**.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the data update schedule set to weekly.](../media/weekly.png)

1. Confirm everything looks correct and select **Save and Run**.

1. Confirm that the model is running and select **Done**.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the model configured message.](../media/configured-model.png)

1. Monitor the status of the request to see when it's finished. There's a chance you may receive an error on the first run. If you receive an error, run the prediction model again and it typically works on the second try.

1. It's possible you may receive an error on the first run, select Refresh all to run the model again.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of a failed run message.](../media/error.png)

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the update predictions message.](../media/update.png)

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the refreshing status.](../media/refreshing-status.png)

 **Congratulations!** You have run the Retail channel churn predictive model.