You can create a flow that performs one or more tasks (for example, sending a
report by email) on a specific schedule:

-   Once a day, an hour, or a minute

-   On a date that you specify

-   After a number of days, hours, or minutes that you specify

## Create the flow

1.  Launch [Power Automate](https://flow.microsoft.com/) and sign in using your
    organizational account.

2.  In the left pane, select **+ Create**.

3.  Select **Scheduled cloud flow** under **Start from blank**.

4.  In the dialog box, specify the flow's name and how often the flow should
    run.

    For example, if you want the flow to run every two weeks, enter *2* in the
    **Interval** field, and select *Week* in the **Frequency** field. You can
    also specify the day of the week your flow should run. The text at the
    bottom of the dialog box explains your inputs in plain language.

     ![Screenshot of how to specify the recurrence.](../media/build-scheduled-flow.png)

5.  Once you are satisfied with your inputs, select **Create**.

## Specify advanced options

1.  Once your flow is created, select the title of the **Recurrence** card to
    expand it. Select **Edit** and then **Show advanced options**.

> [!NOTE] 
> The advanced options vary, depending on the value of the **Interval** and **Frequency** fields. If the dialog box that you see does not match the graphic that follows, make sure that the **Interval** and **Frequency** fields are set to the same values that are shown in the graphic.

2.  Here you can specify a time zone to reflect the local time zone, Universal
    Coordinated Time (UTC), or another time zone.

3.  Specify the day or days of the week when the flow should run, and the time
    or times of day when the flow should run.

    For example, set up the flow as shown in the following graphic to start it
    no earlier than noon (Pacific time) on Monday, January 1, 2018, and to run
    it every two weeks, at 5:30 PM (Pacific time) on Tuesday.

     ![Screenshot of Advanced options menu items.](../media/recurrence-advanced-options.png)  

## Use the compose action

Use the **Compose** action to save yourself from entering identical data
multiple times when you are designing a flow. For example, if you need to enter
an array of digits: [0,1,2,3,4,5,6,7,8,9] several times while you design your
flow, you could use the compose action to save the array like this:

1.  Under the Recurrence step, select the **+New step** button.

2.  Search for **Compose**, and then select the **Compose** (Data Operation)
    action.

     ![Screenshot of how to search for and select the compose action.](../media/data-operation-compose-action.png)

3.  Enter the array into the **Inputs** box you want to reference later:

     ![Screenshot of how to configure the compose action.](../media/input-array.png)  

     >[!TIP]
     >For easier reference later, rename the **Compose** card by clicking on the text "Compose" on the title bar of the **Compose** card.

4. Continue adding steps to your flow to perform the actions desired. 

5. Rename your flow by selecting "Untitled" at the top left and entering your flow name. 

6.  Next **Save** the flow in the top right corner

     ![Screenshot of the Save button.](../media/save-flow.png)

7.  Select the back arrow in the top left corner next to the name of the flow

     ![Screenshot of the back button.](../media/flow-back-arrow.png)

8.  Finally, you can **Run** the flow from the command bar at the top

     ![Screenshot of the run the flow command.](../media/command-bar-run-flow.png)