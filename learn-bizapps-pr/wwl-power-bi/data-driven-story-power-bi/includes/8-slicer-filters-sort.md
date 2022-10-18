Power BI Desktop provides three tools that you can use to edit and configure interactions between the visualizations that you add to your report: slicers, filters, and sorting.

The process of filtering allows you to remove all the data that you don't need, so you can focus on the data that you do need. You can apply filtering directly by using the **Filters** pane or by adding and using a slicer. Slicers and filters are similar; both let you filter out the unnecessary data. Experiment with both options to see which one is the best mechanism for your report situation. You might decide to use one option over the other or use a combination of both.

Contrary to filtering, the process of sorting allows you to highlight the important information without removing any of the data.

## Add a slicer

A slicer is a type of filter that you can add to your report, so users can segment the data in the report by a specific value, such as by year or geographical location. Slicers narrow the portion of the dataset that is shown in the other report visualizations.

You can use a slicer to:

-   Provide quicker access to commonly used or important filters.

-   Simplify a user's ability to see the current filtered state without having to open a drop-down list.

-   Filter by columns that are unneeded and hidden in the data tables.

-   Create more focused reports (by putting slicers next to important visuals).

-   Defer queries to the data model by using a drop-down slicer, particularly when you are using DirectQuery.

Slicers are not supported for input fields and drilldown functions.

When you add a slicer, you can change it to populate a list of items that you want to use to filter the elements of your page. You can make that list appear in a drop-down format if you want to save space for more important data on your report page. Rather than using a list format, you can turn your slicer into buttons to make it easier for users to filter data. Also, you can use your slicer with date type columns, so you can select a different data range by using the slider.

To apply a slicer, select the **Slicer** icon in the **Visualizations** pane. Then, in the **Fields** pane, select the fields that you want to include in the slicer or drag them into the slicer visualization.

The visualization then changes to a list of items (filters) with check boxes that you can use to segment the data. When you select an item's check box, Power BI will filter (slice) all the other visualizations on the same report page, as illustrated in the following image.

> [!div class="mx-imgBorder"]
> [![Screenshot of the slicer icon in the Visualizations pane.](../media/8-use-slicer-ss.png)](../media/8-use-slicer-ss.png#lightbox)

You can add as many slicers as you want to a report page. If you use a list type of slicer, you can configure the selection controls. Select the slicer and then, in the **Format** pane, expand the **Selection controls** section to view the following options:

-   **Single select** - This option is **Off** by default. It ensures that only one item can be selected at a time.

-   **Multi-select with CTRL** - This option is **On** by default. It allows you to select multiple items by pressing the **Ctrl** key.

-   **Show "Select all"** - This option is **Off** by default. If you turn on this option, a **Select all** check box is added to the slicer. You might want to add this option so that you can quickly select or clear all items in the list. If you select all items, selecting an item will clear it, allowing an **is-not** type of filter.

While slicers are useful, if you want to filter your data in a basic way, you don't need to add slicers to your report. Power BI Desktop has a **Filters** pane that can handle the basic slicer operations. Therefore, depending on your requirements, you might save time and effort by avoiding the use of slicers and using the **Filters** pane instead. By using this pane, you can reduce the total number of visuals on a report, which will improve performance.

> [!div class="mx-imgBorder"]
> [![Screenshot of the Filters options for the visual.](../media/8-configure-slicer-controls-ss.png)](../media/8-configure-slicer-controls-ss.png#lightbox)



## Customize filters

From the report user's perspective, the **Filters** pane contains filters that you, the report designer, have added to the report. The filters allow users to interact with the visuals at the report, page, and visual level.

As a report designer, you can customize the **Filters** pane in Power BI Desktop as follows:

-   Add and remove fields to filter on.

-   Change the filter state.

-   Format and customize the **Filters** pane so that it seems part of your report.

-   Define whether the **Filters** pane is open or collapsed by default when a consumer opens the report.

-   Hide the entire **Filters** pane or specific filters that you don't want report consumers to see.

-   Control and bookmark the visibility, open, and collapsed state of the **Filters** pane.

-   Lock filters that you don't want consumers to edit.

You can expand and collapse the **Filters** pane so that you can hide it when you do not need it. When you expand the **Filters** pane, depending on the item in the report that you have selected, you will see the following sections:

-   **Filters on this visual** - Filters that apply to the selected visual and nothing else. This section only displays if you have a visual selected.

-   **Filters on this page** - Filters that apply to the whole page that you currently have open.

-   **Filters on all pages** - Filters that apply to all the pages in your report.

-   **Drillthrough** - Filters that apply to a single entity in a report.

> [!div class="mx-imgBorder"]
> [![Screenshot of the Filters options set to Region is All and SalesAmount is All.](../media/8-configure-filter-options-ss.png)](../media/8-configure-filter-options-ss.png#lightbox)

To apply a filter, drag and drop a field from the **Fields** pane into the relevant section of the **Filter** pane.

> [!div class="mx-imgBorder"]
> [![Screenshot of adding the field to the filters pane.](../media/8-add-field-filters-pane-ssm.png)](../media/8-add-field-filters-pane-ssm.png#lightbox)

## Sort data

You can sort the data that is displayed in your visuals so it's displayed to your specifications.

Sorting helps you display the most important data in the most logical way, such as in alphabetical or numeric order. This basic feature can help when you are making significant business decisions. For example, if you display products with the highest sales first, you are helping users see which product is the most popular among the customer base. Similarly, the products with low sales can be discontinued or replaced with new products to help increase revenue.

To sort a visual, start by selecting the **More options...** button in the upper-right corner of the visual, where you will have three sorting options:

-   **Sort descending** - Sorts the visual by the selected column in the order of greatest value to smallest value.

-   **Sort ascending** - Sorts the visual by the selected column in the order of smallest value to greatest value.

-   **Sort by** - Sorts the data by a specific column. Hover over this option to display the list of columns that you can select from.

> [!div class="mx-imgBorder"]
> [![Screenshot of sorting the the data in a visual.](../media/8-sort-visual-data-ss.png)](../media/8-sort-visual-data-ss.png#lightbox)
