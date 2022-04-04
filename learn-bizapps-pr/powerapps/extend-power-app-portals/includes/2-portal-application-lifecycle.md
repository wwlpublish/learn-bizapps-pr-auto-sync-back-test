## Development life cycle

Application lifecycle management (ALM) is important as the applications that your organization builds become more complex and as more of your company depends on their stability.

If you create a model-driven Power App, a Power Automate flow, or any other object to build a business solution on a Microsoft Dataverse environment, you would typically contain these assets in a *solution* and export the single solution file from one environment to another. The solution file can also be *unpacked* into discreet file components and uploaded to a source control system (such as Microsoft Azure DevOps) that will maintain a repository of the solution and track the various changes. Many tools are provided by Microsoft and the community to automate the ALM process. 

For more information, see [Application lifecycle management (ALM) with Microsoft Power Platform](/power-platform/alm/?azure-portal=true).

## Portal metadata

Power Apps portals configuration is stored directly within Dataverse as records known as *portal metadata*. When you provision a Power Apps portal, the portal template that you choose will populate a number of portal-specific Dataverse entities with data that describe the website structure, webpages, content, table list configuration, table form configuration, and so on. As you configure the portal by using Power Apps portals Studio or other tools, you are changing or adding to the portal metadata.

> [!div class="mx-imgBorder"]
> [![Screenshot of the Portal Metadata with portal-specific Dataverse entities with data.](../media/portal-meta-data.png)](../media/portal-meta-data.png#lightbox)

Portal metadata can't be added to a Dataverse solution file. The challenge is how to move the portal metadata records from one environment to another. While model-driven Power Apps have built-in features to export and import data, these features work for a single table and must be sequenced based on data relationships.  

Portal metadata is stored in over 50 interconnected, unique entities. In addition, functionality is built into the portal solutions that will be triggered as records are created. For example, as a webpage record is added to the portal, a corresponding webpage record will be created for each provisioned language. Using an import tool might inadvertently duplicate webpage records.

You can move portal metadata from one environment to another by using tools that are available from the community and Microsoft.

### Configuration Migration tool

The **Configuration Migration** tool is an application that can be run as a Windows desktop application or invoked as a PowerShell cmdlet. The tool can export and import a set of Dataverse records and maintain the table relationships.  

> [!div class="mx-imgBorder"]
> [![Screenshot of the Configuration Migration Tool.](../media/configuration-migration-tool.png)](../media/configuration-migration-tool.png#lightbox)

> [!NOTE]
> The **Configuration Migration** tool is designed for smaller datasets (specifically configuration data, such as portal metadata) and is not suited for high-volume data migrations or integrations.

The **Configuration Migration** tool will use a schema file to determine which Dataverse entities to export to a data file. Microsoft has a predefined schema file for each of the portal templates to identify the specific portal metadata Dataverse entities.

After you have set up your Power Apps portal configuration, you can run the **Configuration Migration** tool to export your portal metadata to an XML file by using the schema that corresponds to your portal template.

Ideally, the portal metadata file should be uploaded to a source control repository, where the changes can be tracked and used to deploy to other environments.

You will also need to deploy any configurations that are made to Dataverse, such as new entities and model-driven forms and views that are used by portal table lists and table forms. You would move this configuration by using *solutions*. For more information, see [Solutions Overview](/power-apps/maker/common-data-service/solutions-overview/?azure-portal=true).

On your destination environment, you can then run the **Configuration Migration** tool to import the portal metadata file to update the portal configuration.

> [!CAUTION]
> Using the **Configuration Migration** tool will move over all and overwrite existing portal metadata. Situations might occur where content is specific to the environment (for example, hyperlinks to specific URLs). After the data has been migrated, you might need to update some content directly in the destination portal.

For more information, see [Migrate portal configuration](/power-apps/maker/portals/admin/migrate-portal-configuration/?azure-portal=true).
