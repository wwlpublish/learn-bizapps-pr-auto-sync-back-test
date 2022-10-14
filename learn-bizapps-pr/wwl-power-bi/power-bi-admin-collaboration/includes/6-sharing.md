Sharing is the easiest way to give people access to your dashboards and reports in the Power BI service. You can share with people inside or outside your organization.

## Inside the organization

When you share a dashboard or report, the people you share it with can view it and interact with it but can't edit it. They see the same data that you see in the dashboard and reports and get access to the entire underlying dataset unless row-level security (RLS) is applied to the underlying dataset. The coworkers you share with can also share with their coworkers, if you allow them to.

## Outside the organization

The people outside your organization can view and interact with the dashboard or report but can't share it.

Power BI enables sharing content with external guest users through Azure Active Directory Business-to-business (Azure AD B2B). By using Azure AD B2B, your organization enables and governs sharing with external users in a central place. By default, external guests have a consumption-only experience. Additionally, you can allow guest users outside your organization to edit and manage content within your organization.

This article provides a basic introduction to Azure AD B2B in Power BI. For more information, see [Distribute Power BI content to external guest users using Azure Active Directory B2B](/power-bi/guidance/whitepaper-azure-b2b-power-bi/?azure-portal=true).

The option to [allow external guest users to edit and manage content in the organization](/power-bi/admin/service-admin-portal?azure-portal=true#allow-external-guest-users-to-edit-and-manage-content-in-the-organization) lets you give guest users the ability to see and create content in workspaces, including browsing your organization's Power BI. This option can be disabled in Tenant settings, plus content owners can revoke guest access to content.
