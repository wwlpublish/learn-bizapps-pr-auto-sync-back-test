In this task, we'll create a topic for the bot to answer common questions from employees about Contoso Coffee swag.

## Task: Switch off the lesson topics

Let’s start by switching off the lesson topics, which aren't needed as part of this chatbot.

1. In the list of existing topics, you'll see topics named Lesson 1, Lesson 2, Lesson 3 and Lesson 4. Switch the **Status** toggle for each of these topics to the **off** position.

    > [!div class="mx-imgBorder"]
    > [![Screenshot highlighting status toggle for each positions.](../media/status-toggle.png)](../media/status-toggle.png#lightbox)
 
1. You'll need to wait a few seconds each time while the topic is turned off. You’ll see a progress message and then a confirmation message at the top of the topics list.

    > [!div class="mx-imgBorder"]
    > [![Screenshot highlighting confirmation message at top of topic list.](../media/confirmation-message.png)](../media/confirmation-message.png#lightbox)

## Task: Create a new topic for questions about Contoso Coffee’s swag

1. Create a new topic by selecting on **+New topic**.
    
    > [!div class="mx-imgBorder"]
    > [![Screenshot highlighting New topic button.](../media/new-topic.png)](../media/new-topic.png#lightbox)

1. By default, you can add trigger phrases upon creation. Add the following trigger phrases by typing them in and selecting the button after each one, until they all appear in the list.

    *Need information on swag*
    *Can I get branded clothes.*
    *What swag is available?*
    *What branded Contoso Coffee things do we have?*
    *How do I get a Contoso Coffee beanie?*

    > [!div class="mx-imgBorder"]
    > [![Screenshot highlighting to add trigger phrases.](../media/add-phrase.png)](../media/add-phrase.png#lightbox)

1. Select Details and give the topic a name by typing: **Swag Information** in the Name box. Then close details pane.

    > [!div class="mx-imgBorder"]
    > [![Screenshot highlighting tp add details.](../media/details.png)](../media/details.png#lightbox)

1. You can save your topic for now by selecting Save. There will be a pop-up that asks you if you'll save topic with errors, you can ignore it for now by selecting Save as it will be done in the steps that follow.

    > [!div class="mx-imgBorder"]
    > [![Screenshot highlighting to save trigger phrases and details.](../media/save-details.png)](../media/save-details.png#lightbox)

1. Your topic is now saved and can be edited in the authoring canvas, with your trigger phrases at the top. This is a drag and drop interface that you'll use to build out your conversation. You'll create a conversation tree with a series of messages, questions and conditional branches.

    > [!div class="mx-imgBorder"]
    > [![Screenshot highlighting that topic is saved.](../media/topic-saved.png)](../media/topic-saved.png#lightbox)

1. Add the following text into the message box: 
    
    *I can help with information about our Contoso Coffee swag.*
    Then select the **Add node** button underneath the message box and select: **Ask a question**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot highlighting to cilck on add icon.](../media/add-message.png)](../media/add-message.png#lightbox)
   
    > [!div class="mx-imgBorder"]
    > [![Screenshot highlighting to add a question.](../media/add-question.png)](../media/add-question.png#lightbox)


1. Type the following text in the question box:
    
    *What would you like to know about?*
 
    > [!div class="mx-imgBorder"]
    > [![Screenshot highlighting to add question.](../media/question.png)](../media/question.png#lightbox)

1. Power Virtual Agents can identify various types of information (known as entities) from unstructured text in the response from the user. When you add a question to your conversation tree, you choose what kind of information the bot should look for and extract from the response.  Set the Identify field to **Multiple choice options**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot highlighting to choose information to identify.](../media/choose-information.png)](../media/choose-information.png#lightbox)

1. Add the following as **Multiple choice options**. You'll see that the conditional branching is automatically created as you add each new option.
    
    *Apparel*
    
    *Accessories*
 
    > [!div class="mx-imgBorder"]
    > [![Screenshot highlighting to add multiple choice option.](../media/apparel-accessories.png)](../media/apparel-accessories.png#lightbox)

    > [!div class="mx-imgBorder"]
    > [![Screenshot highlighting to add conditions.](../media/conditions.png)](../media/conditions.png#lightbox)

1.	The response the user chooses here will be stored as a variable. Edit the variable name by selecting on the pencil icon, and then entering the name **AssetCategory** in the Variable Properties box.

    > [!div class="mx-imgBorder"]
    > [![Screenshot highlighting to enter variable properties.](../media/asset-category.png)](../media/asset-category.png#lightbox)

1.	Close the Variable Properties pane by selecting on the X and then save your chatbot by selecting the Save button.
 
    > [!div class="mx-imgBorder"]
    > [![Screenshot highlighting to save chatbot.](../media/save-variable.png)](../media/save-variable.png#lightbox)

1.	We'll add a message under each Asset Category, giving the user information about the category they choose. 

    Under the first conditional node (Apparel) select the **Add node** button and select **Show a message**:
 
    > [!div class="mx-imgBorder"]
    > [![Screenshot highlighting to add node and select show a message.](../media/show-message.png)](../media/show-message.png#lightbox)

1.	Add the following text to the message box: 

    *The Contoso Coffee apparel we have at the moment includes:*
    - *Caps*
    - *Beanies*
    - *T-shirts*
    - *Long sleeve shirts*

        > [!div class="mx-imgBorder"]
        > [![Screenshot highlighting message added in text box.](../media/message.png)](../media/message.png#lightbox)

1.	Add a node underneath the message to end the conversation with a survey. This will trigger the pre-built “End of Conversation” topic in Power Virtual Agents, which asks the user if their question was answered, and then finish with a satisfaction survey question.  
 
    > [!div class="mx-imgBorder"]
    > [![Screenshot highlighting to end conversation by selecting End with survey.](../media/end-survey.png)](../media/end-survey.png#lightbox)

    > [!div class="mx-imgBorder"]
    > [![Screenshot highlighting end of conversation.](../media/conversation-end.png)](../media/conversation-end.png#lightbox)

1.	Under the **Accessories** node, add this **message**.

    The types of accessories we have available at the moment include Contoso Coffee-branded mugs and drinking glasses.

1.	Add a node to **End with survey**.
 
    > [!div class="mx-imgBorder"]
    > [![Screenshot highlighting to add node to End with survey.](../media/add-node.png)](../media/add-node.png#lightbox)

1.	Select **Save** to save your topic.
    
## Task: Test your chatbot

1. Toggle the “Track between topics” setting in the Test bot pane to on. This means that as you test your bot, you'll see the tracking of the conversation flow across different topics.

    > [!div class="mx-imgBorder"]
    > [![Screenshot highlighting to Track between topics toggle.](../media/track-topic.png)](../media/track-topic.png#lightbox)

1. Test your chatbot in the Test bot pane by typing in one of the trigger phrases (for example, what swag is available?) and going through the conversation. You'll see the path the bot has followed indicated with green ticks in the authoring canvas, and you'll see it move from the topic you created to the built-in End of Conversation topic.
 
    > [!div class="mx-imgBorder"]
    > [![Screenshot showing to test your Test bot.](../media/home-page-virtual-agent.png)](../media/home-page-virtual-agent.png#lightbox)

1.	You can reset your Test bot pane by using the reset button at any stage.

    > [!div class="mx-imgBorder"]
    > [![Screenshot highlighting reset button to reset your Test bot.](../media/reset-button.png)](../media/reset-button.png#lightbox)

1.	Select the **Back** button to return to the Topics page.
 
    > [!div class="mx-imgBorder"]
    > [![Screenshot highlighting back button to return to Topics page.](../media/back-button-topic.png)](../media/back-button-topic.png#lightbox)
