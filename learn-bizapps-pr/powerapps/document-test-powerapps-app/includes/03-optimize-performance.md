When analyzing performance of Microsoft Dataverse, it is important to understand areas affecting the performance of an app. 

## Environment

By carefully examining various environmental factors you can improve your overall experience with Dataverse apps, even before your business begins to use it.

### Network

Network capacity can greatly affect performance of the apps from the end-user point of view. That includes web apps, Dynamics 365 for Outlook app, and custom applications using Web API.

There are two primary network characteristics affecting the performance: network bandwidth and latency. Collaboration with your network team is essential to making sure that network configuration is adequate and does not affect app performance.

### Client configuration

CDS apps are web-based applications and use web browsers, such as Edge or Chrome, as the user interface to view, add, or edit information that you’ve stored in the apps database. You may need to work with your system administrators to make sure that the client machines and software settings are optimized for performance. 

## App performance

Design of the app itself can greatly affect performance. One of the strengths of Microsoft Power Platform is ability to quickly build robust small apps targeting specific users and specific functionality. Instead of a monolithic app that is more likely to suffer from performance issues you now have the ability to design several separate apps. This separation ensures that each app can be analyzed and tuned independently without too much impact on the others.

Design techniques for individual components may also affect performance of an app.

### Model-driven apps

#### Forms

To improve form performance, design them so that only the information essential for the users is included. If information required depends on the user’s role, consider creating multiple forms instead of one monolithic form that includes every single column. Hiding tabs and sections that are not required to be immediately visible can also improve form responsiveness and performance.

One of the most common sources of performance issues on the forms is custom scripts added by developers. Good collaboration within the team is a key to identify and resolve any performance bottlenecks introduced during the development. 

#### Views

To improve performance of the table views, limit the number of columns displayed only to those required by the business. As often the case, it’s a balance between the responsiveness and bringing enough information to improve usability of the view. 

Customize your views so that they bring back an actionable number of rows. For example, Active Contacts view may contain hundreds of thousands of rows while My Active Contacts will limit that view only to the contacts that are owned by the user. At the same time consider limiting the number of rows per page so that the views return much more quickly.

#### Quick search

Optimizing the quick search view only to include columns that makes sense to search will make a noticeable performance impact on searches within the views. 

![Screenshot showing my active contacts view and search box.](../media/T1_PerformanceTuningandOptimization_image1.png)

When a user searches for rows within a view, Dataverse performs a query that searches only predefined columns. Which columns are searched is defined by the Find Columns settings in the system Quick View.

![Screenshot showing the add find columns window.](../media/T1_PerformanceTuningandOptimization_image2.png) 

The fewer number of columns that are selected, the faster quick search will be. Balance the number of find columns with the effectiveness of the search.

### Canvas apps

The primary source of performance issues in canvas apps are poorly designed data access, excessive or suboptimal formula use, and overly complex user interface.

#### Loading data

Apps will perform poorly when most of the heavy lifting is done on the client and not on the server. Erroneous choice of how to query your data may lead to performance issues. Understanding [delegation](/power-apps/maker/canvas-apps/delegation-overview/?azure-portal=true) in canvas apps is the key to improving you app performance when it comes to data access. Delegation is where the expressiveness of Power Apps formulas meets the need to minimize data moving over the network. In short, Power Apps will delegate the processing of data to the data source, rather than moving the data to the app for processing locally.

Where this becomes complicated, is because not everything that can be expressed in a Power Apps formula can be delegated to every data source. The Power Apps language mimics Excel's formula language, designed with complete and instant access to a full workbook in memory, with a wide variety of numerical and text manipulation functions. As a result, the Power Apps language is far richer than most data sources can support, including powerful database engines such as SQL Server.

Working with large data sets requires using data sources and formulas that can be delegated. It's the only way to keep your app performing well and ensure users can access all the information they need. Take heed of delegation warnings that identify places where delegation isn't possible. If you're working with small data sets (fewer than 500 rows), you can use any data source and formula because the app can process data locally if the formula can't be delegated.

There are some canvas apps features that you would want to consider when optimizing your app start performance by using Concurrent function to load data from multiple sources concurrently. 

#### Controls optimization

Another aspect that can affect performance is the number of screens and controls used in your app. Minimizing the number of controls and reducing complexity of the controls used can help boost your app performance. It will improve the performance while authoring the app as well. There are strategies to optimizing the number of controls used in your app. For example, you can use a gallery control instead of a Canvas/Data Cards when the data displayed is uniform or vary only slightly. Gallery can be powerful in reducing complexity, making your app easier to maintain.

There are other optimizations techniques available, make sure that canvas apps developers familiarize themselves with [detailed documentation](/power-apps/maker/canvas-apps/performance-tips/?azure-portal=true).

### Workflows 

Real-time workflows can be very effective but, if designed poorly, will affect the performance of the most common operations such as creating or updating a row. Consider converting poorly performing or long running workflows to background ones where the impact on the system will be smaller.

Background workflows create a log row when an instance of the workflow is executed. The default setting is to delete log entries for successfully executed workflows. If this setting is changed to keep the entries, jobs log will grow and may reach the point where it affects performance of the asynchronous services. Only use this flag for troubleshooting and avoid leaving it on in production.

### Plugins

Custom extensions such as plugins are the common source of the performance issues. Work with developers to identify and resolve those.

