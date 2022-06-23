Portal templates provide more features that extend the functionality of Microsoft Dynamics 365 apps. The following sections describe the features that can be found in portal templates.

## Case management

The case management capabilities extend Dynamics 365 Customer Service by allowing portal users to log and update support cases, tickets, and questions. This information is stored in the Dynamics 365 case table and communications are tracked by using portal comments.

This feature is a common use case for portals and provides customer service organizations with a key channel to interact with their customers. A key benefit is that customers who want to submit a ticket are presented with options to review existing knowledge articles and forum posts because these items might resolve the customer's question in a faster manner.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RWrBLh]

## Knowledge management

One way for an organization to provide its external stakeholders with access to corporate information is to use the knowledge management features of Power Apps portals.

Knowledge articles can be created, approved, and curated in Dynamics 365 Customer Service and will then appear on the portal. Portal users will be able to browse and search knowledge articles, as needed.

Portal users who attempt to log a support case might be presented with a list of potential knowledge articles that could answer the specific query, deflecting the need to log a support case.

Knowledge management is available by default on the Customer self-service, Partner, Employee, and Community portal templates.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RWrEmA]

## Forums

Forums allow members of a particular community who share common interests to post questions, start discussions, or ask for help. Having an active and engaging forum strengthens a particular community and potentially alleviates customer and community support resources.

Forums are set up and configured by using the Portal Management app. For information on how to configure forums, see [Set up and manage forums](/dynamics365/portals/setup-manage-forums/?azure-portal=true). The **Forums** feature is also available on the Community, Modern Community, Customer self-service, Employee self-service, and Partner portals.

Forums fully support multilingual deployments and can be language-agnostic or linked to a specific language, which allows you to create portals that encourage global and local conversations between participants. 

The organization can control from whom and how forum threads and posts are created, as determined by the related Forum Access Permissions, which will link to specific web roles.

## Blogs

The Community portal has the ability for members of its online community to post blog articles. Having an engaging blog will provide updated and compelling content to help promote the community or an organization's products and services.

See [Manage blogs](/dynamics365/customer-engagement/portals/manage-blogs/?azure-portal=true) to learn how to configure and set up blogs on Power Apps portals.

Blogs can also be configured to allow authenticated, unauthenticated, moderated, and unmoderated comments in response to the blog article.

The **Blog** feature is unique to the Community portal but it can be shown on other portal types.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RWrtZx]

## Ideas

For an organization to best serve their customers or constituents, it's important that they allow an easy feedback mechanism. 

The **Ideas** feature is an extension of the **Forums** feature in that it will allow members of the public to crowdsource particular ideas or suggestions. It's available on the Community, Modern Community, Customer self-service, and Employee self-service portals.

To configure ideas on the Community portal, see [Crowdsource ideas](/dynamics365/customer-engagement/portals/crowdsource-ideas/?azure-portal=true).

When a user adds a new idea, the autocomplete feature on the **Topic** field can be configured to allow visibility of existing ideas to reduce the number of duplicate or similar ideas.  

After the idea has been posted, other portal visitors will be able to vote on the idea or add their own comments or feedback. The policies of feedback and voting are configured from the Dynamics 365 Portal app. These policies could include the ability for users to vote on an idea, the number of votes allowed, and types of comments that are permitted.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RWrrm5]

## Project Service Automation 

The **Project Service Automation** feature is specific to the Partner portal template. To provide the **Project Service Automation** features, the Dynamics 365 Project Service app will need to be provisioned. The **Project Service Automation** portal extensions can be selected during the Partner portal installation or it can be installed later from the Portal admin center.

> [!div class="mx-imgBorder"]
> [![Screenshot of the enable packages feature.](../media/2-project-service-provision.png)](../media/2-project-service-provision.png#lightbox)

> [!div class="mx-imgBorder"]
> [![Power Apps Portals admin center, install Project Service automation extension.](../media/2-project-service-admin.png)](../media/2-project-service-admin.png#lightbox)

The key features of the **Project Service Automation** extension are:

- Ability for external stakeholders to view project information
- Process to confirm bookable resources
- Approve quotes
- View invoices
- Review contract and order forms

For more information, see the [Project Service Portal Extension](/dynamics365/portals/integrate-project-service-automation/?azure-portal=true) documentation.

## Field Service integration 

The Partner Field Service portal integration extends the Dynamics 365 Field Service module to the Partner portal template. To add the Field Service portal extension, the Dynamics 365 Field Service app will need to be provisioned. The Field Service portal features can be selected during the Partner portal installation or they can be installed later by using the Portal admin center.

> [!div class="mx-imgBorder"]
> [![Power Apps Portals admin center, install Field Service extension.](../media/2-field-service-admin.png)](../media/2-field-service-admin.png#lightbox)

The main features of the Field Service extension are:
- Ability for external stakeholders to view customer assets
- Allow customers to view and request work orders from the portal
- Customers can view invoices on the portal

For more information, see the [Field Service Portal Extension](/dynamics365/portals/integrate-field-service/?azure-portal=true) documentation.

In the Dataverse instance with Dynamics 365 Field Service app installed, a separate Field Service Portal can be provisioned that provides your customers with email and SMS updates, ETAs, and the [real-time technician location for their next service visit](/dynamics365/field-service/reminders-arrival-time/?azure-portal=true).