In this exercise, you'll complete the following tasks:

- Set up mandatory Power Automate connections for Intelligent Order management.

- Enable Bing Maps integration.

- Enable the **Timeline** feature.

## Task 1: Set up system connections
To set up system connections, follow these steps:

1.	Open an InPrivate or Incognito window in your browser and then go to [Microsoft Power Apps](https://make.powerapps.com/?azure-portal=true).

1. Ensure that you choose the correct environment from the **Environment** dropdown menu.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the selected environment in Power Apps.](../media/environment.png)

1. Select **Apps** on the left navigation bar.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the Power Apps navigation bar with Apps selected.](../media/apps.png)

1. Select **Intelligent Order Management**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Intelligent Order Management app selected in the Apps list.](../media/intelligent-order-management.png)](../media/intelligent-order-management.png#lightbox)

1. Select the **Get Started** button on the welcome screen in Intelligent Order Management.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the welcome screen with the Get Started button.](../media/get-started.png)](../media/get-started.png#lightbox)

1. On the Intelligent Order Management screen, select **Getting Started** in the left navigation pane and then select the **Manage** button next to the **Configure settings** option to set up connections that are required by Intelligent Order Management.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Getting Started page in Dynamics 365 Intelligent Order Management.](../media/manage.png)](../media/manage.png#lightbox)

   A list of **System Connection References** should display. These references are used by Intelligent Order Management to communicate with Microsoft Dataverse, Power Automate, and IOM Data Transformer. The general setup process for each system connection is the same. Administrator privileges are required to set up these system connections.

1. Select the **IOM Data Transformer** record.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the System Connection References page with the I O M Data Transformer record selected.](../media/system.png)

1. Select **Retrieve Link**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the I O M Data Transformer page with the Retrieve Link button highlighted.](../media/transformer.png)](../media/transformer.png#lightbox)

1. A **Power Automate** portal will open. If you're opening Power Automate for the first time, then a welcome screen will display.

    > [!Important]
    > Select **United States** as your country/region and then select the **Get started** button for this lab.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the Welcome to Power Automate screen with country set to United States.](../media/welcome.png)

1. Ensure that the correct environment is selected from the **Environment** dropdown menu.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the Environment selected in Power Automate.](../media/environment-2.png)

1. On the left pane, select **Data > Connections**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the Connections option highlighted in Power Automate.](../media/connections.png)

1. Select **+ New connection**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the add New connection button.](../media/new-connection.png)

1. Search for **IOM Data Transformer** in the search bar in the upper-right corner of the screen, and then select **IOM Data Transformer** to add the connection.

    > [!Note]
    > If you don’t find the connection, close this browser tab and then repeat the steps from Step 9.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the connection search results for I O M Data Transformer.](../media/iom-data.png)](../media/iom-data.png#lightbox)

1. Select the plus (**+**) button to add the connection.

1. Select the **Create** button on the **IOM Data Transformer** dialog.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the I O M Data Transformer dialog showing the Create button.](../media/create-transformer.png)

1. This connector will prompt for credentials. These account and connection details will be used by the IOM Data Transformer connector in the Intelligent Order Management Power Automate flows to transform data by using a Microsoft Power Query online API for Intelligent Order Management application. For this task, you can use your **In A Day** user account (credentials that you're using to sign in to [Power Apps](https://make.powerapps.com/?azure-portal=true)) to establish the connection. However, in a customer's environment, make sure that you use a dedicated service account instead of a user's account.

1. After you’ve established the connection, select the ellipsis (**...**) menu on the connection and then select **Details**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the ellipsis menu selected to reveal the Details option.](../media/details.png)](../media/details.png#lightbox)

1. On the **Details** page, copy the **URL** from browser's address bar.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Power Automate Connections page in a browser with the U R L highlighted.](../media/url.png)](../media/url.png#lightbox)

1. Go to the Dynamics 365 Intelligent Order Management application page in your browser, paste the URL into the **Connection URL** field for the **IOM Data Transformer** record, and then select **Save & Close** on the command bar.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Intelligent Order Management sandbox I O M Data Transformer connections with the Connection U R L highlighted.](../media/connection-url.png)](../media/connection-url.png#lightbox)

1. Return to the **Power Automate** page on your browser, and on the left pane, select **Data > Connections**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the Power Automate navigation pane with Connections highlighted.](../media/connections.png)

1. Select **+ New connection**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the add New connection button again.](../media/new-connection.png)

1. Search for **Microsoft Dataverse** in the search bar that’s located in the upper-right corner of the screen, and then select the plus (**+**) button to add the connection.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the search results for Dataverse with the plus icon next to Microsoft Dataverse selected.](../media/dataverse.png)](../media/dataverse.png#lightbox)

1. Select the **Create** button on the **Microsoft Dataverse** dialog.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the Microsoft Dataverse dialog with the Create button highlighted.](../media/create-dataverse.png)

1. This connector will prompt for credentials. The Microsoft Dataverse connector uses these account and connection details in the Intelligent Order Management Power Automate flows to perform CRUD operations on this environment's database. For this task, you can use your user account (credentials that you use to sign in to [Power Apps](https://make.powerapps.com/?azure-portal=true)) to establish the connection. However, in a customer's environment, use a dedicated service account instead of a user's account.

1. After you’ve established the connection, select the ellipsis (**...**) menu on the connection and then select **Details**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the list of connections and showing the ellipsis button next to the Dataverse connection selected to reveal the Details option.](../media/dataverse-details.png)](../media/dataverse-details.png#lightbox)

1. On the **Details** page, copy the **URL** from the browser's address bar. Save this URL in your OneNote or Notepad because you'll need to paste the URL in the next step and in the next exercise.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Microsoft Dataverse connection page in Power Automate, showing the U R L highlighted.](../media/dataverse-url.png)](../media/dataverse-url.png#lightbox)

1. Go to the Dynamics 365 Intelligent Order Management application page in your browser. Paste the same URL into the **Connection URL** field on the **Microsoft Dataverse**, **Microsoft Dataverse - Application** and **Microsoft Dataverse - Integration** system connection reference records.

    When you're done, the **System Connection References** list will show the records as **Active**, except for the **Power Automate Management** record, which will show as **Inactive**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the System Connection References list with Microsoft Dataverse and others showing a status reason of Active, while Power Automate Management shows a status reason of Incomplete.](../media/system-connection.png)

1. Go to the Power Automate page in your browser and repeat the previous steps to add the **Power Automate Management** connection in Power Automate. Leave the **Authentication Type** as **First Party** and then select **Create**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Power Automate Management dialog with Authentication Type set to First Party.](../media/power-automate-management.png)](../media/power-automate-management.png#lightbox)

1. A new window prompt will ask for credentials. These account/connection details will be used by the Power Automate Management connector. For this task, you can use your **In A Day** user account (credentials that you're using to sign in to [Power Apps](https://make.powerapps.com/?azure-portal=true)) to establish the connection. However, in a customer's environment, make sure that you use a dedicated service account instead of a user's account.

1. Paste the connection URL in the **Power Automate Management** record in Dynamics 365 Intelligent Order Management.

1. Go to Dynamics 365 Intelligent Order Management page and, when the **Status Reason** for all listed **System Connection References** are in an **Active** state, select **Activate System** on the command bar.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the System Connection References list with the Activate System button highlighted.](../media/activate-system.png)](../media/activate-system.png#lightbox)

1. It takes about five minutes to activate all system connections. The following message should appear on the screen while connections are being activated.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the Activating System Connection References message.](../media/activating.png)

> [!Note]
> An error might occur if Intelligent Order Management is unable to activate a system connection within a timeout window. If so, make sure that you close the error message and retry by selecting the **Activate** button. The root cause is that activating one or more system connections might take longer than usual, thereby causing the application to raise a timeout error. If an error message doesn’t display in your retries, then the connections have been successfully activated.

Congratulations, you’ve finished setting up Power Automate connections.

## Task 2: Enable Bing Maps for Intelligent Order Management

Dynamics 365 Intelligent Order Management can display information about fulfillment order source and destination locations by using Bing Maps. In this task, you'll enable Bing Maps for Intelligent Order Management.

1. While in Dynamics 365 Intelligent Order Management, select **Settings** (gear icon) in the upper-right corner and then go to **Advanced Settings**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Dynamics 365 Intelligent Order Management Welcome page with the Advanced Settings option highlighted.](../media/advanced-settings.png)](../media/advanced-settings.png#lightbox)

1. A new window should open and direct you to Dynamics 365. The page might take a while to load. If it's been longer than a minute, stop and reload the page. Then, the page should load faster, when you’ll be directed to the Business Management section of Dynamics 365.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Dynamics 365 Settings page.](../media/dynamics-365.png)](../media/dynamics-365.png#lightbox)

1. On the top command bar, next to Dynamics 365, select the **Settings** dropdown menu, and then select **Administration** in the third column under **System**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Dynamics 365 Settings page with Administration highlighted under System.](../media/system-administration.png)](../media/system-administration.png#lightbox)

1. Select **System Settings**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Administration settings page with System Settings highlighted.](../media/system-settings.png)](../media/system-settings.png#lightbox)

1. On the **General** tab, select **Yes** for **Show Bing Maps on forms**, and then select **OK**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the General tab with the Enable Bing Maps option highlighted and set to Yes.](../media/enable-bing.png)](../media/enable-bing.png#lightbox)

Congratulations, you’ve enabled Bing Maps integration, which will show the information about fulfillment order source and destination locations by using Bing Maps.

## Task 3: Enable the Timeline feature

The **Timeline** feature aims to improve user experience and give users a timeline of business events that are associated with a sales order.

1. On the top command bar, next to Dynamics 365, select the **Settings** dropdown menu, and then select **Activity Feeds Configuration** in the fourth column.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Dynamics 365 Settings page, showing Activity Feeds Configuration highlighted under System.](../media/activity-feeds.png)](../media/activity-feeds.png#lightbox)

1. Under **Entity Name**, select **salesorder** and then select the **Activate** button. You can find the **salesorder** entity name by typing the name in the search box in the upper-right corner or by selecting the **O** in the lower part of the screen and then selecting the **salesorder** entity.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Post Configurations page in Dynamics 365 Settings with the Activate button highlighted.](../media/activate.png)](../media/activate.png#lightbox)

1. Select **Activate** on the dialog.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the Confirm Post Configuration Activation dialog.](../media/confirm.png)

1. After they’ve been enabled, sales orders will start displaying a timeline of business events. To view a timeline, select a sales order and **Timeline** will be populated.

1. Open the **Intelligent Order Management** application and select **Sales Orders** in the left navigation pane.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Sales Orders page in Dynamics 365 Intelligent Order Management, showing the list of Intelligent Order Management orders.](../media/sales-orders.png)](../media/sales-orders.png#lightbox)

1. Select any available sales order to view its details.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the order summary with the Timeline highlighted.](../media/timeline.png)](../media/timeline.png#lightbox)

> [!Note]
> Enabling the **Timeline** feature doesn’t retrospectively populate the timeline of events for existing orders. However, after the **Timeline** feature has been enabled, if an order changes states and/or goes through different states (events), those are reflected under **Timeline**.

Congratulations, you’ve finished setting up the **Timeline** feature.
