Many authentication options that are supported by Power Apps portals are configured by using site settings. Site settings are stored in the **Site Settings** table, where each setting is defined as a Name/Value pair.

To view site settings:

1. Sign in to [Power Apps](https://make.powerapps.com/?azure-portal=true).
1. Select a target environment by using the environment selector in the upper-right corner.
1. On the left menu, select **Apps**.
1. Select **Portal Management** app.
1. In the app, select **Site Settings** in the navigation panel.

> [!div class="mx-imgBorder"]
> [![Screenshot of active site settings for portals.](../media/active-site-settings.png)](../media/active-site-settings.png#lightbox)

Only a few of the many available authentication-related site settings are installed when you provision a starter portal. Settings that are not created assume their documented default values.

## Example of a setting

An example of the need to add a site setting is when you provision a custom portal and the form for registering a new local account requires an email address and a username.

> [!div class="mx-imgBorder"]
> [![Screenshot of register with username in customer portal.](../media/register-username.png)](../media/register-username.png#lightbox)

To enable a local account sign-in by using an email address instead of a username, you can add the `Authentication/Registration/LocalLoginByEmail` setting and set it to **True**.

> [!div class="mx-imgBorder"]
> [![Add new site setting](../media/add-new-site-setting.png)](../media/add-new-site-setting.png#lightbox)

As a result, the form and the process for registering a new local account now require an email address only.

> [!div class="mx-imgBorder"]
> [![Screenshot of register with email address only in customer portal.](../media/register-email-address.png)](../media/register-email-address.png#lightbox)

Also, the sign-in form will now refer to **Email** instead of **Username**.

> [!div class="mx-imgBorder"]
> [![Screenshot of sign-in by email for customer portal.](../media/local-sign-email.png)](../media/local-sign-email.png#lightbox)

> [!NOTE]
> Where a function is enabled by default, a site setting needs to be created to disable that function. For example, adding the `Authentication/Registration/ResetPasswordEnabled = False` setting is required to disable the password reset feature for local authentication.

## Authentication settings categories

All authentication-related site settings start with **Authentication**.

Authentication settings can be grouped into three broad categories, each covering settings to control various aspects of authentication processes.

| Group                                | Description                                                  |
| ------------------------------------ | ------------------------------------------------------------ |
| **Authentication/Registration**      | The most extensive group of settings that cover options such as enabling/disabling specific authentication methods, controlling invitation behaviors, password resets, confirmation emails, two-factor authentication, and more. |
| **Authentication/UserManager**       | [User credential validation](/power-apps/maker/portals/configure/set-authentication-identity?azure-portal=true#user-credential-validation) are settings for adjusting username and password validation parameters. Validation occurs when users sign up for a new local account or change a password. Also included are [user account lockout settings](/power-apps/maker/portals/configure/set-authentication-identity?azure-portal=true#user-account-lockout-settings). |
| **Authentication/ApplicationCookie** | It's not uncommon to see enterprise requirements for specific cookie behaviors such as expiration time span. This group defines [Cookie authentication site settings](/power-apps/maker/portals/configure/set-authentication-identity?azure-portal=true#cookie-authentication-site-settings) for modifying the default authentication cookie behavior. |

For more information, see [Set authentication identity for a portal](/power-apps/maker/portals/configure/set-authentication-identity/?azure-portal=true).
