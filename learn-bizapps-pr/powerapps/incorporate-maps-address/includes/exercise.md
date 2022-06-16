In this unit, you'll enable geospatial features in your Power Platform environment and see the value that the address input field can add for users looking for an address in a field.

## Enable Geospatial features

1.  Navigate and log into [Power Platform admin center](https://admin.powerplatform.microsoft.com/?azure-portal=true). You must be an admin to complete these steps. If you don't have access, you'll need to request someone complete the following steps, then you can execute the subsequent sections of this exercise.

1.  In the left hand side of the Power Platform admin center, select Environments and select the environment where you'll be creating the address input field for this exercise.

1.  Select **Settings** for the selected environment.

1.  Expand the **Product** section and select **Features**.

1.  On the **Geospatial services** field, turn it on.

1.  Select the check box for the terms of service and then select **Enable**.

1.  Select **Save**.

## Add an address input field to a Power App

1.  Log into [Power Apps](https://make.powerapps.com/?azure-portal=true).

1.  Make sure you are in the environment where you previously enabled Geospatial Services.

1.  Select **+Create** and select **Blank app**.

1.  Under Blank canvas app, select **Create**.

1.  Name the app 'Address Input Test' with the format **Tablet**.

1.  Select **Create**.

1.  In the tool bar, select **Insert,** then **Input,** and then select **Address input**.

1.  In the address input properties for the new field, select the **Country set** value based on the ISO 3166 alpha-2 format and the address you'll search within. For example, in the United States, select 'US'.

## Test the address input field

1.  Press F5 on your keyboard or select the play button for the Power App.

1.  In the address field, enter an address in the country you previously configured in the properties menu.

1.  Upon entering data, you'll see the field suggest locations that match the address you were entering.

1.  Select the suggested address. This address is then a verified address that can be used within your canvas app.
