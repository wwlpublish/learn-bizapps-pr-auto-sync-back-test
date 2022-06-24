> [!VIDEO https://www.microsoft.com/videoplayer/embed/]

Solutions are used to transport apps and components from one environment to another or to apply a set of customizations to existing apps. A solution can contain one or more apps and other components such as site maps, tables, processes, web resources, choices, flows, and more.

Solutions are the mechanism for implementing application lifecycle management (ALM) in Power Apps and other Power Platform products, such as Power Automate.

> [!NOTE]
> For detailed information about the solution concepts and how solutions are used for application lifecycle management, see [Overview of ALM with Microsoft Power Platform](/power-platform/alm/overview-alm/?azure-portal=true) in the Power Platform ALM guide.

There are some known limitations when it comes to working with canvas apps, flows, and custom connectors in solutions:

-   Canvas app instant flows must be created from an app already in a solution since adding this type of flow from outside solutions is blocked.

    -   Workaround for this limitation: Remove the trigger, replace with another trigger like recurrence, save the flow, add it into a solution, and then change the trigger as needed.

-   Canvas apps won't display in the classic solution explorer. Use the modern experience. There are no plans for them to be added to classic solution explorer.

-   Flows created from solutions won't be displayed in the **Shared with me** list. They must be accessed through a solution.

-   The [Power Automate mobile app](/power-automate/mobile-manage-flows/?azure-portal=true) doesn't currently support flows created in a solution.

-   The Flow action menu in [Power Apps Mobile](/powerapps/mobile/run-powerapps-on-mobile/?azure-portal=true) and [Dynamics 365 for phones and tablets](/dynamics365/mobile-app/overview/?azure-portal=true) doesn't currently support flows created in a solution.

-   Flows in solutions don't support delegated authentication. For example, access to a flow can't be automatically granted based on having access to the SharePoint list the flow was created from.

-   Custom connectors created outside solutions can't be added to solutions at this time.

-   Canvas apps shared with 'Everyone' that go through environment backup and environment restore operations aren't shared with 'Everyone' in the restored environment. Notice that, the canvas app can be shared with a security group and the app in the restored environment will be shared with that security group.

-   Flows using [connectors](/connectors/connector-reference/?azure-portal=true) that are 'indexed' can't be added into solutions. Indexing isn't supported for solution cloud flows yet. Indexing enables the quick retrieval of those flows to display in a menu or list. Indexed connectors include Power Automate instant (button) flows, Power Apps, Teams, SharePoint, Dynamics 365 Customer Voice, Microsoft Forms, legacy Dataverse connector, Dynamics 365, Excel Online, Microsoft Project, Azure IOT Central V2, and Project Online.

    -   Workarounds for this limitation:

        -   Edit the flow to remove the indexed connector triggers/actions, add it into a solution, and then change it back.

        -   Create a new flow in a solution.

-   Flows triggered from Microsoft 365 applications such as Excel can't see/show cloud flows in solutions since they use indexing.

## Recommended Content

[Solutions overview](/power-apps/maker/data-platform/solutions-overview/?azure-portal=true)

[Create a solution](/power-apps/maker/data-platform/create-solution/?azure-portal=true)

[Export Solutions](/power-apps/maker/data-platform/export-solutions/?azure-portal=true)

[Import Solutions](/power-apps/maker/data-platform/import-update-export-solutions/?azure-portal=true)

[Upgrade or update a solution](/power-apps/maker/data-platform/update-solutions/?azure-portal=true)