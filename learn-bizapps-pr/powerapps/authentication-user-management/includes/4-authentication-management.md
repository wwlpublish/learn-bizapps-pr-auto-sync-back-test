Power Apps portals administrators have several options for controlling authentication behavior for the portal user. These options are accessed through the **Web Authentication** tab on the **Portal Contact** form.

> [!div class="mx-imgBorder"]
> [![Screenshot of portal contact web authentication information.](../media/portal-contact-web-authentication.png)](../media/portal-contact-web-authentication.png#lightbox)

The following table explains some of the options that are available on the **Web Authentication** tab.

| Field                  | Description                                                  |
| ---------------------- | ------------------------------------------------------------ |
| Username               | The username is for local authentication. The password can be reset by running the **Change password for portal contact** task flow: [Change password for a contact in Power Apps portal app](/power-apps/maker/portals/configure/configure-contacts?azure-portal=true#change-password-for-a-contact-in-dynamics-365-portal-app). |
| Email Confirmed        | This flag indicates if the email has been confirmed, that is, a validation code has been emailed to and confirmed by the user. Unless the email is confirmed, it can't be used for password resets or two-factor authentication. If required, it can be set manually by the administrator. |
| Mobile Phone Confirmed | This field is similar to **Email Confirmed**, except that text (SMS) messaging is used for confirmation and other operations. Messaging providers are not included out of the box, but if an organization has one, the authentication flows can be extended to include SMS as a valid confirmation channel. |
| Two Factor Enabled     | Defines if two-factor authentication has been enabled for the contact. A confirmed email address is required for two-factor authentication to be used. |
| Login Enabled          | Clearing this check box (or setting the field value in a workflow) will disable all forms of authentication for the contact, including external providers. |
| Lockout Enabled        | Defines if the contact can be locked after a preconfigured number of failed attempts. |
| Lockout End Date       | When the contact is locked out, this field defines when it's going to be unlocked automatically. Traditional use of this value is to lock out a contact for a number of minutes (which is controlled in site settings) after a preconfigured number of failed sign-in attempts. |
| Local Login Disabled   | Defines if the local authentication option is available for the user. Site settings might disable local authentication for all users, in which case, this flag will have no effect. |

For more information, see [Set authentication identity for a portal](/power-apps/maker/portals/configure/set-authentication-identity/?azure-portal=true).

## External identities

The **External Identities** list includes all external providers that are registered for a specific user. Multiple external identities permit user sign-in with any of the registered providers. Entries in this list should not be edited manually; they are added/removed when the user connects/disconnects the providers by using the **Manage External Authentication** link on their **Profile** page.

> [!div class="mx-imgBorder"]
> [![Screenshot of manage external identities authentication.](../media/manage-external-authentication.png)](../media/manage-external-authentication.png#lightbox)
