An active Azure subscription is required in your Microsoft 365 tenant to light up certain Microsoft Cloud for Retail components. This module will walk through the steps to obtain a free trial Azure subscription and create a resource group that will be used in the subsequent labs.

> [!NOTE]
> The Azure Terms of Use agreement limits free trial activation only for a user that's new to Azure. If you have already had any other type of Azure subscription, you will not be able to activate a free trial.

## Task 1:  Obtain a Trial Azure Subscription

In this task, we'll walk through the steps to obtain a trial Azure subscription.

1. Sign into [Microsoft Azure](https://portal.azure.com/?azure-portal=true) with the new credentials obtained while creating a new tenant in the earlier tasks and then select the **Start** button.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Microsoft Azure welcome screen showing the Start with an Azure free trial option.](../media/azure.png)](../media/azure.png#lightbox)

1. It will open the sign-up page in a new tab page in the browser. The details entered while creating the new tenant in the earlier tasks will be auto populated on the sign-up screen. Verify the profile details, provide the phone number, and validate it either by Text or call, accept the customer agreement and select the **Next** button.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Create your Azure free account screen with profile details.](../media/create-azure.png)](../media/create-azure.png#lightbox)

1. Provide your credit card details and select **Sign up**.

    > [!Note]
    > A credit card is only required to verify your identity. You will not be charged unless you upgrade your subscription. Please read the following Microsoft Docs to understand how to [Avoid charges with your Azure free account](/azure/cost-management-billing/manage/avoid-charges-free-account/?azure-portal=true).
    >
    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Create your Azure free account screen showing Identity verification by card.](../media/card.png)](../media/card.png#lightbox)

**Congratulations!** You have successfully set up your Trial Azure subscription.

## Task 2: Create a resource group

In this task, you'll learn the steps to create a resource group that will be used in the subsequent labs.

> [!NOTE]
> It may take 1-2 hours for the Azure Subscription to appear after creation.

1. In [Azure](https://portal.azure.com/?azure-portal=true), search for **Resource groups**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the search results for resource with Resource groups selected.](../media/resource-groups.png)](../media/resource-groups.png#lightbox)

1. You may also find Resource groups in the upper left flyout menu.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the flyout menu with Resource groups selected.](../media/menu.png)](../media/menu.png#lightbox)

1. Select **Create**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of Microsoft Azure Resource groups showing the Create button.](../media/create.png)](../media/create.png#lightbox)

1. Enter the following values for your new resource group:

    - **Subscription**: Select your Azure subscription.

    - **Resource group**: Enter a new resource group name (for example, Training).

    - **Region**: Select an Azure location.

1. Select **Review + create**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Create a resource group dialog.](../media/create-resource-group.png)](../media/create-resource-group.png#lightbox)

1. Select **Create** once validation has passed.

1. Select **Create**. It takes a few seconds to create a resource group.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Create a resource group dialog showing validation passed.](../media/validation.png)](../media/validation.png#lightbox)

1. Select **Refresh** from the top menu to refresh the resource group list, and then select the newly created resource group to open it. Or select **Notification** (the bell icon) from the top and select **Go to resource group** to open the newly created resource group.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Notifications drop-down showing the go to resource group option.](../media/notifications.png)](../media/notifications.png#lightbox)

**Congratulations!** You've successfully created a Resource Group in your Azure subscription. You'll use this resource group when creating Azure resources, such as the Azure Blob storage.
