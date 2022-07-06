With Microsoft Power Automate, you can automate a task, get or send notifications, and track the completion of tasks. The following exercise demonstrates how you can create a notification when an emission factor for Company Cooling has been recorded to have a CO2 calculation as greater than 1,800 lbs.

1. Sign in to [Power Apps portal](https://make.preview.powerapps.com/environments/839eace6-59ab-4243-97ec-a5b8fcc104e4/home/?azure-portal=true).
2. Expand **Data** on the left navigation pane and then select **Connections** to create a connection to Microsoft Dataverse, Microsoft Teams, and Office 365 Outlook. 

    > [!div class="mx-imgBorder"]
    > [![Screenshot of Power apps home showing to select connections.](../media/connections.png)](../media/connections.png#lightbox)

3. Select **+ New connection**.
4. Select the application from the list to make a connection and then select **Create**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot showing to create access to the org-based database on Microsoft Dataverse in current environment.](../media/dataverse.png)](../media/dataverse.png#lightbox)

5.	Sign in with your credentials.
6.	Select **Flows** from the left navigation pane.
 
    > [!div class="mx-imgBorder"]
    > [![Screenshot of Power apps left navigation panel showing flow is selected.](../media/flow.png)](../media/flow.png#lightbox)

7. Select + **New flow**.
8. Select **Automated cloud flow** from the list.

    > [!div class="mx-imgBorder"]
    > [![Screenshot showing how to create new flow and select new flow as Automated cloud flow.](../media/new-flow.png)](../media/new-flow.png#lightbox)

9. Name the flow.
   
    > [!div class="mx-imgBorder"]
    > [![Screenshot showing to enter flow name and choose your flow's trigger.](../media/flow-name.png)](../media/flow-name.png#lightbox)

10.	Select **When a row is added, modified, or deleted for Microsoft Dataverse** and then select **Create**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot highlighting a trigger is selected as when a row is added or modified or deleted.](../media/flow-trigger.png)](../media/flow-trigger.png#lightbox)

11.	Select the following fields:
    - **Change type** - Added
    - **Table name** - Emissions
    - **Scope** - Organization
        
        > [!div class="mx-imgBorder"]
        > [![Screenshot showing selected fields as Added, Emissions and Organisation respectively.](../media/flow-fields.png)](../media/flow-fields.png#lightbox)

12. Select the **+Add** button to add a condition.

    > [!div class="mx-imgBorder"]
    > [![Screenshot showing that you can add flow conditions accordingly.](../media/flow-condition.png)](../media/flow-condition.png#lightbox)

13.	For the **If yes** action condition, select the **Send Office 365 email** action.

    > [!div class="mx-imgBorder"]
    > [![Screenshot showing when a condition is true send an email and showing subjects and body of mail.](../media/condition-true.png)](../media/condition-true.png#lightbox)

14. Save the flow.
