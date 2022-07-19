In this unit, you will create a model-driven app by using one of the standard
entities that is available in your Microsoft Power Apps environment.

## Create a model-driven app

1.  Sign in to [Power Apps](https://make.powerapps.com/) by using your
    organizational account.

2.  Select the environment you want, or go to the [Power Apps admin
    center](https://admin.powerapps.com/) to create a new one.

3.  On the **Home** page, select **Blank App**.

4.  On the Create screen, select **Blank app based on Dataverse**, and click
    **Create**.

    ![Model-driven app from blank](../media/model-driven-app-from-blank.png)

5. On the **New model-driven app** page, enter a **name** and **description** for the app. (For example, enter My first app for the name, and this is my first model-driven application for the description.)

6. After a few minutes, your new app will appear.

    ![Model-driven app designer](../media/app-designer-configuration-screen.png)

## Add Account table to your app

You can add pages to your app by using the App Designer.

1.  If necessary, using the navigation on the left, select the **show or hide
    menu names button** (looks like 3 horizontal lines) to show the menu names.

2.  Select the **Group1** text. On the right-hand side of the screen change the
    Title to **Customers**.

    ![Renaming the customer group](../media/app-designer-rename-group.png)

3. Using the command bar at the top, select the **+ Add Page** button. 

4. On the Add Page screen, select **Table based view and form,** then select the **Next** button.

5. On the Add table view and form pages screen, select **Account** then select the **Add** button.  

## Add forms and views to your app

Now that we have added a table to our app, we are going to specify which Account
forms and views should be used with the application.

1.  Using the navigation on the left, select **Pages.**

2.  Expand **Account** and select **Account** form.

3.  On the right-hand side of the screen, select **Add form**.

4.  From the list of Forms that appears, select **Account.** 

    ![Account main form](../media/account-forms.png)

5.  Under **Pages** on the left, select **Account** view.

6.  On the right-hand side of the screen, select **Add view**.

7. Select the **My Active Accounts** view. 

8. Select **Add view** again.

9. Select **Active Accounts**.

10. Select **Add view**.

11. Select **Inactive Accounts.**

	- My Active Accounts

	- Active Accounts

	- Inactive Accounts

## Add Contact page to your app

Next, we are going to add another table to our application. In this case we are
going to add the Contacts table since a customer could be either an account or a
contact.

1.  On the command bar at the top, select the **Add Page** button.

2.  On the Add page screen, choose **table based view and form**, then select
    the **Next** button.

3.  In the **Search** field, enter **Contact**, then select the **Contact**
    table.

4.  Select the **Add** button.

## Save and publish your app

Now that you have successfully created your first model driven application,
let’s get ready to use it.

1.  Using the command bar at the top select the **Save** button.

2.  Once your application has been saved, select the **Publish** button.

3.  To test your application, select the **Play** button.

    ![Playing the published app](../media/published-app.png)

> [!NOTE]
> It is possible that you will not have any data in your environment. Select either Account or Contact and add a few sample records to test functionality. 
