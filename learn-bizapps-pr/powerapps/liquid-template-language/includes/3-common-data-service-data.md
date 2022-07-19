Portal makers can use HTML to build the output that includes static content. Similarly, makers can use Liquid when working with multiple pages and dynamic content that comes from Microsoft Dataverse and making changes from one page to the next. The Liquid elements act as placeholders, and before the output is sent to the browser, the Liquid elements are replaced by data from Dataverse.

Power Apps portals implement many extensions that are specific to the portals and Dataverse.

Some of the [available Dataverse-specific Liquid objects](/power-apps/maker/portals/liquid/liquid-objects/?azure-portal=true) include:

| Object        | Description                                                  |
| ------------- | ------------------------------------------------------------ |
| `page`        | Refers to the current portal request page. The `page` object provides access to things like the breadcrumbs for the current page, the title or URL of the current page, e.g., `{{ page.title }}`, and any other columns or related tables of the underlying Power Apps row. |
| `user`        | Refers to the current portal user, allowing access to all columns of the underlying Power Apps contact row. If no user is signed in, this variable will be `null`. |
| `website`     | Refers to the portal website, allowing access to all columns of the Power Apps Website (adx_website) row for the portal. |
| Generic&nbsp;tables | A table object provides access to the rows and columns in a Dataverse table. Collection of all tables is referred to as `entities`. For example, `{{ entities.contact[request.params.contactid].firstname }}` refers to the first name column in the contact row identified by `contactid` request parameter. |

[Microsoft Dataverse-specific tags](/power-apps/maker/portals/liquid/portals-entity-tags/?azure-portal=true) are used to load and display Dataverse data, or use other Power Apps portals framework services. These tags are Dataverse-specific extensions to the Liquid language. Some of the tags include:

| Tag     | Description                                                  |
| ------- | ------------------------------------------------------------ |
| `chart` | Adds a Power Apps chart to a web page. For steps to add a Power Apps chart to a web page, see [Add a chart to a web page in portal](/power-apps/maker/portals/configure/add-chart/?azure-portal=true). |
| `powerbi`    | Adds the Power BI dashboards and reports within pages. For steps to add a Power BI report or dashboard to a webpage in portal, see [Add a Power BI report or dashboard to a webpage in portal](/power-apps/maker/portals/admin/add-powerbi-report/?azure-portal=true). |
| `entitylist` | A Liquid block tag that loads a given list, by name or ID. If the list is loaded successfully, the content within the block will be rendered. |
| `entityview` | A Liquid block tag that loads a given Dataverse view, by name or ID. If the view is loaded successfully, the content within the block will be rendered. |
| `fetchxml`   | Allows user to query data from Dataverse, and render the results in a page. |
| `codecomponent` | Allows you to embed code components using a Liquid tag. See [Use Liquid template tag for code components](/power-apps/maker/portals/component-framework-liquid/?azure-portal=true) for more information. |

In the following example, the **Active Currencies** view is being loaded and all returned rows are displayed. In portals Studio, this code produces output because of the implicit design-time privileges of the maker. However, on the portal, the user needs to have Read privileges assigned on the **currency** table for the fragment to return any data.

```php
{% entityview logical_name:'transactioncurrency', name:'Active Currencies' %}
<p>We support {{ entityview.total_records }} currencies.</p>
<ul>
  {% for cur in entityview.records -%}
  <li>{{ cur.currencyname }}</li>
  {% endfor %}
</ul>
{% endentityview %}
```

The output would look like the following example:

> We support 4 currencies.
>
> * Australian dollar
> * Canadian dollar
> * Euro
> * US dollar

By using Liquid in Power Apps portals, you can:

* Add dynamic content directly to webpage content or to a content snippet.

* [Store source content by using web templates](/power-apps/maker/portals/liquid/store-content-web-templates?azure-portal=true), entirely through configuration within Power Apps, for use throughout the Power Apps portals content management system.

* [Render a website header and primary navigation bar](/power-apps/maker/portals/liquid/render-site-header-primary-navigation/?azure-portal=true), entirely through configuration within Power Apps.

* [Use code components](/power-apps/maker/portals/component-framework/?azure-portal=true) built with [Power Apps component framework](/power-apps/developer/component-framework/overview/?azure-portal=true) to provide an enhanced experience for users working with data on forms, views, and dashboards.

In these scenarios, you'll have dynamic access to Power Apps portals features, such as site settings, content snippets, lists and basic forms, and so on.

> [!IMPORTANT]
> Liquid statements are only processed as *output*. Liquid does not have the capacity to extend server-side code that deals with user interactions such as form submissions.
