In [Power Apps](https://make.powerapps.com/?azure-portal=true), you can use a sample app to explore design possibilities. You'll also discover concepts that you can apply as you develop your own apps. Every sample app uses fictitious data to showcase a real-world scenario.

For more details, be sure to check out the documentation that's specific to each sample app.

![Screenshot of Fundraiser sample app in Power Apps.](../media/updated-fundraiser-app1.png)

## Get sample apps

Before you can experiment with or edit the model-driven sample apps, you must set them up in a Microsoft Dataverse database. If you have not already created a trial enviroment, follow the steps in the [Create a trial (standard) environment in the Power Platform admin center](/power-platform/admin/trial-environments/?azure-portal=true) learning module. Make sure that you select the **Deploy sample apps and data** toggle. If you do not have the correct permissions to create a trial environment, consider setting up a trial tenant. For more information on doing so, see [Sign up for the Power Apps Developer Plan](/power-apps/maker/developer-plan).

![Deploy sample apps and data toggle screenshot.](../media/deploy-sample-apps.png)

In Power Apps, select the environment you want, or go to the [Microsoft Power Platform admin center](https://admin.powerplatform.microsoft.com/?azure-portal=true) to create a new one. Select **New**, provide a name, **Yes** to Create a database for this environment, and select **Save**.

> [!IMPORTANT]
> By selecting the **Deploy sample apps and data** toggle, you will install all available sample apps in your database. Sample apps are for educational and demonstration purposes. We don't recommend installing them in production databases.

## Run a sample app

To run a sample app, follow these steps:

1. Sign in to [Power Apps](https://make.powerapps.com/?azure-portal=true) to see a list of available sample apps. For this example, select **Fundraiser**.

	![Screenshot of the Power Apps list of available sample apps with Fundraiser selected.](../media/updated-fundraiser-app2.png)

1. At the top of the page, select **Show Visual Filter** to show graphs and charts where you can see how donations to fundraisers are performing. In the next steps, you'll create a new fundraiser and submit a donation to that fundraiser.
1. On the left pane, under **Fundraiser**, select **Fundraisers**.
1. Select **+ New** to add a new fundraiser.
1. Under the **General** tab, enter the following information:

   **Name** - My Fundraiser

1. In the upper-right corner, select the drop-down arrow next to **Total Donations**.
1. From the drop-down menu, enter the following information:

   **Fundraiser Goal** - 500
   
1. On your keyboard, press **Enter**.
1. Select **Save & Close**.
1. On the left pane, under **Fundraiser**, select **Donations**.
1. Select the drop-down arrow to the right of **Other Activities**.
1. From the drop-down menu, select **Donation**.
1. Enter the following information:
	- **Subject** - My First Donation
	- **Donation Amount** - 100
	- **From** - Nancy Anderson (sample)
	- **Regarding** - My fundraiser
1. Select **Save & Close**.
1. On the left, select **Dashboards**.
1. Select **Show Visual Filter**.
1. Notice **Total Donations vs Goal by Fundraiser** shows your donation.

You have successfully run a sample model-driven app, added a new fundraiser, and added a donation to the fundraiser. While this is a quick look at an app and the related pieces, there is much more to learn about creating an app.
