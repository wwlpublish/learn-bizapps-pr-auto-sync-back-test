In this exercise, you'll complete the following tasks:

1. About IOM providers and their role.

1. Configure a provider for BigCommerce that enables communication between IOM and third-party e-commerce platform BigCommerce.

1. Configure Internal-External Mappings in IOM.

1. Configure a first-party provider for Intelligent Fulfillment Optimization. This provider enables the use of intelligent fulfillment optimization capabilities in IOM.

1. Configure a first-party provider for Inventory Visibility. This provider enables use of inventory feasibility capabilities in Dynamics 365 IOM.

## Overview of providers

A key value proposition of Dynamics 365 Intelligent Order Management is the ability to seamlessly integrate with other systems. To do so, Intelligent Order Management uses "providers". [Providers](https://docs.microsoft.com/dynamics365/intelligent-order-management/work-providers?azure-portal=true#components) are constructs that allow you to connect Intelligent Order Management to external systems.

Intelligent Order Management providers were designed with the following properties:

- **Extensibility**: Providers can be extended and customized by using the Microsoft Power Platform.

- **Low code customization**: Because providers are built on the Power Platform, customizations require little to no code.

- **Scale**: Providers use Power Automate, so providers can scale with volume of incoming messages.

Key components of a provider are:

- Connection

- Business event

- Action

- Parameter

- Transformation

## Task 1: Configure the BigCommerce provider

1. Open your browser in In-Private or Incognito window, navigate to [Power Apps](https://make.powerapps.com/?azure-portal=true).

1. Ensure to choose the correct environment from the upper right **Environment** drop-down is selected.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the environment selected from the drop down menu.](../media/environment.png)](../media/environment.png#lightbox)

1. Select **Apps** on the left navigation bar.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Power naps navigation pane with Apps selected.](../media/apps.png)](../media/apps.png#lightbox)

1. Select **Intelligent Order Management**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the list of apps with Intelligent Order Management highlighted.](../media/intelligent-order-management.png)](../media/intelligent-order-management.png#lightbox)

1. On the left pane, select **Providers** > **Catalog**. The form will display a list of pre-built Providers. IOM also supports custom providers. For our lab, we'll be using BigCommerce as our source system so select **Add provider** button on **BigCommerce** tile.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Dynamics 365 Intelligent Order Management Providers Catalog page with BigCommerce highlighted.](../media/big-commerce.png)](../media/big-commerce.png#lightbox)

1. To accept the terms and conditions, select the **Create** button and it will take a few seconds to process.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the terms and conditions dialog.](../media/terms.png)](../media/terms.png#lightbox)

1. The system will automatically open the Big Commerce provider screen with BigCommerce connection. Select BigCommerce Connection to enable communication between Dynamics 365 Intelligent Order Management to the associated BigCommerce account.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the BigCommerce provider overview tab with the BigCommerce connection highlighted.](../media/big-commerce-connection.png)](../media/big-commerce-connection.png#lightbox)

1. Select the **Retrieve Link**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the BigCommerce connection overview page with the Retrieve link button highlighted.](../media/retrieve.png)](../media/retrieve.png#lightbox)

1. Selecting **Retrieve Link** will take you to **Power Automate**. Ensure the correct environment from the upper right **Environment** drop-down is selected.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the correct environment selected.](../media/environment-2.png)](../media/environment-2.png#lightbox)

1. On the left pane, select **Data** > **Connections**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Power Automate navigation pane with Connections highlighted.](../media/connections.png)](../media/connections.png#lightbox)

1. Select **New Connection**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the New Connection button.](../media/new-connection.png)](../media/new-connection.png#lightbox)

1. Search for **BigCommerce** in the search bar located in the top right edge and then select **BigCommerce** to add the connection.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the search results for BigCommerce.](../media/big-commerce-search.png)](../media/big-commerce-search.png#lightbox)

1. You'll be prompted for **API Key**. Copy/paste the **Access token** generated during the training environment setup module - Exercise 1 under task 2 - step 4 that you had copied from the screen as below.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the BigCommerce A P I Credentials dialog showing client I D, client secret, and access token fields.](../media/credentials.png)](../media/credentials.png#lightbox)

1. Paste the API key as below and select **Create**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the BigCommerce dialog with the A P I key entered.](../media/key.png)](../media/key.png#lightbox)

1. Once a connection has been created based on the API key, you should see the status of the connection as Connected.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Connections in Intelligent Order Management Trial dialog with BigCommerce showing a status of connected.](../media/connected.png)](../media/connected.png#lightbox)

1. Select BigCommerce connection to view the details of this connection. Copy the **URL** shown in the address bar of your browser.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Power Automate Connections page for BigCommerce in a browser with the U R L highlighted.](../media/big-commerce-url.png)](../media/big-commerce-url.png#lightbox)

1. Navigate to Dynamics 365 IOM and paste the URL in the **Connection URL** field in BigCommerce Provider Connection Reference screen. Once pasted, select **Save** and then **Activate**. IOM will then take a 15-20 seconds to activate a Provider for BigCommerce.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the BigCommerce connection overview with the connection U R L highlighted.](../media/big-commerce-connection-url.png)](../media/big-commerce-connection-url.png#lightbox)

1. Select **Save and Close**.

1. Select **BigCommerce Dataverse (current environment)**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the BigCommerce provider with the BigCommerce Dataverse connection highlighted.](../media/big-commerce-dataverse.png)](../media/big-commerce-dataverse.png#lightbox)

1. Paste the Dataverse connection URL used in Exercise 2 - Task 1 - Step 1. Once pasted, select **Save** and then select **Activate**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the BigCommerce Dataverse Connection overview.](../media/big-commerce-dataverse-connection.png)](../media/big-commerce-dataverse-connection.png#lightbox)

1. At this stage, you should have connections for BigCommerce and Dataverse configured and activated.

1. Select **Save and Close**.

1. Switch to Dynamics 365 IOM screen and on the **BigCommerce** provider screen, select the **Parameters** tab.

1. To find your store hash from BigCommerce site, sign in to your BigCommerce Store (created in Exercise 1 - Task 1). Go to **Advanced Settings** > **Select API Accounts** > **Create API Account (V2/V3 Token)**. You can find a field named API Path, with the following structure `https://api.bigcommerce.com/stores/<storehash>/v3`. You can also find it from the store URL, and highlighted below.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the BigCommerce Fabrikam retail A P I accounts create account page with the hash section of the A P I path highlighted.](../media/hash.png)](../media/hash.png#lightbox)

1. Paste the store hash value into the **value** field for **BigCommerce Store Hash** and then select **Save** and then **Activate**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the BigCommerce provider with the store hash added and the Activate button highlighted.](../media/store-hash.png)](../media/store-hash.png#lightbox)

1. If all the connections are provided correctly, then you should see a message that reads that the record's status is Active.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Intelligent Order Management BigCommerce provider overview with the record status of Active highlighted.](../media/active.png)](../media/active.png#lightbox)

    > [!Note]
    > You may encounter an error message as shown in the below screenshot if the System Connections have not been configured as mentioned in the earlier exercises and tasks.
    >
    > [!div class="mx-imgBorder"]
    > [![Screenshot of the error message on the BigCommerce 1 provider page showing the parameters tab with the wrong store hash value.](../media/error.png)](../media/error.png#lightbox)

## Task 2: Configure Internal-External Mappings for BigCommerce provider transformations

Once BigCommerce Provider has been configured, next step is to configure Mappings in IOM. Mappings enable translation of fields between third-party platforms such as BigCommerce and IOM. With the internal external ID mappings functionality, you can perform the following tasks:

1. Define the relationship between identities in an enterprise across applications and operating systems.

1. Use the mapping for multiple integrations.

1. Enable an end-to-end visualization of mapping across multiple systems.

1. Configure and add your own mapping and mapping tables.

In context of BigCommerce Provider, following Internal External Mappings must be configured before orders generated in BigCommerce are visible in IOM:

- Accounts

- Products

- Price Lists

- Units

1. We need a customer account to map it to BigCommerce providers. To create a customer test account, navigate to **Customers** > **Accounts**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Dynamics 365 navigation pane with Accounts highlighted under Customers.](../media/accounts.png)](../media/accounts.png#lightbox)

1. Select **New** on the command bar.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the My Active Accounts page with the New button highlighted on the command bar.](../media/new-account.png)](../media/new-account.png#lightbox)

1. Enter the following fields and select **Save & Close** in the command bar.

    - **Account Name**: TestBCAccount

    - **Account Number**: TestBCAccount

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Test B C Account summary with the fields filled.](../media/test-account.png)](../media/test-account.png#lightbox)

1. To access Mappings configuration, On the left pane of Dynamics 365 IOM, Change the area in left bottom edge of the screen from **Intelligent Order Management** to **Configurations**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Dynamics 365 Intelligent Order Management navigation pane with Mappings expanded to show Configurations.](../media/mappings.png)](../media/mappings.png#lightbox)

1. To configure Internal-External mapping for **Accounts**, select **New**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the New Account Mapping page.](../media/account-mapping.png)](../media/account-mapping.png#lightbox)

1. Enter the following details and then select **Save & Close**.

    - **Provider**: BigCommerce

    - **Customer**: TestBCAccount

    - **External Field Name**: ProviderName

    - **External Field Value**: BigCommerce

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the New Account Mapping general page showing BigCommerce values filled in.](../media/big-commerce-account-mapping.png)](../media/big-commerce-account-mapping.png#lightbox)

1. Select **Save & Close**.

1. To configure the product mapping, on the left pane, select **Products**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Dynamics 365 navigation pane with Products selected under Mappings.](../media/products.png)](../media/products.png#lightbox)

1. Select **New** and enter the following fields:

    - **Provider**: BigCommerce

    - **Product**: Accu Scale (We'll be mapping this item to ABS from BigCommerce platform.)

    - **External Field Name**: sku

    - **External Field Value**: ABS

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the New Product Mapping page.](../media/product-mapping.png)](../media/product-mapping.png#lightbox)

    > [!Note]
    > Product Mapping step must be completed for each individual product which you expect to come through on orders from BigCommerce or any other third-party (3P) platform. If an order item doesn't have a corresponding item, then those orders will not flow through to IOM via a Provider.

1. Select **Save & Close**.

1. To configure the **Price Lists,** select **Price Lists** on the left pane.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Dynamics 365 navigation pane with Price Lists selected under Mappings.](../media/price-lists.png)](../media/price-lists.png#lightbox)

1. Select **New** and enter the following fields and select **Save & Close**.

    - **Provider**: BigCommerce

    - **Price List**: Master price list

    - **External Field Name**: ProviderName

    - **External Field Value**: BigCommerce

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the New Price List Mapping screen filled in.](../media/price-list-mapping.png)](../media/price-list-mapping.png#lightbox)

1. To configure Units, Navigate to **Units** in the left pane.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Dynamics 365 navigation pane with Units selected under Mappings.](../media/units.png)](../media/units.png#lightbox)

1. Select **New** and then enter the values as below and select **Save & Close**.

    - **Provider**: BigCommerce

    - **Unit**: ea

    - **External Field Name**: unit

    - **External Field Value**: each

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the New Unit Mapping screen filled in.](../media/unit-mapping.png)](../media/unit-mapping.png#lightbox)

**Congratulations!** You have finished configuring BigCommerce Provider and Internal-External Mappings to enable flow of orders from BigCommerce.
