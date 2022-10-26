There are several recommendations regarding gateway installation, however, the overarching question as to where the gateway should be installed is dependent on the type and volume of data you plan to process through the gateway. Also, the gateway does not have to run on the same machine as the data source, but does require access or a connection to the machines where your data sources reside.

## Hardware

- Start with an 8-core CPU

- 8 GB of memory

- A 64-bit version of Windows Server 2012 R2 or later

- Solid-state drive (SSD) for spooling

## Related considerations

-   Gateways are not supported on Server Core installations.

-   The user installing the gateway must be the admin of the gateway.

-   The gateway can't be installed on a domain controller.

-   If you're planning to use Windows authentication, make sure you install the gateway on a computer that's a member of the same Active Directory environment as the data sources.

-   Don't install a gateway on machines that might be turned off, go to sleep, or disconnected from the internet. The gateway can't run under any of those circumstances.

-   If a gateway uses a wireless network, its performance might suffer.

-   You could install other applications on the gateway machine, but this may degrade gateway performance. If you do install other applications on the gateway machine, be sure to monitor the gateway closely to check if there's any resource contention.

-   You can install up to two gateways on a single computer: one running in personal mode and the other running in standard mode. You can't have more than one gateway running in the same mode on the same computer.

For more information regarding on-premises data gateway installation, see this [article](/data-integration/gateway/service-gateway-install/?azure-portal=true).

## Keep an eye on your performance counters

Performance counters track workload on your gateway and record such things as user access volumes and server performance. Be sure to scale your gateway to adequately handle usage and throughput demand.

Properly scaling your gateway depends on several factors; however, two that are critical are:

-   The frequency and data volume of data model refreshes processed in your Power BI environment

-   The volume of direct queries, including the number of concurrent users, types of visualizations for interactive querying, whether row level security (RLS) is used, and the number of pinned dashboard tiles over direct query and live connect updating in the background

For information on troubleshooting Power BI gateways, refer to this [article](/power-bi/connect-data/service-gateway-onprem-tshoot#performance/?azure-portal=true).
