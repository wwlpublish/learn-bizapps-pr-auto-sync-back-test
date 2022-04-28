In this exercise, you'll be completing the following tasks:

- Configure mandatory Power Automate connections for IOM

- Enable Bing Maps integration

- Enable Timeline feature

## Task 1: Configure system connections

1. Open an In-Private or Incognito window in your browser and navigate to [Power Apps](https://make.powerapps.com/?azure-portal=true).

1. Ensure you choose the correct environment from the upper right **Environment** drop-down is selected.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the selected environment.](../media/environment.png)

1. Select **Apps** on the left navigation bar.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the Power Apps navigation bar with Apps selected.](../media/apps.png)

1. Select **Intelligent Order Management**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the intelligent order management app selected in the apps list.](../media/intelligent-order-management.png)](../media-intelligent-order-management.png#lightbox)

1. Select **Get Started** button on the welcome screen in **IOM**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the welcome screen with the get started button.](../media/get-started.png)](../media/get-started.png#lightbox)

1. On the Intelligent Order Management screen, select **Getting Started** in the left navigation pane and select **Manage** on **Configure settings** to configure connections required by IOM.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Dynamics 365 Intelligent Order Management Getting started page.](../media/manage.png)](../media/manage.png#lightbox)

1. You should see a list of System Connection References. These are used by IOM to communicate with Dataverse, Power Automate and IOM Data Transformer. The general configuration process for each system connection is the same. Administrator privileges are required to configure these system connections.

1. Select **IOM Data Transformer** record.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the System connection references with I O M data transformer record selected.](../media/system.png)

1. Select **Retrieve Link**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the I O M Data Transformer page with the Retrieve link button highlighted.](../media/transformer.png)](../media/transformer.png#lightbox)

1. It will open up **Power Automate** portal. If you're opening **Power Automate** for the first time, then you'll see a welcome screen.

    > [!Important]
    > Select **United States** as your country/region and then select the **Get started** button for this lab.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the Welcome to Power Automate screen with country set to U S.](../media/welcome.png)

1. Ensure the correct environment from the upper right **Environment** drop-down is selected.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the environment selected in Power Automate.](../media/environment-2.png)

1. On the left pane, select **Data** > **Connections**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the Connections option, again.](../media/connections.png)

1. Select **New Connection**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the New connection button.](../media/new-connection.png)

1. Search for **IOM Data Transformer** in the search bar located in the top right edge and then select **IOM Data Transformer** to add the connection.

    > [!Note]
    > In case you do not find the connection, close this browser tab and repeat the steps from Step 9.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the connection search results for I O M Data Transformer.](../media/iom-data.png)](../media/iom-data.png#lightbox)

1. Select the '+' button to add the connection.

1. Select the **Create** button on the dialog box.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the I O M Data Transformer dialog showing the Create button.](../media/create-transformer.png)

1. This connector will prompt for credentials. These account and connection details will be used by the IOM Data Transformer connector in the IOM Power Automate flows to transform data using Power Query online API for IOM application. For this task, you can use your In A Day user account (credentials that you're using to sign in to [Power Apps](https://make.powerapps.com/?azure-portal=true)) to establish the connection however in a customer's environment, make sure to use a dedicated service account instead of a user's account.

1. Once the connection has been established, select ... on the connection and then select **Details**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the ellipsis icon selected to reveal the Details option.](../media/details.png)](../media/details.png#lightbox)

1. On the **Details** page, copy the **URL** from browser's address bar.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Power Automate Connections page in a browser with the U R L highlighted.](../media/url.png)](../media/url.png#lightbox)

1. Navigate to the Dynamics 365 IOM application tab page in your browser and paste the URL into the **Connection URL** field for **IOM Data Transformer** record and then select **Save & Close** on the command bar.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Intelligent Order Management sandbox I O M Data Transformer connections with the Connection U R L highlighted.](../media/connection-url.png)](../media/connection-url.png#lightbox)

1. Navigate back to **Power Automate** tab page on your browser and on the left pane, select **Data** > **Connections**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the Power Automate navigation pane with Connections highlighted.](../media/connections.png)

1. Select **New Connection**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the new connection button again.](../media/new-connection.png)

1. Search for **Microsoft Dataverse** in the search bar located in the top right edge and then select **+** to add the connection.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the search results for Dataverse with the plus icon next to Microsoft Dataverse selected.](../media/dataverse.png)](../media/dataverse.png#lightbox)

1. Select the **Create** button on the dialog box.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the Microsoft Dataverse dialog with the create button highlighted.](../media/create-dataverse.png)

1. This connector will prompt for credentials. The Microsoft Dataverse connector uses these account and connection details in the IOM Power Automate flows to perform CRUD operations on this environment's database. For this task, you can use your user account (credentials that you use to sign in to [Power Apps](https://make.powerapps.com/?azure-portal=true)) to establish the connection. However, in a customer's environment, use a dedicated service account instead of a user's account.

1. Once the connection has been established, select ... on the connection and then select **Details**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the list of connections with the ellipsis button next to the dataverse connection selected to reveal the details option.](../media/dataverse-details.png)](../media/dataverse-details.png#lightbox)

1. On the **Details** page, copy the **URL** from the browser's address bar. Save this URL in your OneNote or Notepad as you'll need to paste the URL in the next step and in the next exercise.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the power automate dataverse connection page with the U R L highlighted.](../media/dataverse-url.png)](../media/dataverse-url.png#lightbox)

1. Navigate to the Dynamics 365 IOM application tab page in your browser and paste the same URL into the **Connection URL** field on **Microsoft Dataverse**, **Microsoft Dataverse - Application** and **Microsoft Dataverse - Integration** System Connection References records.

    When you're done, you'll see the System Connection References complete except for **Power Automate Management**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the System Connection References list with Microsoft Dataverse and others showing status reason Active, and Power Automate Management showing status reason Incomplete.](../media/system-connection.png)

1. Navigate to Power Automate tab page in your browser and repeat steps similar to steps 20-27 to add **Power Automate Management** connection in Power Automate. Leave the Authentication type to "First Party" and select **Create**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Power Automate Management dialog with authentication type set to first party.](../media/power-automate-management.png)](../media/power-automate-management.png#lightbox)

1. A new window prompt will ask for credentials. These account/connection details will be used by the Power Automate management connector. For this task, you can use your In A Day user account (credentials that you're using to sign in to [Power Apps](https://make.powerapps.com/?azure-portal=true)) to establish the connection however in a customer's environment, make sure to use a dedicated service account instead of a user's account.

1. Finally, paste its connection url in **Power Automate Management** record in Dynamics 365 IOM.

1. Navigate to Dynamics 365 IOM page and once the **status reason** for all the listed **Connection References** are in **active** state, select **Activate System** on the command bar.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the System Connection References list with the Activate System button highlighted.](../media/activate-system.png)](../media/activate-system.png#lightbox)

1. It takes about 5 minutes to activate all system connections. You should see the following message on the screen while connections are being activated.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the message Activating system connection references.](../media/activating.png)

> [!Note]
> You may see an error if IOM is unable to activate a system connection within timeout window. If this is the case, please close the error message and retry by selecting the Activate button. The root cause is that sometimes it can take longer than usual to activate one or more system connections thereby causing the application to raise a timeout error. If you don't see any error message in your retries then it means that the connections have been successfully activated.

**Congratulations!** You have finished configuring platform Power Automate connections.

## Task 2: Enable Bing maps for IOM

Dynamics 365 Intelligent Order Management can display information about fulfillment order source and destination locations using Bing Maps. In this task, you'll learn the steps to enable Bing maps for IOM.

1. While in Dynamics 365 IOM, select the **gauge icon** in the upper right corner and navigate to **Advanced Settings**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Dynamics 365 Intelligent Order Management Welcome page with the advanced settings option highlighted.](../media/advanced-settings.png)](../media/advanced-settings.png#lightbox)

1. A new window should open and navigate to Dynamics 361. It may take a while to load. If it's been longer than a minute, stop and reload the page. It should then load faster. It will land you in the Business Management section of Dynamics 365.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Dynamics 365 settings page.](../media/dynamics-365.png)](../media/dynamics-365.png#lightbox)

1. On the top command bar next to Dynamics 365, select **Settings** to open the drop-down, then select **Administration** in the third column under System.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Dynamics 365 settings page with Administration highlighted under System.](../media/system-administration.png)](../media/system-administration.png#lightbox)

1. Select **System Settings**

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Administration settings page with System settings highlighted.](../media/system-settings.png)](../media/system-settings.png#lightbox)

1. On the **General** tab, select **Yes** for **Show Bing Maps on forms**, and then select **OK**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the general tab with the Enable Bing Maps option highlighted.](../media/enable-bing.png)](../media/enable-bing.png#lightbox)

**Congratulations!** You have enabled Bing Maps integration, which will show the information about fulfillment order source and destination locations using Bing Maps.

## Task 3: Enable Timeline feature

This feature aims to improve user experience and give users a view of the timeline of business events associated with a sales order.

1. On the top command bar next to Dynamics 365, select **Settings** to open the drop-down, then select **Activity Feeds Configuration** in the fourth column.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Dynamics 365 settings showing Activity Feeds Configuration highlighted under System.](../media/activity-feeds.png)](../media/activity-feeds.png#lightbox)

1. Select **salesorder** and then select the **Activate** button. You can find the Entity Name **salesorder** by either typing the name in the Search textbox on the top right corner or you can select "O" at the bottom of the screen and select the **salesorder** entity.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Dynamics 365 Settings Post Configurations page with the Activate button highlighted.](../media/activate.png)](../media/activate.png#lightbox)

1. Select **Activate** on the dialog form.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the Confirm Post Configuration Activation dialog.](../media/confirm.png)

1. Once enabled, sales orders will start displaying a timeline of business events. To view timeline, select a sales order, and you'll see **Timeline** populated.

1. Open **Intelligent Order Management** Application and Select **Sales Orders** from Left Navigation Bar

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Dynamics 365 Intelligent Order Management Sales orders page showing the list of intelligent order management orders.](../media/sales-orders.png)](../media/sales-orders.png#lightbox)

1. Select any available Sales Order to see its details.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Order summary with the timeline highlighted.](../media/timeline.png)](../media/timeline.png#lightbox)

> [!Note]
> Enabling the Timeline feature does not retrospectively populate the timeline of events for existing orders. However, after the Timeline feature is enabled, if an order changes states and/or goes through different states (events), those are reflected under Timeline.

**Congratulations!** You have finished configuring the Timeline feature.
