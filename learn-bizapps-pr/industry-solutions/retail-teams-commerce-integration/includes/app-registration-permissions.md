In this exercise, we enable **Dynamics 365 Commerce** to integrate with **Microsoft** **Teams** to help customers and their employees to improve productivity by synchronizing task management between the two applications. The seamless task management that Dynamics 365 Commerce and Microsoft Teams integration provides lets store managers and employees create task lists, assign tasks to multiple stores, and track the status of tasks across stores, from either application.

Before you can enable Microsoft Teams integration with Commerce, you must register the Teams application with your tenant in the Azure portal.

In this exercise, you'll be doing the following:

1. Register an app with Azure Active Directory

1. Add a Secret to the registered app

1. Add API permissions to the registered app

1. Configure registered application to expose a web API

1. Configure a client application to access a web API

## Task 1: Register an app with Azure Active Directory

1. Sign in to Azure and ensure to select the right tenant. In the Azure portal search bar, search for "Active Directory." Azure Active Directory will show up in the services. Choose it to open **Azure Active Directory**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of Microsoft Azure showing the search results for active directory with Azure Active Directory highlighted.](../media/active-directory.png)](../media/active-directory.png#lightbox)

1. In Azure Active Directory, select **App registrations**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Microsoft Azure showing app registrations selected.](../media/app-registrations.png)](../media/app-registrations.png#lightbox)

1. In App registrations, select **New registration**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the New registration button and owned applications.](../media/new-registration.png)](../media/new-registration.png#lightbox)

1. Name the app registration "Microsoft Teams Commerce."

1. Under Supported account types, choose **Accounts in this organizational directory only** (Microsoft only—Single tenant).

1. Under Redirect URI, select **Web** and provide the Commerce Finance and Operations URL and add the "oauth" suffix. The full URL should look like `https://fabrikam.sandbox.operations.dynamics.com/oauth`.

1. Select **Register** at the bottom to complete.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Microsoft Azure Register an application page with name, supported account types, and redirect U R I filled in.](../media/register.png)](../media/register.png#lightbox)

1. **Important**: Save the **Application (client) ID** in the text editor of your reference. It will be used in the steps later.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Microsoft Azure Microsoft Teams Commerce page with Application (client) I D filled in.](../media/application-id.png)](../media/application-id.png#lightbox)

## Task 2: Add a secret to the registered app

1. In the Microsoft Teams Commerce registered app, select **Certificates & secrets**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Microsoft Teams Commerce page showing the Certificates and secrets option.](../media/certificates.png)](../media/certificates.png#lightbox)

1. Select add **New client secret**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Microsoft Teams Commerce Certificates and secrets page with the New client secret button highlighted.](../media/secrets.png)](../media/secrets.png#lightbox)

1. In the **Description**, provide a name of your choice for the client secret and select **Add**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Add a client secret dialog showing description and expires fields.](../media/add-client-secret.png)](../media/add-client-secret.png#lightbox)

1. Copy the key **value** generated for the client secret and save it in a text editor of your choice. The client secret **value** will be used in the steps later. After you close this page, it won't be possible to retrieve the value again and if you fail to make note of it, you must generate a new client secret.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the secret in the list of secrets with the Value field highlighted.](../media/value.png)](../media/value.png#lightbox)

## Task 3: Add API permissions to the registered app

1. Select **API permissions** in the left tab, then select **Add a permission**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Microsoft Teams Commerce A P I permissions page with the Add a permission button highlighted.](../media/add-permission.png)](../media/add-permission.png#lightbox)

1. In the **Request API permissions** pop-up, select **Microsoft Graph**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Request A P I permissions page showing Microsoft Graph.](../media/request.png)](../media/request.png#lightbox)

1. Select **Delegated permissions**, then in **Select permission** type **Group** to filter results.

1. Under **Group** and select **Group.ReadWrite.All**, then select the **Update permissions** button.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Request A P I permissions page showing search results for group and with Group.ReadWrite.All selected.](../media/group-permissions.png)](../media/group-permissions.png#lightbox)

1. Select **Add a permission** again to add more permissions.

1. In the **Request API permissions** pop-up, choose **Microsoft Graph**.

1. Select **Application permissions**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Request A P I permissions dialog with Application permissions selected.](../media/application-permissions.png)](../media/application-permissions.png#lightbox)

1. With **Application permissions** selected, then in **Select permissions** search field type **Group** to filter results.

1. Select **Group** to expand and select **Group.ReadWrite.All**, then select **Add permissions** button.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the group search results with Group.ReadWrite.All selected.](../media/group.png)](../media/group.png#lightbox)

1. In **API permissions**, select **Add Permission**.

1. In the **Request API permissions** pop-up, select **APIs my organization uses** tab, then search for **Microsoft Teams Retail Service** and select it.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Request A P I permissions dialog with A P I s my organization uses selected showing search results for Microsoft Teams Retail Service.](../media/my-organization.png)](../media/my-organization.png#lightbox)

1. Select **Delegated permissions**

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Request A P I permissions dialog with Delegated permissions selected.](../media/delegated.png)](../media/delegated.png#lightbox)

1. Select **TaskPublishing** to expand, select **TaskPublishing.ReadWrite.All**, then select **Add** **permissions** button.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the task publishing permission selected.](../media/task-publish.png)](../media/task-publish.png#lightbox)

## Task 4: Configure registered application to expose a web API

1. In Azure portal, go to **Azure Active Directory**.

1. **App registrations**, and then select your API's app registration.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Owned applications tab showing Microsoft Teams Commerce in the list.](../media/owned.png)](../media/owned.png#lightbox)

1. Select **Expose an API** and then select **Add a scope**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Expose an A P I page with the add a scope button highlighted.](../media/expose.png)](../media/expose.png#lightbox)

1. You can use the default value provided, which is in the form `api://<application-client-id>`, or specify a more readable URI like `https://contoso.com/api`.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Add a scope dialog with the Application I D U R I filled in.](../media/scope.png)](../media/scope.png#lightbox)

1. Select **Save and Continue**.

1. In the **Add a Scope** page fill the fields with the following values:

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Add a scope dialog filled out.](../media/add-scope.png)](../media/add-scope.png#lightbox)

1. Add another scope by clicking in **Add Scope** again and while repeating the process use the following values.

    | Setting | Value |
    |---------|-------|
    | **Scope name** | Employees.Write.All |
    | **Who can consent** | Admins only |
    | **Admin consent display name** | Write access to records |
    | **Admin consent description** | Allow the application to have write access to all Employee data |

1. Leave the remaining fields empty and make sure the **state** is set to **Enabled**.

1. Select **Add Scope**.

1. The final result should be similar to the picture below.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the list of scopes showing the ones added.](../media/scopes.png)](../media/scopes.png#lightbox)

## Task 5: Configure a client application to access a web API

1. In Azure portal, go to **Azure Active Directory**.

1. Go to **App registrations**, and then select your app registration created in Task 1.

1. Select **API permissions**, **Add a permission**, and then **My APIs**.

1. In My APIs, select the Application ID registered in the previous step.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Request A P I permissions dialog on the My A P I s tab with Microsoft Teams Commerce highlighted.](../media/my-api.png)](../media/my-api.png#lightbox)

1. Under Select permissions, expand the resource whose scopes you defined for your web API, and select the permissions.

1. If you used the example scope names specified in the previous quickstart, you should see **Employees.Read.All** and **Employees.Write.All**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Request A P I permissions dialog with delegated permissions and employees highlighted.](../media/employees.png)](../media/employees.png#lightbox)

1. Select **Add Permissions**.

## Task 7: Add Delegated permissions to access Microsoft Graph

1. In Azure portal, go to **Azure Active Directory**.

1. App registrations, and then select your API's app registration.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the owned applications tab with Commerce selected.](../media/owned.png)](../media/owned.png#lightbox)

1. Select **API permissions**, **Add a permission**, and then **Microsoft Graph**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the A P I permissions page with add a permission highlighted.](../media/add-permission.png)](../media/add-permission.png#lightbox)

1. Choose **Microsoft Graph**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Microsoft A P Is tab with Microsoft Graph selected.](../media/graph.png)](../media/graph.png#lightbox)

1. Select **Delegated permissions**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Request A P I permissions dialog with Microsoft Graph and Delegated permissions selected.](../media/graph-delegated.png)](../media/graph-delegated.png#lightbox)

1. In Select Permissions, search for "email."

1. Under Permission, select **email**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the email search results with email selected.](../media/email.png)](../media/email.png#lightbox)

1. In Select Permissions, search for "offline_access."

1. Under Permission, select **offline_access**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the offline access search results with offline access selected.](../media/offline.png)](../media/offline.png#lightbox)

1. In Select Permissions, search for "openid."

1. Under Permission, select **openid**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the openid search results with openid selected.](../media/open-id.png)](../media/open-id.png#lightbox)

1. In Select Permissions, search for "profile."

1. Under Permission, select **profile**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the profile search results with profile selected.](../media/profile.png)](../media/profile.png#lightbox)

1. Select **Add permissions** to complete the process.

## Task 8: Add application permissions to access Microsoft Graph

1. In Azure portal, go to **Azure Active Directory**.

1. App registrations, and then select your API's app registration.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the owned applications with commerce selected.](../media/owned.png)](../media/owned.png#lightbox)

1. Select **API permissions**, **Add a permission**, and then **Microsoft Graph**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Azure A P I permissions page with add a permission highlighted.](../media/add-permission.png)](../media/add-permission.png#lightbox)

1. Choose **Microsoft Graph**.

1. Under Request API permissions, select **Application permissions**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the application permissions option.](../media/application-permissions.png)](../media/application-permissions.png#lightbox)

1. In Select Permissions, search for "files."

1. Under Permission, select **Files.Read.All**.

1. Select **Add permissions** to complete the process.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the files search results with Files.Read.All selected.](../media/files.png)](../media/files.png#lightbox)
