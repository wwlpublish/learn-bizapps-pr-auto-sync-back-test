The **Decomposition Tree** visual automatically aggregates your data and lets you drill down into your dimensions so that you can view your data across multiple dimensions. Because **Decomposition Tree** is an AI visual, you can use it for improvised exploration and conducting root cause analysis.

In this example, you've built visuals for the Supply Chain team, but the visuals do not answer all the team's questions. In particular, the team wants to be able to analyze the percentage of products that the organization has on back order, in other words, the percentage of products that are out of stock. The **Decomposition Tree** visual can help you accomplish that task.

Add the **Decomposition Tree** visual to your report by selecting the **Decomposition Tree** icon on the **Visualization** pane. Then, in the **Analyze** field well, add the measure or aggregate that you want to analyze. In the **Explain by** field well, add the dimension(s) that you want to drill down into. In this case, you want to analyze the **Sales** field by drilling down into a number of dimensions, such as **Country**, **City**, and **Product**, as illustrated in the following image.

> [!div class="mx-imgBorder"]
> [![Screenshot of the Sales field drill down dimensions.](../media/4-use-decomposition-tree-visual-ss.png)](../media/4-use-decomposition-tree-visual-ss.png#lightbox)

The visual updates according to the fields that you added and displays the analysis summary result. In this case, the value of sales is USD 13,499,680.00. You can select the plus (**+**) sign, which will present the drill-down options that you have added. You can select any of the fields in the drop-down list to drill down into the data and see how it contributed to the overall result.

At the top of the list of dimensions that you added are two additional options that are marked with lightbulb icons. These options are referred to as *AI splits*, and they'll automatically find high and low values in the data for you.

> [!div class="mx-imgBorder"]
> [![Screenshot of the AI split options of high and low values.](../media/4-ai-split-options-ss.png)](../media/4-ai-split-options-ss.png#lightbox)

AI splits work by considering all available fields and determining which one to drill into to get the highest/lowest value of the measure that is being analyzed. You can use the results of these splits to find out where you should look next in the data. The following image illustrates the result of selecting the **High value** AI split.

> [!div class="mx-imgBorder"]
> [![Screenshot of the high value AI split in a decomposition tree.](../media/4-apply-ai-split-decomposition-tree-ss.png)](../media/4-apply-ai-split-decomposition-tree-ss.png#lightbox)

For more information, see [Create and view decomposition tree visuals in Power BI](/power-bi/visuals/power-bi-visualization-decomposition-tree?azure-portal=true).
