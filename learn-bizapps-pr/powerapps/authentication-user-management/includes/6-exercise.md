The purpose of this hands-on lab is to introduce the Power Apps portals invitation-based user registration process.

The exercises work best when you have sample data to work with. Depending on the environment that you are working with, you might want to install sample data to assist with the exercises. Dynamics 365 does provide the ability to add sample data, as needed. If the environment that you are working in does not have sample data installed, follow the steps in the [Add or remove sample data](/power-platform/admin/add-remove-sample-data/?azure-portal=true) documentation to install the sample data into your environment.

## Learning objectives

At the end of these exercises, you will be able to:

- Customize an invitation template.
- Create and send invitations to contacts to register.
- Redeem invitations.
- Extend the invitation process by a custom workflow.

**Estimated time to complete this exercise**: 10 to 15 minutes

### Prerequisites

The prerequisites for this exercise are as follows:

1. System Administrator access to the Dynamics 365 instance with Dynamics 365 for Customer Service solution installed.
1. A provisioned Customer self-service, Community, or Customer Power Apps portal.
1. An enabled and working server-side email synchronization.

When you provision a Dynamics 365 for Customer Engagement trial, Office 365 licenses are not provisioned automatically and the email integration will not work. To enable server-side email synchronization, follow the subsequent procedure.

> [!IMPORTANT]
> You must be an Office 365 Global Administrator to complete this configuration.

1. Go to the [Admin portal](https://portal.office.com/adminportal/?azure-portal=true).
1. Select **Billing > Purchase Services**.
1. Locate the **Office 365 E3** product and select the **Get free trial** option.
1. Assign the Office 365 license to your user account.
1. Open the [Microsoft Power Platform admin center](https://aka.ms/ppac/?azure-portal=true).
1. Select **Environments**, select your environment, and then select **Settings**.
1. Select **Mailboxes**.
1. Open your mailbox record and select **Approve Email**.
1. Select **Test & Enable Mailbox**.
1. Ensure that the **Outgoing Email Status** field has the **Success** value.

## Scenario

Your organization has been using Dynamics 365 for Customer Engagement for some time and has been recording information about customers and suppliers. You have provisioned and configured a Power Apps portal. You want to invite one of your suppliers who is responsible for your websites to register as an administrative portal user so that they are able to sign in and administer the portal by using the front-end interface.

## High-level steps

To send invitations to your customers, and for them to redeem the invitations, complete the following tasks:

- Modify the Send Invitation template.
- Select a contact and create an invitation.
- Ensure that the invitation contains required information.
- Send the invitation to the contact.

### Create a test contact

To create a test contact, follow these steps:

1. Open [Dynamics 365 Home](https://dynamics.microsoft.com/?azure-portal=true).
1. Select the **Power Apps portals** app.
1. Select **Contacts** and then select **New**.
1. Create a new record for Nancy Davolio. Fill in the first name, last name, and email address information (*use an email address where you can receive the email*).
1. Select **Save**.

### Customize the workflow

The workflow process of sending the invitation email is generic and needs to be customized prior to use.

1. Open the [Power Apps portal](https://make.powerapps.com/?azure-portal=true).

1. Select **Solutions**, and then locate and select **Default Solution**.

1. Change the filter from **All** to **Processes**.

1. Locate and open the **Send Invitation** workflow process.

   > [!TIP]
   > Use search to locate the process.

1. Deactivate the workflow.

1. Select **Set properties** for the **Create an email to act as an email template** step.

1. Enter the **Subject** as **Join our community**.

1. Replace the content of the email template with the following sample content. Use the workflow editor to insert values for the **First Name** field from **Invited Contact** and use the hyperlink button to insert the link and **Encoded Invitation Code** value.

   ```al
   Dear {First Name(Invite Contact (Contact));customer}

   invites you to join our community. To redeem your invitation, please follow <hyperlink><name>this link</name><value>https://yourportalurl.powerappsportals.com/register/?returnurl=%2f&invitation={Encoded Invitation Code(Encode Invitation Code)}</value></hyperlink>

   Best regards
   Contoso Team
   ```

1. Activate the workflow.

### Create and send the invitation

To create and send the invitation, follow these steps:

1. Open the Nancy Davolio contact record.
1. Select **Create Invitation**.
1. The invitation will be prepopulated. Select **Save**.
1. Under **Assign to Web Roles**, select **Add Existing Web Role**.
1. Search and add the **Administrators** role.
1. Select **Flow > Send Invitation**. Confirm that the invitation has been sent.

### Redeem the invitation

To redeem the invitation, follow these steps:

1. Open the mailbox for the email that you used for Nancy Davolio.

1. Locate and open the invitation email.

   > [!NOTE]
   > Server-side synchronization might take up to 15 minutes to synchronize and send the email.

1. Select the link in the email.

   The **Redeem Invitation** page will open.

1. Select **Register**.

1. Enter username **nancyd** and then a password of your choice.

1. Select **Register**.

   Your account will be registered and you will be signed in automatically and redirected to the profile page. The front-side editing toolbox will appear, and you will see the **Edit** button when hovering over the elements of the page. The ability to edit indicates that you have been automatically assigned the role with sufficient front-side editing privileges (Administrators in this case).

1. Switch to the Power Apps portals app.

1. Select **Invitations** and then select the **Completed Invitations** view.

1. Confirm that the **Nancy Davolio** invitation is listed.

1. Open the invitation and confirm that **Status Reason** is now **Redeemed**.
