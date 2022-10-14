To create or edit calculation groups, you'll need to use an external tool because Power BI Desktop doesn't support this functionality. You can use Tabular Editor, which is an external tool for creating DAX calculation groups. While the latest version, Tabular Editor 3, is commercially available, you can choose to use Tabular Editor 2, which is free.

> [!TIP]
> Apart from creating calculation groups (and other capabilities that aren't supported by Power BI Desktop, such as perspectives and object-level security), you'll receive other benefits from using Tabular Editor as a data modeling tool. For more information, see [Power BI usage scenarios: Advanced data model management](/power-bi/guidance/powerbi-implementation-planning-usage-scenario-advanced-data-model-management/?azure-portal=true).

To download the latest version of Tabular Editor 2, go to [this webpage](https://github.com/TabularEditor/TabularEditor/releases/latest/?azure-portal=true).

Installing Tabular Editor is straightforward. However, before you install the software, be sure to close any open Power BI Desktop windows. When you launch the installer, follow the wizard steps to agree to the license terms (MIT license) and set some basic installation options.

When the installation has completed, open Power BI Desktop and then select the **External Tools** ribbon tab. The **Tabular Editor** tool (and perhaps other tools that you've installed) will appear on this ribbon tab.

> [!div class="mx-imgBorder"]
> [![Screenshot highlighting to select the External Tools in ribbon tab after installation.](../media/external-tool.png)](../media/external-tool.png#lightbox)

Whenever you develop a data model in Power BI Desktop, you can launch Tabular Editor from the ribbon. Then, you can use the Tabular Editor application, which is available in a separate window, to inspect the model design or make changes to it.

> [!IMPORTANT]
> Take care to explicitly save your Tabular Editor work so that changes propagate to the Power BI Desktop file.

In the next unit, you'll have the opportunity to create two calculation groups. If you intend to do so, install Tabular Editor 2 now.