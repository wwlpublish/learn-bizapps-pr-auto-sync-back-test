Now that you have a new business process flow, you can try it out and discover how the data is stored after it has been run.

1.  Select the **Update** button in the top ribbon.

1.  Close the business process flow designer after you see the message that the process flow has been updated successfully.

1.  Go back to **My Flows**. Select **Business process flows**, where you should see the new flow listed.

	> [!NOTE]
	> You can see all of the immersive business process flows that are in process or that have been run by going to the main Power Automate page, selecting the **My flows** icon on the left menu, and then selecting the **Business process flows** tab.

1.  Select the **Run** arrow, as shown in the following screenshot.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of Power Automate on the Flows page Business process flows tab. Customer Check In and the Run button next to it are highlighted.](../media/21-run-check-business-process-flow.png)](../media/21-run-check-business-process-flow.png#lightbox)

    This selection will launch a new instance of the flow that you created.

	> [!NOTE]
	> You should see both the **Customer Info** and **Automobile Information** stages in this flow. If not, then redo the previous unit to confirm you followed the steps and clicked on **update**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of Power Automate on the Flows page Business process flows tab with both stages displayed.](../media/stages.png)](../media/stages.png#lightbox)

1.  Enter a name in the **Name** field on the **General** form (main form) and then select **Save**, as shown in the following figure.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of New Customer Check In Stage 1 with Name, New Stage, and the Save button highlighted.](../media/22-check-stage-1.png)](../media/22-check-stage-1.png#lightbox)

1.  After you select the **Save** button, select the red circle for the first stage, fill out the information, and then select the **Next Stage** button.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of New Stage dropdown with customer contact info filled in.](../media/23-stage-1.png)](../media/23-stage-1.png#lightbox)    

1.  Select the second stage, fill out the vehicle information, and then select the **Finish** button.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of second New Stage dropdown with automobile info filled in.](../media/24-stage-2.png)](../media/24-stage-2.png#lightbox)

    After you select the **Finish** button, the button in Stage 2 should turn green and the data that you entered is automatically saved.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of second New Stage dropdown with the green Finished button highlighted.](../media/25-business-process-flow-complete.png)](../media/25-business-process-flow-complete.png#lightbox)

1.  You can create more records by launching Power Automate, selecting **My Flows** and **Business process flows**, and then selecting the arrow next to the **Customer Check In** business process flow, as shown in the following screenshot.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the business process flow running again.](../media/26-run-business-process-flow-again.png)](../media/26-run-business-process-flow-again.png#lightbox)

## View the created data

You can view the data that you created for running the flow by following these steps:

1.  Go to [Power Apps](https://make.powerapps.com/?azure-portal=true) and sign in.

1.  Select the environment that you used to create the **Customer Check In** business process flow.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of environment selected.](../media/27-launch-power-apps.png)](../media/27-launch-power-apps.png#lightbox)    

1.  Select the **Data** menu on the left side of the screen and Double-click the down arrow to expand. Select **Tables**

	> [!div class="mx-imgBorder"]
	> [![Screenshot of Power Apps navigation menu with Data expanded and Table highlighted.](../media/30-expand-tables-menu.png)](../media/30-expand-tables-menu.png#lightbox)

1.  Select the **Customer Check In** Table.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of Power Apps Data, Tables with Customer Check In highlighted.](../media/31-select-check-table.png)](../media/31-select-check-table.png#lightbox) 

1.  Select the **Data** tab then click **Select view** on the right side of the screen, and then select the **All Data** view option.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of Power Apps Data, Tables, Customer Check In page with the Data tab and Select View button highlighted.](../media/32-select-data-tab-all-data-view.png)](../media/32-select-data-tab-all-data-view.png#lightbox)

	> [!div class="mx-imgBorder"]
	> [![Screenshot zoomed in to show the Select View All Columns.](../media/33-select-all-columns-view.png)](../media/33-select-all-columns-view.png#lightbox)    

Now, you can view all of the data that you created with your new immersive business process flow.

> [!div class="mx-imgBorder"]
> [![Screenshot shows the Customers entered with the immersive business process flow.](../media/34-close-up-all-data-view.png)](../media/34-close-up-all-data-view.png#lightbox)

In the next and final module of this learning path, you will improve your new immersive flow by customizing the form that is associated with your flow, adding logical branching, and adding instant workflow notification to make your new immersive business process flow even more powerful.