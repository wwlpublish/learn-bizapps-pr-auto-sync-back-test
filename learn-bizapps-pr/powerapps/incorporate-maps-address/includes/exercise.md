In this exercise, you'll enable geospatial features in your Microsoft Power Platform environment. Additionally, you'll determine the value that the **Address input** field can add for users who are looking for an address in a field.

## Enable geospatial features

To enable geospatial features, follow these steps:

1.  Sign in to [Microsoft Power Platform admin center](https://admin.powerplatform.microsoft.com/?azure-portal=true). You must be an admin to complete these steps. If you don't have access, you'll need to request that someone completes the following steps for you, and then you can complete the subsequent sections of this exercise.

1.  On the left side of the Power Platform admin center, select **Environments** and then select the environment where you'll be creating the address input field for this exercise.

1.  Select **Settings** for the selected environment.

1.  Expand the **Product** section and then select **Features**.

1.  Turn on the **Geospatial services** field.

1.  Select the checkbox for the terms of service and then select **Enable**.

1.  Select **Save**.

## Add an address input field to an app

To add an address input field to an app, follow these steps:

1.  Sign in to [Power Apps](https://make.powerapps.com/?azure-portal=true).

1.  Make sure that you're in the environment where you previously enabled geospatial services.

1.  Select **+ Create** and then select **Blank app**.

1.  Under **Blank canvas app**, select **Create**.

1.  Name the app **Address Input Test** with the format of **Tablet**.

1.  Select **Create**.

1.  In the toolbar, select **Insert > Input > Address input**.

1.  In the address input properties for the new field, select the **Country set** value based on the ISO 3166 alpha-2 format and the address that you'll search within. For example, in the United States, select **US**.

## Test the Address input field

To test the **Address input** field, follow these steps:

1.  Press the **F5** key on your keyboard or select the play button for the app.

1.  In the **Address** field, enter an address in the country that you previously set up in the properties menu.

1.  After you've entered data, the field will suggest locations that match the address that you entered.

1.  Select the suggested address. Then, this address will be a verified address that you can use within your canvas app.
