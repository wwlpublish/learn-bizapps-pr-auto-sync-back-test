The Microsoft Power Apps portals Studio provides a maker with a tool to update static content and also add pages, components, and themes to a Power Apps portal. However, many aspects of a portal project cannot be added or edited by using the Power Apps portals Studio alone. 

When a Power Apps portal is provisioned, one of the assets that is created on the Microsoft Dataverse environment is the Portal Management model-driven app. The app can also appear as the Dynamics 365 Portals app for environments with the Dynamics 365 app provisioned.

> [!div class="mx-imgBorder"]
> [![Screenshot of Power Apps Portal Management Apps screen.](../media/1-portal-management-app-ss.png)](../media/1-portal-management-app-ss.png#lightbox)

## Launch the Portal Management app

You will have access to the Portal Management app after you have a portal provisioned in your Dataverse or Dynamics 365 environment. To access the Portal Management app:

1. Go to [Power Apps maker portal](https://make.powerapps.com/?azure-portal=true).
1. Select the target environment by using the environment selector in the upper-right corner.
1. From the **Apps** list, locate the Portal Management app (the app Type will be Model-driven).
1. Select the app name to open it.

This process will launch the Portal Management app and will allow makers to access all metadata and data that defines portal content and behavior.  

> [!TIP]
> Because the Portal Management app is a standard model-driven app, you can also open it from the [Dynamics 365 Home page](https://dynamics.microsoft.com/?azure-portal=true).

## App overview

The Portal Management app allows makers to perform advanced configuration actions on the portal by providing direct access to the portal metadata records that define the appearance, language, security, and functionality of a portal.  

The Portal Management app consists of standard model-driven views and forms in which to add and update metadata. Some of the record forms will have specialized controls, such as HTML editors, to allow deeper customization of portal content.

> [!div class="mx-imgBorder"]
> [![Screenshot of the About Footer content snippet H T M L editing.](../media/1-html-editor-content-snippet-ss.png)](../media/1-html-editor-content-snippet-ss.png#lightbox)

The Portal Management app contains the following areas:

- **Website** - Controls various operational aspects of the portal such as site and portal settings, page templates, temporary and permanent redirects within the site, and others.
- **Content** - Provides access to static content that appears on the portal, navigation, and records that control portal access to Dataverse data.
- **Security** - Defines security assets such as web roles and table permissions.
- **Administration** - Includes miscellaneous portal features like portal wizard and integration with traffic analyzers and search engines.

## Portal wizard

The Portal Management app includes a portal wizard that can be used to generate webpages with a table list and a corresponding table form. This tool can be used to quickly build a working portal application over the existing Dataverse data.

> [!div class="mx-imgBorder"]
> [![Screenshot of the Create Portal Content wizard.](../media/1-portal-wizard-ss.png)](../media/1-portal-wizard-ss.png#lightbox)

For more information about how to use the portal wizard, see [Create and expose portal content easily](/dynamics365/portals/create-expose-portal-content/?azure-portal=true).
