In this exercise, you will learn how to:

- Create a new Power Apps solution.

- Create a new business process flow for tracking loans in the Loan Tracker application.

- Publish the business process flow to the Loan Tracker application.

The business process flow presents the current application stage. This feature allows the loan manager to see the application's current stage in the process. The bank can choose to set as many stages as needed.

When the Loan Tracker application is installed, the business process flow contains four stages:

-   Loan verification

-   Loan processing

-   Underwriting

-   Closure

In this exercise, you will extend the business process flow for loans to include a new **Quality Check** stage.

> [!div class="mx-imgBorder"]
> [![Screenshot of the Loan verification step in the loan application process.](../media/loan-verification.png)](../media/loan-verification.png#lightbox)

## Task 1: Create a new Power Apps solution

To create a new Power Apps solution, follow these steps:

1.  Use an In-Private or Incognito window and go to [Power Apps](https://make.powerapps.com/?azure-portal=true).

1.  Select the correct environment from the **Environment** dropdown menu in the upper-right corner.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Environment menu in Power Apps.](../media/environment-menu.png)](../media/environment-menu.png#lightbox)

1.  Select **Solutions** on the left navigation bar.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the navigation menu with Solutions selected.](../media/solutions.png)](../media/solutions.png#lightbox)

1.  Select **+ New solution**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the New solution button.](../media/new-solution.png)](../media/new-solution.png#lightbox)

1.  Name the new solution **Woodgrove Banking**, select **CDS Default Publisher**, and then select **Create**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the New solution details, showing the Create button.](../media/solution-details.png)](../media/solution-details.png#lightbox)

## Task 2: Extend the loan application business process flow

To extend the loan application business process flow, follow these steps:

1.  Select **Woodgrove Banking** to open the solution.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of Woodgrove Banking selected in the Solutions list.](../media/woodgrove-banking.png)](../media/woodgrove-banking.png#lightbox)

1.  Select **+ Add existing** and then select **Automation** and **Process**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Add existing menu with Process selected.](../media/add-process.png)](../media/add-process.png#lightbox)

1.  In the search box, enter **BPF**, select **Loan application BPF**, and then select **Add**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of Loan application BPF selected, showing the Add button.](../media/loan-application.png)](../media/loan-application.png#lightbox)

1.  Open **Loan application BPF**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of Loan application BPF being selected.](../media/loan-application-business-process-flow.png)](../media/loan-application-business-process-flow.png#lightbox)

1.  Deactivate the business process flow.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of Loan application BPF in Power Apps, with the Deactivate button.](../media/deactivate.png)](../media/deactivate.png#lightbox)

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Process Deactivate Confirmation message with the Deactivate button selected.](../media/deactivate-confirmation.png)](../media/deactivate-confirmation.png#lightbox)

1.  Extend the business process flow by selecting and dragging a stage in between the **Underwriting** and **Closure** stages.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the steps to extend the business process flow.](../media/extend.png)](../media/extend.png#lightbox)

1.  Select the **New stage**, give it a **Display Name** of **Quality Check**, and then select **Apply**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the new stage named Quality Check and the Apply button selected.](../media/quality-check.png)](../media/quality-check.png#lightbox)

1.  Expand **Steps** under the new stage and then select **Data Step #1**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of Data Step 1 selected.](../media/data-step.png)](../media/data-step.png#lightbox)

1.  Enter the following information and then select **Apply**:

	- **Step Name** - Confirmed By
	
	- **Data Field** - Text placeholder
	
	- **Required** - Yes

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Data Step details.](../media/data-step-details.png)](../media/data-step-details.png#lightbox)

1. Select **Save** to save your changes.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Save button to save changes.](../media/save.png)](../media/save.png#lightbox)

1. Select **Activate** to activate the business process flow.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Activate button to activate the business process flow.](../media/activate.png)](../media/activate.png#lightbox)

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Process Activate Confirmation window.](../media/activate-confirmation.png)](../media/activate-confirmation.png#lightbox)

**Congratulations**, you have extended the Loan application business process flow by adding another stage for loan applications in Microsoft Cloud for Financial Services.
