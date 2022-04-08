Data model developers set up RLS by creating one or more *roles*. A role has a unique name in the model, and it usually includes one or more *rules*. Rules enforce filters on model tables by using Data Analysis Expressions (DAX) filter expressions.

> [!NOTE]
> By default, a data model has no roles. A data model without roles means that users (who have permission to query the data model) have access to all model data.

> [!TIP]
> It's possible to define a role that includes no rules. In this case, the role provides access to all rows of all model tables. This role set up would be suitable for an admin user who is allowed to see all data.

For Power BI Desktop developed models, it's possible to create, validate, and manage roles in Power BI Desktop. For Azure Analysis Services or SQL Server Analysis Services models, it's possible to create, validate, and manage roles by using SQL Server Data Tools (SSDT).

It's also possible to create and manage roles by using SQL Server Management Studio, or by using a third-party tool, like [Tabular Editor](https://tabulareditor.com/?azure-portal=true).

## Apply star schema design principals

The first step to achieve an effective RLS solution is to develop a well-designed model. We recommend you apply [star schema](/power-bi/guidance/star-schema/?azure-portal=true) design principals to produce a model comprising dimension and fact tables. It's common that Power BI enforces rules to filter dimension tables, and [model relationships](/power-bi/transform-model/desktop-relationships-understand/?azure-portal=true) efficiently propagate those filters to fact tables.

The following image is the model diagram of the Tailspin Toys sales analysis data model. It shows a star schema design comprising a single fact table named **Sales**. The other four tables are dimension tables that support the analysis of sales measures by date, state, region, and product. Notice the model relationships connecting all tables. These relationships propagate filters (directly or indirectly) to the **Sales** table.

> [!div class="mx-imgBorder"]
> ![Screenshot of a Power B I Desktop model diagram comprising the tables and relationships as described in the previous paragraph.](../media/tailspin-toys-model-diagram.png)

This model design supports examples presented in this module.

## Define rules

Rule expressions are evaluated within *row context*. Row context means the expression is evaluated for each row using the column values of that row. When the expression returns TRUE, the user can "see" the row.

> [!TIP]
> To learn more about row context, work through the [Add calculated tables and columns to Power BI Desktop models](/learn/modules/dax-power-bi-add-calculated-tables/?azure-portal=true) module. While this module describes adding model calculations, it includes a unit that introduces and describes row context.

You can define rules that are either *static* or *dynamic*.

### Static rules

Static rules use DAX expressions that refer to constants.

Consider the following rule applied to the **Region** table that restricts data access to New England sales.

```dax
'Region'[Region] = "New England"
```

The following steps explain how Power BI enforces the rule. It:

1.  Filters the **Region** table, resulting in one visible row (for New England).
1.  Uses the model relationship to propagate the **Region** table filter to the **State** table, resulting in six visible rows (the New England region comprise six states).
1.  Uses the model relationship to propagate the **State** table filter to the **Sales** table, resulting in thousands of visible rows (the sales facts for the states that belong to the New England region).

The simplest static rule that you can create restricts access to all table rows. Consider the following rule applied to the **Sales Details** table (not depicted in the model diagram).

```dax
FALSE()
```

This rule ensures users can't access any table data. It could be useful when salespeople are allowed to see aggregated sales results (from the **Sales** table) but not order-level details.

Defining static rules is simple and effective. Consider using them when you need to create only a few of them, as might be the case at Tailspin Toys where there are only six regions. However, be aware of some disadvantages: setting up static rules can involve significant effort to create and set up. It would also require you to update and republish the dataset when new regions are onboarded.

If there are many rules to set up and you anticipate new rules will be added in the future, consider using dynamic rules instead.

### Dynamic rules

Dynamic rules use specific DAX functions that return environmental values (as opposed to constants). Environmental values are returned from three specific DAX functions:

-   [USERNAME](/dax/username-function-dax/?azure-portal=true) or [USERPRINCIPALNAME](/dax/userprincipalname-function-dax/?azure-portal=true) - When using the *For your organization* scenario, these functions return a text value describing the authenticated user. When using the *For your customers* scenario, they return a text value that your app passes.

-   [CUSTOMDATA](/dax/customdata-function-dax/?azure-portal=true) - When using the *For your organization* scenario, it returns the **CustomData** property passed in the connection string. When using the *For your customers* scenario, it returns a text value that your app passes.

> [!NOTE]
> Be aware that the USERNAME function returns the user in the format of DOMAIN\username when used in Power BI Desktop. However, when used in the Power BI service, it returns the format of the user's User Principal Name (UPN), like username@tailspintoys.com. Alternatively, you can use the USERPRINCIPALNAME function, which always returns the user in the user principal name format.

Consider a revised model design that now includes the (hidden) **AppUser** table. Each row of the **AppUser** table describes a username and region. A model relationship to the **Region** table propagates filters from the **AppUser** table.

> [!div class="mx-imgBorder"]
> ![Screenshot of a revised model diagram that now includes the AppUser table. This table has two columns: Region and UserName.](../media/appuser-table.png)

The following rule applied to the **AppUser** table restricts data access to the region(s) of the authenticated user.

```dax
'AppUser'[UserName] = USERPRINCIPALNAME()
```

Defining dynamic rules is simple and effective when a model table stores username values. They allow you to enforce a *data-driven* RLS design. For example, when salespeople are added to, or removed from the **AppUser** table (or are assigned to different regions), this design approach just works.

> [!IMPORTANT]
> When using the *For your customers* scenario, the USERNAME and USERPRINCIPALNAME functions don't need to return an actual user name. Instead, your app can pass any text value to filter the model.

## Validate roles

When you create roles, it's important to test them to ensure they apply the correct filters. For data models created in Power BI Desktop, there's the **View as** function that allows you to see the report when different roles are enforced, and different username values are passed.

> [!div class="mx-imgBorder"]
> ![Screenshot of the Power B I Desktop Modeling ribbon. The "View as" command is highlighted.](../media/view-as-command.png)

## Set up role mappings

Role mapping is done differently depending on the embedding scenario.

When using the *For your organization* scenario, role mappings must be set up in advance of users accessing Power BI content. Role mapping involves assigning Azure Active Directory (Azure AD) security objects to roles. Security objects can be user accounts or security groups.

> [!TIP]
> When possible, it's a good practice to map roles to security groups. That way, there will be fewer mappings, and you can delegate the group membership management to the network administrators.

For Power BI Desktop developed models, role mapping is typically done in the Power BI service. For Azure Analysis Services or SQL Server Analysis Services models, role mapping is typically done in SQL Server Management Studio (SSMS).

When using the *For your customers* scenario, role mapping is done by the app at runtime. Your app logic sets one or more *effective identities* to enforce RLS. Setting effective identities is described in unit 4.

For more information about setting up RLS, see:

-   [Row-level security (RLS) with Power BI](/power-bi/enterprise/service-admin-rls/?azure-portal=true)

-   [Row-level security (RLS) guidance in Power BI Desktop](/power-bi/guidance/rls-guidance/?azure-portal=true)
