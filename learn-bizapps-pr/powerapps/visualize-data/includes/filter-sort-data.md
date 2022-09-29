By now, you've reviewed how to create and modify views and how to add or remove columns that are presented for the listed records. In this unit, you'll go through the steps involved to define which records this list should contain and in which order the records should be organized.

## Filter data

The process you use to define which records will be part of a view is to configure the **Filter by** property of that view.

> [!div class="mx-imgBorder"]
> ![Partial screenshot of the view designer. Focus is on the Filter by section in the right pane.](../media/filter.png)

A filter is composed of one or multiple criteria that are applied against each record to determine if it should be displayed--that is, when the criteria set is valid or not displayed if invalid. The different rules can be grouped and set with an **Or** clause when either is valid or set with an **And** clause when all must be valid.

> [!div class="mx-imgBorder"]
> [![Screenshot of the Edit filters configuration page. Focus is on the Boolean operators And, Or.](../media/edit-filters.png)](../media/edit-filters.png#lightbox)

The filtering criteria may be set on columns of the table the view is for, or for columns of related records. For example, an **Account** has a **Primary Contact** that can be assigned. As a filter criterion, it's possible to filter records where the primary contact's last name begins with the letter *S*.

> [!div class="mx-imgBorder"]
> ![Partial screenshot of the Edit filters configuration page. Focus is on the Primary Contact (Contact) field and Last Name Begins with S criterion.](../media/primary-contact-begins.png)

When you add a new criterion, three options are available:

- **Add row:** to add a single criterion

- **Add group:** to group multiple criteria together

    > [!div class="mx-imgBorder"]
    > ![Partial screenshot of the Edit filters configuration page. Focus is on the Add flyout menu displaying the available options: Add row, Add group, Add related table.](../media/add-group.png)

- **Add related table:** to add rules against records that are related to the current one being evaluated

From a simple criterion to a complex set of criteria, a filter definition is set by using a series of logical operations that determines whether a record should be displayed.

The filter definition isn't limited to the visible columns of a view, but for those visible columns, a shortcut is available to add a **Filter by** criterion. By selecting the column heading in the view editor, you can select a menu option to define the rule to apply.

> [!div class="mx-imgBorder"]
> ![Partial screenshot of the view designer. Focus is on the Email (Primary Contact) column headings and Filter by option in the flyout menu.](../media/email-filter.png)

> [!div class="mx-imgBorder"]
> ![Partial screenshot of the view designer. Focus is on the Filter by configuration flyout menu.](../media/filter-by.png)

## Sort data

The list of records presented in a view is presented in a sequence based on the **Sort by** definition.

This definition is composed of a list of columns that must be part of the visible columns of the view and are processed one after the other.

> [!div class="mx-imgBorder"]
> [![Partial screenshot of the view designer. Focus is on the Sort by section in the right pane with a list of available columns. Focus is also on the column headings displayed in the view.](../media/sort.png)](../media/sort.png#lightbox)

Each of the selected columns can be sorted in ascending or descending sequence. This configuration can be set by selecting the column heading and then the type of sort sequence required.

> [!div class="mx-imgBorder"]
> ![Partial screenshot of the view designer. Focus is on the Main Phone column heading and Sort ascending, Sort descending options in the flyout menu.](../media/main-phone.png)

## Modify filters and sort criteria in Power Apps

For users of model-driven apps, the filters and sort criteria can be modified in the application. Select **Edit filters** to modify the criteria and apply the filter and sort criteria temporarily to the current view. An asterisk will be appended to the view name to indicate such a change was applied.

> [!div class="mx-imgBorder"]
> [![Partial screenshot of a model-driven app. Focus is on Edit filters and the asterisk next to the view name.](../media/asterisk.png)](../media/asterisk.png#lightbox)

For users who want to save a modified version of a view as a **personal view**, select **Save as new view** under **Create view**.

> [!div class="mx-imgBorder"]
> ![Partial screenshot of a model-driven app. Focus is on Create view and Save as new view.](../media/save-view.png)

## Next steps

You now have learned how to modify the list of records that are presented in a view by creating or editing the view's filter criteria. You also have learned how to apply a sorting order to that list of records. Next, you'll apply those learnings in an exercise applicable to the **Account** table.
