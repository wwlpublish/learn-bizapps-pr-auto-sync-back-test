To create a business process flow, refer to the [PowerApps maker portal](https://make.powerapps.com/?azure-portal=true) documentation.

You can create business process flows from three places.

1. Select **Flows** in the left panel and select the **Business process flows** tab. Then select **New** in the action pane.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Flows page.](../media/flows.png)](../media/flows.png#lightbox)

1. You can create a business process flow from a solution. Under **New** in the action pane, select the **Automation** menu. Under **Automation**, select **Process**, and then select **Business process flow**.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the Automation menu and submenus.](../media/menus.png)](../media/menus.png#lightbox)

1. Open a model-driven app in the edit mode. Select the **Automation** icon in the left panel and select **Add business process flow**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the Automation area where you select Add business process flow.](../media/automation.png)

    When you create the business process flow, you need to select a table, which will be the primary table of the business process flow. By default, a stage will be created with a step in it.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of stage with a default step.](../media/default-stage.png)

1. In the stage property, enter the display name. You can also select the category of the stage. A category lets you group stages by a type of action. It's useful for reports that will group rows by the stage they are in. The options for the stage category come from the Stage Category global choice. You can add more options to this global choice and change the labels of existing options if you want. Following are the category global choices:

    - Qualify

    - Develop

    - Propose

    - Close

    - Identify

    - Research

    - Resolve

    - Approval

1. Select **Data Step #1**, and in the property panel, select the data field. You can select the required option in the Data Step property if the data field is mandatory.

1. To add a new step within the stage, select **Add** in the action pane and select **Add Data Step** under **Composition**.

    > [!div class="mx-imgBorder"]
    > ![Screenshot of the Add Data Step section.](../media/action-menu.png)

1. If you have multiple data steps within a stage, you can use the **Sequence** property to sequence the data fields.

1. You can add multiple stages by selecting the **Add** button in the action pane, followed by the **Add Stage** button under **Flow**. Business process flows can have up to 30 stages.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of business process flow step creation.](../media/multiple-stages.png)](../media/multiple-stages.png#lightbox)

## Business process flow with multiple tables

You need to select a base table to create a business process flow. The default table for all the stages is the base table created during the creation of a new stage. From the second stage onward, you can change the table.

> [!div class="mx-imgBorder"]
> [![Screenshot of adding an entity from the second stage.](../media/entity-relationship.png)](../media/entity-relationship.png#lightbox)

If a relationship between two tables exists, a relationship block appears in the property pane. You need to enter a relationship when the preceding stage in the process is based on a different table. For the stage currently being defined, you need to choose Relationship block in the property pane to identify a relationship to use when moving between the two stages. Relationships define the column mapping between two tables, which automatically carry over data between rows, minimizing data entry.

## Branching capability

To design a business scenario, you can create a linear business process flow. To manage a complex business process flow, you need to use branching. The branching condition consists of multiple logical expressions that use a combination of *AND* or *OR* operators.

> [!div class="mx-imgBorder"]
> [![Screenshot of AND or OR operators in branching.](../media/branching.png)](../media/branching.png#lightbox)

To initiate a branching, select **Add** in the action pane and under **Flow**, select **Add condition**. In the condition block, you can define single or multiple conditions supported by various operators, like *equals*, *does not equal*, and *contains data*. Two endpoints (true and false) of the condition block can be connected to different stages. You can select the **Connector** button in the action pane to reconnect the branched-out stage.

## Security features

Different users in an organization may follow different processes to execute the same operation. To perform the same function, different conditions may be applied for different users. You can have up to 10 active business process flows per entity to provide appropriate processes for different situations. You can associate business process flows with security roles so that only people with those security roles can see or use them. You can also set the order of the business process flows so that you can control which business process flow will be set by default. To set business process flow order, you need to open a business process flow in the designer and then select **Order Process Flow** on the command bar.

> [!div class="mx-imgBorder"]
> [![Screenshot of an Order Process Flow.](../media/order-process-flow.png)](../media/order-process-flow.png#lightbox)

Each business process flow definition is represented as a custom entity. It comes with its own set of privileges that can be edited within a security role. You can specify the privileges in the **Business Process Flows** tab for a security role.

In the next unit, you'll learn how a canvas app can be embedded in a model-driven app form by using the canvas app component.
