In this exercise, you'll integrate Microsoft Clarity with Dynamics 365 E-Commerce. During the setup process, you need to use the live production domain URL associated with your Commerce site. You should have already created a new web page on Dynamics 365 E-Commerce in Lab 1. You'll use that web page.

## Task 1: Create Clarity project for your Dynamics 365 E-Commerce page

1.  Go to [Microsoft Clarity](https://clarity.microsoft.com/?azure-portal=true) and sign in.

2.  Select **My Projects**.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the Clarity homepage with My Projects menu.](../media/my-projects.png)

    This will open the Projects Listing Page shown below.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Porjects Listing Page.](../media/projects-view.png)

3.  Select Add new project.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the add new project window.](../media/new-project.png)

4.  Create a new project for tracking your Dynamics 365 E-Commerce page using your page's direct URL for the Dynamics 365 Commerce page created in Lab 1 > Task 1. (Example: `https://mcriad.commerce.dynamics.com/mcrdemopage`)

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the project website URL.](../media/project-url.png)
	
	Select **Add new project**.

## Task 2: Configure content security policy for Clarity

For Clarity to function on a Dynamics 365 E-Commerce site, some CSP directives must be configured to allow Clarity resources to be called. The configuration steps in Task 2 may already have been performed initially for lab environment setup by your instructor. Follow the steps below to verify that the configuration is complete, if settings aren't present you can use the steps below to configure.

1.  Open the D365 Commerce site builder URL in an in-private window.

2.  Select the active E-commerce project.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the sites list of active e-commerce projects.](../media/active-project.png)

3.  Select **Site Settings > Extensions**.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the site settings selected in the menu.](../media/site-settings.png)

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the extensions selected in the menu.](../media/extensions.png)

4.  Select the **Content security policy tab**, scroll to **child-src,** **connect-src** and **script-src**  directive sections, check if `https://www.clarity.ms` is added in all three sections.

5.  If not select **Add** and enter `https://www.clarity.ms` in all three sections, **child-src,** **connect-src** and **script-src**.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the add button under extensions.](../media/add-extensions.png)

6.  The Extensions should look like below:

	> [!div class="mx-imgBorder"]
	> ![Screenshot of how the extensions should look.](../media/extensions-example.png)

	> [!div class="mx-imgBorder"]
	> ![Screenshot of how the extensions should appear.](../media/extensions-sample.png)

7.  Select **Save and Publish** at the top of the Extensions blade to save your changes.

## Task 3: Embed Clarity tracking script code into your site page

You can embed Clarity tracking script code into any Commerce site page that you want to track with Clarity.

1.  Copy the tracking code from **Microsoft Clarity Settings, Setup, How to install Clarity, Clarity tracking code**.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the setup Clarity tracking code with copy to clipboard button.](../media/copy-code.png)

2.  In the In-Private or Incognito window, navigate to the site builder URL.

3.  Open the Site mentioned by the instructor and select your page created in Lab 1.

	> [!NOTE]
	> Use the page which was created as part of Lab 01(Seamless Customer Service).

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the Pages list with page created selected.](../media/page.png)

4.  For you to be able to add the tracking script on a D365 E-=Commerce page, the **Template** that the **page** is inheriting should support **inline script**. To verify that,

    1.  Select the shown **Template** in **Properties** blade under **Page attributes** of the Page view.

		> [!div class="mx-imgBorder"]
		> ![Screenshot of the template selected in the page attributes of the properties blade.](../media/template.png)

	1.  From the **Template** view, go to **Outline** blade, select **Core Root 1,**expand **HTML** **Head** and check if you have **Inline script.**

		> [!div class="mx-imgBorder"]
		> ![Screenshot of the template view with outline blade expanded and inline script shown for Core root 1 HTML head.](../media/inline-script.png)

	1.  If you don't have **Inline script,** select **Edit**.

	1.  From **Outline**, **Core Root 1,** **HTML** **Head** select **...** and **+Add module**.

		> [!div class="mx-imgBorder"]
		> ![Screenshot of the add module button.](../media/add-module.png)

	1.  From the pop-up window, select **Inline script** and select **OK**.

		> [!div class="mx-imgBorder"]
		> ![Screenshot of the ok button for the inline script.](../media/inline-script-ok.png)

	1.  Now you should see **Inline script** under **HTML Head**. Select **Finish editing** and then **Publish** your changes.

5.  Go back to your Page and select **Edit**. 

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the edit button.](../media/edit.png)

6.  Select **Outline > Settings Icon** and switch to **Advanced outline view**.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the settings outline area with advanced outline view button.](../media/advanced-outline-view.png)

7.  Expand **Core root 1** menu.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the core root 1 menu explanded.](../media/core-root-menu.png)

8.  Expand **HTML Head** menu.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the HTML head menu expanded.](../media/html-head-menu.png)

9.  Select the **Inline Script** under **Core Root 1,** **HTML** **Head** on the advanced view of **Outline** blade. Now you should see the **Inline Script** in **Properties** blade.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the properties blade with inline script displayed.](../media/properties-inline-script.png)

10. Paste the tracking script you copied from **Microsoft Clarity** in the **Inline script** text box. Make sure to remove the surrounding **<script type=\"text/javascript"\> </script\>** tags if you copied the script string. IT will be added by the builder.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the tracking script added to the inline script field.](../media/inline-script-added.png)

11. Select **Finish Editing**.

12. Select **Publish** and publish the page.

**Congratulations!** You've integrated your Dynamics 365 E-Commerce website page with Microsoft Clarity. Now you need to create some traffic on your Dynamics 365 E-Commerce website page like you did with the custom page to be able to observe it Microsoft Clarity.