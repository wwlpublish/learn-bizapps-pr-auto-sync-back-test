When provisioning a Power Apps portal, the most important choices to consider are the audience, workload, and choosing a specific portal template that would best align with the particular business requirements.

Several portal templates are available that can be provisioned. These templates will accelerate the configuration of a portal based on the intended audience and workload.

![Screenshot of portal templates that are available for provisioning.](../media/portal-templates.png)

If you are building a custom business application by using Microsoft Dataverse without Dynamics 365 apps enabled, your only choice is the **Blank website** option available under the **Blank app** selection.

If you are using Microsoft Dynamics 365 apps such as Dynamics 365 Sales or Dynamics 365 Service, you have a choice of five additional portal templates:

- Community
- Modern Community (requires [Dynamics 365 Customer Service Community app](/dynamics365/customer-service/community-get-started/?azure-portal=true))
- Customer self-service
- Employee self-service
- Partner
- Field Service portal
- Customer portal (Dynamics 365 Supply Chain Management)
- Intelligent Order Management (requires [Dynamics 365 Intelligent Order Management](/dynamics365/intelligent-order-management/?azure-portal=true))

## Portal templates

Each starter portal includes a particular set of features designed to accelerate solution development that targets the selected audience.

> [!NOTE]
> The starter portal selection defines a specific set of features. If a portal is provisioned within a Dataverse environment with Dynamics 365 apps installed, specific features from the other starter portals can be added later, as required.

| Portal template | Audience | Workload |
|-----------------|----------|--------- |
| Community | Partner, Customer | Choose this template to provision a portal that is focused on an online community. This portal will contain features such as forums, ideas, blogs, and case management. |
| Customer self-service | Partner, Customer | This template provides the ability for portal users to search knowledge articles, submit cases, and participate in discussion forums to resolve issues. |
| Employee self-service | Employee | This portal allows employees to access a centralized knowledge article and to also submit cases. |
| Partner | Partner, Customer, Field Agent | Choose this template to build a portal where external partners can manage and collaborate on accounts and opportunities. Add-ons are available for Dynamics 365 Field Service or Dynamics 365 Project Service. |
| Field Service | Customer | This portal enables self-service scheduling capabilities for your customers. Requires Dynamics 365 Field Service. |
| Customer portal | Enterprise B2B | The Dynamics 365 Supply Chain Management Customer portal is a template that provides portal access to Dynamics 365 Supply Chain Management data by using dual-write Microsoft Dataverse tables. |
| Modern Community | Customer, Community | This solution helps your organization invite customer suggestions and crowd-source portfolios of outside-in ideas. End users can share new ideas with organizations and collaborate on a social scale. Requires Dynamics 365 Customer Service Community solutions installed from App Source. |
| Intelligent Order Management | Customer | Dynamics 365 Returns gives the customer with a hassle-free return experience with choices from a whole range of delivery providers to drop off their items. |
| Blank website | Other | The blank website template is meant for unique line-of-business scenarios where the other templates are not a good fit. The portal can be configured and customized to address a variety of requirements. |

> [!IMPORTANT]
> Review current licensing guides to determine the licenses, subscriptions, and capacity that is required for internal and external authenticated users and anonymous page views. For more information, see the [Dynamics 365 Licensing Guide](https://go.microsoft.com/fwlink/p/?LinkId=866544) or the [Power Apps Licensing Guide](https://go.microsoft.com/fwlink/?linkid=2085130). Integration to other services such as SharePoint, Power BI, or Azure Blob storage will require appropriate capacity and licensing.

Make sure that you define the type of audience who will visit the new portal. The audience will determine which options of portals you will be given.

## Portal features

All portal templates are built on a common foundation (portal base) and include the following features:

- Ability to configure the portal by using the Portal studio.
- Content management, including content publishing, design, theming, search, multi-lingual support, and templating.
- Extensibility that is built on webpages, templates, table forms, table lists, and more.
- Security that is based on identity management, integration with authentication providers, web roles, content permissions, and table permissions.
- Common features like ads, polls, ratings, and comments. These features are not standalone and can be used throughout other parts of the implementation. For example, ratings and comments can be enabled for a page, and ads can be included as part of a template. Some features will require Dynamics 365 apps to be enabled. For example, knowledge articles require a Microsoft Dynamics 365 app.

Where the portal templates are different is around the functional areas that target *specific business processes* such as case management. These features are deployed as additional managed solutions, making it easier to add missing features if necessary.

| Feature | Blank website | Customer self-service | Partner | Employee self-service | Modern Community | Community |
|---------|---------------|-----------------------|---------|---|---|---|
| Portal base | • | • | • | • | • | • |
| Forums | | • | • | • | • | • |
| Ideas | | | | | • | • |
| Blogs | | | | | | • |
| Support/Case management | | • | • | • | | • |
| Knowledge management | | • | • | • | | • |
| Azure AD Authentication <sup>^</sup> | | | | • | | |
| Partner pipeline | | | • | | | |
| Project Service Automation integration | | | • | | | |
| Field Service integration | | | • | | | |

<sup>^</sup> Support for Azure Active Directory (Azure AD) as authentication provider is included in the portal base. The Azure AD Authentication feature, as used by the Employee self-service portal, is different. In the Employee self-service portal, the sign-in process validates that the user has a required license and access is denied if the user does not have a license assigned.

If a particular feature, for example case management, is available in two different templates, it will be the same feature offering the same functionality.

## Additional considerations

The following sections explain the additional factors that you should consider when choosing the correct portal template.

### Dependencies

Some portal templates have prerequisites for their installation, so an installation will fail if the prerequisites are not met. For example, to install Field Service for a Partner portal, the Partner portal and Field Service solutions must have already been installed. If you attempt to install Field Service first, the installation will fail and give you an error message.

If Dynamics 365 apps are not enabled in a Dataverse environment, the only available portal template will be **Blank website**.

### Employee portal access

When an employee accesses the portal functionality, an appropriate app license might be required. The simplest way to assess the licensing requirements is to keep in mind that the requirements do not change based on the method of access; they are the same regardless of whether an employee accesses an app by using a portal or through a custom Power App or one of the Microsoft Dynamics 365 apps.

For example, if an employee has a Dynamics 365 Customer Service license assigned, they cannot manage opportunities by using the Partner portal because access to opportunities requires a Dynamics 365 Sales license.

The license that is required depends on the tables and functionalities that are accessed. For more information, see [Dynamics 365 Licensing Guide](https://go.microsoft.com/fwlink/?LinkId=866544&clcid=0x409) or [Power Apps Licensing Guide](https://go.microsoft.com/fwlink/?LinkId=2085130&clcid=0x409).

### Other solutions

Other solutions add features to the portal that can greatly enhance user experience. Some of these capabilities might be agnostic to the choice of template, for example:

- Power Virtual Agents Chatbot
- Click to call
- Customer journey tracking

Alternatively, Microsoft Power Platform and Dynamics 365 independent software vendors and partners that offer Microsoft Power Platform and Dynamics 365 vertical solutions might often include portal extensions that are designed for their solution needs. When you are working with a vendor who offers portals as part of their overall solution, it would be sensible to discuss portal requirements and the portal template selection beforehand.
