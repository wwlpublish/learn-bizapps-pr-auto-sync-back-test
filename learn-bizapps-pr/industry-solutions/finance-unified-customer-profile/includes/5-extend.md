In this exercise, you'll customize the Unified customer profile application in the following ways:

- Use the Unified customer profile application as a base and then edit it to add a new control to it.

- Edit the Unified customer profile controls such as **Life event type** to add a new life event type.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE57aY1]

## Task 1: Add new controls to Unified customer profile

In this task, you'll create a new solution and then customize the Unified customer profile application to add new controls.

1. Go to [Power Apps](http://make.powerapps.com/?azure-portal=true) in an In-Private or Incognito window.

1. Select the proper **Environment** in the upper right.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Environment in the upper-right corner.](../media/environment.png)](../media/environment.png#lightbox)

1. In Power Apps, select **Solutions** in the left site map. Select **+ New solution** and then set the following values.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the New solution button in Power Apps.](../media/new-solution.png)](../media/new-solution.png#lightbox)

1. Create a new solution with the properties that are shown in the following screenshot. When you're finished, select **Create**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the new solution details, showing the properties filled in and the Create button highlighted.](../media/solution.png)](../media/solution.png#lightbox)

1. After you've created the solution, select the solution name in the **Display name** column to begin adding components.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the solution name selected in the Display name column.](../media/solution-name.png)](../media/solution-name.png#lightbox)

1. In the solution explorer, select **Add existing** > **App** > **Model-driven app**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the steps to add an existing model-driven app.](../media/add-model-driven-app.png)](../media/add-model-driven-app.png#lightbox)

1. Select **Unified Customer Profile** from the list and then select **Add**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Unified Customer Profile application selected and the Add button highlighted.](../media/unified-customer-profile-application.png)](../media/unified-customer-profile-application.png#lightbox)

1. Select **Unified Customer Profile** to edit the application.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of Unified Customer Profile selected in Power Apps.](../media/edit-unified-customer-profile.png)](../media/edit-unified-customer-profile.png#lightbox)

    The application editor will open in another tab.

1. Select the **Forms** dropdown menu and then select the edit icon for **Unified customer profile**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Forms dropdown menu, showing the edit icon selected for Unified customer profile.](../media/forms-edit.png)](../media/forms-edit.png#lightbox)

1. The form designer for Unified customer profile will open. Select the **Switch to classic** menu item to launch the classic form designer.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Switch to classic button in the form designer.](../media/classic.png)](../media/classic.png#lightbox)

1. In the form designer, select the **Summary** tab.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Summary tab selected in the form designer.](../media/summary.png)](../media/summary.png#lightbox)

1. Select **Insert > One Column**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Insert window with the One Column option selected.](../media/insert-column.png)](../media/insert-column.png#lightbox)

   A new tab will be added to the form under **Summary**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the new tab added beneath the Summary tab.](../media/new-tab.png)](../media/new-tab.png#lightbox)

1. After the tab has been added, clear the **Only show unused fields** checkbox.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Only show unused fields checkbox showing as cleared.](../media/checkbox.png)](../media/checkbox.png#lightbox)

1. In the fields list, look for the **Placeholder** field. Drag and drop the field to the newly added tab.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Placeholder field highlighted.](../media/placeholder.png)](../media/placeholder.png#lightbox)

1. Double-click the **Placeholder** field on the form to open the **Field Properties** dialog. Select the **Controls** tab.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Controls tab on the Field Properties dialog.](../media/controls.png)](../media/controls.png#lightbox)

1. Select **Add Control** and then find **CustomerSummaryControl** in the list.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Add Control button on the Controls tab on the Field Properties dialog.](../media/add-control.png)](../media/add-control.png#lightbox)

1. Select **CustomerSummaryControl** and then select **Add**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of CustomerSummaryControl selected and the Add button highlighted.](../media/customer-summary-control.png)](../media/customer-summary-control.png#lightbox)

1. After the control has been added, you can edit its properties individually. First, select the edit icon for the **Contact** property.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the edit icon for the Contact property.](../media/edit-contact.png)](../media/edit-contact.png#lightbox)

1. In the dialog that opens, set the **Bind to a value on a field** property to **contactid(SingleLine.Text)** and then select **OK**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Bind to a value on a field property set to contact ID.](../media/bind-value.png)](../media/bind-value.png#lightbox)

1. Select the edit icon next to the **Component** property.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the edit icon selected for the Component property.](../media/edit-component.png)](../media/edit-component.png#lightbox)

1. Set the **Bind to static options** value to **Life events** and then select **OK**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Bind to static options value set to Life events and the OK button highlighted.](../media/bind-static.png)](../media/bind-static.png#lightbox)

1. The **Field Properties** dialog should now look similar to the following screenshot. Select **OK**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Field Properties dialog, showing the changes.](../media/field-properties.png)](../media/field-properties.png#lightbox)

1. For **CustomerSummaryControl**, set the **Web**, **Phone**, and **Tablet** options to true and then select **OK**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the customer summary control settings enabled.](../media/customer-summary-control-settings.png)](../media/customer-summary-control-settings.png#lightbox)

1. Now that the form is ready, select the **Home** menu on the ribbon and then select **Save** > **Publish**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Home menu with the Save and Publish buttons selected.](../media/publish.png)](../media/publish.png#lightbox)

1. Close the tab, which will close the classic editor.

1. Return to the modern editor and select the newly created tab in the **Tree view**. Ensure that the values in the **Properties** pane are set as shown in the following screenshot.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the modern editor with the newly created tab selected and the properties set.](../media/modern-editor.png)](../media/modern-editor.png#lightbox)

1. **Save** and **Publish** the changes.

1. Launch **Unified customer profile** again from any contact record. The new tab should display along with the **Life events** control.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the newly added tab, showing the Life events control.](../media/tab-added.png)](../media/tab-added.png#lightbox)

## Task 2: Add a new life event type

In this task, you'll extend the data model to add a new life event type to the Life event table. Then, you'll observe how the changes show in Unified customer profile.

1. In Power Apps, select **Dataverse > Tables** in the left site map. Select the **All** tab and then search for **life event**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the search set to Managed with a search for life event.](../media/managed-life-event.png)](../media/managed-life-event.png#lightbox)

1. In the search results, select the **Life event** table.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Life event table selected in the search results.](../media/life-event-table.png)](../media/life-event-table.png#lightbox)

1. Select **Columns** in the **Schema** section.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Columns selection.](../media/life-event-columns.png)](../media/life-event-columns.png#lightbox)

1. Select **Life event type** to edit it. Scroll down to see all the choices.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the edit life event type.](../media/edit-choice.png)](../media/edit-choice.png#lightbox)

1. Select **New choice** to add the new life event type.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Edit choice button.](../media/edit-choice-new.png)](../media/edit-choice-new.png#lightbox)

1. Enter **University Enrollment** in the new item row.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of adding the new life event type.](../media/new-life-event-type.png)](../media/new-life-event-type.png#lightbox)

1. Copy the **Value** field and then save it for the next steps.

    Your environment's value might differ from the value that's shown in the following image.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Value field.](../media/value.png)](../media/value.png#lightbox)

1. Select **Save**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Save button and the Done button.](../media/save-done.png)](../media/save-done.png#lightbox)

1. Go to the **Tables** tab.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Save Table button.](../media/save-table.png)](../media/save-table.png#lightbox)

1. Select the **All** tab and search for the **Life event type config** table.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the search for life event type config.](../media/life-event-type-config.png)](../media/life-event-type-config.png#lightbox)

1. Select the **Life event type config** table from the search results, which will show details of the table and a preview table of the data. Select **Edit** to add record.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Data button to load the Life event type config table data.](../media/data.png)](../media/data.png#lightbox)

1. Select **+ New row using form**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the New row button for the Life event type config table.](../media/add-record.png)](../media/add-record.png#lightbox)

1. A new tab will open up. Set the following values to create a **New Life event type config**. Select **Save**.

    - **Name** - University Enrollment

    - **Type code** - Enter the value that you copied from the **Value** field in a previous step

    - **Display order** - 1

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the New Life event type config details.](../media/life-event-details.png)](../media/life-event-details.png#lightbox)

1. After you save the record, select the **Related** tab, and then select **Category types relations**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Related tab with Category types relations selected.](../media/category-types.png)](../media/category-types.png#lightbox)

1. In the **Category types relations** tab, select **+ New Category types relations** to create a new record.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the New Category types relations button.](../media/new-category-types-relations.png)](../media/new-category-types-relations.png#lightbox)

1. Set the following values to create a new **Category types relations** record and then select **Save**.

    - **Name** - University Enrollment Category Types Relations

    - **Lifemomentcategory configurations** - Select the **Education** record

    - **Life event type configurations** - Select the **University Enrollment** record

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the category types relations general details.](../media/general-details.png)](../media/general-details.png#lightbox)

    The life event configurations are now complete.

1. Launch the Unified customer profile application.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Unified Customer profile app launch.](../media/launch-unified-customer-profile.png)](../media/launch-unified-customer-profile.png#lightbox)

    And select a contact from the list.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of Unified Customer Profile contact list.](../media/unified-customer-profile-list.png)](../media/unified-customer-profile-list.png#lightbox)

1. Select **Add new event**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Add new event button on the Life events screen.](../media/add-new-event.png)](../media/add-new-event.png#lightbox)

   The new life event type of **University Enrollment** will now show in the **Education** category.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of University Enrollment added as a type in the Education category.](../media/education-university-enrollment.png)](../media/education-university-enrollment.png#lightbox)

**Congratulations**, you've extended the Unified customer profile application to edit controls on the view and add new life event configurations.
