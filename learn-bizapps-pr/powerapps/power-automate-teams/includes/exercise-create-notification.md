In this exercise, we'll extend the flow to send a Teams message to the user to let them know whether their request has been approved or rejected.

## Task - Edit your flow

1. Navigate back to Power Apps using the icon on the left menu bar of Teams. Select the **Build** tab, select your team and Select **See all**.

    > [!div class="mx-imgBorder"]
    > [![A screenshot of Power Apps in Teams- Build tab.](../media/built-team.png)](../media/built-team.png#lightbox)

1. Go to Cloud flows and Select the **Request approval** flow in the list to open it for editing.

    > [!div class="mx-imgBorder"]
    > [![A screenshot of Power Apps in Teams- open Request Approval flow.](../media/cloud-flows.png)](../media/cloud-flows.png#lightbox)

1. Select **Edit** to open your flow.

    > [!div class="mx-imgBorder"]
    > ![A screenshot of Power Apps in Teams- edit flow.](../media/edit-button.png)

1. Select the **Condition** step to open it.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of flow with Condition highlighted.](../media/condition-step.png)](../media/condition-step.png#lightbox)

1. In the **If yes** path, under the Update a row action, Select **Add an action**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of adding an action to the if yes path in the flow.](../media/if-yes-add-action.png)

1. Search for the get a row by ID and select **Get a row by ID Microsoft Dataverse**.

1. Select **Users** as the Table name. In the Row ID field, add the dynamic content **Owner (Value)** from the Dataverse When a row is added, modified or deleted action.

    > [!div class="mx-imgBorder"]
    > [![Screenshot editing Table name and Row ID in Get a row action card.](../media/owner.png)](../media/owner.png#lightbox)

1. Add a new action underneath. Search for post a message, and select the action called **Post message in a chat or channel**. You may have to wait a moment for the connection with the Microsoft Teams connector to be established and for the sign-in process to complete.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of flow: add Teams action- Post a message in a chat or channel.](../media/post-message.png)](../media/post-message.png#lightbox)

1. Fill in the details as follows:

    - **Post as:** Flow bot

    - **Post in:** Chat with Flow bot

    - **Recipient:** Select dynamic content Primary Email.

    - **Message:**

        > Approved!
        >
        > Your request has been approved by APPROVER NAME APPROVER EMAIL
        >
        > Details:
        > REQUEST NAME
        > ASSET NAME
        > Request No: REQUEST NUMBER
        >
        > Approver Comments: APPROVER COMMENTS

        > [!NOTE]
        > Make note of the capitalized items in the message. These are the parts you'll replace with dynamic content. Follow the instructions below for each section.
        >
        > [!div class="mx-imgBorder"]
        > [![A screenshot of Power Automate- Post message in a chat or channel Teams action.](../media/post-message-chat.png)](../media/post-message-chat.png#lightbox)

1. Replace the capitalized text with the following dynamic content.

    APPROVER NAME. Search for **approver** and select **Responses Approver name**. It comes from the Start and wait for approval action. Doing so will place your Teams action in an Apply to Each control.

    > [!div class="mx-imgBorder"]
    > [![A screenshot of Power Automate- Post message in a chat or channel Teams action with Responses approver name highlighted.](../media/approver-name.png)](../media/approver-name.png#lightbox)

    APPROVER EMAIL. Search for **approver** and select **Responses Approver email**. It comes from the Start and wait for approval action.

    > [!div class="mx-imgBorder"]
    > [![A screenshot of Power Automate- Post message in a chat or channel Teams action with Responses approver email highlighted.](../media/approver-email.png)](../media/approver-email.png#lightbox)

    REQUEST NAME. Search for **name** and scroll down until you find **Name** in the **When a row is added, modified or deleted** section There are multiple columns in your flow now called **Name**. Here we want to find the name of the request record, which triggered the flow.

    > [!div class="mx-imgBorder"]
    > [![A screenshot of Power Automate- Post message in a chat or channel Teams action with Name highlighted.](../media/request-name.png)](../media/request-name.png#lightbox)

    ASSET NAME. Search for **name** and scroll down until you find **Asset** **Name** in the **Get a row by ID** section There are multiple columns in your flow now called name--here we want to find the name of the asset.

    > [!div class="mx-imgBorder"]
    > [![A screenshot of Power Automate- Post message in a chat or channel Teams action with Asset Name highlighted.](../media/asset-name-action.png)](../media/asset-name-action.png#lightbox)

    REQUEST NUMBER. Search for **request number** and select **Request Number**. in the **When a row is added, modified or deleted** section.

    > [!div class="mx-imgBorder"]
    > [![A screenshot of Power Automate- Post message in a chat or channel Teams action with Request Number highlighted.](../media/request-number.png)](../media/request-number.png#lightbox)

    APPROVER COMMENTS. Search for **comment** and select **Response Comments** in the **Start and wait for an approval** section to bring in the comments the approver adds when they approve the request.

    > [!div class="mx-imgBorder"]
    > [![A screenshot of Power Automate- Post message in a chat or channel Teams action with Responses Comments highlighted.](../media/responses-comments.png)](../media/responses-comments.png#lightbox)

1. You can make changes to the formatting of the message. Highlight the word **APPROVED** indicated below. Change the font size to 16, bold the text and use the color picker to change the color to green.

    > [!div class="mx-imgBorder"]
    > [![A screenshot of Power Automate- Post message in a chat or channel Teams action with formatting buttons highlighted.](../media/format.png)](../media/format.png#lightbox)

1. Highlight the word **Details:** indicated below. Bold and underline the text.

    > [!div class="mx-imgBorder"]
    > [![A screenshot of Power Automate- Post message in a chat or channel Teams action with Details highlighted.](../media/details-format.png)](../media/details-format.png#lightbox)

1. **Save** the flow.

## Task - Test your flow

1. A confirmation message next to the name of the flow shows you that your flow has saved. Navigate back to the team you've been working on by selecting the main Teams icon in the left-hand navigation bar.

    > [!div class="mx-imgBorder"]
    > ![A screenshot of Power Automate- exit flow.](../media/saved.png)

1. Open your **Swag Request App** in the tab and submit a new request.

    > [!div class="mx-imgBorder"]
    > [![A screenshot of Swag Request App in Teams- submit a new request.](../media/new-request.png)](../media/new-request.png#lightbox)

1. In a moment, you'll receive a Teams notification. Approve the request and add a comment. You can approve it from either the email or Teams.

    > [!div class="mx-imgBorder"]
    > [![A screenshot of Microsoft Teams approval notification.](../media/approve-it.png)](../media/approve-it.png#lightbox)

1. Once approved, you should see a notification in Teams chat. Open the chat to see your Teams message notification that your request has been approved.

    > [!div class="mx-imgBorder"]
    > [![A screenshot of Microsoft Teams approval message.](../media/approved.png)](../media/approved.png#lightbox)
