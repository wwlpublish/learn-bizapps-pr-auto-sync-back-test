Businesses that have Dynamics 365 or a custom Microsoft Dataverse solution already in place can quickly build a portal that is more secure and build their entire website, all without requiring developers.

A Power Apps portal is not automatically provisioned when a new Dataverse environment is created. You will need to provision a Power Apps portal and determine the name, default URL, language, and template.

Power Apps portals evolved from Dynamics 365 Portals, which is now referred to as Power Apps portals. The key difference is that several additional portal templates are available for Dynamics 365-enabled environments.

> [!IMPORTANT]
>
> To provision a portal, you must be assigned to the System Administrator role of the Dataverse environment that is selected for the portal.

## Portal templates

Portal templates are preconfigured portal solutions that are available to accelerate deployment. Power Apps portals are customizable, but a portal template will provide a preconfigured environment that is immediately suitable for specific scenarios.

The following portal templates are available:

- Portal from blank
- Custom (Dynamics 365 apps)
- Community (Dynamics 365 apps)
- Customer self-service (Dynamics 365 apps)
- Employee self-service (Dynamics 365 apps)
- Partner (Dynamics 365 apps)
- Supply Chain Management Customer (Dynamics 365 apps)

The Partner portal also includes optional Field Service and Project Service add-ons that are available if your Dynamics 365 environment includes Dynamics 365 Field Service and Dynamics 365 Project Service solutions.

Each of the starter portals includes a particular set of features that are designed to accelerate solution development that targets the selected audience.

## Portal features

Power Apps portals is a platform and includes a long list of components and features out of the box. The following table shows how these features map into the key capability areas of Power Apps portals.

| Content                          | Extensibility          | Security                   | Functionality                              |
| -------------------------------- | ---------------------- | -------------------------- | ------------------------------------------ |
| Accessibility                    | Web Forms              | Profile Management         | Case Deflection                            |
| Bootstrap Design                 | Web Templating         | Web Roles                  | Case Management                            |
| Branding                         | Table Forms           | Invitations                | Knowledge Management                       |
| Content Publishing               | Table Lists           | Content Permissions        | Discussion Forums                          |
| Responsive Design                | Table Actions         | Table Permissions         | Ideas, Blogs                               |
| Webpages                        | Automation    | Identity                   | Customer, Account, & Opportunity Management |
| Faceted Search and SEO           | Charts & Graphs        | Authentication             | Delegated Administration                   |
| Multilingual Portals            | Azure Integration      | Auth Providers integration | Multi-Partner Collaboration                |
| Ads, Polls, Ratings, and Comments | SharePoint Integration |                            | Entitlements & SLAs                        |
| Theming  | Power BI Integration   |                            | Localization into 43 Languages             |
| Web Files | Client-side JavaScript |||
|| Liquid Templates |||
|| Web API |||

All components and features that are listed under **Content**, **Extensibility**, and **Security** form the portal foundation. They are part of the base solution and included in all portals. Features from the **Functionality** area focus on the specific needs of the target audience. Starter portal selection defines which subset of functional features is included.

> [!NOTE]
>
> The starter portal selection might lock you into a specific set of features. Portal features are deployed into the target Dynamics 365 environment as managed solutions. Portal features can be added or removed later.

## Provision a portal

Only one Power Apps portal can be provisioned for each Dataverse environment.

The high-level steps to provision a starter portal are:

1. Go to [https://make.powerapps.com](https://make.powerapps.com/?azure-portal=true).

2. Select a target environment by using the environment selector in the upper-right corner.

3. On the left menu, select **+ Create**.

4. Select **Portal from blank**. If you have Dynamics 365 apps deployed in your Dataverse environment, additional portal templates, such as Customer self-service, will be available.

5. Provide a name for the portal.

6. Provide a unique address (URL) for the portal.

7. Select the language.

8. Select **Create** to start the portal provisioning process.

   After portal provisioning has completed, the portal will appear in the list as an app of type Portal.

9. Select the ellipsis (**...**) next to the portal app name and then select **Browse** to open the portal website.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4yoJw]
>
>
>
Step-by-step instructions to provision a portal are available at [Provision a portal](/dynamics365/portals/provision-portal?azure-portal=true).
