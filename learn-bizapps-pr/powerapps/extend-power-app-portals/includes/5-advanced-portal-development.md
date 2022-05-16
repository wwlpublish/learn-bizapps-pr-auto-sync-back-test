Using JavaScript and CSS to manipulate client-side visibility and functionality of portal pages can help you achieve considerable success in satisfying some key business requirements. To satisfy more complex scenarios, a developer can be creative and use other strategies to extend Power Apps portals.

### Partner libraries

JavaScript can use other JavaScript libraries that deliver functionality such as UX enhancements (masked controls, for example), real-time communications (SignalR), sophisticated UI building (Angular, Vue, React), and other various business services like address validations, map API, routing services, logistics, and so on.

Power Apps portals create a clean, responsive layout with predictable element names, which helps make manipulating the data and UI easier.

For an example of a sophisticated implementation that can be hosted in Power Apps portals and that uses Angular framework for communications, go to the [Set up the event website](/dynamics365/marketing/set-up-event-portal/?azure-portal=true) documentation for Dynamics 365 Marketing.

### API calls

Combined with custom web templates that use Liquid code to deliver *data* instead of HTML, JavaScript can call *back* into Power Apps portals to retrieve the data and then use it to create alternative UX. For example, instead of using the **Table List** calendar view, you can retrieve list data in JSON format instead and then use other calendaring libraries, like FullCalendar, to create sophisticated calendar visualization. Alternatively, you can retrieve opportunity data and use another charting JavaScript library for sophisticated interactive charting.

> [!IMPORTANT]
> When you use web templates, it is only possible to implement REST service for GET operations. No other operation, such as PUT, is supported by Liquid code.

### Companion app

Situations might occur where you want to communicate securely with external services while maintaining the security context, such as when you are processing online payments. Power Apps portals enables this scenario by providing support for [OAuth 2.0 implicit grant flow within your portal](/power-apps/maker/portals/oauth-implicit-grant-flow/?azure-portal=true).

This feature allows a customer to make client-side calls to external APIs and secure them by using OAuth implicit grant flow. This method helps ensure that the identity information of a signed-in user is passed in a secured manner to the external calls.

In this scenario, you build a custom web application and Power Apps portals would communicate to this application by using JavaScript to call the API.  

CSS and JavaScript enable a number of integration and extensibility scenarios that range from simple UI adjustments, to validation and data input, to sophisticated client-side applications that interact with other services.
