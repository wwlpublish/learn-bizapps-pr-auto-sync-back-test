Congratulations! You're now officially an app creator!

In this unit you'll learn, at a high level, how to manage and maintain your new app. This includes things like app sharing, versions, data sources, connections and also some helpful tips to ensure a successful app rollout.

Let's start off with how to share your app.

## Share the My Expenses app

As the app creator, you're the only person with access to the app until you decide to share it with other users in your organization. Even if any users had the link to the app, without the app being shared with them, they would just see an Access denied type message. For those users you want to share the app with, navigate to the [**Power Apps Home Page**](https://make.powerapps.com/?azure-portal=true), and see below:

> [!div class="mx-imgBorder"]
> [![Demonstration of the My Expenses app functionality.](../media/expenses-app.gif)](../media/expenses-app.gif#lightbox)

> [!NOTE]
> As a new app creator, or even an experienced app creator, before releasing the app to everyone it should go through some kind of UAT plan. This will help catch any potential issues or bugs in the app and get them fixed. Your end-users first impression of the app will be crucial to ensuring a strong user-adoption rate and the overall success of the app.

## App updates and versions

Over time, your app(s) will require updates to be made, maybe you want to add some new functionality, rework existing app functionality or implement new a feature(s) based on Microsoft updates. As you may already be aware, Office 356 and Power Apps are constantly changing. Keeping up with the changes is important so you can determine if you should apply these updates to older apps. Just like a car or truck needs regular servicing and maintenance, so do your apps to ensure that they're performing as expected. So as new features and or controls become available, it doesn't hurt to review any older apps you built before this feature to see if it's worth implementing.

## Data sources and connections

In Power Apps, most canvas apps use external information that is stored in Data Sources. A common example is a table in an Excel file that is stored in OneDrive for Business or SharePoint. Apps access these data sources by using connections. Some connections allow Power Apps to read and write stored data. In Power Apps, you can add many data sources to your apps through built-in or custom connectors. Some of the most popular data sources are shown in the following figure.

> [!div class="mx-imgBorder"]
> [![Screenshot of the list of available Power Apps data sources.](../media/data-sources.png)](../media/data-sources.png#lightbox)

Many data sources are cloud services, like Salesforce. Even Twitter can be a data source if, for example, you're tracking your company's hashtags. Connectors might not seem like the most exciting part of app development; however, they're essential when you work with data that you, your colleagues, and your customers care about. When an app shows up with your data source for the first time, you might suddenly find that they are, in fact, exciting.

For data that's stored on-premises instead of in the cloud, you can use a gateway to provide a reliable connection between Power Apps and your data source. The gateway sits on an on-premises computer and communicates with Power Apps.

An advantage of building your business apps in Power Apps is being able to connect to many data sources in a single app. With the connectors in Power Apps, you can connect to where your data lives. To learn more about data sources in Power Apps, refer to the [Work with data in a Power Apps canvas app](/learn/paths/work-with-data-in-a-canvas-app/?azure-portal=true) learning path.

