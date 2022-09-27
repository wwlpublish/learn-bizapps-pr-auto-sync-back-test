Now that you've established a gateway connection and built a desktop flow, it's time to build a cloud flow with which to connect. Cloud flows are stored and run on the cloud, as opposed to desktop flows, which are stored and run on a desktop. Cloud flows have the advantage of hundreds of predefined connections with thousands of triggers and actions at your disposal. However, desktop flows can work in desktop programs without a predefined connection or existing actions. Both flows have their benefits. By combining these two types of flows, you'll gain the benefits of both.

To begin creating your cloud flow, open [Power Automate](https://flow.microsoft.com/?azure-portal=true) and select **My flows > Cloud flows**.

> [!div class="mx-imgBorder"]
> [![Screenshot of the Cloud flows view.](../media/cloud-flows.png)](../media/cloud-flows.png#lightbox)

Next, select **New flow > Instant cloud flow**.

> [!div class="mx-imgBorder"]
> [![Screenshot of the New flow and Instant cloud flow options.](../media/instant-cloud-flow.png)](../media/instant-cloud-flow.png#lightbox)

Name your flow. The following screenshot shows the name as "Manual trigger Desktop flow to enter invoice." Select the **Manually trigger a flow** option and then select **Create**.

> [!div class="mx-imgBorder"]
> [![Screenshot of the Flow name field and trigger option list.](../media/name-flow.png)](../media/name-flow.png#lightbox)

When the screen changes to the flow builder, select **New step** and then search for and select **Run a flow built with Power Automate for desktop**.

> [!div class="mx-imgBorder"]
> [![Screenshot of the Run a flow built with Power Automate for desktop option.](../media/run-desktop-flow-action.png)](../media/run-desktop-flow-action.png#lightbox)

In the ***Desktop flow** drop-down menu, select **+ Create a new desktop flow**.

> [!div class="mx-imgBorder"]
> [![Screenshot of the create a new desktop flow action.](../media/create-new-desktop-flow.png)](../media/create-new-desktop-flow.png#lightbox)

In the **Build a desktop flow**, add the same flow name and then click on **Launch app**.

> [!div class="mx-imgBorder"]
> [![Screenshot of build a desktop flow window with name field and launch button.](../media/build-desktop-flow.png)](../media/build-desktop-flow.png#lightbox)

This will automatically add the new flow in Power Automate Desktop and will open another window with the flow which is currently editing.

> [![Screenshot of the desktop flow open.](../media/flow.png)](../media/flow.png#lightbox)

Under Actions, search for **launch** and click on **Launch new Microsoft Edge**.

> [![Screenshot of the launch new Microsoft Edge button.](../media/launch-edge.png)](../media/launch-edge.png#lightbox)

In **Initial URL** add **https://powerautomate.microsoft.com** and then click on **Save**.

> [![Screenshot of the initial U R L added.](../media/initial-url.png)](../media/initial-url.png#lightbox)

Finally, click on the **Save** button and then close the window.

> [!div class="mx-imgBorder"]
> [![Screenshot of the save flow button.](../media/save-flow.png)](../media/save-flow.png#lightbox)