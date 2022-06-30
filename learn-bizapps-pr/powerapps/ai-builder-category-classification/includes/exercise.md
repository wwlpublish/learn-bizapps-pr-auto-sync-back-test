In this exercise, we'll build a category classification model to help a health clinic classify and dispatch patient feedback.

Four customer experience managers are assigned the responsibility of handling customer feedback based on the department they're part of. Patient feedback is captured through a centralized email address that is identified when the patients receive their leave authorization.

## Data preparation

As with all custom models, one of the initial important steps is to identify and prepare data that will be used to train the model. AI Builder category classification is no different and requires historical data to determine patterns that will help predict the tags for new data to process.

To accelerate this exercise, you'll follow the steps described in the following page: [Use sample data to do category classification](/ai-builder/text-classification-sample-data?azure-portal=true#set-up-an-environment-with-data).

For this exercise, you'll reference the **healthcare_feedback** table that is part of the **AI Builder Lab** solution. It contains over 500 patient feedback records that are tagged with one or more of the following category keywords:

- Care

- Facilities

- Check-in

- Staff

> [!div class="mx-imgBorder"]
> ![Screenshot of the healthcare feedback table in the Power Apps Studio with highlight on the text and tags columns.](../media/feedback.png)

## Get started

The category classification model determines the potential tags after analyzing historical data. Providing records that already have categories assigned allows you to train a custom model so it can be published and used to categorize new data.

After having identified the historical data that will be used for training, it's time to create the custom model, following these steps:

1. In the Power Apps studio, in the left navigation menu, under **AI Builder**, select **Explore**, and then select the **Category classification (Custom model)**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the Power Apps Studio displaying the category classification model tile and AI Builder navigation menu.](../media/custom-model.png)

1. Select **Get Started**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the classify text model presentation with highlight on Get Started.](../media/get-started.png)

1. Select the **Select text** button.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the category classification model in the Power Apps studio with highlight on the Select text button.](../media/select-text.png)

1. Search for the **healthcare_feedback** table and select it.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the category classification model in the Power Apps Studio with a pane on the right to select the source table with highlight on healthcare_feedback.](../media/healthcare-feedback.png)](../media/healthcare-feedback.png#lightbox)

1. Select the column named **Text**, and then select **Select Column**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the category classification model in the Power Apps Studio with a pane on the right to select the text column with highlight on Text.](../media/text.png)](../media/text.png#lightbox)

1. Review the tagged text for the selected column, and then select **Next**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the category classification model in the Power Apps Studio with a list of records for the selected text column with highlight on Next.](../media/next.png)

1. Select the **Select tags** button.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the category classification model in the Power Apps Studio with highlight on Select tags.](../media/select-tags.png)](../media/select-tags.png#lightbox)

1. Select the column named **Tags**, and then select **Select Column**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the category classification model in the Power Apps Studio with a pane on the right to select the tag column with highlight on Tags.](../media/select-column.png)](../media/select-column.png#lightbox)

1. Review the different tag separator options, select **Comma**, and then select **Next**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the category classification model in the Power Apps Studio with a presentation of different separator options and the results with highlight on the option for comma.](../media/comma.png)

1. Review the text and tags to validate your selections, and then select **Next**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the category classification model in the Power Apps Studio with a presentation of a list of records with the text and tags with highlight on Next.](../media/review.png)

1. Select **English** as the text language, then select **Next**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the category classification model in the Power Apps Studio with a drop-down list of languages where English is selected and highlight on Next.](../media/language.png)

1. Review the model summary. Select **Train** to move to the next portion of this exercise.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the category classification model in the Power Apps Studio with summary information and highlight on Next.](../media/train.png)](../media/train.png#lightbox)

## Train and publish the model

After selecting the columns that contain the text and related tags for category classification, you must train the custom model before it can be used in Power Apps or Power Automate.

To complete this series of tasks, follow these steps:

1. After selecting **Train** in the last step of the previous portion of this exercise, select **Go to models**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the category classification model in the Power Apps Studio with a popup window indicating the model is training and highlight on Got to models.](../media/models.png)](../media/models.png#lightbox)

1. In the list of AI Builder models, under **My Models**, identify your newly created model that is in **Training**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the list of AI Builder models in the Power Apps Studio with highlight on My models and Training status.](../media/training.png)](../media/training.png#lightbox)

1. When the **status** changes to **Trained**, select your custom model.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the list of AI Builder models in the Power Apps Studio with highlight on My models and Trained status.](../media/trained.png)](../media/trained.png#lightbox)

1. Confirm the performance of the model by selecting **Quick test**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the category classification model in the Power Apps Studio with performance indicator and highlight on Quick test.](../media/quick-test.png)

1. Submit any text value that will allow you to determine if the model performs as expected, and then select **Test**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the Quick test pop-up window with the following text: I have a knee that hurts. Highlight on Test.](../media/test.png)

1. Review the suggested tags and confidence. You can repeat these tests multiple times. When tests are completed, select **Close**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of Quick test pop-up window with the following text: I have a knee that hurts. Highlight on suggested tag and confidence: Care - 70% and on Close.](../media/care.png)

1. If tests and performance level are adequate, select **Publish**. For situations where the performance level isn't satisfactory, you can edit the model and revise the configuration.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the category classification model in the Power Apps Studio with performance indicator and highlight on Publish.](../media/publish.png)

1. Once the model is published, you can move to the next portion of this exercise.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the category classification model in the Power Apps Studio with performance indicator and highlight on the notification message indicating the model is published.](../media/published.png)](../media/published.png#lightbox)

## Create a Power Automate cloud flow

For this exercise, we'll process the patient feedback as it is received in a Microsoft Outlook inbox by creating a cloud flow that integrates the newly created category classification model.

To create this Power Automate cloud flow, follow these steps:

1. For the newly published model, select **Use model**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the category classification model in the Power Apps Studio with performance indicator and highlight on Use model.](../media/use-model.png)

1. Select **Build intelligent automations**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the category classification model in the Power Apps Studio with a right pane where options to use the model are presented and highlight on Power Automate Build intelligent automations.](../media/build.png)](../media/build.png#lightbox)

1. You'll be redirected in a new browser tab, in Power Automate Studio, with a template that corresponds to the scenario of this exercise. Select the **Analyze incoming emails and route them to the right person** tile.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the templates available in Power Automate Studio with a tile for Analyze incoming emails and route them to the right person is highlighted.](../media/templates.png)

1. You'll be redirected to a presentation of the template. After you validated the required connections, select **Continue**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the summary for the selected template in Power Automate Studio with a list of connectors and highlight on Continue.](../media/continue.png)](../media/continue.png#lightbox)

1. You'll be redirected to the cloud flow editor with a new flow created based on the selected template. This template is built by using the prebuilt category classification model. It provides a base for this exercise. We'll modify the template to integrate the custom model. After the **Convert html to text** action, select **Add an action**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the selected flow in Power Automate Studio with highlight on Add an action.](../media/add-action.png)](../media/add-action.png#lightbox)

1. Select the **AI Builder** connector, and then in the list of actions, select **Classify text into categories with one of your custom models**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the selected flow in Power Automate Studio with highlight on AI Builder connector and Classify text into categories with one of your custom models action.](../media/classify.png)

1. Define the required parameters by selecting the custom model created during this exercise and using the output of the previous action as the text to process.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the selected flow in Power Automate Studio with highlight on the newly added action.](../media/parameters-filled.png)](../media/parameters-filled.png#lightbox)

1. Delete the **Categorize text** action.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the selected flow in Power Automate Studio with highlight on the delete option for the original Categorize text action.](../media/delete.png)](../media/delete.png#lightbox)

1. For the **Apply to each** action, select the **results** from the previously added AI Builder action as the output to loop on.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the selected flow in Power Automate Studio with highlight on the Apply to each input and pop-up for the dynamic content selection where results is selected.](../media/results.png)](../media/results.png#lightbox)

1. Edit or create the different **Case** options for the tags of the model (Staff, Facilities, Check-In, Care). For each of the options, edit or add a **Send and email (v2)** action from the Office 365 Outlook connector. Configure the **To** parameter with the adequate customer experience manager. For this exercise, if you don't have multiple accounts, you can also send them to your account and configure the **Subject** to be specific to the tag text, so you'll be able to validate the routing based on that value.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the selected flow in Power Automate Studio with highlight on the different case options and email action.](../media/case.png)](../media/case.png#lightbox)

1. For this exercise, if the monitored account (email address) is the same as the one the results are sent to, it's preferred to add a **Subject Filter** on the **When a new email arrives** trigger so the flow doesn't trigger indefinitely.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the selected flow in Power Automate Studio with highlight on the trigger and Subject Filter with Feedback as the value.](../media/subject-filter.png)](../media/subject-filter.png#lightbox)

1. Once completed, select **Save**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the selected flow in Power Automate Studio with highlight on Save.](../media/save.png)](../media/save.png#lightbox)

## Test the flow and model

Now that both the cloud flow and AI Builder model are created, it's now time to test the exercise scenario. It will use a few sample phrases to send email messages to the monitored inbox. From there, the flow will process the text using the Category Classification model and route them to the right recipient, or to the same inbox (for test purposes) with using a different subject for the sent email messages.

To test the flow, follow these steps:

1. Create and send a new email message to the monitored email address, with **Feedback** as the subject, and a sample text as the body, such as: **The doctors were very professional, nurses were kind and attentive, the room was nice but the food at the cafeteria and in room is terrible**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of a sample email with highlight on the To option, the subject as Feedback, content as The doctors were very professional, nurses were kind and attentive, the room was nice but the food at the cafeteria and in room is terrible, and Send.](../media/email.png)

1. You should then receive a new email with the category classification. This confirms the flow processed the sent message.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the selected flow in Power Automate Studio with highlight on Your flow ran successfully notification message.](../media/success.png)](../media/success.png#lightbox)

You've now successfully created a custom category classification AI Builder model and integrated it in a Power Automate flow.
