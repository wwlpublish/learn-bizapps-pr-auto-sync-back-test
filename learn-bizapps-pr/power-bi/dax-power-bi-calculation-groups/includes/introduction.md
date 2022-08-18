Calculation groups are a relatively new Data Analysis Expressions (DAX) capability. They allow you to quickly create many similar measures, and they can help declutter the **Fields** pane.

You'll likely find that calculation groups are helpful when you need to create *time intelligence* calculations. Time intelligence means modifying the filter context for date filters to achieve calculations, such as:

- Prior year (PY)
- Year-over-year (YoY)
- Year-over-year percentage (YoY%)
- Year-to-date (YTD)

For example, you want to create these four time intelligence calculations for each of the six sales measures: gross sales, net sales, cost, gross profit, net profit, and quantity. Without using calculation groups, that process would involve creating 24 (6 x 4) separate measures.

> [!NOTE]
> You'll create a time intelligence calculation group in Unit 3.

A calculation group is a special type of calculated table. The rows that you add to the table are known as *calculation items*. Calculation items are reusable calculations that Microsoft Power BI can apply to any measure.

## Use calculation groups

Using calculation groups is straightforward. From a report authoring perspective, a calculation group is available in the **Fields** pane, and it looks like a regular a table. When you add the calculation group field to a visual, the visual will group by the calculation items.

For example, the following matrix visual shows monthly sales for fiscal year 2022. A calculation group provides three different perspectives, including PY (prior year), YoY (year-over-year), and YoY percent. You'll have the opportunity to create that calculation group in Unit 3.

> [!div class="mx-imgBorder"]
> [![Matrix visual showing monthly sales for fiscal year 2022 providing three different perspectives.](../media/monthly-sale-matrix.png)](../media/monthly-sale-matrix.png#lightbox)

## Work with calculation group functions

Four special DAX functions are available for you to use when defining calculation items:

- `SELECTEDMEASURE` - Returns a reference to the measure that's currently in context when the calculation item is evaluated. This function doesn't take any parameters.
- `SELECTEDMEASURENAME` - Returns a string value of the name of the measure that's currently in context when the calculation item is evaluated. This function doesn't take any parameters.
- `SELECTEDMEASUREFORMATSTRING` - Returns a string value of the format string of the measure that's currently in context when the calculation item is evaluated. This function doesn't take any parameters.
- `ISSELECTEDMEAUSURE` - Returns a Boolean value that indicates whether the measure that's currently in context is one of those specified in the list of parameters. You can pass in one or more measures.

You'll work with the `SELECTEDMEASURE` DAX function in Unit 3.