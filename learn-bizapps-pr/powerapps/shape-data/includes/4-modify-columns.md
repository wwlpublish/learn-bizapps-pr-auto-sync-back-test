Functions like Filter and Search are used to modify the returned
rows, but sometimes you need to modify the columns of the rows
while using the rows. For example, if you were creating a shopping
cart app for sending digital assets to a customer, you would need a way
to keep track of the selected assets. Ideally, you would have a
temporary column for tracking the selected rows that only exist
inside of Power Apps and does not modify the original data source.
Fortunately, Power Apps offers a solution.

With Power Apps there's a series of functions that modify the columns of your
table only within Power Apps, which means that they don't modify or change
the actual data source. Those functions are:

-   AddColumns

-   DropColumns

-   RenameColumns

-   ShowColumns

AddColumns
----------

The **AddColumns** function adds a column to a table, and a formula
defines the values in that column. Existing columns remain unmodified.

For the previous example of a shopping cart app, you would use the
**AddColumns** function to add a column for tracking if the user selected
the column. You would do this by setting the following formula for the
**OnSelect** property for a **Button** control.

```
ClearCollect(collectDigitalAssets, AddColumns(YourDataSource,"UserSelected", false))
```

When this button is selected, the formula creates a collection named
**collectDigitalAssets** that has all of the rows from
**YourDataSource** and adds the column, "**UserSelected**". The column
value is **false** for all of the rows.

Now in your **Gallery** control, set the **items** property to the
following.

**collectDigitalAssets**

In the **Gallery** control, you would have access to a column named
**UserSelected** and the value would be false. You could then add a
button into your Gallery that **OnSelect** would patch the column to
true.

```
Patch(collectDigitalAssets, ThisItem, {UserSelected: true})
```

Now in the **collectDigitalAssets** collection you are tracking the
rows the user has selected in your app without modifying the columns
in your data source.

DropColumns
-----------

The **DropColumns** function works the opposite of AddColumns. The
function is used to remove columns from the table within Power Apps. This
function is used when you want to create a collection within Power Apps
that has several columns for app functionality. Because these columns will
be added only in the collection for app functionality and not submitted
to the data source, the **DropColumns** function is needed to remove the
column upon submission to the data source.

For example, you create a collection name **collectTimeTracking** to use
in a time tracking application. The collection has five columns: Name,
HoursWorked, DateWorked, LastScreen, and Status. The columns **Name**,
**HoursWorked**, and **DateWorked** track the data to save to
**YourDataSource** based on hours an employee worked. The columns
**LastScreen** and **Status** store data to provide app functionality
while the users is using the app.

When the user is done, one way to save the information back to a data
source is to use the **Collect** function. If the columns match between
the data source, the **Collect** function will write all of the
rows to your collection. In this example, **Name**, **HoursWorked**,
and **DateWorked** are the only columns in the data source.
**LastScreen** and **Status** do not exist in the data source and do not
need to be saved. You can use **DropColumns** to send just
the appropriate columns to the data source.

```
Collect(YourDataSource, DropColumns(collectTimeTracking, "LastScreen","Status"))
```

This function will write the contents of the collection,
**collectTimeTracking,** to the data source, **YourDataSource,** after
dropping the columns **LastScreen** and **Status**. Note,**DropColumns** 
did not alter your collection **collectTimeTracking**. The **LastScreen** 
and **Status** columns are still available within the collection.

RenameColumns
-------------

Use the **RenameColumns** function when you need to manipulate the name
of the column within your app but not within your data source. A common
use is when the data source, which you cannot edit, has difficult to
reference column name or the column name uses reserved words, like "Date".

You can use the function when storing data into a collection. Note that 
the **Collect** function can take the contents of your data
source and store them into a collection.

```
Collect(collectProjectData, ProjectDataSource)
```

This formula would create a collection named **collectProjectData** that
stores all of the rows of data from the data source,
**ProjectDataSource**. If the data source has a column named **Date**,
you might find it easier to work in Power Apps by renaming that column to
**ProjectDate**. You can do that by using the following formula instead
of the previous example.

```
Collect(collectProjectData, RenameColumns(ProjectDataSource, "Date","ProjectDate"))
```

You have the same rows. Now, instead of the column being named
**Date,** it is now named **ProjectDate** within your collection. This
gives you the flexibility to name columns to something that will be less
confusing to work with in the app.

ShowColumns
-----------

**ShowColumns** is used to display one or more columns from your data
source. Use this with controls where you only want a single column
returned. A common example is the **dropdown** control.

With the **dropdown** control, it is common to use a data source, such
as a Microsoft Dataverse table, to provide the options. When you set the items property
to a data source, Power Apps will choose which column, if you
have multiple, to display. You can use the **ShowColumns** function to
select the column that you want to display.

If you wanted to use a data source named **Customers** to display
customer names from the **CustomerName** column. You would use the
following formula in the **Items** property of the **Dropdown** control.

```
ShowColumns(Customers, "CustomerName")
```

With this formula, the **Dropdown** column displays the values from the
**CustomerName** column.

**ShowColumns** can also return more than one column. The **Dropdown**
control will only display the first column, but you will have access to
all the retrieved columns. The following example shows how to add
the **ID** column to your **Dropdown** control.

```
ShowColumns(Customers, "CustomerName", "ID")
```

The dropdown will only display the value from **CustomerName** column in
the **Dropdown** control, but with this formula, you now have access to
the value of the ID column. Add a **Label** control to the screen and
set the **Text** value to the following. If your dropdown is not named
Dropdown1, edit the formula accordingly.

```
Dropdown1.Selected.ID
```

The formula returns the value from the ID column for the selected row
in your **Dropdown** control. 
