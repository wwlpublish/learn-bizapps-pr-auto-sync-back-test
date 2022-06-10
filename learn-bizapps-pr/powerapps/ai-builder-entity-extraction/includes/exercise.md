In this exercise, we'll create a Power Automate cloud flow that is triggered on new incoming emails and then processes the messages with entity extraction.

Based on the results, if one of the recognized entities is a URL, you'll receive a Microsoft Teams notification to inform you that this email is a potential threat. The IT security team should confirm whether the link is legitimate and email can be considered safe or should be quarantined.

## Get started

The entity extraction, as a prebuilt model is ready to be used and doesn't require training. You can create a Power Automate cloud flow by itself and then add the AI Builder entity extraction action in it.

But, for this exercise, we'll take advantage of an existing Power Automate template to get started.

1.  In Power Automate studio, navigate to the **Templates** section and search for **entity extraction**. Select the tile for the template named **Extract entities of received emails using AI Builder**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Power Automate studio, displaying the results for template search on entity extraction.](../media/search-entity-extraction.png)](../media/search-entity-extraction.png#lightbox)

1.  Ensure all required connections are linked to your email account; if needed, create the connection by selecting **Create**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Power Automate studio, for the Extract entities of received emails using AI Builder template with a highlight on the create connection option.](../media/create-content-conversion.png)](../media/create-content-conversion.png#lightbox)

1.  Once completed, select **Continue**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Power Automate studio, for the Extract entities of received emails using AI Builder template with highlight on the continue option.](../media/continue.png)](../media/continue.png#lightbox)

1.  **Save** your flow.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Power Automate cloud flow designer, for the Extract entities of received emails using AI Builder template with highlight on the save option.](../media/save-flow.png)](../media/save-flow.png#lightbox)

## Review the flow actions

The template generated a cloud flow that is triggered on email arrival and then processes that email with entity extraction.

Take the time to familiarize yourself with the different actions contained in that new flow.

1.  The trigger monitors the inbox for the account of the connection selected.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Power Automate cloud flow action, when a new email arrives with highlight on the selected connection.](../media/connections-selected.png)](../media/connections-selected.png#lightbox)

1.  To ensure that no HTML tags interfere with the entity extraction process, the content of the message (**Body**) is converted from HTML to plain text.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Power Automate cloud flow action, Convert email html to text, with a highlight on the body value.](../media/body-value.png)](../media/body-value.png#lightbox)

1.  Assuming the message is in English, the first 5,000 characters (limitation of the model) of the converted text is processed by the entity extraction model.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Power Automate cloud flow action - Extract entities from text with the standard model, with a highlight on the slice formula.](../media/slice-formula.png)](../media/slice-formula.png#lightbox)

1.  Results are converted in an HTML table so they can be easily reviewed when testing the flow.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Power Automate cloud flow action, Create HTML table.](../media/create-table.png)](../media/create-table.png#lightbox)

## Process the results

The entity extraction action returns a series of results that consist of the list of detected entities with detailed information, such as:

-   **Type**: which entity type was detected

-   **startIndex and length**: indication of the position and length of the text portion this entity is for

-   **value**: the extracted portion of the text representing the entity

-   **score**: level of confidence for this detected entity

In the current scenario, we focus on one type of entity, namely **URL**, so we'll now filter the results to only continue and send the notification when that is detected.

1.  Add a filter array action to keep only the **URL** entity type.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Power Automate cloud flow action, Filter array for the URL entity.](../media/entity.png)](../media/entity.png#lightbox)

1.  Add a condition action to continue only if there is at least one item left in the filtered array.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Power Automate cloud flow action, If one of the entities is a URL, with a highlight on the length formula.](../media/length.png)](../media/length.png#lightbox)

1.  When condition is valid, post a Teams notification

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Power Automate cloud flow action, Post message in a chat or channel.](../media/post-message.png)](../media/post-message.png#lightbox)

## Test the flow

The last step is to confirm that the flow processes incoming emails as expected and sends out a Teams notification if a URL is part of a received email message.

To test the flow:

1.  Save the flow.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Power Automate cloud flow with a highlight on Save.](../media/save.png)](../media/save.png#lightbox)

1.  Confirm that the flow is active. Select **Turn on** if available.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the cloud flow in Power Automate studio with highlight on Turn on.](../media/turn-on-button.png)](../media/turn-on-button.png#lightbox)

1.  In Outlook, send yourself (or the monitored email address) a message containing different sentences and items. For the first test scenario, include a link to a website in the email message.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the email content with a URL in the signature.](../media/signature.png)](../media/signature.png#lightbox)

1.  In Teams, confirm that you've received a notification for this email.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Teams notification sent from the Power Automate cloud flow.](../media/notification.png)](../media/notification.png#lightbox)

1.  For the second test scenario, create a new email message that doesn't contain a website link. No Teams notification is received.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the email content without any URL.](../media/email.png)](../media/email.png#lightbox)

1.  To stop processing incoming emails, turn off the flow.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the cloud flow in Power Automate studio with highlight on the Turn off option.](../media/turn-off-button.png)](../media/turn-off-button.png#lightbox)

