When all app users can see all data in Power BI embedded content, there's no need to take special steps. However, when app users should see subsets of model data, it's critical that your solution enforces data permissions.

You typically enforce data permission by setting up models to use RLS. However, when the source data is stored in an Azure SQL Database, and the dataset represents an internal-hosted DirectQuery model, it's possible to leverage RLS set up in the source data. In this case, you need to use token-based identity.

There are many good development practices you should apply to ensure data permissions are enforced accurately and efficiently.

> [!TIP]
> If you're interested in developing an app that embeds Power BI content, see [Power BI Developer in a Day course](https://aka.ms/deviad-online-course/?azure-portal=true). This course includes a self-study kit that guides you through developing an ASP.NET Core MVC app. It explores working with static and dynamic rules.
