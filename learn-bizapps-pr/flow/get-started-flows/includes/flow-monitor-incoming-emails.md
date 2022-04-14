You can create a flow that automatically performs one or more actions after it's triggered by an event. For example, the flow can monitor your Outlook inbox and when an email with a specific subject line and email address arrives, the flow will take the attachment and save it to a SharePoint library.

## Prerequisites

Microsoft Office 365

## Specify the SharePoint site and library
You can use any SharePoint site of your choice and can also use an existing library.

In this scenario, we'll use the following SharePoint site and its default **Documents** library, which is available out-of-box.

![Screenshot of the SharePoint site.](../media/sharepoint-site.png)

## Specify an event to start the flow

First, you must select the trigger (event) that starts the flow.

1. Sign in to [Power Automate](https://flow.microsoft.com) by using your organizational account.

1. Select **My flows**.

1. Select **New flow**, and then select **Automated cloud flow**.

    ![Screenshot of power automate automated cloud flow.](../media/automated-cloud-flow.png)

1. Under **Choose your flow's trigger**, enter *Outlook*, select the **When a new email arrives (V3)** trigger and select **Create**.

    ![Screenshot of selecting Outlook trigger.](../media/create-a-flow.png)

1. Expand **Show advanced options**.

    ![Screenshot of advanced options.](../media/outlook-when-a-new-email-arrives-trigger.png)

1. Add the following:

    **From** -  'no-reply@contoso.com'

    **Include Attachments** - 'Yes'

    **Subject Filter** - 'Daily report'

    **Only with Attachments** - 'Yes'

    ![Screenshot of advanced settings.](../media/advanced-options-settings.png)

## Specify an action

1. Select **New step**, and in the search field, enter *SharePoint*, and then select the **create file** action.

    ![Screenshot of the Office 365 Outlook send an email action.](../media/create-file-action.png)

1. Add the following:

     **Site Address** - Either copy and paste your URL or select the drop-down and select your site
 
     **Folder Path** - Select **/Shared Documents**
 
     **File Name** - Select **Attachments Name** from **Dynamic Content**

     **File Content** - Select **Attachments Content** from **Dynamic Content**

    ![Screenshot of add attachments options.](../media/add-attachments.png)

1. Once the **Attachments Name** is added the **Create file** action is automatically added in an **Apply to each**. This will take care of scenarios when an email comes in with multiple attachments.

    ![Screenshot of the apply to each button.](../media/apply-to-each.png)

You have successfully built a **Power Automate** flow, which will monitor your **Outlook** inbox for any emails that have the text **Daily report** in their **Subject line** and have **Attachments**.

![Screenshot of the flow design.](../media/flow-design.png)