Do you have inefficient or legacy business processes that you would like to modernize? Are you still moving information around using paper or even a shared Excel workbook? Do you want to be able to perform these business processes from different devices like PCs or mobile phones? Then you need Power Apps.

Power Apps is a no-code/low-code platform for building apps that builds off of concepts similar to formulas in an Excel workbook such as SUM and TEXT. You can use Power Apps to build simple solutions like vehicle inspection forms and status reports or complex business solutions for purchasing processes and inventory management. If you can envision an app to solve a business problem, then you can use your existing skills to build it. Although this module is geared towards business users with little background in computer science and coding, Power Apps offers advanced functionality and the ability for seasoned developers to design complex applications with ease.

## Work with your data where it lives

When modernizing a paper-based process, there are likely systems in your organization with data you can leverage. With Power Apps, you have choices. With over 275 connectors you can easily connect to data, using the underlying data service and app platform, Microsoft Dataverse, or a multitude of online and on-premises data sources. Some common data sources include:

- Dataverse

- SharePoint

- Dynamics 365

- SQL Server and Azure SQL

- Office 365

You don't have to choose just one data source. Power Apps easily supports multiple data connections allowing you to bring data together from many platforms into a single app.

## Different types of Power Apps for different scenarios

Power Apps can create three types of apps: canvas, model-driven, and portals. Each is suited to different scenarios and end users.

### Canvas apps

Canvas apps are a great option when you want to build an app from a blank canvas. You start by choosing the screen size: tablet or mobile, then you have a blank screen from which to build. You can interact with data in your app by adding data sources. Drag and drop various controls and add the desired functionality by writing Excel style formulas. Canvas apps provide you complete flexibility when building your apps. 

Below are a couple of examples of a mobile canvas app built by Heathrow Airport.  
    ![Power Apps mobile display for Heathrow Airport Application](../media/mobile-canvas-apps.png)

### Model-driven apps

Model-driven apps build from data in Microsoft Dataverse. Power Apps will build you a great looking, fully functional app to act upon and interact with this data. With model-driven apps, there is no need to worry about choosing the app size; it is responsive, meaning it works on mobile or tablet with no extra work by you. You define the relationships, forms, views, business rules, and more at the data layer, inside of the Dataverse, giving you enough control to get your business result without writing all of the formulas yourself. 

Below is an example of a fundraiser donations tracking model-driven app.  
    ![Power Apps Dashboard](../media/fundraiser.png)

### Portals

Portals bring the power of no-code solutions to building externally facing websites. Through the Power Apps interface, you can build an anonymous or authenticated website that allows users to interact with data held in Dataverse. The same drag and drop experience you enjoy when building apps is available to build these rich, interactive websites.

![External view of portal](../media/portal.png)

## Add artificial intelligence to your app with no code

Prior to Power Apps, adding functionality such as image recognition or prediction models required advanced computer knowledge. There was code to write, data models to design and train, and a whole lot of complicated logic. Power Apps has "democratized" artificial intelligence by providing a wizard-based interface for building and training your model. This unlocks the power of Azure Machine Learning and Cognitive services without writing a single line of code or creating complex machine learning models.

A ready to use AI component is the Business card reader. This component reviews an uploaded photo or picture taken to determine if it is a business card and subsequently extracts the relevant information. No configuration required.

The business card reader is simply one ready-made example which builds off of the underlying AI components which you can deploy in other ways by first building a model. From [https://make.PowerApps.com](https://make.PowerApps.com), a wizard guides you through building and training the model. Currently, there are four available AI models in Power Apps:

- Prediction - This model predicts whether something will happen or not based on previous data history. More details in the following section.

- Form processor - This model extracts text from an image like the business card reader. 

- Object detector - This model identifies objects from an uploaded image or taken photo and then provides a count of the number of objects present.

- Text classification - This model categorizes text by its meaning, making it is easier to analyze. 

### The prediction model

The AI Builder prediction model allows you to create a model that can predict yes or no outcomes based on historical data. You train the model by providing historical data that includes the yes/no outcome and then artificial intelligence does the rest. 

You can build prediction models to solve business problems such as:

- Will a lead become a customer?

- Will a project be profitable?

- Will a customer churn based on activity?

As you can see, AI can help you answer powerful business questions without writing a single line of code. 

## Security and Administration

There are many tools for those in IT or otherwise responsible for governance. Power Apps has a multitude of security, governance, and reporting capabilities to let you manage Power Apps. Also, Power Apps doesn't circumvent security in any way. Users cannot build apps to bypass current access permissions. To manage security for Power Apps, you can access [https://admin.powerplatform.microsoft.com/](https://admin.powerplatform.microsoft.com/). Here you will find options for creating and managing environments, monitoring licenses, working with Data Loss Prevention policies and managing Dataverse Data Integration projects. This allows you to manage the Power Apps throughout your tenant from one single place.

Power Apps also has its own set of PowerShell cmdlets for app creators, administrators, and developers that allow you to automate many of your administrative duties. A common use case of the PowerShell cmdlets is to automate the discovery and permission management of all apps in your tenant, allowing you to better understand and manage apps as they are created and spread throughout your company.

In addition, in the Power Automate module, you will see that Power Automate has the ability to automate these tasks. You can download the [Center of Excellence](https://aka.ms/CoEStarterKitDownload) starter kit, a collection of components or tools that are designed to help get started with developing a strategy for adopting and supporting Microsoft Power Platform, with a focus on Power Apps and Power Automate.

## Driving business value

By now you understand that Power Apps does not require traditional "code" like C#, making  a low technology barrier to entry. If you know your business process, you can get started writing your first app. For many businesses, this means apps are not coming from IT but instead directly from frontline business users. The same way Finance builds their own Excel workbooks today, they can build their own Power Apps. 

Power Apps allows even the most entry level users to reduce paperwork, increase process efficiency, and ensure a single source of truth by combining multiple data sources into one app. Users can build apps with ease, while staying within the guardrails set by IT. This allows for an unprecedented amount of innovation and digitization, eliminating the app backlog, cumbersome paper-based processes and more.

In the next unit, you learn about how Heathrow Airport has built 30 apps that have eliminated 75,000 pages of paperwork, reduced data entry by nearly 1,000 hours, and saved the airport hundreds of thousands of dollars.

