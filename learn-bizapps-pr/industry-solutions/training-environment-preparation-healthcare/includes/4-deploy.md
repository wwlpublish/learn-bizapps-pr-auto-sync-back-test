
A security role defines how users, such as a clinician, field service agent, or knowledge base creator, can access different types of resources. To work with Microsoft Cloud for Healthcare solutions, make sure that you assign correct security roles to users. In this unit, you'll learn about the required security roles that you'll need to assign to a user and an Azure AD app. For more information, see [Security roles and privileges](/power-platform/admin/security-roles-privileges) in Microsoft Power Platform.

| Security roles                   | Description                                                                                                                                                         |   
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Basic User                       | Allows the user to run an app within the Dataverse environment and perform common tasks for the records that they own.                                              |   
| Field Service - Resource         | This role is designed for frontline workers who can read and update their assigned work orders.                                                                     |   
| Knowledge Manager                | Allows the user to create/read/write/delete/append knowledge base records.                                                                                          |     |
| Omnichannel agent                | Allows the user to perform agent tasks.                                                                                                                             |   
| Productivity tools administrator | Required by administrators of Dynamics 365 productivity tools. Allows the administrator to create/read/write/append/delete agent script, script step, and workflow. |   
| Productivity tools user          | Required by users of Dynamics 365 productivity tools. Allows the user to read agent script, script step, and workflow.                                              |   
| System Administrator             | Grants full permission for the user to customize or administer a Dataverse environment.                                                                             |  
| Customer service manager         | Allows a user to review customer service performance and enable the customer service process.                                                                       |   
| Customer service representative  | Allows a user to document customer service events and respond to customer service inquiries.                                                                        |   

## Task 1: Assign a security role to a global administrator

In this task, you'll go through the steps to assign security roles to a global administrator account.

1.  While signed in to your Microsoft 365 tenant, open a new tab and then go to [Power Platform admin center](https://admin.powerplatform.microsoft.com/).

2.  On the left navigation, select **Environments**. In the right pane, select **Lamna Healthcare** environment. On the command bar, select **Settings**, as shown in the following screenshot.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of Environment page with Settings option highlighted.](../media/security-roles-users.png)](../media/security-roles-users.png#lightbox)

3.  On the **Settings** page, select **Users + permissions \> Users**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of User + Permissions page with this option highlighted.](../media/security-user-permission.png)](../media/security-user-permission.png#lightbox)

4.  Select a user who you want to assign security roles to.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of Users page.](../media/security-users.png)](../media/security-users.png#lightbox)

5.  Assign the following security roles:

    -   Basic User

    -   Field Service-Resource

    -   Knowledge Manager

    -   Omnichannel agent

    -   Productivity tools administrator

    -   Productivity tools user

    -   System Administrator

6.  When you're finished selecting security roles, select **Save**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of Purchase services, with Add-ons and Details highlighted.](../media/security-manage-roles.png)](../media/security-manage-roles.png#lightbox)

## Task 2: Assign a security role to an application user

In this task, you'll go through the steps to assign security roles to the Lamna Health Bot app that you registered in Azure AD in the previous unit.

1.  While signed in to your Microsoft 365 tenant, open a new tab and then go to [Power Platform admin center](https://admin.powerplatform.microsoft.com/).

2.  On the left navigation, select **Environments**. In the right pane, select **Lamna Healthcare** environment. On the command bar, select **Settings**, as shown in the following image.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of Environment page with Settings and Lamna Healthcare highlighted.](../media/security-roles-users.png)](../media/security-roles-users.png#lightbox)

3.  On the **Settings** page, select **Users + permissions \> Application users**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of Application users option highlighted.](../media/security-application-users.png)](../media/security-application-users.png#lightbox)

4.  Before you can assign a security role to an application, you'll need to add it as an application user. On the **Application users** page, select **+New app user**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of Application users page with New app user option highlighted.](../media/security-new-app-user.png)](../media/security-new-app-user.png#lightbox)

5.  In the **Create a new app user** panel, select **+ Add an app**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of Add an app option highlighted.](../media/security-add-application.png)](../media/security-add-application.png#lightbox)

6.  In the **Add an app from Azure Active Directory** panel, select **Lamna Health Bot**, which you registered in Azure AD in the
    previous task. Select **Add**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of Add an app from Active Directory page.](../media/security-add-active-directory.png)](../media/security-add-active-directory.png#lightbox)

7.  After adding the Azure AD app, you'll be redirected to the **Create a new app user** panel. From the **Business unit** dropdown menu, select **lamnahealth**. Select the **edit** icon beside the **Security roles** option.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of Create a new app user page with Lamna health selected.](../media/security-create-new-application.png)](../media/security-create-new-application.png#lightbox)

> [!NOTE]
> In the previous unit, you specified lamnahealth as part of the URL while creating the **Lamna Healthcare**  Dataverse environment.*

8.  In the **Add security roles** pane, select **Omnichannel agent** and then select **Save**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of Manage Security Roles page with roles selected.](../media/security-add-roles.png)](../media/security-add-roles.png#lightbox)

9.  You'll be redirected to the **Create a new app user** panel, which should appear as shown in the following screenshot. Select **Create** to add Lamna Health Bot as an application user and assign it the Omnichannel agent security role.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of Create a new app user page with Lamna health bot selected.](../media/security-create-new-app-user.png)](../media/security-create-new-app-user.png#lightbox)

**Congratulations**, you've successfully assigned all security roles to the global administrator account and Azure AD app.
