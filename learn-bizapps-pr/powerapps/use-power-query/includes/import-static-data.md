After following the initial steps presented in Unit 1, you can access the dataflows page. In this unit, you'll be presented with the process to import static data, such as manually entered, into a Dataverse table by using Power Query.

In this scenario, you have a list of contacts (first name, last name, and email addresses) that need to be imported into a temporary Dataverse table for review. This list of contacts could be in a text file or added manually.

A dataflow is created in Power Apps Studio for this process.

## Create a dataflow by using Power Query

To create a dataflow that imports data in Dataverse by using Power Query, follow these steps:

1.  From the dataflow page in Power Apps Studio, select **+ New dataflow**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Power Apps portal's Dataflow window. Focus is on the New dataflow menu option.](../media/new-dataflow.png)](../media/new-dataflow.png#lightbox)

1.  In the New dataflow window, enter a name for the new dataflow, and then select **Create**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the New dataflow window. Focus is on the Name field and Create button.](../media/name-create.png)](../media/name-create.png#lightbox)

1.  From the **Choose Data Source** window of the Power Query, select the data source for your business scenario; for example, select **Blank table**, which allows you to manually define a table structure and add rows to it.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Power Query editor. Focus is on the Choose data source header and Blank table option.](../media/blank-table.png)](../media/blank-table.png#lightbox)

1.  With this next step, you connect to a data source. Credentials and details about the data source may be required, depending on the selected data source. In some cases, such as the **Blank table** option selected in the previous step, you can define information about the data structure and rows. Column names, such as **First Name**, **Last Name**, and **Email Address**, can be added to the definition of a table, such as one named **Contact**. Select **Next** to complete this step.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Power Query editor. Focus is on the Blank table data source, the sample data from that data source, the name of the table, and the Next option.](../media/sample-data.png)](../media/sample-data.png#lightbox)

1.  The next step allows you to transform the data and add columns, based on calculations, groupings, or transformation of other columns of the data source. Select **Next** to complete this step.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Power Query editor. Focus is on the Transform and Add column section headers and Next option.](../media/add-columns.png)](../media/add-columns.png#lightbox)

1.  A Map tables form is displayed. By default, the **Load to a new table** setting is selected. This allows the process to import data into a table, usually a temporary one that is created by the dataflow. For our current scenario, enter a **Table name**, **Table display name**, and **Table description.** The column mapping doesn't require modifications. Select **Next** to complete this step.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Power Query editor. Focus is on the Load to a new table option and the definition fields for that table. Focus is on Next.](../media/load-settings.png)](../media/load-settings.png#lightbox)

1.  The last step of dataflow creation is to configure the refresh settings. Dataflows can be refreshed on demand (**Refresh manually**) or on a predetermined schedule (**Refresh automatically**). Select **Publish** to complete the creation of the dataflow.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Power Query editor. Focus is on the Refresh manually option of the Refresh settings, and on the Publish option.](../media/refresh-settings.png)](../media/refresh-settings.png#lightbox)

	The new dataflow will be part of the list of dataflows with a **Published** status and send a notification that confirms the process is complete.

	> [!div class="mx-imgBorder"]
	> [![Partial screenshot of the dataflow window. Focus is on the notification message confirming the dataflow was published successfully and the Published status to the dataflow.](../media/success-message.png)](../media/success-message.png#lightbox)

1.  To access the newly created table, in the left pane, expand **Dataverse** and select **Tables**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Power Apps portal left navigation pane. Focus is on the expanded Dataverse option and Tables. Focus is also on the newly created table.](../media/tables.png)](../media/tables.png#lightbox)

## Next steps

You now have learned how to create a dataflow that imports manually entered data into a new Dataverse table by using Power Query. Next, you'll learn how to add new accounts from a text file into an existing Dataverse table.
