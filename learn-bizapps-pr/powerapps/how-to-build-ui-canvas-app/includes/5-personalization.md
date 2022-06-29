In Power Apps, you can show information about the current user with the User() function. This includes the full name, email address, and the picture that's associated with the user who's signed into a canvas app. It will match the "Account" information that is displayed in the Power Apps players and studio, which can be found outside of any authored apps. This may not match the current user's information in Office 365 or other services.

The **User** function returns
a [record](/power-apps/maker/canvas-apps/working-with-tables?azure-portal=true#records) of
information about the current user:

| **Property** | **Description** |
| :------------------- | :------------------- |
| **User().Email** | Email address of the current user. |
| **User().FullName** | Full name of the current user, including first and last name. |
| **User().Image** | Image of the current user. This will be an image URL of the form \"blob:*identifier*\". |

Set the [Image property](/power-apps/maker/canvas-apps/controls/properties-visual/?azure-portal=true) of the [Image control](/power-apps/maker/canvas-apps/controls/control-image/?azure-portal=true) to this value to display the image in the app.
Here’s an example of how to add a user's profile picture, email, and name to your app.

1. On the **Insert** tab, click or tap **Media**, and then click or tap **Image**.

2. Set the **Image** property to this formula: **User().Image**

3. On the **Insert** tab, click or tap **Text**, and then click or tap **Label**:

4. Set the **Text** property to this formula: **User().FullName**

5. Move the label so it's below the image control.

6. Add another label, and set its **Text** property to this formula: **User().Email**

7. Move the label so it's below the first label:

![Screenshot of a User Profile with picture, email, and name.](../media/UserProfile.png)
