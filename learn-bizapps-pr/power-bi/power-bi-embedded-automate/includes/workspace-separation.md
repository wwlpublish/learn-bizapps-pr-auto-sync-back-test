Multiple organizations can use a *multi-tenancy app*, where each organization is a tenant. A multi-tenancy app that embeds Power BI analytics will use the *For your customers* scenario because the app users comprise external users. When designing a multi-tenancy app, you can choose from two different tenancy models.

The recommended approach is to use the *workspace separation* model. It's achieved by creating one Power BI workspace per tenant. Each workspace contains Power BI artifacts specific to that tenant, and the datasets connect to a separate database per tenant.

Alternatively, there's the single *multi-customer database* model. Using this model, your solution achieves separation with a single workspace comprising a set of Power BI artifacts that are shared across all tenants. RLS roles, which are defined in the datasets, securely filter the data to ensure organizations only ever see their data.

> [!NOTE]
> To learn more about enforcing RLS, work through the Enforce data permissions for Power BI embedded analytics module.
>
>To learn more about multi-tenancy solutions, including a comparison of a separate database for each customer to a multi-customer database, see [Service principal profiles in Power BI Embedded](/power-bi/developer/embedded/embed-multi-tenancy/?azure-portal=true).

When using the workspace separation model, start by creating a *golden workspace*. A golden workspace is a template workspace that contains default Power BI artifacts, including datasets, reports, and dashboards. Each time a new tenant is onboarded, an automation solution replicates the golden workspace content to a new workspace.

The automation solution can use the following steps to onboard a new tenant:

1.  Use Microsoft Graph to create a service principal.
1.  Use the Power BI REST API to add the service principal as a contributor to the golden workspace.
1.  Using the new service principal, use the Power BI REST API to:
    1.  Create a workspace for the new tenant.
    1.  Replicate the golden workspace content to the new workspace.
    1.  Update the dataset connections to connect to the tenant data.
    1.  Assign the new workspace to a capacity.

> [!NOTE]
> It isn't necessary to create a new service principal for each tenant. However, we recommend creating a service principal profile for each tenant workspace to achieve the highest possible isolation. For more information, see  [Service principal profiles in Power BI Embedded](/power-bi/developer/embedded/embed-multi-tenancy/?azure-portal=true).

To gain a better understanding of how to automate workspace separation, watch the following video.

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4VozD]
