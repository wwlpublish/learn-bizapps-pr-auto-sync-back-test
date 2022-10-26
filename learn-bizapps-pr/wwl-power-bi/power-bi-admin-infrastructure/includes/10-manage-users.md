For on-premises data gateway in standard mode, users can be added in any of the following three categories.

Admin:

-   Administrators have full control of the gateway

-   Can add other admins

-   Can create and manage data sources

-   Can create and manage users

-   Delete gateway

Can use:

-   Users who can create connections

-   Users cannot share the gateway

-   Use this permission for users who will run apps but not share them

-   Applies only to PowerApps and Microsoft Flow

Can use + share:

-   Users who can create a connection

-   Users can share the gateway when sharing an app

-   Use this permission for users who need to share apps with other users or with the organization

-   Applies only to PowerApps and Microsoft Flow

Single sign-on (SSO) allows you to use the same credentials to sign in to your personal computer, local Active Directory, or on to the Power BI service.

However, because Power BI can only be accessed through Azure Active Directory, you must synchronize your local Active Directory with Azure Active Directory to use SSO to sign in to the Power BI service. To allow other on-premises users to use SSO to sign in to Power BI, you would simply have to synchronize their local Active Directory with Azure Active Directory as well.

For more information regarding synchronizing your local Active Directory to Azure Active Directory, see this [article](/power-bi/connect-data/service-gateway-enterprise-manage-ssas?azure-portal=true#synchronize-an-on-premises-active-directory-with-azure-ad).

Power BI allows for mapping usernames for Analysis Services data sources. You can configure rules to map a username signed in with Power BI to a name that's passed for EffectiveUserName on the Analysis Services connection. The map user names feature is a great way to work around when your username in Azure Active Directory (Azure AD) doesn't match a user principal name (UPN) in your local Active Directory instance. For example, if your email address is `nancy@contoso.onmicrsoft.com`, you map it to `nancy@contoso.com` and that value is passed to the gateway.

You can map usernames for Analysis Services in two different ways:

-   Manual user remapping

-   On-premises Active Directory property lookup to remap Azure AD UPNs to Active Directory users (Active Directory lookup mapping)

It's possible to perform manual mapping by using the second approach but doing so is time consuming and difficult to maintain. It's especially difficult when pattern matching doesn't suffice. Examples are when domain names are different between Azure AD and on-premises Active Directory or when user account names are different between Azure AD and Active Directory. That's why manual mapping with the second approach isn't recommended.

For more information regarding manual mapping and on-premises Active Directory property lookup, see this [video](/power-bi/connect-data/service-gateway-enterprise-manage-ssas?azure-portal=true#map-user-names-for-analysis-services-data-sources) and [article](/power-bi/connect-data/service-gateway-enterprise-manage-ssas?azure-portal=true#synchronize-an-on-premises-active-directory-with-azure-ad).