In addition to the core portal features and the features that are provided by the templates, other unique requirements from specific Dynamics 365 applications can be extended by using alternate portal applications and templates.

## Event Management portal (Dynamics 365 Marketing)

The Event Management portal extends the Dynamics 365 Marketing application by providing an [angular.js](https://angularjs.org/?azure-portal=true) based template application that can be embedded in most industry standard content management systems and Power Apps portals.

By using Dynamics 365 Marketing, staff would create a conference or event, design graphics, and define speakers, sessions, and other registration details. These assets will be used to render a conference portal by using the angular.js template. The features of the Event Management portal are:

- Visitors are allowed to view event information, speakers, and sessions.
- Interested parties can create an event portal account.
- Potential attendees can register themselves or others for the event.
- Event participants can purchase passes for the event or specific sessions.
- Participants can modify or cancel their registrations.

Integrations to specific payment gateways will need to be custom developed and are not part of the Event Management portal.

> [!div class="mx-imgBorder"]
> [![Screenshot of the Event Management Portal.](../media/3-event-portal.png)](../media/3-event-portal.png#lightbox)


For more information, see the [Dynamics 365 Marketing Portal](/dynamics365/marketing/set-up-event-portal/?azure-portal=true) documentation.

## Customer portal (Dynamics 365 Supply Chain Management)

The Customer portal template allows you to create an externally facing website that is connected to a Dynamics 365 Supply Chain Management environment. It uses [dual-write capabilities](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page/?azure-portal=true) to link Microsoft Dataverse entities to Dynamics 365 Supply Chain Management data. 

The template provides guidance and a starting point for creating custom websites for business-to-business (B2B) sales-order processing and related scenarios. It helps companies bring dual-write, Power Apps portals, and Dynamics 365 Supply Chain Management together to create a self-service experience for their enterprise customers.

> [!NOTE] 
> You will need to have the dual-write solutions installed on your Dataverse environment to provision the Dynamics 365 Supply Chain Management Customer portal.

The key features of the Customer portal are:

- Visibility to order history
- Ability to view account information
- Ability to create orders on the portal

For more information, see the [Dynamics 365 Supply Chain Management Customer Portal](/dynamics365/supply-chain/sales-marketing/customer-portal-overview/?azure-portal=true) documentation.