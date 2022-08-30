In this exercise, you'll create a flow that calculates the last day of the current month using JavaScript code.

1. Launch the Power Automate for desktop console and create a new flow named **Last day of the month**.

    ![Screenshot of the Power Automate for desktop Build a flow dialog.](..\media\second-exercise-new-flow.png)

1. Under **Actions**, search for **get current**. Then click on **Get current date and time**.

    ![Screenshot of the Power Automate for desktop Get current date and time action.](..\media\first-exercise-get-current-time.png)

1. Use a **Get current date and time** action to store the current date in a datetime variable.

    ![Screenshot of the Power Automate for desktop Get current date and time parameters.](..\media\second-exercise-get-current-date-and-time-action.png)

1. Our next actions include variables. For those, expand **Variables** and double-click on **Set variable**.

    ![Screenshot of the Power Automate for desktop Set variable action.](..\media\run-javascript-set-variables.png)

    Double-click on the default **NewVar** and change it to **Month**. 

    ![Screenshot of the Power Automate for desktop Set new variable action.](..\media\set-new-variables.png)

    Next, click on **{x}** and under **Flow variables**, **CurrentDateTime** select **.Month**. Click on **Select**.

    ![Screenshot of the Power Automate for desktop Set variable action with variable NewVar.](..\media\run-javascript-set-month-variable.png)

    Follow the same steps to add the **Year** variable as well.

    ![Screenshot of the Power Automate for desktop Set year variable action.](..\media\run-javascript-set-year-variable.png)

    ![Screenshot of the Power Automate for desktop Set variable action.](..\media\second-exercise-set-variable-actions.png)

1. Search for **run java** under **Actions** and double-click on **Run JavaScript**.

    ![Screenshot of the Power Automate for desktop Run JavaScript action.](..\media\run-javascript.png)

    In the **JavaScript to run**, type in **var month =**, then click on **{x}**, select **%Month%** and then click on the **Select** button. Then add **;**.

    ![Screenshot of the Power Automate for desktop Run JavaScript add month action.](..\media\run-javascript-add-month.png)

    ![Screenshot of the Power Automate for desktop Run JavaScript action with parameter set to month.](..\media\month-parameter.png)

    In a new line type in **var d = new Date(** then click on **{x}**, select **%Year%** and then click on the **Select** button. Then add **, month,0);**.

    In a new line type in **WScript.Edcho(d);**.

    ![Screenshot of the Power Automate for desktop Run JavaScript action parameters.](..\media\second-exercise-run-javascript-action.png)

1. Search for the **Parse text** action in the workspace and use the presented regular expression to remove the date's unnecessary parts.

    ![Screenshot of the Power Automate for desktop Parse text action.](..\media\second-exercise-parse-text-action.png)

1. Use a **Convert text to datetime** action to convert the parsed text into a datetime variable.

    ![Screenshot of the Power Automate for desktop Convert text to datetime action.](..\media\second-exercise-convert-text-to-datetime-action.png)

1. Reconvert the datetime value to text using the **Convert datetime to text** action. We are deploying this action to create a custom format of the date.

    ![Screenshot of the Power Automate for desktop Convert datetime to text action.](..\media\second-exercise-convert-datetime-totext-action.png)

1. To display the final text variable that contains the last day of the month, use a **Display message** action.

    ![Screenshot of the Power Automate for desktop Display message action.](..\media\second-exercise-display-message-action.png)

1. Save the flow and then execute it. You can try different time zones to ensure that the flow can handle all possible scenarios.

    ![Screenshot of the Power Automate for desktop final flow and the save and run buttons.](..\media\second-exercise-final-flow.png)