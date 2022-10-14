The **Quick insights** feature in Power BI uses machine learning algorithms to go over your entire dataset and produce insights (results) for you quickly. This feature is a great way to build dashboards when you don't know where to start. It also helps you find insights you might have missed when building your reports. From the insights that Power BI discovers, you can generate appealing, interactive visualizations.

> [!NOTE]
> This feature is available in the Power BI web service only. Also, this feature doesn't work with DirectQuery; it only works with data that is imported to Power BI.

Consider the scenario where one of the datasets that you've been given contains substantial data concerning the Help tickets that were created for the Customer Service team. Because of the extensive data, you don't know where to begin analyzing, so you decide to let Power BI do it for you.

## Get quick insights on your dataset

To get quick insights on your dataset, open your Power BI web service and then select the **Content** tab. Locate your report for which you want to get quick insights, which in this case is **TailwindTraders**. Then, select **More options (...) > Quick insights**.

> [!div class="mx-imgBorder"]
> [![Screenshot of the ellipsis button with the Quick insights option.](../media/9-get-quick-insights-ssm.png)](../media/9-get-quick-insights-ssm.png#lightbox)

Power BI will use various algorithms to search for trends in your dataset. This process might take a few seconds, but when it is finished, you'll see a message in the upper-right corner letting you know that the results are ready to be viewed.

> [!div class="mx-imgBorder"]
> [![Screenshot of Insights are ready message.](../media/9-insights-message-ss.png)](../media/9-insights-message-ss.png#lightbox)

Select **View insights** to open the **Quick Insights** page for the selected dataset, and then view the insights that Power BI has found for you. The **Quick Insights** page contains up to 32 separate insight cards, and each card has a chart or graph plus a short description. In this example, one of the insights is a card that displays a visual for **Count of Product by Category Name**, as illustrated in the following image.

> [!div class="mx-imgBorder"]
> [![Screenshot of the Count of Product Quick Insights card.](../media/9-insights-card-ss.png)](../media/9-insights-card-ss.png#lightbox)

## Add a Quick insights result card to a dashboard

If you see an insight card that is particularly compelling, you can add it to your dashboard. On the **Quick Insights** page, hover over the card, then select the pin icon. The visual is added to your dashboard, where you can reposition it as required.

## Interact with the quick insights results

To take a closer look at a particular insight card on the **Quick Insights** page, select an insight card to open. The insight screen opens in **Focus** mode.

> [!div class="mx-imgBorder"]
> [![Screenshot of the Quick Insights focus mode.](../media/9-insights-focus-mode-ss.png)](../media/9-insights-focus-mode-ss.png#lightbox)

You can then perform the following actions:

- Filter the visualization by using the available options in the **Filters** panel.

- Pin the insight card to a dashboard by selecting **Pin visual**.

- Run insights on the card (scoped insights) by selecting **Get insights** in the upper-right corner. The scoped insights allow you to drill into your data.

- Return to the original insights canvas by selecting **Exit Focus mode** in the upper-left corner.
