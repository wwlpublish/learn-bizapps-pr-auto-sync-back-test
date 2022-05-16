After you have created your automation process in WinAutomation, you can run it from a flow in Power Automate through desktop flow, either attended or unattended.

1. Create a new Desktop flow.
1. Delete the default first step of **Record app**.

   ![Screenshot of the Record app first step deletion.](..\media\record-first-step-deletion.png)

1. Select **New step**, select **WinAutomation**, and then select the **Run WinAutomation (preview)** action.

   ![Screenshot of the choose an action select WinAutomation.](..\media\choose-action-select.png)

1. In the **Run WinAutomation (preview)** card, fill in the **process path** and any optional **command-line arguments** for the WinAutomation process that you want to run.

    ![Screenshot of the configure WinAutomation action.](..\media\configure-action.png)

> [!NOTE]  
> You must create and store WinAutomation processes locally. The process path is a case-sensitive path in the WinAutomation console for the process, from a base directory of My processes in the Folders Pane. If you have put the process in a subfolder, you will need to include that information in the process path. Don’t put quotes around the process path.

You can use desktop flow inputs and Dynamic content in the target WinAutomation process path and arguments from Power Automate flow.

1. Save and test your Desktop flow to see how it launches the WinAutomation process.
2. Add the Desktop flow into a flow. You can even connect to other Power Automate connectors and triggers.
3. Select attended or unattended as the run type.

In your WinAutomation process, you can use the Get Command-Line Arguments action to retrieve the command-line arguments. The variable %CommandLineArguments% is a List of Text Values. Any value in the list can be referenced with its index. For example If we have a list of three text values [“Alpha”,”Bravo”,”Charlie”], to retrieve the first item in a list, we will reference it like so: %CommandLineArguments[0]%. The second and third items are referenced with the indices [1] and [2], respectively.

![Screenshot of the Get Command Line Arguments action properties.](..\media\command-line-arguments-action-properties.png)

> [!IMPORTANT]  
> Do not pass sensitive text such as passwords through the command-line arguments.

If you’re running desktop flow on an unattended cluster, ensure that WinAutomation is installed on all machines on which the target process is copied. For more information on attended and unattended desktop flow.

You can save and then run the flow and see it launch the WinAutomation process. The Desktop flow will return after the WinAutomation process run completes. You can view the run results from Power Automate. If the process fails, you can see the error messages as well.

> [!TIP]  
> If you get exceptions, you may not have the latest desktop flow installed. Install the latest desktop flow.

If you want WinAutomation to capture a screenshot when a process fails, do the following:

From the WinAutomation console, right-click a process, select **Edit process's properties**. Go to the **Error Handling** tab and choose **Override Default Options**. Select **Add screenshot to logs** and save. Now if a process fails, you can view the screenshot captured at runtime from the Power Automate for desktop flow run details. For more information on process properties, see WinAutomation docs: process Properties.

   ![Screenshot of the WinAutomation process properties error handling tab.](..\media\winautomation-process-properties-error-handling.png)

Currently you have to use certain WinAutomation steps to write results and outputs from the process into a file in the cloud share or email the results out. Then you can use connectors from Power Automate to access and use those results.
