Welcome to "Visualize data with Dataverse views." This self-paced module will help you learn how you can take advantage of Dataverse table views to visualize data by using only the required columns, records, and applicable sorting.

## Dataverse tables

Tables in a database system, such as Dataverse, provide a definition of the data it contains. The data model that the tables are part of defines the relationships between different tables. In Dataverse, there are a series of standard tables that are already available and have been designed following common business scenarios and best practices. Tables can also be created to suit custom scenarios, and the system tables can be tailored to adapt to those scenarios.

To view the tables in a Dataverse environment, follow these steps:

1. Sign in to the [Power Apps portal](https://make.powerapps.com/?azure-portal=true).

1. In the left pane, expand **Dataverse** and select **Tables**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the Power Apps portal left navigation pane. Focus is on the expanded Dataverse option and Tables.](../media/dataverse-tables.png)

1. In the list of tables, select a table to view its details or customize. For example, you can select **Account**, which is one of the core tables that the system provides during the provisioning of a new Dataverse database.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the list of tables in the Power Apps portal. Focus is on the Account table name.](../media/account-table-name.png)](../media/account-table-name.png#lightbox)

1. The table details provided (and available to edit) include the **columns**, **relationships**, and **keys** that are responsible for the definition of the data structure and position of this table in the database model. A presentation of some **records** is displayed as a default view of that Dataverse table data.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Account table designer. Focus is on the schema section that includes Columns, Relationships, and Keys. Focus is also on the list or records.](../media/account-columns.png)](../media/account-columns.png#lightbox)

## Dataverse table views

Based on the user accessing the data contained in the Dataverse tables, only a subset of columns and records may be required. Dataverse table views provide standardized and accelerated methods of accessing the data based on the user and/or applicable scenarios.

There are three types of views:

- **Personal view:** owned by individuals and visible to other users it's shared with.

- **System view:** special views that Power Apps applications depend on. They're automatically created, and only users with the *system administrator* or *system customizer* security role can edit them. System views are defined as:

  - **Quick Find:** for searches using *Quick Find* in Power Apps applications

  - **Advanced Find:** for searches using *Advanced Find* in Power Apps applications

  - **Associated:** to list records associated with another table's record

  - **Lookup:** for lookup fields

- **Public view:** created by individuals but accessible by all app users. Useful for organization-wide scenarios.

Views are accessible in the maker portal by following these steps:

1. In the Power Apps portal, for a selected table, select **Views**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Account table designer. Focus is on the Views option.](../media/views.png)](../media/views.png#lightbox)

1. This selection will provide you with the list of views that are applicable to this table. This list displays the **Name**, the **View type**, and other key settings such as the active **Status**, **Managed property**, and whether it's **Customizable**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the list of views for the Account table. Focus is on the column headings: Name, View type, Status, Managed, and Customizable.](../media/account-views.png)](../media/account-views.png#lightbox)

## Views in Power Apps

Power Apps applications can take full advantage of Dataverse views for the tables they refer to.

In model-driven types of apps, a view selector is available to the users when they access the main page for a table.

> [!div class="mx-imgBorder"]
> [![Screenshot of a model-driven app. Focus is on the list of available views.](../media/my-active-accounts.png)](../media/my-active-accounts.png#lightbox)

Users of model-driven apps can also create personal views by selecting the **Create view** menu option.

> [!div class="mx-imgBorder"]
> [![Screenshot of a model-driven app. Focus is on the Create view menu option.](../media/create-view.png)](../media/create-view.png#lightbox)

In canvas apps, a view selector is available to the makers when they select a Dataverse table as a data source for a gallery.

> [!div class="mx-imgBorder"]
> [![Screenshot of the canvas app studio with a gallery component. Focus is on Data source and view settings with the list of available views.](../media/data-source-views.png)](../media/data-source-views.png#lightbox)

## Next steps

You now have learned the fundamentals of Dataverse table views. Next, you'll learn how to create and edit views in the Power Apps maker portal.
