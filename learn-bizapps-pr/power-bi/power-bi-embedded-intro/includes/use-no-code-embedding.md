It's possible to embed reports by using techniques that don't require programming. These techniques are known as *no-code embedding*. The process of setting up these techniques is straightforward for business analysts and content consumers.

> [!NOTE]
> The focus of this module is on programmatic embedding of Power BI content. However, it's helpful to know that in some circumstances, you can embed without the need to develop an app.

## Power BI reports

Power BI supports three embedding techniques for Power BI reports that don't require programming. Two techniques allow you to embed content more securely in an internal portal or website:

- Use the Power BI report web part to embed Power BI reports in SharePoint Online.
- Use a secure embed code (or HTML) that's generated by Power BI to embed Power BI reports in internal web portals.

When using these techniques, report consumers must belong to the organization, be authenticated, and have permission to access the reports. Power BI ensures that all permissions and data security are enforced when consumers view the reports. Sometimes, users might be challenged to authenticate by signing in to Power BI.

A third no-code embedding technique is called **Publish to web**. This technique provides access to Power BI reports to anyone on the Internet. It doesn't require authentication and access isn't logged for auditing purposes. Because report consumers don't need to belong to the organization or have a Power BI license, this technique is well suited to data journalism, a process where reports are embedded in blog posts, websites, emails, or social media.

> [!CAUTION]
> The **Publish to web** feature is a powerful technique that shares Power BI reports with the world. However, it has the potential to expose private or sensitive data, whether accidentally or intentionally. For this reason, this feature is disabled by default. A Power BI administrator must enable the feature and should restrict its use to specific trusted users or security groups.

## Power BI paginated reports

Power BI allows you to render a paginated report by using its URL. It's possible to append URL parameters, which encapsulate information such as report parameter values, export format, and many others.

Similar to embedding Power BI reports, paginated report consumers must belong to the organization, be authenticated, and have permission to access the paginated reports. Power BI ensures that all permissions and data security are enforced when consumers view the reports.

For more information, see the following articles:

- [Embed a report web part in SharePoint Online](/power-bi/collaborate-share/service-embed-report-spo/?azure-portal=true)
- [Embed a report in a secure portal or website](/power-bi/collaborate-share/service-embed-secure/?azure-portal=true)
- [Publish to web from Power BI](/power-bi/collaborate-share/service-publish-to-web/?azure-portal=true)
- [URL parameters in paginated reports in Power BI](/power-bi/paginated-reports/report-builder-url-parameters/?azure-portal=true)
