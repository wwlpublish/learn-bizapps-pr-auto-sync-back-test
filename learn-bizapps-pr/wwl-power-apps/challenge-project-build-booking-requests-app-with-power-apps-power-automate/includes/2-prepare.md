<!-- 1. Topic sentence(s) --------------------------------------------------------------------------------

    Goal: briefly summarize the project and setup requirements in 1-3 sentences.

    Heading: none

    Pattern: "You'll be <doing> a <thing> that <goal>. Here, we'll discuss the project <big picture>. We'll also cover the <things> you'll need."

    Example: "You'll be <building> a <Logic App> that <determines the sentiment of new tweets and reacts accordingly>. Here, we'll discuss the project <business logic and target behavior>. We'll also cover the <accounts and software> you'll need."
-->
You'll be creating custom tables and columns to build a canvas app along with some notification flows. Here, we'll discuss the things you'll need to get started.

<!-- 2. Project specification -----------------------------------------------------------------------------

    Goal: Describe the success criteria for the entire project. Avoid hints and guidance on how they'll achieve the goal.

    Heading: "Project specification"

    Structure: The specification format is at the author's discretion and will vary based on project type. For example, you could provide any or all of the following:
        - Functional specification for what this part of the project should do when complete.
        - Acceptance criteria (functionality, capacity, resilience, performance, etc.).
        - List of the technologies they should use.
-->
## Project specification
Contoso Pet Boarding is a local pet boarding facility and veterinary care practice. Lately, customers have requested a way to submit booking requests for pet boarding without having to call the office. You would like to create an app that allows customers to submit the information for their booking request for the office to review. You would like customers to be alerted when their booking request has been recieved and approved or rejected. You want to build an app that allows you to capture these booking requests and decide to accept or decline the booking. 

Bookings previously could only be requested over the phone, causing the Contoso phone line to always be busy. Despite their importance, many customers couldn't get through to the office to request their services. Long wait times could mean customers get frustrated and hang up. This can result in loss of business for Contoso.

A well-built app with some simple automation provides customers with the ability to submit their booking request information on their own time, reducing the time waiting on the phone. Happy customers are likely to share their experience with others and increase business for Contoso Pet Boarding.


<!-- 3. Setup -------------------------------------------------------------------------------------

    Goal: Guide the learner though any needed setup such as required accounts or local software installations.

    Structure:
        1. H2 of "Setup"
        2. 1 paragraph of text giving a conceptual overview of the needed setup
        3. One H3 per setup item explaining the need and giving instructions.
            - Use "Create <service> account" as the H3 for account creation.
            - Use "Install <product>" as the H3 for software installation.
            - For setup items beyond accounts and software, use an H3 that follows the "<verb> <item>" pattern.

    Example:
        "To complete the project, you'll need a Twitter account, an Azure account, and a local installation of Visual Studio Code.

        ### Create Twitter account
            Your Logic App needs to pull new tweets from Twitter using the Twitter connector. Under the hood, the Twitter connector uses the Twitter API. The Twitter API requires authentication via a username and password, which means that you'll need a Twitter account.
            1. Go to <link> and create an account.
            1. Record your username and password, you'll need it later.

        ...

        ### Install Visual Studio Code
            You'll use Visual Studio Code to create your Logic App. All your work will be done directly in VS Code: connecting to your Azure account, selecting your Azure subscription, and building your app. This section guides you through the installation and setup of VS Code on your local machine.
            1. Go to <link> and follow the installation steps for your platform.
            1. Go to <link> and follow the steps to connect to your Azure account from VS Code.
            1. Go to <link> and follow the steps to select your Azure subscription."

    Note: The "Setup" section is optional. If the project doesn't require any setup, omit this entire section.
    In that case, also remove the "Project specification" H2 (while leaving the content of that H2) to avoid a page
    containing a single H2.
-->
## Setup
You need access to Microsoft Power Platform to complete this challenge project. You'll be using Microsoft Dataverse, Power Apps, and Power Automate to complete this work. 

### Sign up for a Microsoft Power Platform trial
If needed, you can sign up for a trial by following these steps:

1. Navigate to https://powerapps.microsoft.com and click **Start free**.
2. Under **Get started**, enter your email address in the text box that says **Enter your work email address.**
3.  You see a prompt that you have an existing account with Microsoft. Select
    **Sign in.**
4.  Enter your password.
5.  Select **Yes** to stay signed in.
6.  Complete your account info and select **Get started** to sign up for your
    Microsoft Power Platform trial.

<!-- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - -->

<!-- Do not add a unit summary or references/links -->
