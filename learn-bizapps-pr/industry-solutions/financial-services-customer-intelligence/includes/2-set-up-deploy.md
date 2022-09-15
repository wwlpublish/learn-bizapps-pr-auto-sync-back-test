In this exercise, you'll explore the Customer intelligence components of Microsoft Cloud for Financial Services. You'll also create a Customer Insights instance and deploy the Customer intelligence capability from Microsoft Solution Center.

[Dynamics 365 Customer Insights](https://dynamics.microsoft.com/ai/customer-insights/?azure-portal=true) is part of the customer data platform in Microsoft, which helps you deliver personalized customer experiences. The platform's capabilities provide insights into who your customers are and how they engage with your platform. Customer Insights helps you unify customer data across multiple sources to get a single view of customers. Customer Insights helps you transform your business into a customer-centric organization. Marketing, sales, and service professionals have the insights that they need to personalize experiences. Customer insights help you connect data from transactional, behavioral, and observational sources to create a 360-degree customer view. The customer data platform is designed to deliver insights that you can immediately act on, helping you achieve faster results.

## Create a Dynamics 365 Customer Insights instance

> [!NOTE]
> If you’ve already installed Customer Insights Environment during the **Financial Services training environment preparation -> Deploy and configure prerequisite components -> Install Customer Insights environment** task, then you can skip the following steps and go to the next unit.  

In this task, you'll create a new Customer Insights sandbox environment. To set up **Customer intelligence** correctly, you need to first create a Customer Insights sandbox environment and then connect it to your Microsoft Dataverse environment with no data sources specified. After you're connected, you'll use [Microsoft Cloud Solution Center](https://solutions.microsoft.com/?azure-portal=true) to deploy **Customer intelligence** from **Unified customer profile**, specifying the Customer Insights environment that you will create in this task.

1. Use an In-Private or Incognito window and go to [Microsoft Power Apps](https://make.powerapps.com/?azure-portal=true).

1. Select the correct environment from the **Environment** dropdown menu in the upper-right corner.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Environment dropdown menu in the upper-right corner.](../media/environment.png)](../media/environment.png#lightbox)

1. Open a new tab in your internet browser and then go to [Customer Insights](https://home.ci.ai.dynamics.com/?azure-portal=true).

1. Select **Individual consumers (B-to-C)** as your business.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Choose your business screen, showing options for Individual consumers and Business accounts.](../media/business.png)](../media/business.png#lightbox)

1. Go to the environment picker and select **New**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of Select environment showing the New button.](../media/select-environment.png)](../media/select-environment.png#lightbox)

1. Fill out the following information and then select **Next**:

    1. **Name** - Customer Intelligence

    1. **Choose your business** - Individual consumers (B-to-C)

    1. **Type** - Trial

    1. **Region** - West US

    > [!NOTE]
    > Region selection will defer depending on the region where your instance was created.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Create an environment wizard on the Basic information tab with the information filled in.](../media/basic.png)](../media/basic.png#lightbox)

1. Set the **Save output data to** dropdown menu to **Customer Insights storage**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Create an environment wizard, on the Data storage tab, showing the Save output data option being set to Customer Insights storage.](../media/storage.png)](../media/storage.png#lightbox)

1. Enter the **URL** for your environment, select the **Configure Data sharing with Microsoft Dataverse** checkbox, and then select **Next**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Create an environment wizard, on the Microsoft Dataverse tab, showing the Microsoft Dataverse environment URL being set.](../media/dataverse.png)](../media/dataverse.png#lightbox)

1. Review your selections and then select **Create**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Review tab on the Create an environment wizard showing the Create button.](../media/create.png)](../media/create.png#lightbox)

1. Open a new tab in your internet browser, go to Microsoft Cloud Solution Center, and then select **Microsoft Cloud for Financial Services**. Select **Unified customer profile**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of Microsoft Cloud Solution Center on the Solutions page with Unified customer profile selected.](../media/solution.png)](../media/solution.png#lightbox)

1. In **Unified customer profile**, select the **Add all Unified customer profile** checkbox and then select **Deploy**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of Microsoft Cloud Solution Center on the Solutions page with Unified customer profile set to Add all unified customer profile.](../media/add-all.png)](../media/add-all.png#lightbox)

1. Under **Additional components**, select **Sample data > Next**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of Set up solutions on the Additional components page with Sample data selected.](../media/sample.png)](../media/sample.png#lightbox)

1. Find your Dataverse environment in the first dropdown list, and then select your Customer Insights deployment in the second dropdown list. Name your deployment, agree to the terms of service, and then select **Next**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of Set up solutions on the Set up new deployment page with environments selected, terms of service agreed to, and the Next button highlighted.](../media/deployment.png)](../media/deployment.png#lightbox)

    > [!NOTE]
    > If you’ve already deployed Customer intelligence during the **Training Environment Preparation** lab you will not be able to select the Customer Insights Environment. In this case you can go ahead to the next unit. 

1. Confirm that everything is correct and then select **Deploy**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of Set up solutions on the Configure pre-deployment dependencies page with Solution dependencies installed and set up, showing the Deploy button.](../media/deploy.png)](../media/deploy.png#lightbox)

1. Your deployment will now begin. When it completes, a confirmation message will display.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of Set up solutions on the Deploy solution page with the message We're getting your solution ready.](../media/deploying.png)](../media/deploying.png#lightbox)

    > [!div class="mx-imgBorder"]
    > [![Screenshot of Set up solutions on the Success page with Deployed solutions listed.](../media/success.png)](../media/success.png#lightbox)

**Congratulations!** You've deployed Dynamics 365 Customer Insights.
