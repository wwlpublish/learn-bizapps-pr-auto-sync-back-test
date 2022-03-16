The Community portal template is meant to be used as a platform for an online community. 

> [!NOTE]
> The Community portal is only available on Microsoft Dataverse environments with Dynamics 365 apps enabled.

These communities are often built around the fact that the community members use services of the same organization. Perhaps the online community is comprised of a local city council that provides ongoing services to its constituents. Alternatively, the online community could be people who purchased products from a manufacturer, and who use the community site to share tips and tricks with each other or assist other members in troubleshooting.

Interactions between an organization and community members are often divided into two channels: 

- **Self-service** - The Community portal extends an organization's self-service capabilities, including:

  - Knowledge base access
  - Access to blog posts that share relevant information
  - Advanced search across the site content

- **Assisted service** - The Community portal allows an organization to access Dynamics 365 service support channels: 

  - Submit cases/tickets through configurable web forms
  - Review, update, and comment on existing cases
  - Participate in discussion/community forums

The Community portal caters to both self-service and assisted service scenarios, and portal visitors are able to participate in the following features:

- Forums
- Blogs
- Ideas
- Knowledge articles
- Support cases

## Forums

Forums allow members of a particular community with common interests to post questions, start discussions, or ask for help.  

Forums are set up and configured by using the Portal Management app. For information on how to configure forums, see [Set up and manage forums](/dynamics365/customer-engagement/portals/setup-manage-forums/?azure-portal=true).

The **Forums** feature is also available on the Community, Customer self-service, Employee self-service, and Partner portals.

An organization will choose forums as a way for their community to interact with each other by asking questions, starting discussions, or by looking for help.

Different forums are created within the Portal Management app in the **Community** area by creating a forum record. Forums can be set up to represent different high-level topics that are based on the needs and goals of an organization, for example, general discussions, support, and so on.

Forums fully support multi-lingual deployments and can be language-agnostic or linked to a specific language, which helps you to create portals that encourage global and local conversations between participants. 

When published, the forums are surfaced on the portal so that visitors can create new discussion threads or respond to existing discussions. The visitor can also subscribe to threads to receive updates or new responses to discussions.

Portal visitors will create new threads, which are stored in the Power Apps portal metadata as **Forum Threads** and will contain at least one post (post record). The post will contain the discussion details and optional file attachments. Depending on permissions, other portal visitors can read or respond to particular threads, which will create additional post records. The collection of posts under a thread will represent a particular discussion or answer to a posted question.  

Having an active and engaging forum will strengthen a particular community and potentially alleviate customer and community support resources.

The organization can control from whom and how forum threads and posts are created by using the related Forum Access Permissions, which will link to specific web roles.

## Blogs

The Community portal provides members of its online community a place to post blog articles.  

To learn how to configure and set up blogs on Power Apps portals, see [Manage blogs](/dynamics365/customer-engagement/portals/manage-blogs/?azure-portal=true).

The organization must first create the blog by using the Portal Management app. After the particular blog has been created, the organization can grant the Blog Author web role to the portal user. Then, the portal user will be able to use the front-side editing tools to create blog articles by writing text and inserting images and reference links.

Blogs can also be configured to allow authenticated, unauthenticated, moderated, and unmoderated comments in response to the blog article.

Having an engaging blog will provide updated and compelling content that helps promote the community or an organization's products and services.

The **Blog** feature is unique to the Community portal, but it can be surfaced on other portal types.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RWrtZx]

## Ideas

The **Ideas** feature of the Community portal is an extension of the **Forum** feature, where it will allow members of the public to crowdsource particular ideas or suggestions.

The **Ideas** feature is available on the Community portal, Customer self-service portal, and the Employee self-service portal.

To configure ideas on the Community portal, see [Crowdsource ideas](/powerapps/maker/portals/customer-engagement-apps/crowdsource-ideas).

For an organization to best serve its customers or constituents, it needs to allow an easy feedback mechanism. The **Ideas** feature allows portal visitors to submit a particular suggestion to the organization, which could be for a policy change, a new feature, or a new product or service suggestion. 

When a user adds a new idea, the autocomplete feature on the **Topic** field can be configured to allow visibility of existing ideas to reduce the number of duplicate or similar ideas.  

After the idea has been posted, other portal visitors will be able to vote on the idea or add their own comments or feedback. The policies of feedback and voting are configured from the Dynamics 365 portal app, such as the ability to vote directly on an idea, number of votes, and comment policies.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RWrrm5]

## Knowledge articles

An effective way to maximize the use of helpful content is the ability to search and surface knowledge articles on a Power Apps portal. This feature uses the Dynamics 365 Customer Service knowledge articles (used for internal customer service management) and provides a mechanism to surface on Power Apps portals.

The Power Apps portals **Knowledge Article** feature is available on the Community, Customer self-service, Employee self-service, and Partner portals.

To configure the Power Apps portals **Knowledge Article** feature, see the [Documentation](/dynamics365/customer-engagement/portals/configure-knowledge-categories-articles/?azure-portal=true).

An organization can determine which of its existing knowledge articles should be surfaced on the portal by setting the **Internal** flag and by associating the knowledge article to the appropriate categories.

A portal visitor will be able to navigate through the category structure to locate a specific knowledge article or by using the keyword search features of the portal.

When entering a support case, the portal user might be redirected to browse potentially related knowledge articles to provide a more immediate response to a question and also reduce the case load of the support organization.

## Support cases

The Dynamics 365 Customer Service Case functionality is surfaced on Power Apps portals by using the **Support Case** portal feature.

This use case is common for Power Apps portals and is available on the Community, Customer self-service, Employee self-service, and Partner portals.

To set up and configure the Power Apps portals Case Management features, see [Manage cases in portals](/dynamics365/customer-engagement/portals/case-management/?azure-portal=true).

An organization can allow customers to sign in to the portal and begin the support process by first seeing if the particular question or issue can be resolved with existing information in forum posts or knowledge articles.  

If the provided information is not sufficient to resolve the issue, the customer can create a new support case through the portal. This action will create a corresponding case record in Dynamics 365 Customer Service. The case can be assigned to a particular support representative or team that is following the same business processes that are defined for using the Customer Service Hub.

The support representative can follow existing processes and procedures to resolve the case, such as referring to a knowledge article or providing steps to resolve the issue by using traditional support channels (phone, email). The support representative can also associate a portal comment activity record to the case, which is visible on the case timeline in Dynamics 365 and the portal. Additional configuration by using Dataverse workflow and email integration will allow the customer to be notified of updates to the case with a hyperlink to the portal.

A customer can also respond and update the case by creating portal comments. When the case is resolved, the customer could have the option to reopen the case if the issue was not resolved.
