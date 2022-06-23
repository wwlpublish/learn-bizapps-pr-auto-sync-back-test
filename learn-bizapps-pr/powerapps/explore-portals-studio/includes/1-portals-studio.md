Microsoft Power Apps portals Studio is a WYSIWYG design tool that will allow portal makers to create webpages and content and specify properties of portal components. Portals Studio is accessible from the Power Apps maker portal.

> [!div class="mx-imgBorder"]
> [![Screenshot of Portal Studio design tool homepage.](../media/1-portal-studio-ss.png)](../media/1-portal-studio-ss.png#lightbox)

## Launch portals Studio

You will only have access to the Power Apps portals Studio when you have a portal that is provisioned in your Microsoft Dataverse or Dynamics 365 environment. To access the Power Apps portal Studio:

1. Sign in to [Power Apps](https://make.powerapps.com/?azure-portal=true).
1. Select a target environment by using the environment selector in the upper-right corner.
1. On the left menu, select **Apps**.
1.  Select the target app of type Portal.
1. Select **Edit**

![Screenshot of steps to launch portals studio in makers environment.](../media/launch-portals-studio.png)

This procedure will launch the Studio, where makers can begin creating webpages and adding static and dynamic content to the portal.  

## Portals Studio anatomy

The portals Studio provides the tools that makers can use to modify and add content.

> [!div class="mx-imgBorder"]
> [![Screenshot showing the Portal Studio Anatomy including tools.](../media/1-portal-studio-anatomy-ssm.png)](../media/1-portal-studio-anatomy-ssm.png#lightbox)

| Section | Name | Description |
| ------- | ---- | ----------- |
| 1 | Command bar | Create a new webpage from an existing template<br />Delete webpage components<br />Displays AutoSave status<br />Sync configuration with updates from Dataverse<br />Clear cache and browse to website to view current page<br />Provide feedback |
| 2 | Toolbelt | Navigate the site hierarchy and organize webpages<br />Add components to webpages such as section layouts and content components<br />Enable custom themes and upload custom CSS<br />View and select portal templates to edit<br />Change common portal settings (for example, Table Permissions)<br />Enable and customize progressive web app |
| 3 | Canvas | Workspace to arrange, add, and edit static and dynamic content to a portal webpage |
| 4 | Footer | Provides a hyperlink to open up source code to allow editing of the current webpage |
| 5 | Properties pane | Displays properties of the currently selected webpage or component and allows the setting of specific component properties |

All additions, configurations, and updates that are done through the portals Studio will update portal metadata in Dataverse.

> [!IMPORTANT]
> Portals Studio will automatically save configuration updates to Dataverse as the maker tabs off a specific control. To ensure that all your updates are committed, check the autosave status in the command bar before browsing to preview the website.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4yYtf]
