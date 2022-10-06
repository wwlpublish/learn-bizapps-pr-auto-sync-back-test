## Task - Discover and add the Power Automate app to Teams

1. Select the **Apps** icon on the left toolbar, and then search for Power Automate.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of Microsoft Teams app store with the Apps icon highlighted.](../media/apps-icon.png)](../media/apps-icon.png#lightbox)

1. Select the **Power Automate App** when you find it in the search results.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of accessing the Power Automate app in Teams.](../media/power-automate-app.png)](../media/power-automate-app.png#lightbox)

1. You'll see a pop-up with information about the Power Automate App for Microsoft Teams. Select the **Add** button.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of accessing Power Automate in Teams.](../media/add-power-automate.png)](../media/add-power-automate.png#lightbox)

1. If prompted, select your country or region and select **Get Started**.

1. You'll now see the Power Automate app in the left-hand navigation bar. Right-click that icon and select **Pin**. Doing so pins the app to the navigation bar, making it easier to return to it when you need to.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of pinning the Power Automate app in Teams.](../media/pin-app.png)](../media/pin-app.png#lightbox)

## Task - Navigate the Power Automate app for Teams

1. On the home screen, you'll see a section for your flows. It's blank because you haven't created any yet. But as you work through this lab and create flows, it's where you go to edit them and to see your flow runs for any troubleshooting.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of Power Automate in Teams.](../media/no-flow.png)](../media/no-flow.png#lightbox)

1. Select the **Create** tab at the top. Here you'll see a range of the most popular templates, and a menu of categories down the side to help you browse all the templates available. Scroll through some of these categories to get familiar with the range and types of Teams templates that are available here for you to work with.

    > [!div class="mx-imgBorder"]
    > [![A screenshot of Power Automate for Teams with the Create option highlighted.](../media/create.png)](../media/create.png#lightbox)

## Task - Create a flow using the "Follow up on a Message" template (Optional)

1. Navigate to the **Productivity** category and select the template called **Follow up on a Message** (you may need to select See more templates).

    > [!div class="mx-imgBorder"]
    > [![A screenshot of Power Automate for Teams with Productivity selected and the template highlighted.](../media/productivity.png)](../media/productivity.png#lightbox)

1. A simple template to get this flow built appears. You'll see the name is already filled in from the template (you can change it but for now we'll leave it as it is). It also prompts you to sign in to any connectors that the flow needs to use. In this case, because it's the first time we're using a flow to connect to Microsoft Teams and Office 365 Users, we need to sign in. Select **Sign in** next to the Microsoft Teams and Office 365 Users connector in the **Sign in** section.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of creating a flow using template.](../media/create-flow.png)](../media/create-flow.png#lightbox)

1. You'll see a spinning wheel while the sign is in progress, and then when it's complete you'll see a green check, which means you're ready to go. Once you see the green check, select **Create Flow**.

    > [!div class="mx-imgBorder"]
    > [![A screenshot of the Power Automate for Teams create a flow dialog with the green checks highlighted.](../media/green-check.png)](../media/green-check.png#lightbox)

1. You'll see a confirmation message that your workflow has been created and how you can trigger the flow. Select **Done** to close the pop-up.

    > [!div class="mx-imgBorder"]
    > [![A screenshot of Power Automate for Teams - workflow created.](../media/confirmation.png)](../media/confirmation.png#lightbox)

1. Select the **Home** tab of Power Automate apps for Teams, then select the Power Automate Flow created.

    > [!div class="mx-imgBorder"]
    > [![A screenshot of Power Automate for Teams - home tab and the flow created.](../media/home.png)](../media/home.png#lightbox)

1. You'll now see the details of your flow--when it was created, what connectors are being used, who the owners are, and details of any run history. There's nothing there yet because the flow hasn't been run. You can return to this screen at any time via the Home tab of the Power Automate app in Teams.

    > [!div class="mx-imgBorder"]
    > [![A screenshot of Power Automate for Teams - workflow details.](../media/details.png)](../media/details.png#lightbox)

## Task - Create a message in Teams and trigger your flow (Optional)

1. Select the main Teams icon in the left navigation bar of Teams, and go to the general channel of the team you have been working in. Start a new conversation and type a message--for example:

    > **Get your swag orders in!**
    >
    > We have some new Contoso Coffee shirts- check them out and place your order via the Swag Request app.

    > [!div class="mx-imgBorder"]
    > [![A screenshot of Teams channel- posted message.](../media/new-message.png)](../media/new-message.png#lightbox)

1. Now let's trigger the flow from this message, to set a reminder to follow up later. Hover over the message, Select the ellipsis button **...** and select **More actions**. In the list of actions, Select **Follow up on a** message. If you don't see it listed, select **See more.**

    > [!div class="mx-imgBorder"]
    > [![A screenshot of Teams- following up on a message posted in channel.](../media/follow-up.png)](../media/follow-up.png#lightbox)

1. You'll be prompted with a question asking you when you'd like to be reminded. Select current date, for the time select time 30 minutes from the current time and select **Submit**.

    > [!div class="mx-imgBorder"]
    > [![A screenshot of Teams- following up on a message posted in channel.](../media/date-time.png)](../media/date-time.png#lightbox)

1. **You can move on to Exercise 2 and continue the rest of this lab while waiting for this flow to run.** In 30 minutes, you'll see a notification in the activity. Select the activity to view the message that you set as a trigger of your flow.

    > [!div class="mx-imgBorder"]
    > [![A screenshot of Teams- notification of a message reminder.](../media/feed.png)](../media/feed.png#lightbox)

1. Return to the Power Automate app using the icon on the left-hand menu bar that you pinned earlier. Open your flow by selecting the name.

    > [!div class="mx-imgBorder"]
    > [![A screenshot of the home screen in Power Automate for Teams.](../media/follow-up-flow.png)](../media/follow-up-flow.png#lightbox)

1. You'll see the run history shows your flow ran successfully.

    > [!div class="mx-imgBorder"]
    > [![A screenshot of the flow runs in Power Automate for Teams.](../media/run-history.png)](../media/run-history.png#lightbox)
