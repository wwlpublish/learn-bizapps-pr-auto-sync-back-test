Microsoft Dataverse is designed to let you quickly and easily create a data model for your application, based on the tables and the table metadata that you include in your app. 

Tables describe the kinds of data that is stored in the Dataverse database. Each table corresponds to a database table and each column (also known as an attribute) within a table represents a column in that table. 

In Dataverse, metadata (data about data), is a collection of tables. Table metadata is what controls the kinds of rows you can create and what kind of actions can be performed on them. When you use customization tools to create or edit tables, columns, and table relationships, you are editing this metadata.

The apps that your customers use to interact with the data in your environment depend on the table metadata, and they adapt as you customize the metadata. 

## When to use standard tables, and when to create new tables
Dataverse comes with many standard tables that support core business application capabilities. Each table also contains many metadata columns that represent common data that the system needs to store for that table. We recommend that you become familiar with the catalog of standard tables, and use them where possible, because any applications written with standard tables will work as you expect in your environment without extra effort.

For minor changes, you might not have to create a custom table: 

- To change the display name of a column, you can edit the table. You don't have to create a new table.
- You can't delete standard tables, but you can hide them. To hide a standard table, change the security role privileges for your organization to remove the Read privilege for that table. This will remove the table from most parts of the application.

If standard tables don't work for your business needs, and if they can't be edited to meet those needs, consider creating a new table, column, or table relationship. If a standard table almost meets your business needs, you can use it as the basis for a new table.

## Table relationships
Table relationships define the different ways table rows can be associated with rows from other tables or the same table [self-referential relationship](/power-apps/maker/data-platform/create-edit-nn-relationships-portal?azure-portal=true#create-a-many-to-many-relationship-with-the-same-table-self-referential-relationship). Table relationships are metadata. They let queries retrieve related data efficiently. Use table relationships to define the formal relationships between tables.

When you look at the solution explorer you might think that there are three types of table relationships but actually there are only two, see below:

- **One-to-many relationships**: In a one-to-many (1:N) table relationship, many related table rows are associated with a single primary table row in a parent/child relationship. 
- **Many-to-many relationships**: In a many-to-many (N:N) table relationship, many table rows are associated with many other table rows. Rows that are related through N:N table relationships are considered peers.

The N:1 (many-to-one) relationship type exists in the user interface because the designer shows you a view grouped by tables. 1:N relationships actually exist between tables and refer to each table as either a Primary/Current table or Related table. The related table, sometimes called the child table, has a lookup column that allows storing a reference to a row from the primary table, sometimes called the parent table. A N:1 relationship is just a 1:N relationship viewed from the related table.

Besides defining how rows can be related to other rows, 1:N table relationships also provide data to address the following questions:

- When I delete a row, should any rows that are related to that row also be deleted?
- When I assign a row to a new owner, do I also have to assign all related rows to the new owner?
- How can I streamline the data entry process when I create a new related row in the context of an existing row?
- How should people who view a row be able to view the related rows?

## Table types
Before creating or editing tables in Dataverse, you should understand the different types of tables that you can create. After a custom table is created, the table type can't be changed. 

### Types of table owners
When you create a custom table, the options for ownership are *User or team owned*, or *Organization-owned*. After a table is created, you can’t change the ownership. 

- **User or team owned**: Actions that can be performed on these rows can be controlled at the user level.
- **Organization-owned**: Access to the data is controlled at the organization level.

### Activity tables
An *activity* is an action that a calendar entry can be made for. Activities have these characteristics:

- They have time dimensions (start time, stop time, due date, and duration) that help define when the action occurred or will occur.
- They have data (like a subject and description) that helps define the action that the activity represents. 
- They can be opened, canceled, or completed. Several substatus values will be associated with the *Completed* status of an activity to clarify how the activity was completed. 
 
Activity tables can be owned only by a user or team. They can't be owned by an organization.

The following default activity tables are available:

- **Appointment**: A commitment representing a time interval that has start/end times and duration.
- **Email**: An activity that's delivered by using email protocols.
- **Fax**: An activity that tracks the call outcome and number of pages for a fax. The activity can optionally store an electronic copy of the document.
- **Letter**: An activity that tracks the delivery of a letter. The activity can store an electronic copy of the letter.
- **Phone Call**: An activity that tracks a telephone call.
- **Recurring Appointment**: The master appointment of a recurring appointment series.
- **Task**: A generic activity representing work that must be done.

### Custom activity tables
You can create new custom activity tables. The metadata values of activity tables differ from the metadata values of other tables. For example, the **Primary** column is set to **Subject**. 

## Business Rules

Business rules provide a simple interface to implement and maintain fast-changing and commonly used rules. The business rules defined for a table apply to both canvas apps and model-driven apps if the table is used in the app.
 
By combining conditions and actions, you can do any of the following with business rules:
- Set column values
- Clear column values
- Set column requirement levels
- Show or hide columns
- Enable or disable columns
- Validate data and show error messages
- Create business recommendations based on business intelligence.

## Differences between canvas and model-driven apps

Model-driven apps can use all actions available on business rules, however not all business rule actions are available for canvas apps at this time. The following actions are not available on Canvas apps:
- Show or hide columns
- Enable or disable columns
- Create business recommendations based on business intelligence.
