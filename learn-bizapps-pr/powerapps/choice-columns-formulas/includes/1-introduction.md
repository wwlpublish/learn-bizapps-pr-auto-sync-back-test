A common requirement for business app data storage is to have a data column that has a standardized, infrequently changing list of values to help ensure data consistency. Users who are entering data would choose an option from a list instead of typing a free-form value. Examples of these options include a list of countries, incident priority, satisfaction rating, and so on.

Microsoft Dataverse has two table column types that support this concept: **choice** and **choices**. Choice columns allow a user to pick a single value from the list, whereas choices columns allow the selection of multiple values. Both column types can use a single list of known values. For example, **Primary Category** could be a choice column and **Other Categories** could be a choices column, which would allow for multiple selections. In this example, both could have the same list of categories.

The system, or a customizer, would define the list of known choice values for a choice or choices column, and they would store the values as table column metadata. Unlike application data, only an app maker can modify it, not a user of an app. A benefit of this feature is when you're building an app that works with a list of values. Your formulas can use the name of the choice list and the display name of the values in the formula. For example, the following formula sets a color on an item's fill property based on the **Category** column, which is a choice column.

> [!div class="mx-imgBorder"]
> [![Screenshot of the following Power Fx formula: Switch( ThisItem.Category, 'Category (Accounts)'.'Preferred Customer', Green, 'Category (Accounts)'.'Standard', Black. )](../media/switch.png)](../media/switch.png#lightbox)

As you compose this formula, the editor will know the possible values for the **Category** column and will allow you to select the value to compare from the list of known values for the choice column.

> [!NOTE]
> If you add or change values on a choice list, and the modified item is not showing in the editor, make sure that you refresh the table on the data panel by selecting the ellipsis (**...**) next to the table and selecting **Refresh** from the pop-up menu.

> [!div class="mx-imgBorder"]
> [![Screenshot of a Refresh menu item in a pop-up menu for a Dataverse table. The menu is invoked by selecting the ellipsis next to the table.](../media/refresh.png)](../media/refresh.png#lightbox)

## Local versus global

You can set up the list of available values as local or global for choice and choices columns. **Local choice** list values are used only for the column where they're defined. The **Global choice** option allows the list to be used for multiple columns in the same table or in different tables. We recommend that you select **Global choice** to encourage reuse of the same choices unless you're confident that the values only apply to that single column. You will select **Global choice** or **Local choice** when you create a new column and a list of values and it can't be changed later.

> [!div class="mx-imgBorder"]
> [![Screenshot of choice column properties in the maker interface, showing the Global choice and Local choice options highlighted.](../media/global.png)](../media/global.png#lightbox)

How you reference the list of values in your formulas depends on if they're local or global. For example, if you created a choice column on the Account table named **Priority**, with values of **High**, **Medium**, and **Low**, you would use the list of values as follows:

- **Local** - 'Priority (Accounts)'.High

- **Global** - 'Priority'.High

The difference between the two options is that the **Local** list includes the table name, **(Accounts)**. This factor matters because you'll need to make sure that you're referencing the correct list of values.

## Display column values

When the data for choice or choices columns is stored in the Dataverse row, only the numeric value is stored, not the text. For choices columns, a comma-separated list of numeric values is stored to represent multiple selections.

How you display values in a control, such as a label, is different for choice and choices columns. Choice fields can be used to set the value of a label to display the list text value. For example, if you had a **Category** choice field for the category of customer, you could display that field in a label in a gallery by using the following formula.

> [!div class="mx-imgBorder"]
> [![Screenshot of the Power Fx formula: ThisItem.Category.](../media/category.png)](../media/category.png#lightbox)

For choices columns, the property on the record is of type Table. It's a single column table with a value column, with each row representing a selected value. To display a user-friendly, comma-separated list of text values, some preprocessing is required. For example, if you had a **Preferred Delivery** column that allowed users to choose one or more weekdays for delivery, you'd use the following formula to set the **Text** property on a label.

> [!div class="mx-imgBorder"]
> [![Screenshot of the Power Fx formula: Concat(ThisItem.'Preferred Delivery',Text(Value), ", ").](../media/delivery.png)](../media/delivery.png#lightbox)

This formula would result in the following display of the list of selected values.

> [!div class="mx-imgBorder"]
> [![Screenshot of a screen showing preferred delivery as Monday and Tuesday, which is the output of the Power Fx formula.](../media/list.png)](../media/list.png#lightbox)

## Choice vs. lookup

One common data modeling decision is choosing between a choice column and a lookup column or between a choices column and a many-to-many relationship. This decision can affect how you manage the list of values and the formulas that you can apply. Consider the differences that are listed in the following table.

| Choice or choices | Lookup or many-to-many relationship |
|-------------------|-------------------------------------|
| List modified by maker, no user editing | List is only table data and normal security applies |
| Data stored as a whole number (choice) or a comma-separated list of numbers (choices) | Data stored as a table reference |
| No built-in way to inactivate or retire choice | Supports inactive state on row and can be filtered by formulas in app to limit selection |
| Treated as a solution component with full ALM support | Treated as reference data |
| Only has label and value, and only label is useable in formulas (for example, filter and sorting only on display label) | Can add other data to a look-up target table that can be used in formulas (for example, filter and sorting on any column that is added to table) |
| Localization built in | Handle localization yourself |
| No built-in support of dependent choice columns | Easier to data model and implement dependent columns (see [Create a dependent dropdown list in a canvas app](/power-apps/maker/canvas-apps/dependent-drop-down-lists/?azure-portal=true)) |

After you have created the column, you can't change the data type; therefore, before you create the column, consider how the apps and automation will be using the data.

The rest of this module explores how to use choice and choices columns when you are building a canvas app from Microsoft Power Apps.
