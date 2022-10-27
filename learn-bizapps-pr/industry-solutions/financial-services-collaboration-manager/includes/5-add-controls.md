In this exercise, you'll embed the **Loan Application** form from the Loan Tracker app so that your users can have access to more information within Collaboration Manager for Loans. All apps in Microsoft Cloud for Financial Services use the same data model, which allows you to mix and match the experiences for the various apps.

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE5aOOL]

## Task 1: Replace a default form within Collaboration Manager

Before creating your customizations, you first need to create a solution to contain the changes. 

1. Go to [https://make.powerapps.com](https://make.powerapps.com/?azure-portal=true) and select **Solutions** in the left navigation.

1. Select **New solution** to create a new solution.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the environment selection.](../media/solution-select.png)](../media/solution-select.png#lightbox)

1. Provide information for the required fields and then select **Save**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the New solution dialog with the Display name, Name, Publisher, and Version fields filled in.](../media/solution.png)](../media/solution.png#lightbox)

1. Open the solution that you created.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Solutions list with the Loan Tracker in Collaboration Manager solution highlighted.](../media/solutions-list.png)](../media/solutions-list.png#lightbox)

1. Because you want to show the Loan Tracker form instead of the default Collaboration Manager form, update the app module so that it shows a different loan application form. Select **Add existing > App > Model-driven app** so that you can begin making those changes.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of Power Apps with Add existing expanded and App expanded to show the Model-driven app option.](../media/app.png)](../media/app.png#lightbox)

1. Select **Collaboration Manager for Loans** and then select **Add** to bring the app into your solution.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Add existing model-driven apps dialog with Collaboration Manager for Loans selected.](../media/add-model-driven.png)](../media/add-model-driven.png#lightbox)

1. Select and open the app when it shows in your solution.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Solution editor.](../media/solution-edit.png)](../media/solution-edit.png#lightbox)

1. Select the **Loan application form** for the **Loan application** entity within the app designer.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Form editor.](../media/form-edit.png)](../media/form-edit.png#lightbox)

1. On the right side, select **+ Add form** and then select the **Loan tracker information form**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of Power Apps showing the app designer for Collaboration Manager for Loans with the options updated.](../media/form.png)](../media/form.png#lightbox)

1. Remove the **Information** form by clicking on the more options and select **Remove**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of how to remove a form.](../media/remove-form.png)](../media/remove-form.png#lightbox)

1. Select **Save**. After the changes are saved, select **Publish**. If you played the app at this point within Microsoft Teams, the components from Loan Tracker will be present, but the collaborative features like tasks, meetings, and notes wouldn't be present.

   > [!div class="mx-imgBorder"]
   > [![Screenshot of save and publish the form.](../media/form-save-publish.png)](../media/form-save-publish.png#lightbox)

## Task 2: Add Collaboration controls experiences in the Loan Tracker form

Now, you'll edit the **Loan tracker information form** so that it includes the **Tasks**, **Meetings**, and **Notes** tabs. 

1. Select the edit icon next to the **Loan tracker information form**.

   > [!div class="mx-imgBorder"]
   > [![Screenshot of Power Apps showing the app designer for collaboration manager for loans with the edit button highlighted.](../media/edit.png)](../media/edit.png#lightbox)

   The **Loan tracker information form** will open in the form designer.

1. In the form designer, drag a **1-column tab** layout component from the **Components** drawer and then drop it to the left of the **Activities** tab.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of Power Apps > Form showing the Components panel with a 1-column tab layout component being dropped to the right of the Activities tab.](../media/1-column-tab.png)](../media/1-column-tab.png#lightbox)

1. After dragging in the tab, rename it to **Tasks** in the **Properties** pane.

1. Select **Expand first component to full tab** in the **Properties** pane.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Tasks tab properties with Label, Name, and Expand properties set.](../media/expand.png)](../media/expand.png#lightbox)

1. Select the section within your new tab so that you can select **Hide label** within the **Properties** pane.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the New Section area, showing the Properties tab with Hide label selected.](../media/hide.png)](../media/hide.png#lightbox)

1. Drag a **Subgrid** control from the **Components** drawer and then drop it into your new section.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of a Subgrid component being dragged from the Components panel and dropped into the new section.](../media/components.png)](../media/components.png#lightbox)

1. For the **Tasks** tab, set the values to **All Tasks** from the **Tasks (Regarding)** table.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Select subgrid views dialog with Table and Default view set.](../media/subgrid.png)](../media/subgrid.png#lightbox)

1. Repeat steps 1-7 for the **Meetings** and **Notes** tabs.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the tabs with Meetings and Notes tabs added to the right of the new Tasks tab.](../media/meetings-notes.png)](../media/meetings-notes.png#lightbox)

    For the **Meetings** tab, set the subgrid to **All Appointments** within the **Appointments (Regarding)** table.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Select subgrid views dialog with Table and Default view set to Appointments.](../media/appointments.png)](../media/appointments.png#lightbox)

    For the **Notes** tab, set the subgrid to **All Activities** within the **Activities (Regarding)** table.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Select subgrid views dialog with Table and Default view set to Activities.](../media/activities.png)](../media/activities.png#lightbox)

1. Set up the custom controls for your subgrids within the classic form designer. Select **Save** and then select **Switch to classic**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of Power Apps > Form with the Switch to classic button highlighted.](../media/classic.png)](../media/classic.png#lightbox)

1. Scroll down in the classic form designer until you find the **Tasks** tab. Double-click the subgrid to open its **Properties** dialog.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of Power Apps classic form designer with the subgrid control highlighted.](../media/subgrid-control.png)](../media/subgrid-control.png#lightbox)

1. While in the **Properties** dialog, select the **Controls** tab to view all custom controls that are assigned to it.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Set Properties dialog Controls tab.](../media/controls.png)](../media/controls.png#lightbox)

1. Select **Add Control...**

1. For the **Tasks** tab, select **TasksControl** and then **Add**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Add Control dialog with an Add button.](../media/add-control.png)](../media/add-control.png#lightbox)

1. Select the **Web**, **Phone**, and **Tablet** buttons for the **TasksControl** to ensure that it shows across all form factors.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Set Properties dialog with TasksControl added and buttons selected.](../media/tasks-control.png)](../media/tasks-control.png#lightbox)

1. Repeat steps 9-14 for the **Meetings** and **Notes** tabs. For the **Meetings** tab, use **EventsControl**, and for the **Notes** tab, use **NotesControl**.

1. Select **Save**.

1. Select **Publish**.

1. You can now open Collaboration Manager for Loans in the Teams environment. All tabs from Loan Tracker and the collaborative tabs from Collaboration controls should now display.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of Microsoft Teams with Collaboration Manager for Loans open in its channel and all Loan Tracker and collaborative tabs showing.](../media/all-tabs.png)](../media/all-tabs.png#lightbox)

**Congratulations**, you successfully added controls from Loan Tracker!