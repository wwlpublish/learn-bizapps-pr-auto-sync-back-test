In this exercise, you'll create a trial Microsoft Azure tenant. Then, you’ll set up a trial Dynamics 365 Customer Insights environment to deploy the Retail churn model.

[Dynamics 365 Customer Insights](/ai/customer-insights/?azure-portal=true) is a part of Microsoft's customer data platform, which helps deliver personalized customer experiences. The platform's capabilities provide insights into who your customers are and how they engage with your platform. With Customer Insights, you can unify customer data across multiple sources to get a single view of customers.

-   [Audience insights](/dynamics365/customer-insights/audience-insights/overview/?azure-portal=true) helps you transform your business into a customer-centric organization. Marketing, sales, and service professionals have the insights that they need to personalize experiences. Audience insights helps you connect data from transactional, behavioral, and observational sources to create a 360-degree customer view. Accordingly, you’ll experience faster results with a customer data platform that’s designed to deliver insights that you can act on.

-   [Retail channel churn predictive model](/dynamics365/industry/retail/retail-use-churn-prediction/?azure-portal=true) is a key feature of Unified customer profile. It uses an AI-based model to help omnichannel retailers use cross-channel data to assess the chance that a customer will churn, meaning that they’ll stop actively buying.

## Task 1: Create a Customer Insights environment

In this task, you'll create a new trial Customer Insights sandbox environment. To set up **Customer intelligence** correctly, you must first create a Customer Insights sandbox environment and then connect it to your Microsoft Dataverse environment with no data sources specified. After you’re connected, you'll go through the [Solution Center](https://solutions.microsoft.com/?azure-portal=true) to deploy **Customer intelligence** from **Unified customer profile**, specifying the Customer Insights environment that you create in this task.

1.  Open an InPrivate or Incognito window and then go to [Customer Insights](https://dynamics.microsoft.com/ai/customer-insights/?azure-portal=true). Select the **Try for free** button.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the Customer Insights page, showing the Try for free button.](../media/customer-insights.png)

1.  Sign in with the account that you created as part of Lab 1: Seamless customer experience -Training environment preparation, Task 1.

1.  Select **Audience insights** as your focus.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of Audience insights selected as the focus.](../media/audience-insights.png)

    After you’ve selected Audience insights, your screen should resemble the following image.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the Audience insights page.](../media/audience-insights-page.png)

1.  In the upper-right corner of the screen, select the environment name and then select **+ New** to create a new environment.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the environment page with New environment selected.](../media/new-environment.png)

1.  Fill out the appropriate fields and then select **Next**.

    1.  **Name** - <<UserName\>\> Retail Churn

    1.  **Choose your business** - Individual consumers (B-to-C)

    1.  **Region** - West US

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the new environment basic information details.](../media/environment-basic-information.png)

1.  Select **Review and finish**.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the Review and finish button for the new environment.](../media/review-finish.png)

1.  Wait for the environment to be created.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the message indicating that the environment is being created.](../media/create-message.png)

Congratulations, you’ve successfully created a Customer Insights environment.

## Task 2: Deploy the Retail churn model
To deploy the Retain Churn Model, follow these steps:

1.  Open a new tab in your internet browser and go to the [Microsoft Cloud Solution Center](https://solutions.microsoft.com/?azure-portal=true).

1.  Expand **Retail** and go to **Unified customer profile**. Select the **Added** checkbox next to Unified customer profile and then select **Deploy**.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of Unified customer profile selected.](../media/unified-customer-profile.png)

1.  Select the **Customer Insights Environment** that you created in the previous task, provide a name for your deployment, and then agree to the **Terms of service**. Select **Next**.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the Customer Insights environment information filled in.](../media/customer-insights-environment.png)

1.  Select **Deploy** to deploy the Retail churn model to your Customer Insights environment.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the Deploy button to deploy the Retail churn model.](../media/deploy.png)

    Deployment will take several minutes to complete.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the deployment status message.](../media/deploy-status.png)

1.  When the deployment process is complete, select **Close**.

	> [!div class="mx-imgBorder"]
	> ![Screenshot showing that the deployment is complete and the Close button.](../media/close.png)

Congratulations, you’ve successfully deployed the Retail churn model.
