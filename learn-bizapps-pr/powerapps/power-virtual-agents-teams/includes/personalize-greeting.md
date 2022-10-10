There are two special users related variables available to help personalize your chatbot conversations, known as claim variables. These variables allow you to show the display name and user ID of the logged in user in your chatbot. 

## Task: Edit and personalize the greeting topic

In this task, we'll edit the greeting topic so that the chatbot greets the user in Teams by their name. We'll also edit the standard greeting topic so that it explains to the user what it's designed to help with.

1. Select **Go to Topics**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot highlighting Go to topics button.](../media/topics.png)](../media/topics.png#lightbox)

1. Find the **Greeting** topic and select it to open the authoring canvas.

    > [!div class="mx-imgBorder"]
    > [![Screenshot highlighting greeting topic.](../media/greeting.png)](../media/greeting.png#lightbox)

1. Let’s personalize the greeting by adding a variable that will display the name of the user. Put your cursor between the word “Hi” and “!” and add a space. Select the variable icon and select **bot.UserDisplayName**.
 
    > [!div class="mx-imgBorder"]
    > [![Screenshot highlighting user display name.](../media/user-display-name.png)](../media/user-display-name.png#lightbox)

1. Edit the rest of the message with the following text:

    *I’m a virtual agent. I can help you with requesting Contoso Coffee Swag*.
    
    > [!div class="mx-imgBorder"]
    > [![Screenshot highlighting to edit User display name.](../media/greeting-message.png)](../media/greeting-message.png#lightbox)

1. Select **Save** and wait until you see the confirmation message.
 
    > [!div class="mx-imgBorder"]
    > [![Screenshot highlighting to save edits.](../media/save-edits.png)](../media/save-edits.png#lightbox)

1. Test your bot by typing **hello** in the test bot pane. 

1. You should see your chatbot uses your new greeting, including your name in the test pane. You'll also see green checks in the authoring canvas showing the successful path the chatbot has followed during your test.
 
    > [!div class="mx-imgBorder"]
    > [![Screenshot highlighting new greeting message.](../media/new-greeting.png)](../media/new-greeting.png#lightbox)

1. Select **Back** to return to your list of topics. 

    > [!div class="mx-imgBorder"]
    > [![Screenshot highlighting back to return to topic lists.](../media/back-button.png)](../media/back-button.png#lightbox)
