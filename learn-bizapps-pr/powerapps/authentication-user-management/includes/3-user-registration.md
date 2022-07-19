Before portal visitors can sign in to Power Apps portals, they need to be registered as portal users. All portal users are tracked as contacts, and they can be registered in two ways:

- **Open registration** - Allows visitors to register directly on the portal.
- **Invitation-based registration** - Requires users to provide an invitation code.

The decision about which option is more appropriate depends on the target audience of your portal and whether the members of the audience are known in advance.

Regardless of the registration configuration, local and external accounts participate equally in the registration workflow. Specifically, users have the option to choose which type of account they want to register.

Registration is enabled by default. The `Authentication/Registration/Enabled` site setting controls the overall registration process, and adding this setting with the value of `False` disables all forms of user registration. Any other registration setting is ignored until the registration is enabled. You can use [Enable or disable user registration](/power-apps/maker/portals/configure/set-authentication-identity?azure-portal=true#enable-or-disable-user-registration) settings to control individual registration options.

## Open registration

Open registration allows visitors to register directly on the portal by using the **Register** tab on the portal **Sign In** page. It's the least restrictive sign-up configuration, where the portal allows a user account to be registered by providing a user identity. When open registration is enabled, any user who completes the registration form is immediately registered and authenticated.

Because users aren't validated prior to sign up, this option works well in more open environments like community portals, where site visitors aren't known in advance. Organizations run these portals for the communities where the users might have some common interests, such as the area where they live, their hobbies, and the industries that they work in. In other words, open registration works best when it's not easy to discover and validate the users in advance.

## Invitation-based registration

Invitation-based registration is the process where an existing contact is validated by an invitation code.

This registration is useful in scenarios when contacts are known in advance. It's commonly used to register customers, partners, or employees. Invitation-based registration works in situations where users can be "pre-validated," such as when you've collected contact information from visitors to your exhibition booth.

Invitations contain many [Invitation columns](/power-apps/maker/portals/configure/invite-contacts?azure-portal=true#invitation-attributes) or attributes that allow you to:

- Send single or group invitations. Group invitations use the same invitation code for all invitees and work well with a restriction on the number of invitations to redeem. For example, a promotional email can be sent by a software company, inviting all their users to participate in a beta program, but intake is limited to the first 100 registrations.
- Specify an expiry date, if desired.
- Specify a portal contact as the inviter. You can use this information to customize invitation emails and in the post-registration workflows.
- Assign the invited contact(s) automatically to an account on invite redemption. This option is useful in partner portal scenarios where all invitees are from the same company.
- Implement a classic workflow automatically on invite redemption. For example, you might want to send a "Thank you" email to the contacts who accepted the invitation.
- Assign the invited contact(s) automatically to web roles on redemption. You can use this feature to grant users who accept the invitation special access rights in your portal.

> [!IMPORTANT]
> Email integration must be enabled in your Microsoft Dataverse instance for the email invitations to work.

The ensuing sections explain the process of sending and redeeming invitations.

### Configure automation

The classic workflow process of sending the invitation email is generic and needs to be customized prior to use. When you're customizing the invitation email, make sure that the link to the **Invite Redemption Page** includes the invitation code. The default link should look like this sample: `https://yourportalurl/register/?returnurl=%2f&invitation={Encoded Invitation Code(Encode Invitation Code)}`

After the invitation code has been generated, you can distribute it through other channels. For example, if you have a text (SMS) messaging solution in place, you might want to replace the steps of creating and sending the invitation email with the custom step of sending an SMS message instead.

> [!IMPORTANT]
> Microsoft Power Automate has significant advantages over the classic workflow model. You should consider using Power Automate to automate your Send Invitation process instead of using the classic workflow.

### Create Invitation

**Create Invitation** is a unique invitation code that is generated when an **Invitation** row is created. The **Invitation** row can be created manually by selecting the **New** command on the **Invitations** view or by using the **Create Invitation** command on a contact row. For more information, see [Create invitations from the Portal Management app](/power-apps/maker/portals/configure/invite-contacts?azure-portal=true#create-invitations-from-portal-management-app).

### Redeem Invitation

When the contact receives the email invitation and follows the URL, they're directed to the **Redeem Invitation** tab of the **Sign In** page.

On this page, they can select the **I have an existing account** option, which opens some automation opportunities where the existing portal users can be sent an invitation code. After the code has been accepted and an existing account is used, you can run a workflow that could, for example, grant user access to other protected content.

> [!div class="mx-imgBorder"]
> [![Screenshot of redeem invitation from an account.](../media/redeem-invitation.png)](../media/redeem-invitation.png#lightbox)

### Register user

If the user doesn't select the **I have an existing account** option, they'll be presented with the registration page. Similar to open registrations, users have the option to register by using any provider that is enabled on the portal. The selected registration will be associated with the invited contact, showing the invitation as redeemed.

> [!div class="mx-imgBorder"]
> [![Screenshot of register invited contact from an account.](../media/register-invited-contact.png)](../media/register-invited-contact.png#lightbox)

After the registration process is complete, depending on the invitation options, the portal user can be associated with the predefined account, or another classic workflow can be run.

For more information, see [Invite contacts to your portals](/power-apps/maker/portals/configure/invite-contacts?azure-portal=true).
