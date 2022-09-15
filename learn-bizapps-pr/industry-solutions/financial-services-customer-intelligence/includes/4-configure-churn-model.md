In this exercise, you'll ingest the Dataverse sample data from your Azure Data Factory into Dynamics 365 Customer Insights. Then, you'll run the Retail banking churn model.

## Task 1: Set up a data source in Customer Insights

In this task, you'll set up the **operationaldata** data source for ingesting data into Dynamics 365 Customer Insights.

1. Using an In-Private or Incognito window, navigate to [Customer Insights](https://home.ci.ai.dynamics.com/). 
1. Select the correct environment from the upper right Environment drop down.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of Customer Insights Environment selection.](../media/customer-insights-environment.png)](../media/customer-insights-environment.png#lightbox)

1. In Customer Insights, go to **Data Sources** and edit **operationaldata**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of Customer Insights on the Data sources page, showing the Edit button next to the operationaldata data source.](../media/operational.png)](../media/operational.png#lightbox)

1. Select **Azure subscription** and then select the appropriate **Subscription**, **Resource group**, and **Storage account** you created in the previous unit. For the **Container** field, select the one you created (example: fsicistagingcontainer). Select **Next**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Enter storage details dialog, showing selections in the dropdown menus and the Container name filled in.](../media/storage-details.png)](../media/storage-details.png#lightbox)

1. Select **Data** folder
 
     > [!div class="mx-imgBorder"]
    > [![Screenshot of the Data folder selection](../media/storage-data-folder.png)](../media/storage-data-folder.png#lightbox)

1. Scroll down and select the **msfsi.manifest.cdm.json** file. Select **Next**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Select a common data model file page, showing the JSON file selected.](../media/select-file.png)](../media/select-file.png#lightbox)

1. Select all entities by selecting **Include** checkbox and select **Save**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of Common Data Model folder showing the message "Indicate which data entities you want to enable data profiling" and all entities selected.](../media/profiling.png)](../media/profiling.png#lightbox)

1. Return to **Data sources** to view the status. The process should complete with some errors showing for the **Analysis preparation** category. This error is normal and won't affect future steps.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Data sources page, showing operationaldata Status as Completed with errors.](../media/errors.png)](../media/errors.png#lightbox)

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the Progress details page, showing that the Analysis preparation had zero of one refreshed.](../media/progress-details.png)

1. Now that the entities have been mapped, go to **Unify** on the site map to run the **Match** by selecting **Run**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of Audience insights with Unify selected in the left navigation pane. On the Match tab of the Unify page, the Run button appears at the top.](../media/run.png)](../media/run.png#lightbox)

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the matching rules setup and conditions.](../media/run-match-rules.png)](../media/run-match-rules.png#lightbox)

1. When the match is complete, numbers for your matches will display, as shown in the following screenshot.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of Unify on the Match tab showing 74 Unique source records, 37 Matched and non-matched records, and 37 Matched records only.](../media/unify.png)](../media/unify.png#lightbox)

1. Before running the prediction model, you need to merge the records. On the **Merge** tab, select **Run** and then select **Run Merge and downstream processes**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Run menu expanded to show options for Run Merge and downstream processes or Run only Merge.](../media/run-merge.png)](../media/run-merge.png#lightbox)

1. When the merge is complete, you will receive a success message, as shown in the following image.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of Unify on the Merge tab showing Current matched records as 37 and the Successful message.](../media/unify-merge.png)](../media/unify-merge.png#lightbox)

1. Expand **Intelligence** on the site map and then go to **Predictions**. The Retail banking churn model should begin to refresh. This step might take several minutes to complete. If it doesn't complete after 10 to 15 minutes, try running the merge in step 9 again.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of Audience insights on the Intelligence Predictions page. The My predictions tab shows the Retail banking churn prediction status as Refreshing.](../media/refreshing.png)](../media/refreshing.png#lightbox)

    > [!div class="mx-imgBorder"]
    > [![Screenshot of Audience insights on the Intelligence Predictions page. The My predictions tab shows the Retail banking churn prediction status as Successful.](../media/successful.png)](../media/successful.png#lightbox)

1. Open the prediction to view the contents of the training model. In this section, you'll find three main areas:

    - **Training model performance** - Displays a letter grade of how well the model has performed.

    - **Likelihood to churn (number of customers)** - Read as X customers are Y% likely to churn.

    - **Most influential factors** - Considered by the AI in predicting the model. These factors will vary depending on the data set.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of Audience insights on the Retail banking churn prediction page, showing Training model performance of A, a churn risk chart, and Most influential factors.](../media/churn.png)](../media/churn.png#lightbox)

1. To view a customer's full profile in Dynamics 365 Customer Insights, go to **Customers** and open any sample record.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of Customer Insights on the Customers page showing 37 customers.](../media/customers.png)](../media/customers.png#lightbox)

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the full profile for the customer Rowan Gray (Sample).](../media/customer-profile.png)](../media/customer-profile.png#lightbox)

1. To view the calculated churn scores, go to **Data**, and then under **Intelligence**, open the **msfsiRetailBankingChurn** entity that was created when you ran the churn model.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the list of Entities showing the churn model under Intelligence.](../media/entity.png)](../media/entity.png#lightbox)

1. Select the **Data** tab to view the calculated churn score for each customer ID in the dataset.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Customer Insights churn Data tab showing the list of Customer IDs with a churn score next to each.](../media/score.png)](../media/score.png#lightbox)

1. To view the churn score in **Dataverse**, open a new tab in your internet browser and then go to your Dataverse environment in [Power Apps](https://make.powerapps.com/?azure-portal=true).

1. Go to **Apps** and then open **Unified Customer Profile**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of Apps with Unified Customer Profile selected.](../media/apps.png)

1. Open any of the 37 sample contact records.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Unified Customer Profile sandbox on the All Contacts page.](../media/sandbox.png)](../media/sandbox.png#lightbox)

1. Scroll down to the bottom of the **Customer snapshot** section and select the information (**i**) icon to view the full details of the churn score.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of a contact's customer profile with the Churn risk score dialog open showing a score of 12 of 100, Low churn risk.](../media/churn-risk.png)](../media/churn-risk.png#lightbox)

**Congratulations!** You've successfully run the Retail banking churn model in Dynamics 365 Customer Insights.
