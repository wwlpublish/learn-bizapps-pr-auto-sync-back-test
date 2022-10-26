Analytical reports can serve various report consumer use cases while providing a structured place for analysis. The primary goal of this report type is to allow the report consumer to discover answers to a broad array of questions.

Because most report consumers have limited time, analytical reports can help them by breaking down complex reports in two ways:

- Condense data volumes into smaller, more targeted results.

- Visualize results graphically to enable quick comprehension of data.

Each data visual on a report page condenses data by using an *analytic query*. An analytic query has three phases that are executed in the following order:

1. **Filter** (or *slicing*) - Targets the data of relevance. Filters can be applied to three different scopes: report, page, or visual.

1. **Group** (or *dicing*) - Divides query results into groups.

1. **Summarize** - Produces a single value result. Typically, numeric columns are summarized by using summarization methods (sum, count, and many others).

    > [!div class="mx-imgBorder"]
    > [![An animation shows the sequence of the filter, group and summarize query phases.](../media/1-filter-group-summarize.gif)](../media/1-filter-group-summarize.gif#lightbox)

Not all analytic queries need to filter, group, and summarize:

- Commonly, report visuals are filtered, perhaps by a time period or geographic location.

- Grouping is optional. For example, a card visual, which is used to display a single value isn't concerned with grouping.

- Report visuals typically summarize. However, one notable exception is the slicer visual, which isn't concerned with summarization.

This module considers a scenario concerning the **Contoso Skateboard Store** company. The company specializes in direct-to-consumer skateboard sales. To modernize their workflow and to gain a deeper understanding of their product sales, they need to create an analytical report to create awareness of sales performance.

Without this report, salespeople who need to see monthly order counts for a specific year would need to make sense of numerous sales orders. Clearly, the task would be challenging to undertake. However, the task is simple and quick for a column chart visual in an analytical report.

In this case, the column chart visual can submit an analytic query to filter by the required year, group by month, and summarize sales amounts by counting the orders. Then, the groups are displayed as columns, and the column heights are set to the summarized order counts.

To better understand analytical reports, watch the following video that describes the key concepts that are presented in this unit.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RWO6gW]
