A fully functional portal that is based on a template is provisioned in an environment with Microsoft Dataverse enabled. This portal can be further configured to meet specific business requirements.

A maker will first choose a particular portal template. Currently, only blank website option is available for environments without Dynamics 365, while a number of portal templates are available for environments with Dynamics 365 apps installed.

> [!div class="mx-imgBorder"]
> [![Screenshot of the blank website selection.](../media/2-starter-portals-ssm.png)](../media/2-starter-portals-ssm.png#lightbox)

### Portal solutions installation

The provisioning process first begins with the installation of a series of solutions in the environment. All portal implementations will contain base portal solutions with additional functionality added in separate solutions, depending on the portal template chosen. The solutions contain tables, forms, views, processes, and a model-driven Portal Management app that you can use to manage the portal metadata.

### Portal metadata

After the portal solutions have been installed, the process will upload portal metadata records based on the specific portal template chosen. The portal metadata will define the initial configuration for the portal. Each template can be installed only once for each environment; however, multiple portal templates can be installed in a single environment. 

> [!NOTE]
> Currently, only environments with Dynamics 365 enabled may contain multiple portal types.

### Portal web application

An Azure web app will be configured for each portal that is provisioned in an environment. 

### Portal app

The provisioned portal will appear in the **Apps** list of type Portal. From this portal app, a maker will be able to edit (i.e. open portals Studio), browse, share, go to settings, delete, or view details about the portal. 

> [!div class="mx-imgBorder"]
> [![Screenshot of the Portal Apps with ellipsis drop down menu and type noted.](../media/2-portal-app-menu-ssm.png)](../media/2-portal-app-menu-ssm.png#lightbox)

A list of all portals in a Microsoft Power Platform tenant can be viewed from Microsoft Power Platform admin center. 

> [!div class="mx-imgBorder"]
> [![Screenshot of te Microsoft Power Platform Admin Center portals list.](../media/2-power-platform-admin-center-portals-ss.png)](../media/2-power-platform-admin-center-portals-ss.png#lightbox)

The Portal Management app will also appear in the **Apps** list.

### Trial portal

By default, a portal will be provisioned in Trial mode. A maker will have 30 days to convert the portal to production, or it will be automatically suspended and later deleted. See [Power Apps portals lifecycle](/power-apps/maker/portals/admin/portal-lifecycle/?azure-portal=true) for more details.

### Delete portal

If you delete a portal app, it will be removed from the list of apps and the portal web application will be deleted as well. However, neither the portal solutions nor portal metadata will be deleted from Dataverse.

### Existing website records

When a portal app is deleted or when a portal configuration migrated from another environment, website records are not bound to an active website. These records can be used as a starting point to create a new portal that re-uses deleted or migrated portal configuration.

To create the portal using an existing website record, check the box **Use data from existing website record** during the provisioning process, and select the website record that you want to use.

![Screenshot of the option to provision a portal and use data from existing website record.](../media/use-existing-portal.png)

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4yWm3]