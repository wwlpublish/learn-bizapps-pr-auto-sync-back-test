Most business apps do not want or need to show the user all the data,
instead only the data that is relevant to them. To do this, you can use
functions such as Filter and Search to provide a more focused view of the information.
These functions, when delegated to the data source to be processed,
also reduce the number of rows that must be downloaded and processed by the app.
This creates a faster experience for your users.

In the previous module, you learned about adding a data source to a gallery.
In this module, you will extend on those concepts by shaping the data to show
what is relevant to the user.

Use the filter function to filter data
----------------

The Filter function is the most commonly used function for shaping data.
With Filter, you can create simple queries that allow you to return only
the data you need. For example, if your data source has a text column
named **IsActive** with **Yes** or **No** values for tracking project
status, you could filter your data by using the following formula in the
Items property of your gallery.

```
Filter(YourDataSourcetable, IsActive = "Yes")
```

Instead of displaying all of the rows from the table, the
gallery would only show the rows that had Yes in the column IsActive.
This gives your users fewer rows to sort through and speeds up the
app by reducing the amount of data downloaded.

And operator
----------------

It is also possible to go a step further and use operators to make a
more complex filter. A common example of this is using the And operator
to combine criteria for the filter. When using the And operator, all
equations must equal true. For example, you could extend the previous
example to show all of the rows where **IsActive** is **Yes** and
**Region** is **North** by using the following query.

```
Filter(YourDataSourcetable, IsActive = "Yes" And Region = "North")
```

This formula will return all of the rows where IsActive is Yes, and
the Region is North. Note, when using the And operator in your formula,
it must be capitalized.

Or operator
---------------

Another common operator to add to a filter is the Or operator. When using
the Or operator, only a single equation must be true to return the
row. Like the And operator, the Or operator must also be capitalized.

Expanding on the previous example, there may be a case where you want to
see all rows where the Region is North or West. To build that query
you would use the Or operator.

```
Filter(YourDataSourcetable, Region = "North" Or Region = "West")
```

This formula will return all of the rows where Region is equal to
North or West. Also, note the syntax in the formula: Region =
"North" Or Region = "West". A common mistake is to write Region =
"North" Or "West". That is an incorrect formula.

Combining operators
-------------------

Sometimes the solution needs more than a single operator. In this case,
you can combine operators and apply more advanced logic. Take the
previous two examples. You may find a case where you want to filter your
data source to return all of the rows where IsActive is Yes, and the
Region is either North or West. To do that you can include parentheses
in your formula. Your formula would be the following.

```
Filter(YourDataSourcetable, IsActive = "Yes" And (Region = "North" Or Region = "West"))
```

The formula will evaluate the parentheses first. In this formula, it
will first determine if the Region is North or West. If either of those
evaluations is true, then the right side will be true. Next, the formula
will check the value of the IsActive column. If that equals "Yes", then
the row is a match and will be returned by the Filter function.
Microsoft Power Apps supports a wide range of operators and the nesting of them to
shape your data.

For more information on the different operators that are available in
Power Apps, see [Operators and data types in Power Apps](/power-apps/maker/canvas-apps/functions/operators/?azure-portal=true)
in the documentation. Other examples include greater
than, less than, not, in, exact in, and more. Also, when evaluating
operators be sure that you understand delegation. Different operators have
different delegation behaviors with different data sources. For a list
of data sources and their operators,
see [Understand delegation in a canvas app](/power-apps/maker/canvas-apps/delegation-list/?azure-portal=true).
