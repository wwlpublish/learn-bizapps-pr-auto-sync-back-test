Microsoft Dataverse allows for many different connections to external data sources. Dual-write and virtual tables (or virtual entities) allow Dataverse to access this data and write back to the original data source.

## Dual-write

Dual-write is an out-of-box infrastructure that provides near-real-time interaction between Dataverse and Finance and Operations apps. When data about customers, products, people, and operations flows beyond application boundaries, all departments in an organization are empowered.

Dual-write provides tightly coupled, bidirectional integration between Finance and Operations apps and Dataverse. Any data change in Finance and Operations apps causes writes to Dataverse, and any data change in Dataverse causes writes to Finance and Operations apps. This automated data flow provides an integrated user experience across the apps.

Find more information on [configuring Dual-write](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/lcs-setup/?azure-portal=true).

## Virtual tables
Virtual tables (also known as virtual entities) enable the integration of data residing in external systems by seamlessly representing that data as tables in Microsoft Dataverse, without replication of data and often without custom coding.

Virtual tables replace previous client-side and server-side approaches to integrating external data, which required customized code and suffered from numerous limitations, including imperfect integration, data duplication, or extensive commitment of development resources. In addition, for administrators and system customizers, the use of virtual tables greatly simplifies administration and configuration.

Find more information on [configuring virtual tables](/power-apps/maker/data-platform/create-edit-virtual-entities/?azure-portal=true).

## When to use Dual-write vs. virtual tables?

Both Dual-write and virtual tables offer useful data integration functionality. It is important to understand when you need to use each tool.

Dual-write should be used when you are working with Dynamics 365 apps and need near real-time integration. Dual-write will duplicate the data in both directions (to and from Dataverse).

Virtual tables should be used when you are connecting to data sources outside of Dynamics 365. There may be built-in connectors for these data sources, or you may have to use a custom connector. 