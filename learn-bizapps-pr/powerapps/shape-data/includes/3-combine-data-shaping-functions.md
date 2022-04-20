Multiple Power Apps functions can be combined in a single formula to
allow you the flexibility to meet the demands of your business. An
example of this is combining Search and Filter into one formula that
provides items for a gallery control.

For the Search function, the first option you are required to provide is
a table of data. The Filter function returns a table of data. This means
it is possible to use the Filter function as a data source for your
Search function. By adding this as the formula for the Items property of
your Gallery control you are displaying to your users the data they need
with the added ability to Search. The following is an example formula.

```
Search(Filter(YourDataSource, State = "Ohio"), SearchInput.Text, "AddressLine1", "AddressLine2")
```

This formula will filter the data source named YourDataSource for all of
the rows where the State equals Ohio. The table of matching rows
is searched for all of the rows where AddressLine1 or AddressLine2
contains the string entered in the text control. Additionally, if the
control is blank, then all of the rows that were returned by the
Filter function will be displayed.

When building formulas like shown above, it is recommended to start
small and then expand. The following is the typical order of operations you 
should follow when building a formula. Always confirm that you see the expected 
data each step along the way.

> [!NOTE]
> The following steps is an example of combining formulas and not intended to work unless a datasource is provided.
> The exercise unit of this module provides step-by-step details.

1.  Add a **Gallery** control to your canvas.

2.  Add YourDataSource to the **items** property and configure the
    gallery to display the columns for your query. Confirm that you see the
    expected rows.

3.  Change the **items** property of the **Gallery** control to use the
    **Filter** function and confirm that you see the expected rows.

    a.  Filter(YourDataSource, State = \"Ohio\")

4.  Add a text input control to the screen and rename it to
    **SearchInput**

5.  Change the **items** property of the **Gallery** control to use the
    Search function and confirm that you see the expected rows.

    a.  Search(YourDataSource, SearchInput.Text, "AddressLine1")

6.  Add any additional columns to the Search function and confirm you
    see the expected rows.

    a.  Search(YourDataSource, SearchInput.Text, "AddressLine1",
        "AddressLine2")

7.  Now that you have confirmed the two formulas are correct, combine
    the formulas and confirm that your results are correct.

    a.  Search(Filter(YourDataSource, State = \"Ohio\"),
        SearchInput.Text, \"AddressLine1\", \"AddressLine2\")

By breaking the complex formula down into smaller, working parts, you
will have a much better experience creating an app. Within Power Apps, you can
utilize the concept of using one function to supply information to
another function in many places. 
