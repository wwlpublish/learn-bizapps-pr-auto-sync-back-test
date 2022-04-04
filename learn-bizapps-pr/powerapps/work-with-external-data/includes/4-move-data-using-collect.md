Collections are a special kind of data source. They're local to the app and not backed by a connection to a service in the cloud, so the information can’t be shared across devices for the same user or between users. Collections can be created dynamically with the Collect function. They don't need to be established ahead of time, as connection-based data sources do. In other words, collections are just variables, so their contents aren't saved if the user closes the app, and anyone else running the app can't access any data that they contain. To save the information from your collection, write it to a data source. There are two primary ways of saving data in
a collection.

## Use the Collect function

The first method works well if your collection's column names match those of the data source. For example, if you had a collection named collectMyFirstCollection that contains two columns, **Name** and **FavoriteColor**. If you had a data source named **YourDataSource** with a **Name** and **FavoriteColor** column, you could save your
collection by using this function:

```
Collect(YourDataSource, collectMyFirstCollection)
```

If these requirements are met, that function creates a record in your data source for each record in the collection:

- All the columns in your collection must exist in the data source. The data source can have additional columns, but the columns in your collection must be present.

- The data type (such as Text, Number, or Date) of each column in the collection must match the data source.

- Your data source must not have required columns that your collection doesn't have.

> [!Tip]
> If necessary, you can use these functions to transform your collection so that the columns match your data source.
>
> - AddColumns
> - DropColumns
> - RenameColumns
> - ShowColumns
> 
> For more information, see [AddColumns, DropColumns, RenameColumns, and ShowColumns functions in Power Apps.](/power-apps/maker/canvas-apps/functions/function-table-shaping/?azure-portal=true)

For more information on Collect function and Collections, see [Collect Documentation.](/power-apps/maker/canvas-apps/functions/function-clear-collect-clearcollect/?azure-portal=true)

## Patch and ForAll

**Patch** is a function that allows you to modify or create a record in your data source. **ForAll** is a function that allows you to run a formula for each record in a table, and collections are tables. You can combine these functions to update your data source with the contents of your collection. This strategy works well when you want to apply additional logic.

For example, you could create a collection named collectColorData that contains three columns: **Name**, **FavoriteColor**, and **UpdateSource**. The **UpdateSource** column could be a Boolean (true or false) column.
Through the process of working with the app, the user would update the value in the column and then select a button that says **Update Source**. You could set the **OnSelect** property for the button to this formula:

```
ForAll(Filter(collectColorData, UpdateSource = true),
Patch(DataSourceName, Defaults(DataSourceName), {NameColumnSource: Name,
FavoriteColorColumnSource: FavoriteColor}))
```

This formula would add records to the data source named **DataSourceName**, setting the **NameColumnSource** and
**FavoriteColorColumnSource** columns with the values from your collection but only for the records where **UpdateSource** was set to true.

This example could be further optimized, but it should demonstrate the concept and pieces for dynamically saving your collection to a data source.

For more information on ForAll, see [ForAll Documentation](/power-apps/maker/canvas-apps/functions/function-forall/?azure-portal=true).

For more information on Patch, see [Patch Documentation](/power-apps/maker/canvas-apps/functions/function-patch/?azure-portal=true).