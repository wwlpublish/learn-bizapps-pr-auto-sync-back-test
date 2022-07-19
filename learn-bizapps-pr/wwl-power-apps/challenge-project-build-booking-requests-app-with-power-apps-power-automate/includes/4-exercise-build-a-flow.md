<!-- 1. Introduction -------------------------------------------------------------------------------------

    Goal: Describe the end state of the project after this exercise. Ideally, each exercise unit will create a feeling of closure in the learner. That is, they'll have achieved something that demonstrates progress towards the overall goal. For example, if they're building software, maybe the app will run and perform part of the target functionality. This introductory paragraph summarizes what part(s) of the project will be completed in this unit.

    Heading: none

    Example: "The chocolate-manufacturer needs a separate storage account for their private information. Here, you will create an account with settings appropriate to hold this mission-critical business data. You'll validate the account settings against requirements to check your work."
-->
Pet Paradise customers need to receive a confirmation email after submitting booking requests in the app. They also need to receive an email when the Pet Paradise staff has made a decision to accept or decline the booking request. Here, you will create at least two Power Automate flosw (you may choose to design this with one flow) that sends an email each time a booking request is submitted and each time the booking request decision column has been updated. You'll validate the flow behavior against requirements to check your work.

<!-- 2. Specification-------------------------------------------------------------------------------------

    Goal: Describe the requirements for the part of the project they'll do in this unit. Avoid hints and guidance on how they'll achieve the goal.

    Structure: The specification format is at the author's discretion and will vary based on project type. For example, you could provide any or all of the following:
        - Functional specification for what this part of the project should do when complete.
        - Acceptance criteria (functionality, capacity, resilience, performance, etc.).
        - List of the technologies they should use in this part.
-->

## Specification
You need to build some automation for your app that meets the following specifications:
- When a customer submits a Booking Request, an email is sent to them confirming that the request was received.
- When a decision has been made on a Booking Request, the customer receives an email to update them on the decision.

You may choose to design this as to Power Automate flows or just one. There is no right answer, as long as you have the expected behavior based on the specifications provided. Think through your decision on number of flows for this design. 

<!-- 3. Validation -------------------------------------------------------------------------------------------

    Goal: Enables the learner to evaluate if they completed the exercise correctly. This feedback is critical for learning.

    Structure:
        1. H2 of "Check your work".
        2. An introductory paragraph describing how they'll validate their work at a high level.
        3. Numbered steps (if the learner needs to perform multiple steps to verify if they were successful).
        4. Video of an expert performing the exact steps of the exercise (optional).

    Example:
         "At this point, the app is scanning Twitter every minute for tweets containing the search text. To verify the app is running and working correctly, we'll look at the Runs history table."
             "1. Select Overview in the navigation menu.
              2. Select Refresh once a minute until you see a row in the Runs history table.
              ...
              6. Examine the data in the OUTPUTS section. For example, locate the text of the matching tweet."
Optional "exercise-solution" video
-->

## Check your work
To validate that you have completed the work to the requirements, test your flow behavior out by following these steps.
1. In your canvas app, create a new Booking Request with your email address provided as the Owner Email. Confirm that you receive an email once the Booking Request is created.
2. On the same Booking Request row, update the Decision field to Declined. Confirm that you receive an email that the Booking Request was declined.
3. On the same Booking Request row, update the Decision field to Accepted. Confirm that you receive another email that the Booking Request was accepted.

<!-- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -->

<!-- Do not add a unit summary or references/links -->
