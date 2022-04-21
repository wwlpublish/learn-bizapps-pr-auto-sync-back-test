Now that you've created an app, you can share it with specific users, groups, or
your whole organization. When you share an app with other people, they can run
it in a browser, or in the players for Apple iOS and Google Android.

Even better, you can give someone permission to update the app.

Sharing your app is your final step as an app creator. You will want to share
the app to test the full functionality with some stakeholders. This will give
them a chance to provide feedback and help you become a better app creator.

## Prepare to share an app

To complete the following steps, open the app that you want to share in Edit
mode.

1.  In Power Apps Studio, select the **File** menu and then select **Save as**
    and then select **The cloud**.

2.  Click **Save** in the bottom right corner.

3.  After the app is successfully saved click **Share**.

4.  On the Share tab, specify the users or groups with whom you want to share
    the app. To add everyone in your organization, type Everyone and select
    **Everyone** in **Company Name**. If you need to share with a large group of
    users, a best practice is to share through an Azure Active Directory
    Security Group.

    By default, the user receives the User permission. If you want the user to
    also be able to edit the app, then select the co-owner check box. The
    following is a description of both permissions:

    -   **Co-owner** - Users can use, edit, and share the app, but can't delete
        or change the owner.

    -   **User** - Users can view and use the app, but they can't change it.

5.  Consider security groups.

    -   If you share an app with a security group, existing members of that
        group and anyone who joins it will have the permission that you specify
        for that group. Anyone who leaves the group loses that permission unless
        they belong to a different group that has access or if you give them
        permission as an individual.

    -   Every member of a security group has the same permission for an app as
        the overall group does. However, you can specify greater permissions for
        one or more members of that group to allow them greater access. For
        example, you can give Security Group A permission to run an app, but you
        can also give User B, who belongs to that group, Co-owner permission.
        Every member of the security group can run the app, but only User B can
        edit it. If you give Security Group A Co-owner permission and User B
        permission to run the app, User B can still edit the app.

6.  To notify users by email, leave the **Send an email invitation to new
    users** check box selected.

    If you select to notify the users by email, everyone you shared the app with
    will receive an email message that has a link to the app. People whom you
    granted Co-owner permission for the app will also receive a link to Edit App
    in Power Apps Studio.

7.  Click **Share**.

    If you make and save changes to a shared app, the people whom you shared it
    with will see your changes as soon as you publish them. This can be useful
    if you improve the app, but it can also negatively affect users if you
    remove or significantly change features. Remember to create a notification
    plan for alerting your users of major updates.

Sharing an app is simple, and it's a great way to make an app that you find
useful available to people across your organization.
