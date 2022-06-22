Performance is a critical component to any mobile-optimized canvas app due to the limitations with multitasking in a mobile device versus a desktop application.

Though you can optimize a canvas app in many ways, keep in mind the following major considerations:

- Selecting and optimizing your data source

- Calling data within the app

- Monitoring the performance of your app to identify performance bottlenecks

## Select and optimize your data source

When you create a canvas app, you'll likely already have a data source that you're building your new canvas app around. Depending on the data source, optimizations are available that you can apply.

When data is retrieved to and from a connector, the connector uses the OData protocol. Depending on the data source, the data request could pass through several locations before it returns to the canvas app. For example, if the data is located within an on-premises SQL server, the data needs to go through more touchpoints, such as a data gateway, than if the data was located in a Microsoft Azure SQL instance. As another example, if the data is connecting to a non-Microsoft, external data source in the cloud that would have more connections than if you were connecting to data in a Microsoft Dataverse environment by using the Dataverse connector.

## Call data within the app

When calling data within your app, you should consider the data that you're recalling and how many records are being returned. For instance, if you have multiple tables with joins in a single form, the performance will be longer than if you're pulling back a single table.

Instead, consider creating a form for each data source and filtering the subsequent forms by the selected record. For example, instead of showing all customers with their sales orders on a single form, you can create a single form that shows all customers. Then, you can filter by sales orders for that customer on the next screen. Though the former example would work for a tablet or desktop, it wouldn't work for a phone due to the form complexity and performance overhead.

## Monitor app performance to identify bottlenecks

In the next unit, you'll learn how to monitor the performance of a canvas app to identify performance bottlenecks.
