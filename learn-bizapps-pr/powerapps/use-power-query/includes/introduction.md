Welcome to "Use Power Query to load data in Dataverse." This self-paced module will help you learn how you can take advantage of Power Query to connect to different data sources and transform data so it can then be imported into a Dataverse table.

## Power Query

Power Query provides a complete solution to transform and prepare data by using a graphical user interface (GUI). You can use the GUI to connect to different data sources and to load data into Dataverse.

Two versions of Power Query are available, one for desktop and one online. In the context of Microsoft Power Platform, the applicable version is Power Query Online and is experienced via the dataflow option.

For most scenarios, the first two steps required when considering using Power Query to import data are:

-   **Get data:** Based on the data source, this may require having proper connection credentials.

-   **Transform data:** This performs various transformations, such as grouping and merging.

To access Power Query Online from Microsoft Power Platform, follow these steps:

1.  Sign in to the [Power Apps portal](https://make.powerapps.com/?azure-portal=true).

1.  In the left pane, expand **Dataverse** and select **Dataflows**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Power Apps portal left navigation pane. Focus is on the expanded Dataverse option and Dataflows.](../media/dataflows.png)](../media/dataflows.png#lightbox)

1.  On the dataflows page, you can access the list of dataflows you created (**My Dataflows**) and dataflows other users created in the same Dataverse environment and then shared with you (**All Dataflows**).

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Power Apps portal's Dataflow window. Focus is on the My Dataflows and All Dataflows section headers.](../media/all-dataflows.png)](../media/all-dataflows.png#lightbox)

1.  To access Power Query for an existing dataflow, you can select **Edit** from the ellipsis related to that dataflow.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Power Apps portal's Dataflow window. Focus is on the ellipsis next to a dataflow and the Edit option of the pop-up menu.](../media/edit.png)](../media/edit.png#lightbox)

The Power Query editor will be displayed.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Power Query editor in the Power Apps studio.](../media/editor.png)](../media/editor.png#lightbox)

Multiple possibilities are available to load and transform data by using Power Query. It's recommended to explore those different options via experimentation in a dedicated environment.

## Next steps

You now have learned the fundamentals of Power Query. Next, you'll learn how to use Power Query to import data from a static file to a Dataverse table.
