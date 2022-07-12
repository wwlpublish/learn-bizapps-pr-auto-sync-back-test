Microsoft Power Apps portals are built on top of Microsoft Dataverse. Power Apps portals extend functionality to internal and external audiences, but this functionality must already be present in a custom Power Apps application by using Dataverse or a Microsoft Dynamics 365 application. For example, if you do not have Dynamics 365 Field Service installed, you will not be able to install the Field Service portal solution.

Conversely, if you have Dynamics 365 Sales installed, you will be able to configure case management functionality in your portal without having to use code. In other words, Power Apps portals are *web enablers* of Power Apps for internal and external audiences.

This architecture comes with a major benefit. All differentiating features of model-driven Power Apps are the features of **Power Apps portals** as well: centralized management, Common Data Model, roles and permissions, forms and views, business rules, declarative workflows and actions, Power Automate flows, plug-in architecture, integration with other services, Dataverse extensibility, audit, and more.

Power Apps portals deliver a complete content management system out of the box, with all content stored in Dataverse, meaning that the content can be edited through the Power Apps portals Studio and directly by using the Portal Management app. Additionally, the Dataverse security model can help you secure content.

## Fit-gap analysis

The following sections examine the various scenarios when portals can be a good fit and others where portals likely wouldn't deliver the same value.

### When to consider portals

Consider using portals in scenarios where you want to:

- Expose Dataverse in a simple, secure web interface. This scenario might include external users (like customers and partners) or internal users that do not require full-featured Power Apps.
- Provide access to simple community forums and self-service knowledge base, and web forms for service requests, cases, or other Dataverse tables.
- Require a website to read, update, and create Dataverse rows in an out-of-the-box, ready to deploy manner.
- Support limited resources and budgets for large-scale web development, business-user, and no-code configuration requirements.
- Create portal content that is accessible across all resolutions, devices, and browsers.
- Provide multilingual implementations to serve audiences of different languages or when you are required to provide multi-language services by law.
- Create and transact selected information from Dataverse to anonymous public access.
- Secure connection to Dataverse to key external stakeholders by using the built-in authentication or external authentication providers such as Azure Active Directory B2C, Facebook, Google, LinkedIn, and more.

### When to exercise caution

When deciding to use portals, you should exercise caution when:

- The majority of data that you want to show on the web resides in an external (non-Dataverse) system.
- Heavy requirements are established around document management, indexing, and searching.
- Commerce requirements include processing a high volume of payments and maintaining an online store.
- The use cases are more appropriate for direct, model-driven, or canvas apps.

## Performance considerations

Power Apps portals do auto-scale as they get more interaction. How much a portal scales depends on how much Dataverse capacity is purchased and assigned to the environment that the portal is placed in. When planning and building a portal, you need to ensure that the implementation is done in a scalable manner by using best practices and tools like solution checker, app checker, portal checker, and so on. It is also important to recognize portal scalability limitations. For example, allowing visitors to upload files without restricting file size or type might have a detrimental effect on the overall portal performance.
