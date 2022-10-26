Roles let you manage who can do what in the new workspaces, so teams can collaborate. New workspaces allow you to assign roles to individuals, and to user groups: security groups, Microsoft 365 groups, and distribution lists.

To grant access to a new workspace, assign those user groups or individuals to one of the workspace roles: Admin, Member, Contributor, or Viewer.

- Everyone in a user group gets the role you've assigned.

- If someone is in several user groups, they get the highest level of permission provided by the roles they're assigned.

- If you nest user groups, all the contained users have permission.

All of these capabilities, except viewing and interacting, require a Power BI Pro license. Read more about [licensing](/power-bi/collaborate-share/service-new-workspaces?azure-portal=true#licenses) in this article.

> [!div class="mx-tdCol2BreakAll"]
> | **Role** | **Capabilities or permissions** |
> |---|---|
> | Administrator | Update and delete the workspace. Add or remove people, including other admins. Allow contributors to update the app for the workspace. Everything a member can do. |
> | Member | Add members or others with lower permissions. Publish, unpublish, and change permissions for an app. Update an app. Share an item or share and app.\*\* Allow others to reshare items.** Feature apps on colleagues' Home. Manage dataset permissions.*** |
> | Contributor | Update an app - if allowed.\* Feature dashboards and reports on colleagues' Home. Create, edit, and delete content in the workspace. Publish reports to the workspace, delete content. Create a report in another workspace based on a dataset in the this workspace.\*\* Copy a report.\*\*\* Schedule data refreshes via the on-premises gateway.**** Modify gateway connection. |
> | Viewer | View and interact with an item.***** Read data stored in workspace dataflows. |

\* Contributors can [update the app associated with the workspace](/power-bi/collaborate-share/service-create-the-new-workspaces?azure-portal=true#allow-contributors-to-update-the-app), if the workspace Admin delegates this permission to them. However, they can't publish a new app or change who has permission to it.

** Contributors and Viewers can also share items in a workspace if they have Reshare permissions.

*** To copy a report, and to create a report in another workspace based on a dataset in this workspace, you need [Build permission for the dataset](/power-bi/connect-data/service-datasets-build-permissions/?azure-portal=true). For datasets in this workspace, the people with Admin, Member, and Contributor roles automatically have Build permission through their workspace role.

**** Keep in mind that you also need permissions on the gateway. Those permissions are managed elsewhere, independent of workspace roles and permissions. See [Manage an on-premises gateway](/data-integration/gateway/service-gateway-manage/?azure-portal=true) for details.

***** Even if you don't have a Power BI Pro license, you can view and interact with items in the Power BI service if the items are in a workspace in a Premium capacity.
