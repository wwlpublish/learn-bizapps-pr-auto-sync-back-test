You can add a Power BI report or dashboard to a webpage in a Power Apps portal to further extend the portal as a powerful web application.

Before you can add a Power BI report to a Power Apps portal, you'll need to enable the Power BI visualization or the Power BI Embedded service in the Power Apps portals admin center.

> [!div class="mx-imgBorder"]
> [![Screenshot of the admin center Set up Power BI integration with Enable Power BI visualization and Enable Power BI Embedded service features.](../media/enable-power-bi.png)](../media/enable-power-bi.png#lightbox)

- **Power BI visualization** - Allows you to embed *publish to web* Power BI reports for anonymous visitors or share Power BI reports or dashboards to Power BI Azure Active Directory authenticated users (for example, on an Employee self-service portal).
- **Power BI Embedded service** - Allows you to share the Power BI reports or dashboards to external users who don't have a Power BI license or Azure Active Directory authentication setup. This feature uses the *new workspaces* feature of Power BI. For more information, see [Create the new workspaces in Power BI](/power-bi/collaborate-share/service-create-the-new-workspaces/?azure-portal=true)).

## Enable Power BI visualization

Enabling Power BI visualization allows a portal maker to add a Power BI component to a portal page and configure it to display a Power BI report or dashboard that is available for being published on the web. A report author will need to generate an embed code in the Power BI Dashboard.  

From the Power Apps portals Studio, you can add the Power BI component to a portal page. This action will add a Liquid tag to the portal page, which can be further configured in the portals Studio source code editor, depending on your specific requirements.

> [!div class="mx-imgBorder"]
> [![Screenshot of the Portal components with Power BI highlighted.](../media/power-bi-component.png)](../media/power-bi-component.png#lightbox)

### Parameters

The `powerbi` Liquid tag accepts the following parameters:

- **path** - Path of the Power BI report or dashboard. If the Power BI report or dashboard is secure, you must provide the authentication type.

   ```twig
   {% powerbi path:"https://app.powerbi.com/groups/00000000-0000-0000-0000-000000000000/reports/00000000-0000-0000-0000-000000000001/ReportSection01" %}
   ```

- **authentication_type** - Type of authentication that is required for the Power BI report or dashboard. Valid values for this parameter for embedded Power BI visualizations are **anonymous** and **aad** (Azure AD). The default value is **anonymous**. While adding the Power BI report or dashboard, ensure that it's shared with Microsoft Dataverse Azure AD authenticated users.

   ```twig
   {% powerbi authentication_type:"aad" path:"https://app.powerbi.com/groups/00000000-0000-0000-0000-000000000000/reports/00000000-0000-0000-0000-000000000001/ReportSection01" %}
   ```

When the Power BI component inserted into a page is selected, makers can set the values of these parameters using either:

-  Source code editor

  ![Screenshot of settings properties for Power BI embed in code.](../media/source-code.png)

- Property pane

  ![Screenshot of settings properties for Power BI embed in property pane.](../media/property-pane.png)

You can also filter the report on one or more values. For more information, see [Filter a report by using query string parameters in the URL](/power-bi/service-url-filters/?azure-portal=true).

> [!IMPORTANT]
> The anonymous reports do not support filtering.

Filtering can be based on dynamic values, making it a great option to display personalized Power BI visualizations. You can also create a dynamic path and save it into a variable by using the `capture` Liquid tag, as shown in the following example:

```twig
{% capture pbi_path %}https://app.powerbi.com/groups/00000000-0000-0000-0000-000000000000/reports/00000000-0000-0000-0000-000000000001/ReportSection01?filter=Executives/Executive eq '{{user.id}}'{% endcapture %}
{% powerbi authentication_type:"aad" path:pbi_path %}
```

- **tileid** - Displays the specified tile of the dashboard. You must provide the ID of the tile.

   ```twig
   {% powerbi 
      authentication_type:"aad" 
      path:"https://app.powerbi.com/groups/00000000-0000-0000-0000-000000000000/dashboards/00000000-0000-0000-0000-000000000001" 
      tileid:"00000000-0000-0000-0000-000000000002" 
   %}
   ```

You can also select the value for the parameters using property pane.

![Screenshot of setting additional properties for Power BI embed in property pane.](../media/property-pane-embed.png)

Before adding the Power BI report or dashboard to a webpage in a portal, you must share it with the required users.

> [!div class="mx-imgBorder"]
> [![Screenshot example of Power BI chart on a portal page.](../media/power-bi-page.png)](../media/power-bi-page.png#lightbox)

## Enable Power BI Embedded service

You can also enable and configure the Power BI Embedded service within the Power Apps portals admin center.  

When you enable the Power BI Embedded service, make sure that you specify the Power BI workspaces that will be available for use on the portal.

> [!div class="mx-imgBorder"]
> [![Screenshot of the Enable Power BI Embedded service integration window.](../media/power-bi-embedded.png)](../media/power-bi-embedded.png#lightbox)

When the Power BI Embedded service is activated, makers will be able to embed Power BI reports on a portal page, which will take advantage of the features and functionality of the Power BI Embedded service without makers needing to write corresponding code on the portal. You'll need to have created a workspace within Power BI and added the appropriate reports, dashboards, and tiles.

When you're adding an embedded Power BI report, specify if the audience is your customers (external users) or your internal employees. Employees will need to authenticate to the portal by using Azure AD. When you're adding a report for external users, set the value of `authentication_type` to **powerbiembedded**, as shown in the following example:

```twig
{% powerbi authentication_type:"powerbiembedded" path:"https://app.powerbi.com/groups/00000000-0000-0000-0000-000000000000/reports/00000000-0000-0000-0000-000000000001/ReportSection01" %}
```

You can also set the correct authentication type by setting **Access type** to **Embed for your customers** in the property pane. 

> [!div class="mx-imgBorder"]
> [![Screenshot of an organization embedded Power BI report.](../media/organization-embedded-power-bi.png)](../media/organization-embedded-power-bi.png#lightbox)

> [!NOTE]
> Power BI sharing requires appropriate licensing to be in place. Licensing requirements depend on the audience and method of sharing.

For more information on setting up Power BI integration, see [Set up Power BI integration](/power-apps/maker/portals/admin/set-up-power-bi-integration/?azure-portal=true).

For more information on sharing and licensing requirements, see [Share Power BI workspace](/power-bi/service-how-to-collaborate-distribute-dashboards-reports#collaborate-with-coworkers-in-an-app-workspace/?azure-portal=true) and [Share Power BI dashboard and report](/power-bi/service-share-dashboards/?azure-portal=true).
