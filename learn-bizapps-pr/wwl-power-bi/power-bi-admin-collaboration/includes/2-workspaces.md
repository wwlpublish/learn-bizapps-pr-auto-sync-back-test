Workspaces are places to collaborate with colleagues to create collections of dashboards, reports, datasets, and paginated reports. The new workspace experience helps you better manage access to content. This unit describes the new workspaces, and how they differ from the classic workspaces. As with classic workspaces, you still use them to create and distribute apps.

New, upgraded workspaces can coexist side by side with existing classic workspaces. The new workspace experience is the default workspace type. You can still create and use [classic workspaces](/power-bi/collaborate-share/service-create-workspaces/?azure-portal=true) based on Microsoft 365 groups, if you need to.

## New and classic workspace differences

With the new workspaces, some features have been redesigned. Here are the main differences.

- **Creating the new workspaces doesn't create Microsoft 365 groups** like classic workspaces do. All the new workspace administration is in Power BI, not in Office 365. You can still manage user access to content through Microsoft 365 groups, if you want. You just add a Microsoft 365 group in the workspace access list.

- **Use more granular workspace roles** for more flexible permissions management in the new workspaces. In classic workspaces, you can add only individuals to the members and admin lists.

- **Assign user groups to workspace roles**: In the new workspaces, you can add multiple Active Directory security groups, distribution lists, or Microsoft 365 groups to these roles, for easier user management.

- **Contact list**: In the new workspaces, you can specify who receives notification about workspace activity.

- **Create template apps**: You can only create *template apps* in the new workspaces. Template apps are apps that you can distribute to customers outside of your organization. Those customers can then connect to their own data with your template app. Read more about [template apps](/power-bi/connect-data/service-template-apps-overview/?azure-portal=true).

- **Share datasets**: To share a dataset outside a specific workspace, you need to save the report that contains the dataset to one of the new workspaces. You can't share datasets from classic workspaces. Read more about [shared datasets](/power-bi/connect-data/service-datasets-across-workspaces/?azure-portal=true).

- **Organizational content packs**: You create and consume organizational content packs in classic workspaces. You can't create or consume them in the new workspaces. Apps and template apps replace organizational content packs in the new workspaces. Organizational content packs are being deprecated, so now is a good time to upgrade your content packs to apps. See the workspace upgrade roadmap section of this blog post [Announcing Power BI admins can upgrade classic workspaces](https://powerbi.microsoft.com/blog/announcing-power-bi-admins-can-upgrade-classic-workspaces-and-roadmap-update/?azure-portal=true) for the timeline.

> [!Note]
> As a best practice, you should encourage end-users to use new workspaces. Admins have the option to block classic workspace creation in the Admin portal. Go to **Tenant settings**, then **Workspace settings**, and select **Block classic workspace creation**.
>
> Classic workspaces will really clutter up your PBI tenant.

More details regarding new and classic workspace differences and new capabilities may be found [here](/power-bi/collaborate-share/service-new-workspaces#how-the-new-workspaces-are-different/?azure-portal=true).

## Other workspace improvements

Based on customer feedback requesting a more flexible approach to collaboration in workspaces, certain features have been improved, and new ones have been added. The following is a list of some of these improvements.

- **Licensing enforcement**: Publishing reports to a new workspace experience enforces existing licensing rules. Users collaborating in new workspaces or sharing content to others in the Power BI service need a Power BI Pro license. Users without a Pro license see the error "Only users with Power BI Pro licenses can publish to this workspace."

- **Members can reshare setting**: The Contributor role in the new workspaces replaces the 'Members can reshare' setting in the classic workspaces.

- **Read-only workspaces**: The Viewer role in the new workspaces replaces granting users read-only access to a classic workspace. The Viewer role allows similar read-only access to the content in the new workspaces.

- **Users without a Pro license** can access a new workspace if the workspace is in a Power BI Premium capacity, but only if they have the Viewer role.

- **Allow users to export data**: Even users with the Viewer role in the new workspace can export data if they have Build permission on the datasets in that workspace. Read more about [Build permission for datasets](/power-bi/connect-data/service-datasets-build-permissions/?azure-portal=true).

- No **Leave workspace** button in the new workspaces.

## New features in the improved workspace experience

### Workspace contact list

The contact list feature allows you to specify which users receive notification about issues occurring in the new workspaces. By default, any user or group specified as a workspace admin in the new workspace is notified. You can add to that list. Users or groups in the contact list are also listed in the user interface (UI) of the new workspaces, so workspace end-users know who to contact.

Read about [how to create the workspace contact list](/power-bi/collaborate-share/service-create-the-new-workspaces#create-a-contact-list/?azure-portal=true).

### Workspace OneDrive

Power BI doesn't create a Microsoft 365 group behind the scenes when you create one of the new workspaces. Still, you might find it useful to have a OneDrive associated with the new workspace. With the Workspace OneDrive feature in the new workspaces, you can configure a Microsoft 365 group whose SharePoint Document Library file storage is available to workspace users. You create the group outside of Power BI.

### Roles

Roles let you manage who can do what in the new workspaces, so teams can collaborate. New workspaces allow you to assign roles to individuals, and to user groups: security groups, Microsoft 365 groups, and distribution lists.

To grant access to a new workspace, assign those user groups or individuals to one of the workspace roles:

- Admin
- Member
- Contributor
- Viewer

Everyone in a user group gets the role you've assigned. If someone is in several user groups, they get the highest level of permission provided by the roles they're assigned. If you nest user groups, all the contained users have permission. All of these capabilities, except viewing and interacting, require a Power BI Pro license. Read more about [licensing](/power-bi/collaborate-share/service-new-workspaces?azure-portal=true#licenses) in this article.

## License and administer

### Licenses

If one of the new workspaces is in a shared capacity, everyone you add to it needs a Power BI Pro license. These users can all collaborate on the dashboards and reports in the new workspace. If you want to distribute content to others inside your organization, either assign Power BI Pro licenses to those users or place the workspace in a Power BI Premium capacity.

### Guest users

By default, [Azure AD B2B Guest users](/power-bi/admin/service-admin-azure-ad-b2b/?azure-portal=true) can't access workspaces. Power BI admins can [allow external guest users to edit and manage content in the organization](/power-bi/admin/service-admin-azure-ad-b2b?azure-portal=true#guest-users-who-can-edit-and-manage-content). Enabled Guest users can access workspaces to which they have permission.

### Administer new workspace experience workspaces

Administration for new workspace experience workspaces is in the Power BI admin portal. Power BI admins decide who within an organization can create workspaces and distribute apps. Read about [managing users' ability to create workspaces](/power-bi/admin/service-admin-portal?azure-portal=true#create-the-new-workspaces) in the "Admin portal" article.

Admins can also see the state of all the workspaces in their organization. They can manage, recover, and even delete workspaces. Read about [managing the workspaces themselves](/power-bi/admin/service-admin-portal?azure-portal=true#workspaces) in the "Admin portal" article.
