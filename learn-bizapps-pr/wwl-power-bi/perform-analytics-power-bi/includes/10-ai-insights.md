The **AI Insights** feature allows you to connect to a collection of pretrained machine learning models that you can apply to your data to enhance your data preparation efforts.

Continuing with the previous example, you now want to add text analytics to the content of the **Comments** field in the ticketing data. This process will help you see if you can determine the sentiment of the customers that are featured in the Help tickets. You can use the **AI Insights** feature to accomplish that task.

To apply the **AI Insights** feature to your data, open Power Query Editor and select the **Add Column** tab. Three **AI Insights** options will be available for you to choose from: **Text Analytics**, **Vision**, and **Azure Machine Learning**.

> [!NOTE]
> Premium capacity is required to use the **Text Analytics** and **Vision** options.

> [!div class="mx-imgBorder"]
> [![Screenshot of A I Insights options in Power Query Editor.](../media/10-ai-insights-options-ssm.png)](../media/10-ai-insights-options-ssm.png#lightbox)

> [!NOTE]
> If you do not see these options, you need to enable the **AI Insights** feature in Power BI Desktop settings. Go to **File > Options and settings > Options**. In the **Global** options list, select **Preview features**, select the check box for the **AI Insights function browser** option, and then select **OK**.

> [!div class="mx-imgBorder"]
> [![Screenshot of the Enable AI Insights feature.](../media/10-enable-ai-insights-feature-ssm.png)](../media/10-enable-ai-insights-feature-ssm.png#lightbox)

On the **Add column** tab, the most relevant **AI Insights** option for this example is **Text Analytics**. This option includes Azure Cognitive Services models, such as Sentiment Analysis, Key Phrase Extraction, and Language Detection, that derive meaning or specific pieces of language from text data. You can use either the Sentiment Analysis or Key Phrase Extraction option to determine the customer sentiments in the Help tickets and visually show the results in Power BI.
