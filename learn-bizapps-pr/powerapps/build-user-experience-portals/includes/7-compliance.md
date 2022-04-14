Organizations are increasingly using Power Apps portals to reach out to external audiences. One of the many important aspects of the global reach is the ability to deliver solutions that are compliant with the relevant standards, regulations, and applicable laws. Compliance is especially important when Power Apps portals are used within the government or financial organizations.

## Accessibility

The out-of-the-box portals (Community, Partner, Customer self-service, Employee self-service) are accessible. However, customizers must ensure that the portal remains accessible after any customizations or changes have been made.

You can retrieve specific Power Apps portals conformance reports by searching for "Dynamics 365 Customer Engagement" at [Microsoft Accessibility Conformance Reports](https://cloudblogs.microsoft.com/industry-blog/government/2018/09/11/accessibility-conformance-reports/?azure-portal=true). These reports cover the following standards:

- **EN 301 549** - The European standard that sets out accessibility requirements for information and communication technology that is procured by the public sector.
- **Section 508** - Under Section 508 of the Rehabilitation Act, US government agencies must give access to employees with disabilities and members of the public to information that is comparable to the access that is available to others.
- **WCAG** - Web Content Accessibility Guidelines are published and maintained by W3C.

## Data protection 

You can configure your portal to meet data protection standards. Two important parts of data protection standards that are covered by portals are:

- Identifying minor portal users and obtaining parental consent
- Agreeing to terms and conditions

### Minor portal users

Regulations for identifying minors vary by country and/or region. Because a minor can only access the portal with parental consent, you can configure the portal to identify minors by using these columns in the portal contact row:

- **Is Minor** - Indicates that the contact is considered a minor in their jurisdiction. By default, **No** is selected.
- **Is Minor with Parental Consent** - Indicates that the contact is considered a minor in their jurisdiction and has parental consent. By default, **No** is selected.

By using additional site settings, you can configure the portal to deny access to minors or minors without parental consent. Related messages that are displayed to the users are also configurable.

It's up to the organization to define how the information about a user being a minor and/or having parental consent is collected. For example, a registration form can be customized to include a **Birth Date** column and, if required, a parental consent flag. You might want to further enhance the functionality by implementing workflow rules that would calculate user age at the sign-in time and then set or clear the **Is Minor** flag.

Special considerations must be given when using external providers such as Azure Active Directory B2C. Only limited information is available from the providers, and providers might or might not have a mechanism for minor protection. Therefore, when someone registers by using an external provider, and the portal is configured to block minors or minors without parental consent, the contact row is not created and the user is not authenticated.

For more information, see [Identifying minor portal users and obtaining parental consent](/power-apps/maker/portals/configure/implement-gdpr?azure-portal=true#identifying-minor-portal-users-and-obtaining-parental-consent).

### Terms and conditions

Your organization will have policies regarding rules for using your portal. These rules are typically described in Terms and Conditions and include what portal users can do, what is prohibited, and a disclaimer to limit your liability when these users access your portal. In addition, portal users must agree to the terms and conditions to allow marketing, profiling, or access to private information.

You can publish terms and conditions to get consent of the portal user before they are authenticated to the site.

Power Apps portals use content snippets to store terms and conditions and to support the process of getting consent from a portal user before they are authenticated to the site. Because content snippets are language-aware, it's possible to configure terms and conditions to be displayed in the language of the user's choice.

The contact table includes the **Portal Terms Agreement Date**, which indicates the date and time that the person agreed to the portal terms and conditions.

For more information, see [Agreeing to terms and conditions](/power-apps/maker/portals/configure/implement-gdpr?azure-portal=true#agreeing-to-terms-and-conditions).
