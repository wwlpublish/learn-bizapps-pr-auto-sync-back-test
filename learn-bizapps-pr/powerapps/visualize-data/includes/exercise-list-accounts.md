In this exercise, you'll apply your learned knowledge to create a view for accounts that you manage and where the records are sorted from the highest annual revenue to the lowest.

In a Dataverse environment where you can proceed with modifications to the tables, such as dedicated training or development environment, follow these steps:

1. Sign in to the [Power Apps portal](https://make.powerapps.com/?azure-portal=true).

1. In the left pane, expand **Dataverse**, and then select **Tables**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the Power Apps portal left navigation pane. Focus is on the expanded Dataverse option and Tables.](../media/dataverse-tables.png)

1. In the list of tables, select **Account**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the list of Tables in the Power Apps portal. Focus is on the Account table name.](../media/account-table-name.png)](../media/account-table-name.png#lightbox)

1. In the Power Apps portal, for the Account table, select **Views**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Account table designer. Focus is on the Views option.](../media/views.png)](../media/views.png#lightbox)

1. Select the **New view**.

    > [!div class="mx-imgBorder"]
    > [![Partial screenshot of the list of views for the Account table. Focus is on the New view.](../media/new-view.png)](../media/new-view.png#lightbox)

1. Define a name and a description for the new view. Select **Create** to proceed to the view designer.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Create a view form. Focus is on the Name and Description fields and the Create button.](../media/create-name.png)](../media/create-name.png#lightbox)

1. Add columns to the view, including **Annual Revenue** and **Owner**.

    > [!div class="mx-imgBorder"]
    > [![Partial screenshot of the view designer. Focus is on the Actual Revenue column being selected from the flyout menu of the + View column.](../media/add-columns.png)](../media/add-columns.png#lightbox)

    > [!div class="mx-imgBorder"]
    > [![Partial screenshot of the view designer. Focus is on the Owner column being selected from the flyout menu of + View column.](../media/add-column.png)](../media/add-column.png#lightbox)

1. Set the order of the records to display in order of revenue. Select **Annual Revenue**, and then select **Larger to smaller**.

    > [!div class="mx-imgBorder"]
    > ![Partial screenshot of the view designer. Focus is on the Actual Revenue column heading and Larger to smaller option from the flyout menu.](../media/annual.png)

1. Filter the accounts to be displayed so only the records you manage are listed. Select the **Owner** column heading, and then select **Filter by**.

    > [!div class="mx-imgBorder"]
    > ![Partial screenshot of the view designer. Focus is on the Owner column heading and Filter by option from the flyout menu.](../media/owner.png)

1. In the list of users, select your name, and then select **Apply**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the Filter by flyout menu. Focus is on the selected user and Apply.](../media/apply-filter.png)

1. To apply changes and make them available to Power Apps users, select **Save**, and then select **Publish**.

    > [!div class="mx-imgBorder"]
    > ![Partial screenshot of the view designer. Highlight on Save and Publish.](../media/save-publish.png)

## Exercise steps (video)

In the following video, you're taken through the steps for this exercise.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/]

## Next steps

You now have learned how to add filter and sort criteria to a Dataverse table view. Next, you'll have the opportunity to validate the learned concepts for this module.
