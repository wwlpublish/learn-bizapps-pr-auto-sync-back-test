Regardless of the portal template that you choose, a Power Pages site has a set of core features that allow makers to build or configure a powerful, externally facing web site on Microsoft Power Platform.

## Content management

Webpages, static text, images, and other content can be quickly created in a portal web application by using the Power Pages design studio and other tools.

> [!div class="mx-imgBorder"]
> [![Screenshot of the portal web application using Power Apps portals Studio.](../media/1-content-management.png)](../media/1-content-management.png#lightbox)

## Multi-language

Site content and navigation can be viewed in up to 43 different languages. Site visitors will be able to switch to different languages and not lose their current page or navigation. Other languages will need to be provisioned within Microsoft Dataverse to use the multi-language capabilities in a portal.

> [!NOTE]
> Content will still need to be translated and updated on the webpages and in the content snippets for the specified enabled languages. Any Dataverse assets that are added to the portal, such as tables, forms, views, or columns, will also need to have corresponding label translations by using the Dataverse multilingual functionality.

> [!div class="mx-imgBorder"]
> [![Screenshot of the switch language in Portals feature.](../media/1-multi-language-portals.png)](../media/1-multi-language-portals.png#lightbox)

## Access to Dataverse data

The main feature of Power Pages sites is the ability to show and interact with rows in Dataverse. Dataverse rows can be shown on a portal page by using Lists or through custom web templates. Rows can be created and edited individually by using Forms or as part of a step-by-step process by using Multistep Forms. Pro developers can use portals Web API to interact with Dataverse data directly from JavaScript and create richer user experience inside Power Pages site. The data is protected by using a combination of web roles and table and column permissions to ensure that portal visitors only have the appropriate access to Dataverse rows.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4yWn4]

## Themes

A Power Pages maker has the ability to apply their unique corporate branding and styling directly to a Power Pages site by using a dedicated CSS and Bootstrap toolkit.

> [!div class="mx-imgBorder"]
> [![Screenshot of customized Portals theme using a CSS and Bootstrap toolkit.](../media/1-custom-theme.png)](../media/1-custom-theme.png#lightbox)

## Global search

Power Pages makers can configure the portal to search across specified Dataverse tables so that users can quickly locate specific data on a portal results page. Dataverse search is the same search service used in model-driven apps and other Microsoft Power Platform services built on Microsoft Dataverse. Results of the global search are protected by table permissions so that portal users don't inadvertently discover protected information.

> [!div class="mx-imgBorder"]
> [![Screenshot of a page containing Dataverse search results.](../media/1-global-search.png)](../media/1-global-search.png#lightbox)

## Authentication and security

Users who are browsing to a Power Pages site will be able to authenticate by using a built-in authentication or by using an integrated external authentication provider such as Microsoft Azure Active Directory B2C (Azure AD B2C), LinkedIn, Facebook, or other authentication providers.

An authenticated portal user can be assigned a web role with associated webpage access control rules and table permissions to control access to specific webpages and Dataverse rows.

> [!div class="mx-imgBorder"]
> [![Screenshot of the configure identity provider window.](../media/1-configure-identity-provider.png)](../media/1-configure-identity-provider.png#lightbox)

## Profile management

An authenticated site user will be able to manage their own profile information on a dedicated site form that will update their corresponding Dataverse contact row. This feature allows stakeholders to ensure that their contact information is up to date.

> [!div class="mx-imgBorder"]
> [![Screenshot of the Profile Management window.](../media/1-profile-management.png)](../media/1-profile-management.png#lightbox)

## Customization and extensibility

Power Pages provides many tools to create content, add Dataverse data, and configure the appearance of a portal application. Power Pages capabilities can also be further extended by using custom web templates, Liquid template language, JavaScript, Cascading Style Sheets (CSS), and Portals Web API. Power Pages sites can also use other Microsoft Power Platform development technologies such as plug-ins, Power Automate, and classic workflows.

> [!div class="mx-imgBorder"]
> [![Screenshot of the Category Details web template from Partner starter portal.](../media/1-web-template.png)](../media/1-web-template.png#lightbox)
