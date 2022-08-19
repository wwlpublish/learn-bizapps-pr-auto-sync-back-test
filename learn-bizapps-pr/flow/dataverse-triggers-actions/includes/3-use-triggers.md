All triggers in Power Automate produce information, which is called dynamic content. Occasionally, this information only references who began the flow by selecting a button, but all Dataverse triggers give, at minimum, a row of data from a table.

When using a Dataverse trigger, you need to specify the following parameters:

- **Environment** - Environments are like containers in which you can organize tables, flows, apps, and more. Some organizations only use a single environment, but many have multiple environments for various priorities and developments.

- **Table Name** - Allows you to specify the exact table where your data is held, which will trigger your flow. 

- **Scope** – This parameter allows you to specify when the flow runs according to the user who triggered it. Various scopes that you can choose from are:

  - **Business unit** – Actions that are taken on a record that your business unit owns will trigger the flow. 
  - **Parent: Child business unit** – A trigger with this scope will be initiated on actions that are taken on a record that your business unit or any child business unit owns. 
  - **Organization** – The flow will be triggered for actions that are taken on the record, regardless of owner.
  - **User** - Only actions on a record that you own will trigger the flow.


> [!div class="mx-imgBorder"]
> [![Screenshot of the When a record is updated trigger information.](../media/trigger-info.png)](../media/trigger-info.png#lightbox)

One trigger allows you to request more inputs. When a user creates, updates, or deletes a record, you don't have the opportunity to ask for more information because the user could be performing those actions from multiple places. However, with the **When a flow step is run from a business process flow** trigger (when this trigger is selected it's titled **When a flow step is executed**), the user can trigger the flow from a button on the table inside Dataverse. Because Power Automate knows where the user is performing the action, you can request additional input for use later in the app. 

Select **Add an input**, specify the type of input that you want, and then enter a short message to the user. For example, the following screenshot shows a request for an email address. The scope hasn't been requested because any user who has access to the table in Dataverse would be able to select the button on any record that they have access to.

> [!div class="mx-imgBorder"]
> [![Screenshot of the When a record is selected email input information.](../media/email-input.png)](../media/email-input.png#lightbox)

Now that you've learned about the mechanics of triggers and how to use them, let's learn about the actions that you can perform within your flows.
