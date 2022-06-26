When it comes to Canvas Apps, we'll be specifying the users we identified on a previous phase to run the app, but we can also specify who can modify the app, and even reshare it with other users. You can also share the app with the entire organization if the app was built to be used by everyone.

Here are the steps to share our Canvas App.

1.  Sign in to [Power Apps](https://make.powerapps.com/?azure-portal=true).

1.  On the left pane, select **Apps**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of Apps in the Power Apps menu.](../media/apps.png)](../media/apps.png#lightbox)

1.  Select the app that you want to share by selecting its icon.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the app selected.](../media/app-selected.png)](../media/app-selected.png#lightbox)

1.  On the command bar, select **Share**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the share button on the command bar.](../media/share.png)](../media/share.png#lightbox)

1.  Specify by name or alias the users or security groups in Azure AD with whom you want to share the app.

    In this case, we'll allow our technicians to run the app (but not modify or share it), we enter **Technicians** in the sharing panel. Users inside the Technicians Group will be able to find this app by setting the apps list filter to "Org apps".

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the people menu used to selected share feature.](../media/people.png)](../media/people.png#lightbox)

    You can share an app with a list of aliases, friendly names, or a combination of those (for example, Amber Rodriguez `amber.rodriguez@contoso.com`) if the items are separated by semicolons. If several people have the same name but different aliases, the first person found will be added to the list. A tooltip appears if a name or alias already has permission or can't be resolved.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of an individual name in the lookup feature.](../media/individual-name.png)](../media/individual-name.png#lightbox)

	> [!NOTE]
	> You can't share an app with a distribution group in your organization or with a group outside your organization.

1.  If you want to allow users to edit and share the app, select the **Co-owner** check box.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the co-owner checkbox for user.](../media/co-owner.png)](../media/co-owner.png#lightbox)

	In the sharing UI, you can't grant Co-owner permission to a security group if you [created the app from within a solution](/power-apps/maker/canvas-apps/add-app-solution/?azure-portal=true). However, it's possible to grant co-owner permission to a security group for apps in a solution by using the [Set-PowerAppRoleAssignment cmdlet](/powershell/module/microsoft.powerapps.administration.powershell/set-adminpowerapproleassignment/?azure-portal=true).

	> [!NOTE]
	> Regardless of permissions, no two people can edit an app at the same time. If one person opens the app for editing, other people can run it but not edit it.

1.  If your app connects to data for which users need access permissions, specify security roles as appropriate.

	For example, your app might connect to a table in a Dataverse database. When you share such an app, the sharing panel prompts you to manage security for that table.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the assign a security role menu.](../media/security-role.png)](../media/security-role.png#lightbox)

	For more information about managing security for a table, go to [Manage table permissions](/power-apps/maker/canvas-apps/share-app?azure-portal=true#manage-table-permissions).

	If your app uses connections to other data sources such as an Excel file hosted on OneDrive for Business ensure that you share these data sources with the users you shared the app with.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the data permissions.](../media/data-permissions.png)](../media/data-permissions.png#lightbox)

	For more information about sharing canvas app resources and connections, go to [Share canvas app resources](/power-apps/maker/canvas-apps/share-app-resources/?azure-portal=true).

1. If you want to help people find your app, select the **Send an email invitation to new users** check box.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the email invitation checkbox.](../media/email.png)

1. At the bottom of the share panel, select **Share**.

	Users can now run the app by using Power Apps Mobile on a mobile device or from AppSource on [Microsoft 365](https://www.office.com/apps/?azure-portal=true) in a browser. Co-owners can edit and share the app in [Power Apps](https://make.powerapps.com/?azure-portal=true).

If you sent an email invitation, users can also run the app by selecting the link in the invitation email:

-   If a user selects the link on a mobile device, the app opens in Power Apps Mobile.

-   If a user selects the link on a desktop computer, the app opens in a browser.

Co-owners who receive an invitation get another link that opens the app for editing in Power Apps Studio.

## Recommended Content

[Privileges required to view and access apps](/power-apps/maker/model-driven-apps/app-visibility-privileges/?azure-portal=true)

[Share a canvas app with guest users](/power-apps/maker/canvas-apps/share-app-guests/?azure-portal=true)

## Model-driven apps

Model-driven apps use role-based security for sharing. The fundamental concept in role-based security is that a security role contains privileges that define a set of actions that can be performed on tables within the app. This approach means that while two people are able to use the app, one user might only be able to read records, or records that they themselves created. The other user might be able to see all records and have the rights to delete those records.


All app users must be assigned one or more predefined or custom security roles. Or, security roles can be assigned to teams. When a user or team is assigned to one of these roles, the person or team members are granted the set of privileges associated with that role.


The process for sharing a model-driven app is different from sharing a canvas app. Model-driven app sharing depends on how the Microsoft Dataverse data table privileges are assigned for the tables that are in the app.


In our case, we'll be granting access to our new model-driven app to any user with the Dive Shop App Access security role.


1. Sign in to [Power Apps](https://make.powerapps.com/?azure-portal=true).

1. On the left pane, select **Apps**, then open the model-driven app you want to set security for.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Apps with app selected for security settings.](../media/app-security.png)](../media/app-security.png#lightbox)

1. Select the App name to open the menu of Apps Available.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the app name to selected to open the menu.](../media/app-name.png)](../media/app-name.png#lightbox)

1. Open the More Options menu and then select **Manage Roles**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the name roles option in the menu.](../media/manage-roles.png)](../media/manage-roles.png#lightbox)

1. Select the roles you want to grant access to and select Save.


	> [!div class="mx-imgBorder"]
	> [![Screenshot of the role selected and save button.](../media/roles-selected.png)](../media/roles-selected.png#lightbox)


> [!NOTE]
> If your app contains custom tables that haven't had privileges assigned in a security role, you must do this for users to access those records in your app. However, you don't have to create a security role if existing roles grant access to the table data in your app.

## Recommended Content

[Share a model-driven app using Power Apps](/power-apps/maker/model-driven-apps/share-model-driven-app/?azure-portal=true)

