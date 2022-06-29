A typical use case of Microsoft Power Apps portals is to extend functionality from Dynamics 365 applications to internal and external audiences. The portal templates that are based on Dynamics 365 apps offer built-in functionality to these audiences by adding features like case life cycle, knowledge article access, partner opportunity management, and so on.

Additionally, Power Apps portals can extend applications that are built on Microsoft Dataverse and then display the data and business logic and make them available on your portal to an external audience, based on user permissions. 

Consider the following scenarios:

- You have extended case management features of Dynamics 365 Customer Service. Your app now handles product warranties, return management authorization (RMA), refunds, and product replacements. You can extend the Customer self-service portal to bring this functionality to your customers, allowing them to register the warranty, make a claim, fill in an RMA form directly on the site, and so on.
- You have built an application in Dataverse to track charitable donations, from both individual and corporate donors, and fundraising campaigns. You can build a portal to allow individuals to donate online and for employers to view and match their employees' donations.
- You use Dataverse to track the progress of your certification programs from the application process, to the evaluation of various skill assessments, to awarding a certification level to a candidate. A Power Apps portal can be configured to allow online applications, provide access to update evaluations, and allow candidates to view their progress.

> [!NOTE]
> A Power Apps portal can only access Dataverse data in the same instance where the portal is provisioned. Connecting to multiple instances and accessing data across the instances or across the tenants is not supported.

Model-driven Power Apps are low-code/no-code methods that you can use to build unique line-of-business applications (see [What are model-driven apps in Power Apps?](/power-apps/maker/model-driven-apps/model-driven-app-overview/?azure-portal=true)). Part of the app creation process is to define the model and UI elements such as views and forms (see [Understand model-driven app components](/power-apps/maker/model-driven-apps/model-driven-app-components/?azure-portal=true)). Power Apps portals extends these UI elements to the web by using table lists, table forms, and web forms:

- **Table lists** - Define how the list of Dataverse records is displayed on the portal pages. They are defined by one or more model-driven app table views and include functionality like filtering and sorting.
- **Table forms** - Add the ability for the portal pages to interact with the records in a specific table by using a model-driven app form definition as a layout template.
- **Web forms** - Render one or more model-driven app forms on a portal website with support for single or multi-step navigation and conditional branching logic.

> [!div class="mx-imgBorder"]
> [![Lists and forms in Model-Driven Apps and Portal](../media/1-list-form-model-portal-c.png)](../media/1-list-form-model-portal-c.png#lightbox)
