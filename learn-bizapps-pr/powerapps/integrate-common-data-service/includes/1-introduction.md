You can add lists to webpages by using Microsoft Power Apps portals Studio, where you can configure some of the main properties. Additional configuration options are available by using the Portal Management app.

## Create list

Portals Studio provides a maker experience for creating and configuring lists. To create lists in the Power Apps portal Studio, use the following procedure:

1. Sign in to [Power Apps](https://make.powerapps.com/?azure-portal=true).

1. Select a target environment by using the environment selector in the upper-right corner.

1. On the left menu, select **Apps**.

1. From the **Apps** list, locate the portal app (the app Type will be Portal).

1. Select the ellipsis (...) and then select **Edit**. The portals Studio will launch.

1. From the command bar, select **+ New Page > Blank** template.

1. On the page canvas, select column content.

1. On the toolbelt, select **Components (+)**, then select **List**.

   ![Screenshot of insert list component.](../media/list-component-insert.png)

1. Enter the following in the properties panel:

   - Select **Create new**.

   - Enter **Suppliers** as **Name**.

   - Select **Account (account)** as **Table.**

   - Select **Active Accounts** as **View.**

   ![Screenshot of list properties panel.](../media/list-properties.png)

> [!IMPORTANT]
> We have not configured table permissions. If you try to browse the page now, you will receive a "You don't have permissions to view these records." message. This is expected.

As the page auto-saves and refreshes, the list layout will be displayed directly on portals Studio canvas.

![WYSIWYG list layout on canvas in portals Studio](../media/list-layout.png)

## Configure list

Portals Studio also provides an interface for managing lists; however, not everything can be configured in portals Studio. Makers can customize all list features and properties by using the Portal Management app. To access lists in the Portal Management app, use the following procedure:

1. Sign in to [Power Apps](https://make.powerapps.com/?azure-portal=true).

1. Select a target environment by using the environment selector in the upper-right corner.

1. On the left menu, select **Apps**.

1. From the **Apps** list, locate the **Portal Management** app (the app Type will be Model-driven).

1. Select the app name to open it.

1. In the left navigation, select **Lists**.

1. Open the list that was previously created in portals Studio.

> [!div class="mx-imgBorder"]
> [![Screenshot of the New list in Portal Management.](../media/list-portal-app.png)](../media/list-portal-app.png#lightbox)

A list can be as simple or as complicated as your business requirements specify. To begin, the only required properties for the list, other than the name and the website, are the target **Table Name** and one or more **Views**.

Lists are highly configurable and have several settings that define the list behavior. Lists can also include actions for the user to interact with the items on the list.

> [!div class="mx-imgBorder"]
> [![Diagram of list structure and overview.](../media/entity-list-overview.png)](../media/entity-list-overview.png#lightbox)

The following sections describe some of the most common features and settings.

> [!NOTE]
> Most of the options that add interactive elements, such as buttons, support customization of the elements in multiple languages. For example, if multiple views are enabled, the name for each of the views in the view selector can be customized for each of the enabled portal languages.

### Views

Selected views define the Microsoft Dataverse table columns, list layout, and the default sort order.

- **Multiple views** - If more than one view is specified, a drop-down list renders to allow the user to switch between the views.

- **Sorting and pagination** - Sorting is enabled on any of the displayed columns, and the page size is configurable.

> [!div class="mx-imgBorder"]
> [![Screenshot of the Entitlement Contacts view and features.](../media/entity-list-features.png)](../media/entity-list-features.png#lightbox)

> [!NOTE]
> Lists include the **Web Page for Details View** and **Web Page for Create** general properties. These properties are for backward compatibility only. The functionality is included as part of the **View Actions** and **Item Actions** grid configuration.

### Configuration

You can configure list data by using filtering and searching or by selecting various display options.

#### Filtering and searching

Filtering and searching functionalities help you configure the data in the following ways:

- **Search** - When Quick Search is enabled, the portal renders a text search box. It is similar to the Quick Search feature in model-driven apps. Quick Search runs across the view columns and lets users locate information within larger lists by using plain text input. Portal users can enter the asterisk wildcard character to search for partial text.

- **Portal filters** - List data can be filtered by the current portal user, the current portal user's parent account, and the current portal website. This feature enables some common scenarios by using configuration only, without the need for additional development:

  - List of product reviews that are left by the current user.

  - List of the buildings on the campus for the department (account) of the current user.

  - List of all draft pages for the current website when multiple portals are provisioned.

If both the current portal user and the current portal user's parent account filters are enabled, the portal renders a drop-down menu, which allows the user to view their own data (My) or their parent account's data (account name is displayed).

- **Metadata filters** - This feature is also configuration-only. Rows in the list can be filtered on any of the list columns, including ranges, lookups, choices, and custom FetchXml expressions. Portal users have access to the interactive filtering panel when the list is rendered.

> [!div class="mx-imgBorder"]
> [![Screenshot of the list search and filtering features.](../media/entity-list-features-filtering.png)](../media/entity-list-features-filtering.png#lightbox)

#### Display options

Views can render as traditional grid lists, calendars, or maps.

> [!div class="mx-imgBorder"]
> [![Screenshot of the list rendered as a map and calendar.](../media/entity-list-map-calendar.png)](../media/entity-list-map-calendar.png#lightbox)

Alternative views might require additional configuration, such as start and end date columns for a calendar or latitude and longitude columns for a map.

> [!IMPORTANT]
> Maps and calendars require page templates that can render the view. When a starter portal is provisioned, **Rewrite** page templates like **Page** or **Full Page** support this functionality. Pages that use web templates will render the default list view.

### Actions

Lists can have actions associated with them to enable commands for each list, such as **Create** and **Download** (as a Microsoft Excel spreadsheet), or commands for each row, such as **View** or **Edit**, and to trigger workflows.

> [!div class="mx-imgBorder"]
> [![Screenshot of the list features and commands.](../media/entity-list-features-commands.png)](../media/entity-list-features-commands.png#lightbox)

For more detailed information about list attributes and relationships and how to use them to configure list behavior, see [About lists](/power-apps/maker/portals/configure/entity-lists/?azure-portal=true).
