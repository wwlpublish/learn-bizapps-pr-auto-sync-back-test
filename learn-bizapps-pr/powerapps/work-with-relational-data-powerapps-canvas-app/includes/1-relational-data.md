As you start to build complex apps with Power Apps, one concept that you'll need to become familiar with is relating data. Relating data is when you create a connection between two different data sources. An example is a travel expense app where you want to have one record for the trip and then one or more records for the individual expenses like food and lodging.

The following table is an example of storing all of the expense data in
one Microsoft Dataverse table.

| ID | Destination | Date      | Trip reason    | Expense type | Expense amount  |
| - | -----------|----------|---------------|-------------|----------------|
| 1  | Seattle     | 4/10/2020 | Customer Visit | Hotel        | 205.75          |
| 2  | Seattle     | 4/10/2020 | Customer Visit | Dinner       | 31.33           |
| 3  | Seattle     | 4/10/2020 | Customer Visit | Flight       | 450.54          |
| 4  | Cincinnati  | 5/2/2020  | Training       | Cab          | 23.99           |
| 5  | Cincinnati  | 5/2/2020  | Training       | Lunch        | 12.44           |

The example above shows that there's redundant data because each row has all of the information for the entire trip. A better way to store this data would be with parent and child tables, and then create a relationship between the two entities. The next example shows what the two tables would look like.

First, the parent table with only one entry per trip.

| ID | Destination | Date      | Trip reason    |
| - | -----------|----------|---------------|
| 1  | Seattle     | 4/10/2020 | Customer Visit |
| 2  | Cincinnati  | 5/2/2020  | Training       |

Then, the child table that has one entry per expense item with a
reference to the parent record.

| ID | Expense type | Expense amount | TripID       |
| -  | -------------|---------------|-------------|
| 1  | Hotel        | 205.75         | 1            |
| 2  | Dinner       | 31.33          | 1            |
| 3  | Flight       | 450.54         | 1            |
| 4  | Cab          | 23.99          | 2            |
| 5  | Lunch        | 12.44          | 2            |

Here you see one entry for each expense. There's also a new column for
TripID. This column creates the relationship by specifying the record ID
of the parent record. This allows you to query the details of the
associated trip.

When building relationships, you can also relate data from two
different data sources. An example of this is storing customer
information in a CRM system, such as Dynamics 365, and then using that
information as part of a list in Microsoft Lists for sales regions. With
Power Apps, the setup and design of referencing the ID of the customer in
Dynamics 365 from your list works the same. This is one of
the many benefits of Power Apps, connecting to multiple data sources from
within one app is seamless.

> [!NOTE]
> Dataverse can define relationships using Lookup columns, creating the structure and connecting the tables for you. This is outside the scope of this primer on relationships but worth noting as you consider data sources.

In the next section, you'll learn the functions and formulas for
using relationships in Power Apps.
