With the **Query Caching** feature, you can use the local caching services of Power BI to process query results. Instead of relying on the dataset to calculate queries, which when overloaded can reduce performance, you can use cloud resources on your Premium capacities on Power BI service to load your report and, thereby, ensure constant performance. 

To continue with the module scenario, as you begin collaborating with more teams to build reports and dashboards, you notice that some of your datasets are causing the reports to load more slowly than before, an issue that is starting to annoy your users. The Sales team wants to know how they can improve performance and make these reports load faster. You decide to use the **Query Caching** ability in Power BI to help solve this problem.

## Query caching 

**Query Caching** is a local caching feature that maintains results on a user and report basis. This service is only available to users with Power BI Premium or Power BI Embedded.  

When using query caching, the query results are only specific to a user, and you can only use query caching on a specific page of a report. Several benefits to using query caching include:  

-   Improvement of the performance of reports, dashboards, and dashboard tiles by reducing loading time and increasing query speed; this notion is especially true for datasets that are not refreshed often and are accessed frequently.  

-   It respects bookmarks and default filters, so even if you enable query caching, any bookmarks that you have created still exist. 

-   Cached query results are specific to the user. 

-   All security labels are followed.   

-   It reduces the load on your dedicated capacity. 

To access and configure query caching, follow these steps:

1. Go to a dataset in your workspace and open its **Settings** page. In this example, you will enable query caching for **SalesDataset**.  

   > [!div class="mx-imgBorder"]
   > [![Query Caching in Settings](../media/9-query-caching-settings-ssm.png)](../media/9-query-caching-settings-ssm.png#lightbox)

2. Select the **Datasets** tab and expand the **Query Caching** options, as shown in the following image.  

   > [!div class="mx-imgBorder"]
   > [![Query caching options](../media/9-query-caching-options-ss.png)](../media/9-query-caching-options-ss.png#lightbox)

3. On the **Query Caching** page, choose one of the available options. The default option is that query caching is turned off; however, you can also select **Off**, which turns off query caching for the specific dataset in question. If you select **On**, query caching will be turned on for this specific dataset only. For this example, you will select **On** for your dataset because you want to apply query caching to your specific dataset.  

> [!NOTE]
> Switching from **On** to **Off** will clear all previously saved query results. When turning off query caching (either through the default or the **Off** option), a small delay will occur in query loading because the report queries are running against the dataset and it does not have saved queries to fall back on.

> [!WARNING]
> If many datasets have query caching enabled, and a refresh occurs, a reduction in performance might occur because a large number of queries are being processed at once.  

For more information, see [Query Caching in Power BI](/power-bi/connect-data/power-bi-query-caching/?azure-portal=true).

