A Microsoft Power Apps portal that is provisioned in a Microsoft Dataverse environment is composed of three main components:

- Portal solutions
- Portal metadata
- Portal web app

> [!div class="mx-imgBorder"]
> [![Diagram of Portal Architecture with solutions, metadata, and web app components.](../media/1-portal-architecture-c.png)](../media/1-portal-architecture-c.png#lightbox)

A portal requires a Dataverse database to be available in the environment to install and configure its components. A blank website portal can be configured in a Dataverse environment without any of the Microsoft Dynamics 365 apps installed, however many of the templates (Customer self-service, Employee self-service, Partner, and Community portals) have dependencies on Microsoft Dynamics 365 Sales or Dynamics 365 Customer Service.

## Portals solutions

Numerous Dataverse solutions are installed in the environment. These solutions contain a model-driven portal management app, tables, forms, views, and processes to store and manage the portal metadata. Other solutions are installed to enable the functionality of specific templates. Solutions contain several actions, classic workflows, and plug-ins that are deployed to automate the creation of specific portal rows and assist with the management of portal users.

The solutions are installed as part of the portal provisioning process and shouldn't be installed individually.

> [!div class="mx-imgBorder"]
> [![Screenshot of the Power Apps Portal Solutions list.](../media/1-portal-solutions-ss.png)](../media/1-portal-solutions-ss.png#lightbox)

## Portals metadata

Power Apps portal metadata will describe the portal website, webpages, web templates, content snippets, basic and advanced forms, lists, site settings, and other configuration data. The data is stored in Dataverse. A portal maker can add, modify, or delete portal metadata to configure a portal application by using the Power Apps portals Studio or the Portal Management app.

One of the distinctive features of Power Apps portals is using Dataverse as a centralized storage for the information that is required to run the portal website. Everything that portals require to run, including metadata and content, is stored in a Dataverse database, which helps make backing up and transporting portal solutions between the environments easier.

> [!div class="mx-imgBorder"]
> [![Screenshot of the Portal web template metadata.](../media/1-portal-metadata-ss.png)](../media/1-portal-metadata-ss.png#lightbox)

## Portals web app

A Microsoft Azure web app is configured to run the portal site by using the portal solutions and metadata. The web app is automatically configured in the same region as the Dataverse environment. This web app is accessible through a unique URL that is specified during the provisioning process. The web app isn't customizable; however, portal administrators have many configuration options available to them. For example, they can configure the portal web app to capture detailed diagnostics logs for troubleshooting purposes.

> [!div class="mx-imgBorder"]
> [![Screenshot example of the Portals web app.](../media/1-portal-server-ss.png)](../media/1-portal-server-ss.png#lightbox)