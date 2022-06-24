> [!VIDEO https://www.microsoft.com/videoplayer/embed/]

You can also create lists on SharePoint that can be used as data points to track the data needed by the organization in case your design only includes canvas apps. Model-driven apps rely on Dataverse for data storage.

Now remember that sometimes our apps will access data and tables that are already being used, perhaps from another system the organization has been using for some time.

In [Power Apps](https://make.powerapps.com/?azure-portal=true), create a connection to one or more data sources, delete a connection, or update its credentials.

Your canvas app's data connection can connect to SharePoint, SQL Server, Office 365, OneDrive for Business, Salesforce, Excel, and many other [data sources](/power-apps/maker/canvas-apps/connections-list/?azure-portal=true).

There are other kinds of data sources that aren't tables, such as email, calendars, twitter, and notifications.

Using the [Gallery](/power-apps/maker/canvas-apps/controls/control-gallery/?azure-portal=true), [Display form](/power-apps/maker/canvas-apps/controls/control-form-detail/?azure-portal=true), and [Edit form](/power-apps/maker/canvas-apps/controls/control-form-detail/?azure-portal=true) controls, it's easy to create an app that reads and writes data from a data source.

Power Apps includes a powerful set of functions for filtering, sorting, and shaping tables of data in a canvas app: [Filter](/power-apps/maker/canvas-apps/functions/function-filter-lookup/?azure-portal=true), [Sort](/power-apps/maker/canvas-apps/functions/function-sort/?azure-portal=true), and [AddColumns](/power-apps/maker/canvas-apps/functions/function-table-shaping/?azure-portal=true) functions to name just a few. With these functions, you can provide your users with focused access to the information they need. For those with a database background, using these functions is the equivalent of writing a database query.

Remember that one important key to building efficient apps is to minimize the amount of data that must be brought to your device. Perhaps you need only a handful of records from a sea of million, or a single aggregate value can represent thousands of records. Or only the first set of records can be retrieved, and the rest brought in as the user gestures that they want more. Being focused can dramatically reduce the processing power, memory, and network bandwidth that your app needs, resulting in snappier response times for your users, even on phones connected via a cellular network.

*Delegation* is where the expressiveness of Power Apps formulas meets the need to minimize data moving over the network. In short, Power Apps will delegate the processing of data to the data source, rather than moving the data to the app for processing locally.

Work with large data sets requires using data sources and formulas that can be delegated.

Lastly, if the data source you need to access with your Power App that isn't in the cloud, you can install an on-premises data gateway to transfer data quickly and securely between your Power App and your internal data source. You can connect to on-premises data over the [connectors](/connectors/connector-reference/connector-reference-powerapps-connectors/?azure-portal=true) that use data gateway.

## Recommended Content

[Manage connections in canvas apps](/power-apps/maker/canvas-apps/add-manage-connections/?azure-portal=true)

[Understand delegation in a canvas app](/power-apps/maker/canvas-apps/delegation-overview/?azure-portal=true)

[Manage an on-premises data gateway in Power Apps](/power-apps/maker/canvas-apps/gateway-management/?azure-portal=true)
