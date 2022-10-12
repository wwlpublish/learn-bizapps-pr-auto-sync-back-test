A Microsoft Power Pages site that is provisioned in a Microsoft Dataverse environment is composed of three main components:

- Power Pages solutions
- Power Pages metadata
- Power Pages web app

> [!div class="mx-imgBorder"]
> [![Diagram of Power Pages Architecture with solutions, metadata, and web app components.](../media/1-portal-architecture.png)](../media/1-portal-architecture.png#lightbox)

A Power Pages site requires a Dataverse database to be available in the environment to install and configure its components. A website can be configured in a Dataverse environment without any of the Microsoft Dynamics 365 apps installed, however many of the templates (Customer self-service, Employee self-service, Partner, and Community portals) have dependencies on Microsoft Dynamics 365 Sales or Dynamics 365 Customer Service.

## Power Pages solutions

Numerous Dataverse solutions are installed in the environment. These solutions contain a model-driven portal management app, tables, forms, views, and processes to store and manage the portal metadata. Other solutions are installed to enable the functionality of specific templates. Solutions contain several actions, classic workflows, and plug-ins that are deployed to automate the creation of specific portal rows and assist with the management of portal users.

The solutions are installed as part of the portal provisioning process and shouldn't be installed individually.

> [!div class="mx-imgBorder"]
> [![Screenshot of the Power Pages solutions list.](../media/1-portal-solutions.png)](../media/1-portal-solutions.png#lightbox)

## Portals metadata

Power Pages site metadata will describe the portal website, webpages, web templates, content snippets, basic and advanced forms, lists, site settings, and other configuration data. The data is stored in Dataverse. A portal maker can add, modify, or delete portal metadata to configure a portal application by using the Power Pages design studio or the Portal Management app.

One of the distinctive features of Power Pages is using Dataverse as a centralized storage for the information that is required to run the portal website. Everything that portals require to run, including metadata and content, is stored in a Dataverse database, which helps make backing up and transporting portal solutions between the environments easier.

> [!div class="mx-imgBorder"]
> [![Screenshot of the Portal web template metadata.](../media/1-portal-metadata.png)](../media/1-portal-metadata.png#lightbox)

## Portals web app

A Microsoft Azure web app is configured to run the portal site by using the portal solutions and metadata. The web app is automatically configured in the same region as the Dataverse environment. This web app is accessible through a unique URL that is specified during the provisioning process. The web app isn't customizable; however, portal administrators have many configuration options available to them. For example, they can configure the portal web app to capture detailed diagnostics logs for troubleshooting purposes.

> [!div class="mx-imgBorder"]
> [![Screenshot example of the Portals web app.](../media/1-portal-server.png)](../media/1-portal-server.png#lightbox)