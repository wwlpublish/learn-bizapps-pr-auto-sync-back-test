<!-- 1. Introduction -------------------------------------------------------------------------------------

    Goal: Describe the end state of the project after this exercise. Ideally, each exercise unit will create a feeling of closure in the learner. That is, they'll have achieved something that demonstrates progress towards the overall goal. For example, if they're building software, maybe the app will run and perform part of the target functionality. This introductory paragraph summarizes what part(s) of the project will be completed in this unit.

    Heading: none

    Example: "The chocolate-manufacturer needs a separate storage account for their private information. Here, you will create an account with settings appropriate to hold this mission-critical business data. You'll validate the account settings against requirements to check your work."
-->
Contoso Pet Boarding needs an app that allows customers to submit booking requests. Here, you will create the table and columns needed to store the booking request information and build a canvas app for customers to use. You'll validate your app against requirements to check your work. 

<!-- 2. Specification-------------------------------------------------------------------------------------

    Goal: Describe the requirements for the part of the project they'll do in this unit. Avoid hints and guidance on how they'll achieve the goal.

    Structure: The specification format is at the author's discretion and will vary based on project type. For example, you could provide any or all of the following:
        - Functional specification for what this part of the project should do when complete.
        - Acceptance criteria (functionality, capacity, resilience, performance, etc.).
        - List of the technologies they should use in this part.
-->

## Specification
Create a Power Apps canvas app called Contoso Booking Requests that meets these specifications:
- Create a custom table for Booking Requests that can store the following information: 
    - Start and End Dates
    - Pet Name
    - Owner’s Name and Email
    - Decision (with the option to choose between Undecided, Accepted, and Declined)
    - Notes
- The customer must provide the Start Date, End Date, Pet Name, Owner Name, and Email to submit a Booking Request.
- New Booking Requests should default to a decision of Undecided until a Contoso Pet Boarding employee reviews it.
- Employees can view all Undecided Booking Requests and update the Decision column to Accepted or Declined.
- Create your app for your new custom table that allows users to create Booking Requests. The following wireframe shows a mockup of your canvas app: 
    ![Mockup of canvas app for submitting booking requests.](../media/canvas-app-mockup.png)
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
To validate that you have completed the work to the requirements, test your app behavior out by following these steps.
1. Run your app. Create a new booking request with the Start Date, Pet Name, Owner Name, and Email populated, leaving the End Date blank. Submit the request to verify that the user cannot submit a request without the End Date populated.
2. Run your app. Create a new booking with the Start Date, End Date, Pet Name, Owner Name, and Email populated. Submit the request to verify that the user can submit a request when all the required information is provided.
3. View the Booking Request that you created. Verify that the Decision column is set to Undecided. Update the column to Accepted.

  > [!TIP]
  > If you get stuck here, reviewing [How to build a canvas app](https://docs.microsoft.com/en-us/learn/modules/build-app-solution/) may help. 
<!-- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -->

<!-- Do not add a unit summary or references/links -->
