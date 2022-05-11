In the previous module, we showed all the licenses needed for the pre-requisite platforms and how to acquire trial licenses for them. In this module, we'll go through the details of how to install the pre-requisite components needed and how to configure them before we can proceed to install the Microsoft Cloud for Financial Services.

## Task 1: Install Dynamics 365 Customer Service environment

In this task, we'll create a Dynamics 365 Customer Service Trial Environment. This is the Dynamics 365 Environment in which the FSI Data model and Applications are installed on. Capabilities such as Banking Customer Engagement use the Dynamics 365 Customer Service.

1.  Navigate to [Dynamics 365 free trial](https://trials.dynamics.com/?azure-portal=true).

1.  Select **Try for free** on Dynamics 365 Customer Service card.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Dynamics 365 Customer Service card with try for free button.](../media/try-free.png)](../media/try-free.png#lightbox)

1.  Enter the user email of the tenant administrator of the newly created Tenant that was created in the previous steps and select Start your free trial.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the start your free trial button.](../media/start-trial.png)](../media/start-trial.png#lightbox)

1.  Fill the relevant information in the following screen and select Submit.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the country/region and phone number fields with submit button.](../media/submit.png)](../media/submit.png#lightbox)

1.  The newly created Customer Service workspace application is launched.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Customer Service workspace application.](../media/customer-service-application.png)](../media/customer-service-application.png#lightbox)

1.  Copy and note the root URL of the launched application. It will be of the format **Error! Hyperlink reference not valid...**. This URL will be referenced at a later step.

1.  Using your tenant administrator credentials, navigate to [https://admin.powerplatform.com](https://admin.powerplatform.com/?azure-portal=true) and select Environments. The newly created Customer Service Environment will be named as **Customer Service Trial**.

1.  Select **Customer Service Trial** to open the Environment details.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the customer service trial.](../media/customer-service-trial.png)](../media/customer-service-trial.png#lightbox)

1.  Select Edit and update the name of the organization to your preferred name and the URL to your preferred URL and select **Save**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the edit details view.](../media/edit-details.png)](../media/edit-details.png#lightbox)

## Task 2: Install Customer Insights environment

In this task, we'll walk through the Customer insights installation process.

1.  Navigate to [Dynamics 365 Customer Insights](https://home.ci.ai.dynamics.com/startB2C/?azure-portal=true). 

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the welcome to Customer Insights message with country/region menu and continue button.](../media/welcome.png)](../media/welcome.png#lightbox)

1.  Select an appropriate country/region and select **Continue**. The Home page is launched as seen below.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Customer Insights home page.](../media/home.png)](../media/home.png#lightbox)

1.  Select **Sign up for trial** at the top right corner of the page.

1.  This launches the Customer Insights trial experience. Enter the same tenant email address that you have been using so far, and select **Next**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Customer Insights trial sign up.](../media/trial.png)](../media/trial.png#lightbox)

1.  Select **Sign in**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the sign in button.](../media/sign-in.png)](../media/sign-in.png#lightbox)

1.  Update the account info and select **Get started**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the account information with get started button.](../media/get-started.png)](../media/get-started.png#lightbox)

1.  Complete the setup by selecting **Get started**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the confirmation details page with get started button.](../media/confirm-details.png)](../media/confirm-details.png#lightbox)

1.  This relaunches the Customer Insights trial screen. Select focus as **Audience Insights**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Customer Insights trial with Audience Insights selected.](../media/audience-insights.png)](../media/audience-insights.png#lightbox)

1.  Choose business as Individual consumers (B-to-C).

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the business set as individual consumers.](../media/individual-consumers.png)](../media/individual-consumers.png#lightbox)

1. Select **+New** to create a new Customer Insights environment.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the +new button to create an environment.](../media/new.png)](../media/new.png#lightbox)

1. Environment Creation Page is displayed. Provide the **Name**, Keep the Business as Individual consumers (B-to-C), Select the **Type** and **Region** as appropriate and select **Next**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the environment creation page with basic information fields.](../media/basic-information.png)](../media/basic-information.png#lightbox)

1. Input the Data Storage options and select **Next**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the data storage output field.](../media/data-storage.png)](../media/data-storage.png#lightbox)

1. Provide the Microsoft Dataverse Environment URL that you copied over in Task 1, step 6. This is important to tie the Customer Insights environment to the correct Dataverse endpoint.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Microsoft Dataverse environment URL field.](../media/dataverse.png)](../media/dataverse.png#lightbox)

1. The review page is shown. Review the selections and select **Create**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the review page with create button.](../media/create-environment.png)](../media/create-environment.png#lightbox)

Upon successful creation of the Customer Insights Tenant, you can proceed forward.

## Task 3: Add Microsoft Cloud for Financial Service trial licenses

In this step, we'll walk through how to obtain the Microsoft Cloud for Financial Services Trial licenses.

1.  To obtain a trial license for Microsoft Cloud for Financial Services, navigate to this [Microsoft Form](https://aka.ms/FSITrial/?azure-portal=true) and fill out the required information.

1.  You'll then receive an email with a URL that contains an offer code that can be used to claim a 30-day trial license for Microsoft Cloud for Financial Services. Once you receive that email, copy the URL, open a new tab while logged into your tenant and paste the URL.

	> [!NOTE]
	> Ensure that there are no trailing hidden spaces when copying the URL.

1.  The following confirmation screen is shown.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the confirmation message with continue button.](../media/confirmation.png)](../media/confirmation.png#lightbox)

1.  It will show the **email address** associated with your tenant, select **Continue**.

1.  Select **Try now** in the Checkout screen.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the try now button.](../media/try-now.png)](../media/try-now.png#lightbox)

1.  Select Continue in the order receipt page.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the continue button in order receipt.](../media/continue.png)](../media/continue.png#lightbox)

## Task 4: Configure Prerequisite configurations

Now that we have necessary licenses and the necessary platform elements created, in this task we'll walk through the pre-requisite configurations that need to be set up before Microsoft Cloud for Financial Services Capabilities can be installed.

### Configure Teams configurations

In this step, we'll walk through the teams configuration settings for Microsoft Teams to integrate with Dynamics 365 platform.

1.  Using your tenant administrator credentials, navigate to [Power Platform admin center](https://admin.powerplatform.com/?azure-portal=true) and select your environment.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the environments list.](../media/environment.png)](../media/environment.png#lightbox)

1.  Select the Environment that was created and open its details page. Select **Settings**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the settings button.](../media/settings.png)](../media/settings.png#lightbox)

1.  The below settings page opens. Select **Integration** and Select **Teams integration settings**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the settings page with integration Teams integration settings selected.](../media/teams-integration-settings.png)](../media/teams-integration-settings.png#lightbox)

1.  Change setting to **Yes** on **Turn on the linking of Dynamics 365 records to Microsoft Teams channels**. Change setting to **Yes** on **Turn on Enhanced Microsoft Teams Integration**. Select **Save**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the setting toggles set to yes with save button.](../media/settings-save.png)](../media/settings-save.png#lightbox)

### Create Power Apps portal

In this task, we'll create a Power Apps Portal that will be used as a sample portal by the Customer onboarding capability.

1.  While signed into your Microsoft 365 tenant, open a new tab and go to [Power Apps](https://make.powerapps.com/?azure-portal=true). 

1.  Change your **Environment** from default to the Trial environment you created in the previous section.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the the trial environment.](../media/change-environment.png)](../media/change-environment.png#lightbox)

1.  In the left nav, select **Apps** and then select **+New App > Portal**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the apps menu with new app button.](../media/new-app.png)](../media/new-app.png#lightbox)

1.  Set the new portal properties as shown below and select **Create**.

    **Name:** Woodgrove Banking Portal

    **Address :** fsitrialdemo

    Select **Use data from existing website record**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the portal details.](../media/portal-details.png)](../media/portal-details.png#lightbox)

    Your portal will provision in the background. Proceed only after the Portal provisioning completes.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the portal provisioning in progress message.](../media/portal-status.png)](../media/portal-status.png#lightbox)
