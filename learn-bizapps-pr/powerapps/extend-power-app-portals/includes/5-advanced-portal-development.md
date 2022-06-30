Using JavaScript and CSS to manipulate client-side visibility and functionality of portal pages can help you achieve considerable success in satisfying some key business requirements. To satisfy more complex scenarios, a developer can be creative and use other strategies to extend Power Apps portals.

## Partner libraries

JavaScript can use other JavaScript libraries that deliver functionality such as UX enhancements (masked controls, for example), real-time communications (SignalR), sophisticated UI frameworks (Angular, Vue, React), and other various business services like address validations, map API, routing services, logistics, and so on.

Power Apps portals create a clean, responsive layout with predictable element names, which helps make manipulating the data and UI easier.

For an example of a sophisticated implementation that can be hosted by Power Apps portals and that uses Angular framework for communications, go to the [Set up an event website (Dynamics 365 Marketing)](/dynamics365/marketing/set-up-event-portal/?azure-portal=true) documentation for Dynamics 365 Marketing.

## Code components

Pro developers can use Power Apps component framework to create code components for model-driven and canvas apps. These code components can provide an enhanced experience for users working with data on forms, views, and dashboards. 

Power Apps portals now supports controls for model-driven apps created using Power Apps component framework. To use code components in portals webpages, follow these steps:

1. Create and package your code component or use an existing code component.
2. Add the code component to a column on a model-driven form.
3. Configure basic form for code component.

For more information, see [Use code components in portals](/power-apps/maker/portals/component-framework/?azure-portal=true).

## Portals Web API

Pro developers can use portals Web API to interact with Dataverse data directly from JavaScript and create a richer user experience inside portal pages. You can use the Web API to perform create, read, update, and delete operations across all Microsoft Dataverse tables.

The data is protected by using a combination of web roles as well as table and column permissions to ensure that portal visitors only have the appropriate access to Dataverse rows and columns.

For more information, see [Overview of portals Web API ](/power-apps/maker/portals/web-api-overview/?azure-portal=true).

## Companion apps and services

Situations might occur where you want to communicate securely with external services while maintaining the security context, such as when you are processing online payments. Power Apps portals enables this scenario by providing support for [OAuth 2.0 implicit grant flow within your portal](/power-apps/maker/portals/oauth-implicit-grant-flow/?azure-portal=true).

This feature allows a customer to make client-side calls to external APIs and secure them by using OAuth implicit grant flow. This method helps ensure that the identity information of a signed-in user is passed in a secured manner to the external calls.

In this scenario, you build a custom web application and Power Apps portals would communicate to this application by using JavaScript to call the API.  

CSS and JavaScript enable a number of integration and extensibility scenarios that range from simple UI adjustments, to validation and data input, to sophisticated client-side applications that interact with other services.
