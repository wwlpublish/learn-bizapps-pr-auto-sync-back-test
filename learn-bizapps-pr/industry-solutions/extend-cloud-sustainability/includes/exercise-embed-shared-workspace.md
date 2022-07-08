You can add a shared workspace for a custom Power BI report to Microsoft Cloud for Sustainability for easier access within the application.

> [!Note]
> This exercise assumes that a Power BI report already exists in a shared workspace in Power BI in the same Office 365 tenant. Also, it assumes that the Power BI report has at least one report and one dashboard. 

1. Sign in to [Power Apps](https://make.powerapps.com/?azure-portal=true) **> Solutions > New solution** to create a solution. In the given example, the name of the solution is **Demo solution**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of power apps portal showing demo solution create as a new solution under solutions option.](../media/demo-solutions.png)](../media/demo-solutions.png#lightbox)

2. Open **Demo solution** and then go to **New > Dashboard > Power BI embedded**.
    
    > [!div class="mx-imgBorder"]
    > [![Screenshot of Demo solution's object showing how to create Power BI embedded in new dashboard.](../media/demo-solutions-object.png)](../media/demo-solutions-object.png#lightbox)

3. In the right pane, complete the following actions:
    - Enter a name in the **Display name** field.
    - In the **Type** section, choose **Power BI report** or **Power BI dashboard**.
    - In the **Power BI workspace** dropdown menu, select the existing shared workspace.
    - In the **Power BI report** dropdown menu, select the existing Power BI report. 
    - Select **Save**.
        > [!div class="mx-imgBorder"]
        > [![Screenshot representing New Power BI embedded dashboard.](../media/embedded-dashboard.png)](../media/embedded-dashboard.png#lightbox)

4. In the same solution, go to **Add existing > App > Model-driven app**. 

    > [!div class="mx-imgBorder"]
    > [![Screenshot showing demo solution's object how to create Model-driven app.](../media/model-driven.png)](../media/model-driven.png#lightbox)

5. Select the **Cloud for Sustainability Preview** app. Select the ellipsis (...) next to **Cloud for Sustainability Preview > Edit > Edit in preview**.
6. In the left pane, go to the **Navigation** section and expand **Overview**. 
7.	Select **Overview > Add > Subarea**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot showing how to add subarea under navigation section.](../media/subarea-dashboard.png)](../media/subarea-dashboard.png#lightbox)

8.	In the **New subarea form**, select **Content type** as **Dashboard**.
9.	Select **Demo Power BI report** for the **Dashboard** field.
10.	Provide a title for the dashboard and then select **Add**. 
11.	**Save** and **Publish** the model-driven app.
