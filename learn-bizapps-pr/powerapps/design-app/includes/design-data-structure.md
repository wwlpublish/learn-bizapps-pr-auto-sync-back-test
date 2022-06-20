> [!VIDEO https://www.microsoft.com/videoplayer/embed/]

We rarely start an application with zero existing data. The first step when it comes to designing your data structure is understanding where is the data that will be used by your app.

Existing data will either be imported into your application, or you'll be integrating your application with an existing system or data source.

## Find and organize the information required

> [!div class="mx-imgBorder"]
> ![Diagram of available data sources.](../media/data.png)

Existing data is typically imported when your application will be replacing an existing solution, whether that is an older application or static data from a Spreadsheet. I personally like to review which data is available and decide how much of it will be required by the application. Perhaps the data you're working with is 10+ years old but users only need access to the last three years' worth of data, this is a good point in time to do some data cleaning before we import it into our environment. It's also a good time to get rid of any duplicate records, inaccurate records, and other data that will be irrelevant to the tasks the users will be completing in the application. Analyze the contents of legacy fields and identify any that are rarely used. If these fields aren't needed in the new system, it may not make sense to migrate data from them.

Cleaning up data won't only surface relevant data to users but it also helps you identify data storage capacity. Exceeding storage capacity is one of the greatest setbacks an enterprise can encounter during the deployment of Power Apps.

Analyzing the existing data also allows you to identify columns or fields to be added to your app. You can come up with a plan describing which origin fields will match which destination fields and how these fields will look after migration.

## Integrate with existing systems and apps your users are already using

> [!div class="mx-imgBorder"]
> ![Diagram of data transformation logic with source data and target data.](../media/data-transformation.png)

Apps created with Power Apps have two ways to integrate to existing data. One is by using a connector, which allows you to connect directly to a data source. The other is by using a dataflow, which copies a snapshot of the data.

-   **Using a connector**: A connector is a feature in Power Apps where you can connect to various systems and sources, such as SharePoint, SQL Server, or Office 365 and directly retrieve data from them or save data to them. For more information, see [Overview of canvas-app connectors for Power Apps](/power-apps/maker/canvas-apps/connections-list/?azure-portal=true).

-   **Using a dataflow**: Dataflow is a feature in Power Apps where you can extract, transform, and load data from another system to Dataverse or Azure Data Lake storage. Unlike a connector, it fetches data in a scheduled batch. Instead of just retrieving the data as-is from the data source, you can use Power Query Online to manipulate, cleanse, and transform data before you store it to the target storage. For more information, see [Self-service data prep with dataflows](/power-apps/maker/data-platform/self-service-data-prep-with-dataflows/?azure-portal=true).

The method you choose depends on your use cases and how data needs to be handled. The following table lists some items to use for comparison.

|      Item to compare         |      Connectors                                     |      Dataflow                                        |
|------------------------------|-----------------------------------------------------|------------------------------------------------------|
|     Freshness of data        |     Real-time                                       |     Static or snapshot                               |
|     Direction                |     Bidirectional                                   |     One direction (from origin to Dataverse)         |
|     Modify existing data?    |     Yes                                             |     No                                               |
|     Example Use cases        |     Production order, Timesheet, Sales quotation    |     Customer master, Past invoices, Employee list    |

Depending on the data that you need to access you may need more technical assistance. When you need to work and integrate with existing enterprise systems such as SAP and Oracle, you should seek cooperation and support from your IT administration team or the team in charge of the system.

For more information regarding the intricacies of working with enterprise systems, see [Working with enterprise systems](/power-apps/guidance/planning/enterprise-systems/?azure-portal=true).
