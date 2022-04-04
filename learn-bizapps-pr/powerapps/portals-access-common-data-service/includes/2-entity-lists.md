The **Table Lists** component allows a maker to display a list of Microsoft Dataverse records on a portal webpage by using configuration only. Table lists are defined by using model-driven app views and can be further configured to filter data based on table permissions. Table lists can have additional features enabled such as running workflows and navigating to show detail records. 

## Create a table list 

A table list can be added as a component to a webpage in Power Apps portals Studio. After placing the list component on a page, the maker will need to set the properties of the table list. Then, the maker will choose the table and one or more model-driven views to be used to render the table list on the page.

> [!div class="mx-imgBorder"]
> [![Screenshot of table list in Portal Studio.](../media/2-entity-list-portal-studio-ss.png)](../media/2-entity-list-portal-studio-ss.png#lightbox)

### List rendering

Adding a list component in portals Studio will add the corresponding Liquid tag to the webpage content.

When the webpage is requested, the list rendering process is as follows:

1. The webpage is retrieved.
1. The webpage will render the table list based on the Liquid tag that was added when the list component was added to a webpage.

    ```twig
    {% include 'table_list' key: '<<Table List Name>>' %}
    ```

## Configure the table list

Power Apps portals Studio provides a basic interface for creating and configuring a table list. Makers can customize all table list features and properties by using the Portal Management app. To access table lists in the Portal Management app:

1. Go to the [Power Apps maker portal](https://make.powerapps.com/?azure-portal=true).
1. Select the target environment by using the environment selector in the upper-right corner.
1. From the **Apps** list, locate and open the Portal Management app (type will be Model-driven).
1. Select **Table Lists** in the left navigation.
1. Open the list that you previously created in portals Studio.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Table List in Portal Management.](../media/2-list-portal-app-ssm.png)](../media/2-list-portal-app-ssm.png#lightbox)

A table list can be as simple or as complicated as your business requirements specify. The only required properties for the table list, other than the name and the website, are the target **Table Name** and one or more **Views**. 

Table lists are highly configurable and have many settings that define the list behavior. Lists can also include actions for the user to interact with the items on the list.

> [!div class="mx-imgBorder"]
> [![Diagram of Table List structure and overview.](../media/2-entity-list-overview-c.png)](../media/2-entity-list-overview-c.png#lightbox)

The following sections explain some of the most common features and settings. 

> [!NOTE]
> Most of the options that add interactive elements, such as buttons, support customization of the elements in multiple languages. For example, if multiple views are enabled, the name for each of the views in the view selector can be customized for each of the enabled portal languages.

### Views

Selected view(s) define the Dataverse table columns, list layout, and the default sort order. 

**Multiple views** - If more than one view has been specified, a drop-down list will be rendered to allow the user to switch between the views. 

**Sorting and pagination** - Sorting is enabled on any of the displayed columns and the page size is configurable.

> [!div class="mx-imgBorder"]
> [![Screenshot of the Entitlement Contacts view and features.](../media/2-entity-list-features-ssm.png)](../media/2-entity-list-features-ssm.png#lightbox)

> [!NOTE]
> Table lists include the **Web Page for Details View** and **Web Page for Create** general properties. These properties are for backward compatibility only. The functionality is included as part of the **View Actions** and **Item Actions** grid configuration.

### Configuration

The following sections describe the different types of configuration that are available in table lists.

#### Filter and search

Table lists provide you with several options to filter and search list data:

**Search** - When quick search is enabled, the portal will render a text search box. It is similar to the quick search feature in model-driven apps. Quick search runs across the view columns and allows you to locate the information within the larger lists by using plain text input. Portal users can use the asterisk wildcard character to search on partial text.

**Portal filters** - The list data can be filtered by the current portal user, the current portal user's parent account, and the current portal website. This feature enables some common scenarios without needing additional configuration:

- List of product reviews that are left by the current user
- List of campus buildings for the current user's department (account)
- List of all draft pages for the current website, only when multiple portals are provisioned 

If the current portal user and current portal user's parent account filters are enabled, the portal will render a drop-down list to allow the user to view their own data (My) or their parent account's data (account name will be displayed).

**Metadata filters** - Records in the list can be filtered on any of the list columns, including ranges, lookups, option sets, and custom FetchXML expressions. Portal users have access to an interactive filtering panel when the table list is rendered.

> [!div class="mx-imgBorder"]
> [![Screenshot of the Table list search and filtering.](../media/2-entity-list-features-filtering-ssm.png)](../media/2-entity-list-features-filtering-ssm.png#lightbox)

#### Display options

Views can be rendered as traditional grid lists, a calendar, or a map. Delivering list content as an OData feed is also supported. 

> [!div class="mx-imgBorder"]
> [![Screenshot of the Table list rendered as a map and calendar.](../media/2-entity-list-map-calendar-ss.png)](../media/2-entity-list-map-calendar-ss.png#lightbox)

Alternative views might require some additional configuration such as start and end date columns for a calendar or latitude and longitude columns for a map.

> [!IMPORTANT]
> Map and calendar views require page templates that can render the view. When a starter portal is provisioned, **Rewrite** page templates like **Page** or **Full Page** support this functionality. Pages that use web templates will render the default table list view.

### Actions

Table lists can have actions associated with them to enable per list commands, like Create and Download (as a Microsoft Excel spreadsheet), or per record commands like View or Edit, and to trigger workflows.

> [!div class="mx-imgBorder"]
> [![Screenshot of Table list commands and views.](../media/2-entity-list-features-commands-ssm.png)](../media/2-entity-list-features-commands-ssm.png#lightbox)

For more information, see [About table lists](/power-apps/maker/portals/configure/entity-lists/?azure-portal=true).

Watch the following video to learn how to configure and display the view on a portal page and add interactive filtering capabilities on an existing Dataverse table.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4ArhG]

Now that you've observed how the table lists are built and rendered, you can learn how portals can display and interact with individual records.
