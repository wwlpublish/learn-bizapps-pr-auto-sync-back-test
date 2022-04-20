Have you ever run into a situation where you'll be away from your work device for an unplanned, extended period of time? Wish you had a way to block your work calendar and let your manager know? Then this is the unit for you! In a few clicks, you can modify an existing template, and then have it available to trigger from the Power Automate mobile app.

## Prerequisites

- Access to [Power Automate](https://flow.microsoft.com/?azure-portal=true).

- Access to Power Automate mobile app.

- A basic understanding of Power Automate and experience with creating a flow is recommended.

## Open the template

1. Launch Power Automate and sign in using your organizational account.

1. Select **Templates** and search *block calendar*.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the block calendar template.](../media/block-calendar-template.png)

1. Select the *Block out my Office 365 calendar for an hour* tile.

1. Select **Continue**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the office 365 outlook connector.](../media/office-365-outlook-connector.png)

1. Select the drop-down available for the **Calendar id** and select **Calendar**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of select Calendar.](../media/select-calendar.png)

Next, we're going to send an email notification to our manager, to do this we'll use the combination of **Get my profile (V2)** and **Get manager (V2)**.

1. Select **+ New step** and search for **Office 365 Users** and select the **Get my profile (V2)** action. This action will provide us the User Principal Name.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of get my profile.](../media/get-my-profile.png)

1. Select **+ New step** and search for **Office 365 Users** and select the **Get manager (V2)** action.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of get manager.](../media/get-manager.png)

1. Click inside the **User (UPN)** file. In Dynamic content, select UPN. Make sure you select the UPN that is under the **Get my profile (v2)**

    > [!div class="mx-imgBorder"]
    > ![Screenshot of user principal name.](../media/user-principal-name.png)

1. Finally, select **+ New step** and search for **Outlook** and select the **Send an email (V2)** action.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of send an email.](../media/send-an-email.png)

1. Click inside the **To** field and in **Dynamic content** select **Mail** under the **Get manager (V2)**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of get manager mail.](../media/get-manager-mail.png)

1. Finally, you can add your desired text in the **Subject** and the **Body** section. Here's an example:

    > [!div class="mx-imgBorder"]
    > ![Screenshot of subject and body.](../media/email-subject-body.png)

Here's an overview of the entire flow:

> [!div class="mx-imgBorder"]
> ![Screenshot of block calendar flow overview.](../media/block-calendar-flow-overview.png)

And here's what the virtual button looks like in the Power Automate mobile app:

> [!div class="mx-imgBorder"]
> ![Screenshot of block calendar flow overview in the mobile app.](../media/button-mobile-device.png)
