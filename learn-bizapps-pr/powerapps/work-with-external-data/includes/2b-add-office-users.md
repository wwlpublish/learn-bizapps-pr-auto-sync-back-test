The Office 365 Users connection for Power Apps lets you access user profiles in your organization using your Office 365 account. You can perform various actions such as get your profile, get a user's profile, get a user's manager, or get direct reports.

You can display this information in a label on your app. You can display one function, multiple functions, or even combine different functions. For example, you can use this function to make the app sound more personal by greeting the user with their display name and saving the time of logging into the app by automatically populating certain fields.

## Add a connection

The Office 365 Users is a Standard connector that can be used in Power Apps. To add the connector, select Data, Add data and search for 'Office'. Select Office 365 Users and select Office 365 Users again.

> [!div class="mx-imgBorder"]
> [![Screenshot of the data icon with add data button and search results for office.](../media/office-365-users-connector.png)](../media/office-365-users-connector.png#lightbox)

> [!div class="mx-imgBorder"]
> [![Screenshot of the add data window with Office 365 users selected.](../media/office-365-users-connector-2.png)](../media/office-365-users-connector-2.png#lightbox)

If this is the first time you're adding this connector in this environment, you'll see the following pop-up message, select Connect to add this connection.

> [!div class="mx-imgBorder"]
> [![Screenshot of the Office 365 users window with connect button.](../media/first-time-office-365-users-connection.png)](../media/first-time-office-365-users-connection.png#lightbox)

## User profile information

You have a few options to get user information in the canvas app. To get information about the user who is using the app, you can either use the function at the **App OnStart** or **OnSelect** of a button.

### App OnStart

Here we'll get the user information we're looking for and save it to a global variable making it easy to reuse it throughout the app.

Select App, select the OnStart property and add the following formula.

`Set(varUserInfo, Office365Users.MyProfileV2())`

> [!div class="mx-imgBorder"]
> [![Screenshot of the OnStart property with the formula displayed.](../media/my-profiler-app-onstart.png)](../media/my-profiler-app-onstart.png#lightbox)

To populate the variable, right-click on **App** and select **RunOnStart.**

With the global variable name **varUserInfo** now populated, you can call that information anywhere in the app. For example, in the **Default** property of a Text control, you can add `varUserInfo.displayName`.

> [!div class="mx-imgBorder"]
> [![alt text](../media/text-default-display-name.png)](../media/text-default-display-name.png#lightbox)

Below shows the attributes that can be automatically populated in your app saving the user time to input them manually.

> [!div class="mx-imgBorder"]
> [![Screenshot of the user profile information.](../media/user-profile-information.png)](../media/user-profile-information.png#lightbox)


### Control OnSelect

If you need to gather information about another user, add a **ComboBox** control and set the Items property to `Office365Users.SearchUser()` , the SelectMultiple property to `false`, the DisplayFields property to `["DisplayName"]`, and the OnChange property to `Set(varUserInfo, Office365Users.UserProfile(ComboBox1.Selected.Id))`.

> [!div class="mx-imgBorder"]
> [![Screenshot of the search results for user.](../media/test-search-user-2.png)](../media/test-search-user-2.png#lightbox)

> [!div class="mx-imgBorder"]
> [![Screenshot of the search box.](../media/test-search-user.png)](../media/test-search-user.png#lightbox)

## Manager information

In addition to getting user information, you can also search for a user's manager information.

For a **ComboBox** control, set the Items property to `Office365Users.SearchUser()`,  the SelectMultiple property to `false`, the DisplayFields property `["DisplayName"]`,  and the OnChange property to `Set(varUserInfo, Office365Users.Manager(ComboBox1.Selected.Id))`.

> [!div class="mx-imgBorder"]
> [![Screenshot of the manager information.](../media/manager-information.png)](../media/manager-information.png#lightbox)

You can confirm this is the correct manager by verifying in Azure Active Directory.

> [!div class="mx-imgBorder"]
> [![Screenshot of the manager information in Azure Active Directory.](../media/verified-manager.png)](../media/verified-manager.png#lightbox)

## View all direct reports

Another feature that comes with Office 365 Users is the ability to find all the users who directly report to a single manager. This information is gathered from Microsoft Azure Active Directory.

We’ll use a combination of a **Collection** and **Gallery** to present the list of users. A **Collection** is a variable that can store a list of information, which can be easily accessible throughout the use of the app. A **Gallery** control can show multiple records from a data source, and each record can contain multiple types of data. In this scenario, our data source is the **Collection**.

Add a **ComboBox** control and set the Items property to `Office365Users.SearchUser()`. Next, set the SelectMultiple property to `false`, the DisplayFields property `["DisplayName"]`, and the OnSelect property to `ClearCollect(colDirectReports, Office365Users.DirectReportsV2(ComboBox1_1.Selected.Id).value)`.

We can now present two pieces of information; one is to see how many users directly report to a manager and also list their names.

To get a count of many users' report, add a **Label** control and set it's **Text** property to `CountRows(colDirectReports)`.

> [!div class="mx-imgBorder"]
> [![Screenshot of a label contrl with text property set.](../media/label-county-direct-reports.png)](../media/label-county-direct-reports.png#lightbox)

To display all the direct reports, add a **Vertical Gallery** option from the Insert menu and set its **Items** property to **colDirectReports**.

> [!div class="mx-imgBorder"]
> [![Screenshot of the vertical gallery option from the insert menu with items property set.](../media/list-direct-users-names.png)](../media/list-direct-users-names.png#lightbox)

For more information on the Office 365 User connection, see [Office 365 Users Connector Documentation.](/connectors/office365users/?azure-portal=true)