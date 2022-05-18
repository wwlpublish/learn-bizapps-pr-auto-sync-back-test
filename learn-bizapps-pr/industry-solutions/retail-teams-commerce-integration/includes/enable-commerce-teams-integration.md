In this lab, you’ll play the role of an IT administrator and will enable Microsoft Dynamics 365 Commerce and Microsoft Teams integration.

In this exercise, you'll complete the following tasks:

1. Create users in the tenant for these personas:

    - Retail communication manager

    - Store manager

    - Store employee

1. Associate an external identity for the worker in Dynamics 365 Commerce.

1. Add the Retail Task Manager role to the retail communication manager who publishes tasks.

1. Customize the POS screen layout to add task management.

1. Provision Teams in Commerce Finance and Operations.

1. Validate Teams provisioning in the Teams admin center.

1. Download Commerce organizational hierarchy to Teams.

1. Install the Microsoft Teams PowerShell module.

1. Upload organization hierarchy to Teams.

1. Publish a test task list in Teams.

## Task 1: Create user roles for personas

In this task, you’ll create user roles for the retail communication manager, store manager, and store employee personas.

> [!Important]
> To perform this task, you’ll need administrator access to the tenant to create users.

1. Sign in to [Microsoft 365 admin center](https://admin.microsoft.com/?azure-portal=true) and create users in the tenant that you're using.

1. Create a user by selecting **Add user** in the **User management** section. This user will act as retail communication manager.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of Microsoft 365 admin center showing Support remote workers with Teams and User management.](../media/add-user.png)](../media/add-user.png#lightbox)

1. Create the user and assign licenses. Update the fields as below:

    - **First name**: Michael

    - **Last name**: Ellen

    - **Username**: michaelellen

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Add a user dialog, showing the Set up the basics page with information filled in.](../media/basics.png)](../media/basics.png#lightbox)

1. Because the retail communication manager will be publishing tasks for store employees by using Microsoft Teams, make sure that they’re assigned a Microsoft 365 E5 license.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the checklist of licenses with Microsoft 365 E5 selected.](../media/office-365-e-5.png)](../media/office-365-e-5.png#lightbox)

1. In the **Add a user** dialog, under the **Profile info** section, set the **Job title** to **Retail communications manager** so that the title will appear in Teams. Set the department to **Fabrikam retail**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Add a user dialog, showing the job title being entered on the Optional settings page.](../media/optional.png)](../media/optional.png#lightbox)

1. Create a user who will act as store manager to sign in to POS and assign tasks to store employees. To do so, enter the user’s information in the **Basics** page.

    - **First name**: Emma

    - **Last name**: Harris

    - **Username**: emmah

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Basics page filled out for the store manager.](../media/manager.png)](../media/manager.png#lightbox)

1. Because the store manager will sign in to POS, assign the Microsoft Dynamics AX7 User Trial license.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Product licenses page in the Add a user dialog with Microsoft Dynamics AX7 User Trial selected.](../media/commerce.png)](../media/commerce.png#lightbox)

    > [!Note]
    > In an actual customer environment, you'd choose Dynamics 365 Commerce instead of the AX7 User Trial license.

1. In the **Add a user** dialog, on the **Optional settings** page, set the **Job title** to **Store manager**, and the **Department** to **Fabrikam Retail**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Add a user dialog Optional settings page with job title and department fields filled in.](../media/manager-2.png)](../media/manager-2.png#lightbox)

1. Repeat the previous steps to create a user for store employee and then assign the appropriate licenses. Update the fields below:

    - **First name**: Chris

    - **Last name**: Gallagher

    - **Username**: chrisg

    - **Profile info**: Store employee

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the employee user added to the list of users.](../media/employee.png)](../media/employee.png#lightbox)

1. Make sure that the store employee has the AX7 User Trial and Microsoft 365 E5 licenses assigned so that they can sign in to Microsoft Teams and mark their tasks as completed.

    > [!Note]
    > In an actual customer environment, you'd choose Dynamics 365 Commerce instead of the AX7 User Trial license.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the Licenses check list showing Microsoft 365 E5 and Microsoft Dynamics AX7 User Trial selected.](../media/licenses.png)

## Task 2: Create an external identity for the worker in Commerce

To create an external identity for the worker in Commerce, follow these steps:

1. On the **Finance and Operations** page, on the left pane, select **Modules**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Finance and Operations navigation pane with Modules highlighted.](../media/modules.png)](../media/modules.png#lightbox)

1. Scroll down in the list of options until you find **Retail and Commerce**.

1. In the right menu, expand **Channels**, expand **Stores**, and then select **All stores**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Retail and Commerce page, with the Channels and Stores nodes expanded to show All stores.](../media/stores.png)](../media/stores.png#lightbox)

1. Scroll to the **Houston** store in the grid.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Stores page with the Retail Channel I D and Name for Houston highlighted.](../media/retail.png)](../media/retail.png#lightbox)

1. On the top menu, select **Set up > Workers**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Set up page with the Workers option highlighted.](../media/workers.png)](../media/workers.png#lightbox)

1. Find the employee, Chris Gallagher, who is a store employee. You can find the role details by selecting the employee's name.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Worker page with the store employee selected.](../media/worker-manager.png)](../media/worker-manager.png#lightbox)

1. After identifying the store employee, associate an Azure Active Directory identity for the employee so that they can sign in to Microsoft Teams. To do so, select **Commerce > Associate existing identity**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Commerce page with the Associate existing identity button highlighted.](../media/create-identity.png)](../media/create-identity.png#lightbox)

1. In the search options, select **Search using email**, and provide the email account that was created as part of Task 1, then select **OK**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Use existing external identity  dialog showing the search results for chrisg.](../media/use-existing.png)](../media/use-existing.png#lightbox)

1. On the Commerce tab, update the fields with these values:

    - **Block POS login**: No

    - **User needs to change the password**: No

    - **Password**: Set the password and make a note of it. (You can assign the same password you used when you created the user in the tenant.)

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Create new identity entry with the Alias and Password fields highlighted.](../media/password.png)](../media/password.png#lightbox)

1. Repeat the previous steps to associate the store manager to their user identity in stores, as shown in the following image.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Commerce page for an employee, showing them being connected to an external identity.](../media/external-identity.png)](../media/external-identity.png#lightbox)

1. Repeat the same steps for all stores that you want to integrate with Microsoft Teams.

1. Assign the person to user Chris Gallagher (store employee in this example), and assign **Retail store manager** to the roles, so that the user can use POS to update tasks.

    1. Navigate to **Retail and Commerce > Employees > Users**.

        > [!div class="mx-imgBorder"]
        > [![Screenshot of the Retail and Commerce page with Employees expanded and Users selected.](../media/users-2.png)](../media/users-2.png#lightbox)

    1. On the **Users** form, in the **Username** field, search for the username "Chris" as below. Then select the **User ID** field to open the user details.

        > [!div class="mx-imgBorder"]
        > [![Screenshot of the Commerce page with Chris selected.](../media/users-3.png)](../media/users-3.png#lightbox)

    1. On the person, drop down the lookup field for person and choose “Chris Gallagher” as shown below.

    1. Select **Assign roles** and choose **Retail store manager** to assign the role to the user as below.

        > [!div class="mx-imgBorder"]
        > [![Screenshot of the employee page, showing assign roles selected and the Assign roles to user dialog with retail store manager selected.](../media/retail-manager.png)](../media/retail-manager.png#lightbox)

    1. Once assigned it appears as below.

        > [!div class="mx-imgBorder"]
        > [![Screenshot of the employee page, showing retail store manager added to the roles.](../media/roles.png)](../media/roles.png#lightbox)

1. Follow the previous steps to verify that the user “Emma Harris” is associated to the Employee role and check that the user has the **Retail store manager** role.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the employee page for Emma, showing retail store manager added to the roles.](../media/role.png)](../media/role.png#lightbox)

1. To update the login method in the functionality profile of the store, navigate to **Retail and Commerce > All stores**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Finance and Operations navigation pane with Retail and Commerce selected, Channels expanded, and Stores expanded to reveal All stores.](../media/stores-2.png)](../media/stores-2.png#lightbox)

1. After opening the Stores form, scroll to the **Houston** store on the grid. Select the **Retail Channel Id** field to open the store details form.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Stores page showing the Houston store's retail channel I D selected.](../media/houston.png)](../media/houston.png#lightbox)

1. On the store tab page, select the **Functionality profile** field as highlighted below.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Houston page showing the Functionality profile field highlighted under P O S Register.](../media/functionality.png)](../media/functionality.png#lightbox)

1. On the Functionality profile form, select **Edit** and set the **Logon Authentication Method** to **Azure AD with single sign-on**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the P O S functionality profiles with P O S  staff logon authentication method set to Azure A D with single sign-on.](../media/single.png)](../media/single.png#lightbox)

## Task 3: Create user and assign the retail task manager role

To create a user and assign the retail task manager role, follow these steps:

1. Navigate to **Retail and Commerce > Employees > Users**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Finance and Operations navigation menu with Retail and Commerce selected and the Employees menu expanded to show Users.](../media/users.png)](../media/users.png#lightbox)

1. Select **Import users** as shown below. In the Import users form, choose **Michael Ellen**, the retail communication manager created as part of Task 1.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the users list with the store manager user I D selected.](../media/user-id.png)](../media/user-id.png#lightbox)

1. Select the user, then select **Assign roles**.

    > [!div class=”mx-imgBorder”]
    > [![Screenshot of the User details page for the manager, showing the Assign roles button.](../media/assign-roles.png)](../media/assign-roles.png#lightbox)

1. Select **Retail task manager** and then select the **OK** button.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Assign roles to user dialog with Retail task manager selected.](../media/retail-task-manager.png)](../media/retail-task-manager.png#lightbox)

Congratulations, you’ve successfully imported the user and assigned the Retail task manager role to the task manager.

## Task 4: Customize the POS screen layout to add task management

The POS application from Dynamics 365 Commerce has task management features that allow store managers and workers to manage tasks and update task status. Store workers can access tasks by selecting the **Tasks** tile on the POS home page or by selecting task notifications.

By default, the **Task management** button isn't available in the POS screen layout; hence, in this task, you'll add the **Task management** action to the POS screen layout. After you’ve added this button, the store workers will be directed to the **My tasks** tab, where they can view the tasks that are assigned to them. However, they can switch to the **Overdue tasks**, **Open tasks**, and **Task lists** tabs as needed.

1. Go to the Finance and Operations URL and go to the **Retail and Commerce** module from the navigation pane. Go to **Channel setup > POS setup > POS** and then go to **Screen layouts**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the navigation pane with Channel setup expanded to show Channel profiles, P O S setup, P O S, with Screen layouts highlighted.](../media/screen-layouts.png)](../media/screen-layouts.png#lightbox)

1. On the **Screen layouts** page, you can choose to design any screen layout and then assign it to the worker who’s associated with your user. For this example, select **A3MGR**, which is the screen layout assigned to the store manager (Emma Harris). Select the screen layout to navigate the screen layout form. Use the designer to customize the button grids. In this example, you’ll choose **Welcome screen1** and then select **Designer**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Screen layouts page with the Designer button highlighted.](../media/designer.png)](../media/designer.png#lightbox)

1. After you’ve selected the designer, a pop-up window will appear asking you to sign in to access the designer. Sign in with the admin account that you’ve used for this exercise.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Microsoft Dynamics sign-in page.](../media/sign-in.png)](../media/sign-in.png#lightbox)

   The designer will show the screen layout editor, as shown in the following screenshot.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the screen layout editor.](../media/editor.png)](../media/editor.png#lightbox)

1. Add a button called **Task management** next to the **Current transaction** button. Right-click the first button with the shopping bag icon and then select **Button properties**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Button grid design context menu with the Button properties option highlighted.](../media/button-properties.png)](../media/button-properties.png#lightbox)

1. In the button properties, change the **Size in columns** value from **4** to **2**, as shown in the following image. Select **Save**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Appearance properties showing Size in columns set to 2.](../media/columns.png)](../media/columns.png#lightbox)

1. The screen layout will resemble the following image. Select **New button** to add the new button beside the **Current transaction** button.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Button grid design with the New button option highlighted.](../media/new-button.png)](../media/new-button.png#lightbox)

1. Select **Button properties** to set properties for the new button.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Button grid design with the Button properties option highlighted.](../media/button-properties-2.png)](../media/button-properties-2.png#lightbox)

1. Select **Button properties** to set the following properties for the new button:

    **Action**: Task management

    **Button text**: Task management

    **Size in columns**: 2

    **Size in rows**: 2

    **Use custom theme**: Select this checkbox

    **Back color**: Choose an appropriate color that matches the screen layout

    **Select image**: Choose an image that’s suitable for task management

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Configure button with properties set and the Select image button highlighted.](../media/select-image.png)](../media/select-image.png#lightbox)

1. After you’ve selected the screen, the layout will be updated with the new **Task management** button, as shown in the following screenshot.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Button grid design updated with the new button.](../media/updated.png)](../media/updated.png#lightbox)

1. To publish the screen layout changes, go to **Retail module** > **Retail and Commerce IT**, and then select **Distribution schedule**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the navigation pane with Distribution schedule selected.](../media/distribution-schedule.png)](../media/distribution-schedule.png#lightbox)

1. Select **All jobs** from the list of jobs and then select **Run now**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the list of jobs with All jobs selected and the Run now button highlighted.](../media/all-jobs.png)](../media/all-jobs.png#lightbox)

1. After the job has run, a message will display, indicating that it's been added to the batch queue.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the message stating that the incremental sync with schedule 9999 job is added to the batch queue.](../media/queue.png)](../media/queue.png#lightbox)

1. After the job has run, you can select the **History** button to check the status of the job.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Download history page showing the status as Available.](../media/history.png)](../media/history.png#lightbox)

## Task 5: Provision Teams in Commerce

To provision Teams in Commerce, go to the Finance and Operations page and follow these steps:

1. Go to **Retail and Commerce** > **Channel setup** > **Microsoft Teams Integration Configuration**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Finance and Operations navigation pane with Retail and Commerce selected and Channel setup expanded to reveal Microsoft Teams Integration Configuration.](../media/integration-configuration.png)](../media/integration-configuration.png#lightbox)

1. Under **Settings**, set the **Enable Microsoft Teams Integration** option to **Yes**.

1. Provide the **Application ID** (also referred to as **Client ID**), that was generated during the application registration process in Task 1.

1. Provide the **Application key** (also referred to as **App password**). It's the value that’s generated from the application secret key that was generated in the previous steps.

1. Select **Save** after you’ve updated all values.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of Microsoft Teams Integration Configuration settings with values filled in and integration enabled.](../media/enable.png)](../media/enable.png#lightbox)

1. On the Action Pane, select **Provision teams**. A batch job named **Teams provision** will be created.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Microsoft Teams Integration Configuration page with the Provision teams option highlighted.](../media/provision-teams.png)](../media/provision-teams.png#lightbox)

1. Go to **System administration > Inquiries > Batch jobs**. Find the most recent job that has the description of **Teams provision**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the navigation pane with System administration selected and Inquiries expanded to reveal Batch jobs.](../media/batch-jobs.png)](../media/batch-jobs.png#lightbox)

1. Wait until this job has finished running.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the list of jobs with the Teams provision job showing with a status of Ended.](../media/ended.png)](../media/ended.png#lightbox)

## Task 6: Validate Teams provisioning in the Teams admin center

To validate Teams provisioning in the Teams admin center, follow these steps:

1. Go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/?azure-portal=true) and sign in as the administrator of your e-commerce tenant.

1. In the left navigation pane, expand the **Teams** menu and then select **Manage teams**.

1. Confirm that one team has been created for each Commerce retail store.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Manage teams page in the Microsoft Teams admin center.](../media/manage-teams.png)](../media/manage-teams.png#lightbox)

1. Select a team and then confirm that store workers have been added to it as members.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the list of members in Teams.](../media/members.png)](../media/members.png#lightbox)

## Task 7: Download Commerce organizational hierarchy to Teams

To download the Commerce organizational hierarchy to Teams, follow these steps:

1. In the **Finance and Operations** page in Commerce, navigate to **Modules > Retail and Commerce > Channel setup > Microsoft Teams Integration Configuration**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the navigation pane expanded to show Microsoft Teams Integration Configuration.](../media/integration-configuration.png)](../media/integration-configuration.png#lightbox)

1. In the **Download targeting hierarchy** dropdown menu, select **Retail Stores by Region** to download a comma-separated values (CSV) file of the organizational hierarchy.

1. Select **Download** to save to a local folder in your computer.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Download targeting hierarchy menu expanded to show the Retail Stores by Region hierarchy selected and the Download button highlighted.](../media/hierarchy.png)](../media/hierarchy.png#lightbox)

## Task 8: Install the Microsoft Teams PowerShell module

**Requirements**: Microsoft Teams PowerShell module requires PowerShell 5.1 or higher on all platforms. Install the [latest version of PowerShell](/powershell/scripting/install/installing-powershell/?azure-portal=true) that’s available for your operating system.

1. Check your PowerShell version. To do so, run the following command from within a PowerShell session:

    `$PSVersionTable.PSVersion`

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the version command in PowerShell.](../media/version.png)](../media/version.png#lightbox)

1. Install by using the PowerShell Gallery.

    `Install-Module -Name PowerShellGet -Force -AllowClobber`

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the allow clobber command in PowerShell.](../media/clobber.png)](../media/clobber.png#lightbox)

1. Install the Teams PowerShell module.

    `Install-Module -Name MicrosoftTeams -Force -AllowClobber`

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the command in PowerShell.](../media/teams-power-shell.png)](../media/teams-power-shell.png#lightbox)

With Windows computers, you might get an error if the execution policy is set to **Restricted**. Set the execution policy to **Unrestricted** to continue further. For more information, see [Set-ExecutionPolicy (Microsoft.PowerShell.Security)](/powershell/module/microsoft.powershell.security/set-executionpolicy/?azure-portal=true).

## Task 9: Upload the organization hierarchy to Teams

To upload the organization hierarchy to Teams, follow these steps:

1. To start working with the Microsoft Teams PowerShell module, sign in with your Azure credentials.

1. **Run** the following command in PowerShell to authenticate.

1. Enter the `Connect-MicrosoftTeams` command, which will result in a prompt asking you to sign in to Teams.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the connect command in PowerShell.](../media/connect.png)](../media/connect.png#lightbox)

1. After you’ve signed in to Teams, upload the TargetingHierarchy.csv to Microsoft Teams. You'll use Microsoft Teams PowerShell module and cmdlet `Set-TeamTargetingHierarchy` that were installed in the previous steps.

    `Set-TeamTargetingHierarchy -FilePath "C:TargetingHierarchy.csv"`

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the team targeting hierarchy command in PowerShell.](../media/set-hierarchy.png)](../media/set-hierarchy.png#lightbox)

1. Run the following command to check the status of your hierarchy upload.

    `Get-TeamTargetingHierarchyStatus`

1. The command will return the following fields:

    | Field | Description |
    |-------|-------------|
    | ID | The unique ID for the upload. |
    | Status | Upload status. Values include **Starting**, **Validating**, **Successful**, and **Failed**. |
    | ErrorDetails | Details if an upload error has occurred. For more information, see the **Troubleshooting** section. If no error has occurred, this field will be blank. |
    | LastUpdatedAt | Timestamp and date of when the file was last updated. |
    | LastModifiedBy | The ID of the last user who modified the file. |
    | Filename | The file name of the CSV. |

## Task 10: Link POS and Teams for task management

To link POS and Teams for task management, follow these steps:

1. Go to **Retail and Commerce > Task management > Tasks integration with Microsoft Teams**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the navigation pane with Retail and Commerce selected and with Task management expanded to reveal Tasks integration with Microsoft Teams.](../media/tasks-integration.png)](../media/tasks-integration.png#lightbox)

1. Set the **Enable Task Management Integration** toggle to **Yes**.

1. On the Action Pane, select **Setup task management**. You should receive a notification indicating that a batch job named **Teams provision** is being created.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Setup task management option selected and the Enable Task Management Integration toggle set to Yes.](../media/setup-task.png)](../media/setup-task.png#lightbox)

1. Provide your credentials if you’re asked for authentication. Select **Close** to continue.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the message stating that you have successfully completed the authentication process.](../media/success.png)](../media/success.png#lightbox)

1. Go to **System administration > Inquiries > Batch jobs**. Find the most recent job that has the description of **Teams provision**. Wait until this job has finished running.

1. Run the **CDX job 1070** to publish the plan ID and store the references to the Microsoft Cloud for Retail server.

Congratulations, you’ve completed this exercise, where you played the role of an IT administrator and successfully enabled Dynamics 365 Commerce and Microsoft Teams integration.
