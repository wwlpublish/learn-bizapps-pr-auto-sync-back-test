In this exercise, you'll learn about several configurations that are required to successfully deploy and use Microsoft Cloud for Healthcare. You can make all major configuration changes by using the following four tools:

-   Microsoft Azure portal

-   Microsoft Power Platform admin center

-   Microsoft Power Apps portals

-   Microsoft Cloud Solution Center

> [!NOTE]
> Setting up Omnichannel for Customer Service and Power Apps portals will take several hours to complete (estimated at 3-4 hours to complete for each). We recommend that you set up both applications concurrently. You'll need to complete all configuration steps before deploying **Microsoft Cloud for Healthcare.**

## Task 1: Register an app in Azure AD

In this task, you'll learn how to register a new application in Microsoft Azure Active Directory (Azure AD), grant delegated and
application permissions, and create a client secret.

1.  While signed in to your **Microsoft 365 tenant**, open a new browser tab, and then go to the [Azure portal](https://portal.azure.com). In the upper-left corner of the page, select the hamburger icon (three horizontal lines) and then select **Azure Active Directory**.

![](media/image1.png){width="6.83in" height="3.75in"}

2.  On the left navigation, select **App registrations** and then select **+ New registration** in the right pane.

![](media/image2.png){width="6.83in" height="3.42in"}

3.  On the **Register an application** page, enter the name for the bot and then select the **Accounts in any organizational directory (Any Azure AD directory - Multitenant)** option button under the **Supported account types** section. Then, select **Register**.

![](media/image3.png){width="6.83in" height="3.56in"}

> [!NOTE]
>  You'll need to register the application as multitenant because it enables Microsoft Azure Bot Service (in the botframework.com tenant) to authenticate requests that are coming from the bot that's registered in your tenant. This requirement is part of the service-to-service authentication protocol that's used by Azure Bot Service. Single tenant application registration is also supported by Azure bot created using Bot Framework version 4.15 or later. However, for this learning path,
you'll register the application as multitenant.*

4.  Select **API permissions** on the left navigation. On the right pane, select **+ Add a permission**.

![](media/image4.png){width="6.83in" height="3.18in"}

5.  On the **Request API permissions** page, select **APIs my organization** **uses**. Use the search box to search for the string
    **Dataverse**. From the search result, select **Dataverse**.

![](media/image5.png){width="6.83in" height="2.48in"}

6.  Select **Delegated permissions**. Under the **Select permissions** section, select the checkbox beside  **user_impersonation**. Then, select **Add permissions**.

![](media/image6.png){width="6.83in" height="6.08in"}

7.  Select **API permissions** on the left navigation. On the right pane, select **+ Add a permission**. Select **Microsoft APIs** and then select **Microsoft Graph**.

![](media/image7.png){width="6.83in" height="6.19in"}

8.  On the **Request API permissions** page, select **Application permissions**. Use the search box to search for the string
    **calendars**. Select the checkbox beside **Calendars.ReadWrite** and then select **Add permissions**.

![](media/image8.png){width="6.83in" height="6.19in"}

9.  Select **Grant admin consent**, as shown in the following image.

![Graphical user interface, text, application, email Description automatically generated](media/image9.png){width="6.83in"
height="3.18in"}

10. On the **Grant admin consent confirmation** pop-up window, select **Yes**.

![](media/image10.png){width="6.83in" height="0.84in"}

The status for each added permission will change to **Granted**, as shown in the following screenshot.

![](media/image11.png){width="6.83in" height="3.18in"}

11. On the left navigation, select **Certificates & secrets**, and then in the right pane, select **+ New client secret**. On the **Add a client secret** blade, provide the **Description**, leave the **Expires** value at its default setting, and then select **Add**.

![](media/image12.png){width="6.83in" height="3.67in"}

> [!NOTE]
> Next, you'll need to create an application secret so that you can use it along with this application ID to authenticate the bot.

12. Copy the secret value and then save it in a notepad so that you can use it later in this learning path.

![](media/image13.png){width="6.83in" height="3.2in"}

> [!NOTE]
> After you've created the secret and the page has refreshed, the secret value will no longer be available to copy.*

13. On the left navigation, select **Overview**. From the right pane, copy the **Application (client) ID** and then save it in a notepad so that you can use it later in this learning path.

![](media/image14.png){width="6.83in" height="1.78in"}

## Task 2: Create a subscription-based, trial Dataverse environment

In this task, you'll create a subscription-based, trial Dataverse environment with a database.

1.  While signed in to your Microsoft 365 tenant, open a new tab, and then go to [Power Platform admin
    center](https://admin.powerplatform.microsoft.com/).

2.  On the left navigation, select **Environments**. In the right pane, select **+ New**.

![](media/image15.png){width="6.83in" height="2.94in"}

3.  On the **New environment** form, provide the following details and then select **Next**.

- **Name** - Lamna Healthcare

- **Region** - United States

- **Type** - Trial (subscription-based)

![](media/image16.png){width="3.5083333333333333in"
height="8.066666666666666in"}

4.  On the **Add database** form, select **Click** **here**, provide details as shown in the following screenshot, and then select
    **Save**.

- **URL** - lamnahealthcare

- **Enable Dynamics 365 apps?** - Yes

- **Automatically deploy these apps** - None

![](media/image17.png){width="2.8333333333333335in"
height="7.216666666666667in"}![](media/image18.png){width="2.67in"
height="7.2in"}

After the environment has been created successfully, it should appear as shown in the following image.

![](media/image19.png){width="6.83in" height="2.17in"}

## Task 3: Enable the Dynamics 365 Field Service app in the Dataverse environment

In this task, you'll install the **Dynamics 365 Field Service** app in the **Lamna Healthcare** environment.

1.  While signed in to your Microsoft 365 tenant, open a new tab and then go to [Power Platform admin
    center](https://admin.powerplatform.microsoft.com/).

2.  On the left navigation, select **Resources** **\>** **Dynamics 365 apps**.

3.  In the upper-right corner of the page, use the search box to search for the string **Field**.

4.  In the right pane, select **Dynamics 365 for Field Service** and then select **Install**, as shown in the following screenshot.

![](media/image20.png){width="6.83in" height="2.72in"}

5.  Select **Lamna Healthcare** as the environment to install the app. Select the **I agree to the terms of service** checkbox and then select **Install**.

![](media/image21.png){width="6.666666666666667in"
height="8.091666666666667in"}

## Task 4: Enable the Dynamics 365 Sales app in the Dataverse environment

In this task, you'll install the **Dynamics 365 Sales app** in the **Lamna Healthcare** environment.

1.  While signed in to your Microsoft 365 tenant, open a new tab and then go to [Power Platform admin
    center](https://admin.powerplatform.microsoft.com/).

2.  On the left navigation, select **Resources** **\>** **Dynamics 365 apps**.

3.  In the upper-right corner of the page, use the search box to search for the string **Sales**.

4.  In the right pane, select **Dynamics 365 Sales, Enterprise Edition App** and then select **Install**, as shown in the following image.

![](media/image22.png){width="6.83in" height="2.75in"}

5.  Select **Lamna Healthcare** as the environment to install the app. Select the **I agree to the terms of service** checkbox and then select **Install**.

![](media/image23.png){width="6.691666666666666in"
height="8.066666666666666in"}

### Task 5: Enable the Dynamics 365 Marketing app in the Dataverse environment

In this task, you'll go through the steps that are involved in setting up the Dynamics 365 Marketing app in the Lamna Healthcare environment.

1.  While signed in to your Microsoft 365 tenant, open a new tab and then go to [Power Platform admin
    center](https://admin.powerplatform.microsoft.com/).

2.  On the left navigation, select **Resources** **\>** **Dynamics 365 apps**.

3.  In the upper-right corner of the page, use the search box to search
    for the string **Marketing**.

4.  In the right pane, select **Dynamics 365 Marketing Application** and then select **Manage**, as shown in the following screenshot.

![](media/image24.png){width="6.83in" height="2.76in"}

5.  Select **Install**.

![](media/image25.png){width="6.83in" height="1.95in"}

When installation begins, the setup will show as in progress.

![](media/image26.png){width="6.83in" height="1.76in"}

6.  When setup is finished, select **Take me to the app**.

![](media/image27.png){width="6.83in" height="1.48in"}

You'll be redirected to the Dynamics 365 Marketing app that's been set up in the Lamna Healthcare environment.

![](media/image28.png){width="6.83in" height="3.75in"}

## Task 6: Enable the Omnichannel for Customer Service app in the Dataverse environment

In this task, you'll go through the steps that are involved in setting up the **Omnichannel for Customer Service** app in the **Lamna Healthcare** environment. In this learning path, you'll enable chat and **Microsoft Teams** channels only.

1.  While signed in to your Microsoft 365 tenant, open a new tab and then go to [Power Platform admin
    center](https://admin.powerplatform.microsoft.com/).

2.  On the left navigation, select **Resources** **\>** **Dynamics 365 apps**.

3.  In the upper-right corner of the page, use the search box to search for the string **omni**.

4.  In the right pane, select **Omnichannel for Customer Service** and then select **Manage**, as shown in the following screenshot.

![](media/image29.png){width="6.83in" height="2.75in"}

5.  On the **Permissions requested** pop-up window, select **Accept**.

![](media/image30.png){width="4.475in" height="9.133333333333333in"}

6.  You'll be redirected to Dynamics 365 Administration Center. Select **+ Add environment**.

![](media/image31.png){width="6.83in" height="0.97in"}

7.  On the **Omnichannel set up** screen, select **Lamna Healthcare** as the environment and then select **Next**.

![](media/image32.png){width="6.83in" height="2.46in"}

8.  Set the **Add chat** toggle to **Yes** and then select **Next**.

![](media/image33.png){width="6.83in" height="2.05in"}

9.  Leave the **SMS** and **Social** settings to their default and then select **Next**.

10. Enable the Microsoft Teams channel and then select **Next**.

11. On the **Confirm your selections** screen, select **Finish**.

![](media/image34.png){width="6.83in" height="3.39in"}

The next screen will show that Omnichannel is being set up.

![](media/image35.png){width="6.83in" height="2.62in"}

> [!NOTE]
> It might take a few hours to complete the setup of Omnichannel.

After Omnichannel setup has finished successfully, the **Summary** screen will appear, as shown in the following screenshot.

![](media/image36.png){width="6.83in" height="4.13in"}

## Task 7: Create the Lamna Healthcare Patient Portal app

In this task, you'll create a **Microsoft Power Apps** portal in the **Lamna Healthcare** environment. This portal app becomes the patient access portal that will be used by **Microsoft Cloud for Healthcare.**

1.  While signed in to your Microsoft 365 tenant, open a new tab and then go to [Power Apps portal](https://make.powerapps.com/).

2.  Select **Environment** as Lamna Healthcare.

3.  In the right pane, select **More create options**, as shown in the following image.

![](media/image37.png){width="6.83in" height="2.46in"}

4.  Use the search box to search for the string **Customer**. Select the **Customer self-service** template.

![](media/image38.png){width="6.83in" height="3.56in"}

5.  On the **Customer self-service** creation page, provide the following information and then select **Create**.

- **Name** - Lamna Healthcare Patient Portal

- **Address** - You can select a desired address for your patient portal (subject to its availability). The portal address is globally unique.

![](media/image39.png){width="6.83in" height="4.41in"}

A pop-up window will appear, indicating that the portal provisioning is in progress.

![](media/image40.png){width="3.933333333333333in"
height="1.2083333333333333in"}

*Note: It might take a few hours for the Customer self-service portal to
complete provisioning.*

6.  After the portal has successfully provisioned, you can review it on the **Apps** page.

![](media/image41.png){width="6.83in" height="1.44in"}

## Task 8: Deploy Microsoft Cloud for Healthcare solutions

In this task, you'll go through the steps to deploy the necessary Microsoft Cloud for Healthcare solutions to complete this training course.

You'll need to complete all previous steps before you can deploy Microsoft Cloud for Healthcare solutions.

1.  While signed in to your Microsoft 365 tenant, open a new tab and go to [Microsoft Solution Center](https://solutions.microsoft.com).

2.  On the left navigation, select **Solutions** **\>** **Healthcare** to view all solution modules that are available in Microsoft Cloud for Healthcare.

3.  Select any solution card. For this learning path, you'll select the **Personalized care** solution card.

![](media/image42.png){width="6.83in" height="3.56in"}

4.  Select **All** from the **Filter by capability** dropdown menu. Select the **Add all Microsoft Cloud for Healthcare** checkbox to add all capabilities. For this learning path, you'll clear the **Health assistant** feature, as shown in the following screenshot. Then, select **Deploy**.

![](media/image43.png){width="6.83in" height="11.57in"}

5.  On the **Set up solutions** page, select the **Name**, **Sample data**, and **Codeable concepts** options to add them as extra
    components and then select **Next**.

![](media/image44.png){width="6.83in" height="3.57in"}

6.  On the **Set up new deployment** screen, from the **Enter Dataverse environment** dropdown menu, select the **Lamna Healthcare** environment that you created in the previous task. In the **Name your deployment** box, enter a name for the deployment. Select the **Terms of service** checkbox and then select **Next**.

![](media/image45.png){width="6.83in" height="3.67in"}

7.  The **Configure pre-deployment dependencies** page will display a list of all dependencies, and their statuses will be marked green to confirm that you can proceed with deployment. Select **Deploy**.

![](media/image46.png){width="6.83in" height="3.62in"}

The **Deploy solution** page will show the progress of the Microsoft Cloud for Healthcare solutions deployment. Because the deployment process can take several hours to complete, you can close this page or keep it open to track the deployment.

![](media/image47.png){width="6.83in" height="9.75in"}

8.  The **Success** page will appear when the deployment of Microsoft Cloud for Healthcare solutions has completed successfully. Select the **Launch solution** option beside any listed solution to open it.

![](media/image48.png){width="6.83in" height="12.14in"}

## Task 9: Update environment variables in Power Apps portal

In this task, you'll go through the steps to update the environment variables that are used by the virtual visit feature in Microsoft Cloud for Healthcare.

1.  While signed in to your Microsoft 365 tenant, open a new tab and go
    to [Power Apps portal](https://make.powerapps.com/).

2.  In the upper-right corner of the page, select **Lamna Healthcare** as your working environment.

3.  On the left navigation, select **Apps**. In the right pane, select the **See environment variables** option, as shown in the following image.

![](media/image49.png){width="6.83in" height="3.56in"}

4.  On the **Environment variables** form, populate the **Virtual Visit Secret** and **Virtual Visit Client ID** boxes with the client secret and client ID that you've copied in Task 1 of this exercise.

![](media/image50.png){width="5.358333333333333in" height="15.225in"}

**Congratulations!**, you've successfully set up the **Lamna Healthcare Dataverse** environment and have deployed **Microsoft Cloud for Healthcare** solutions.




