The timeline helps app users view all activity history. The timeline control is used to capture activities like notes, appointments, emails, phone calls, and tasks to ensure that all interactions with the related table are tracked and visible over time. Use the timeline to quickly catch up on all the latest activity details.

The timeline control provides a common framework to view activity information related to any table, which gives users a better understanding and helps them deliver more personalized service in an efficient and effective manner. If you need to add a custom activity, you need to create an Activity type table. An activity type table is based on the time dimensions that help to track the occurrence of an action. The **Enable attachments** setting in the table will allow users to add attachments and notes to the custom activity table.

For more information about activity tables, see Module 3, Unit 2, "Create a table."

To use the timeline control, you should have activity type tables in the Dataverse. The timeline control can establish a relationship between the activity table and the standard table.

## Add the timeline control

You need to add the timeline control on a standard table to track the activity. For example, you have a department table in Dataverse and you want to track all activities related to the department, like appointment, meeting, phone, email, or task.

To activate the timeline control, open the **Advanced options** section of the table properties and select **Creating a new activity** property under **Making this table an option when** property group.

> [!div class="mx-imgBorder"]
> [![Screenshot of the timeline control configuration options.](../media/activity-table-property.png)](../media/activity-table-property.png#lightbox)

Navigate to the model-driven form of type main under the standard table. Select the area of the form editor where you want to place the timeline control and select **Components** followed by **Timeline** under the **Related data** group.

> [!div class="mx-imgBorder"]
> ![Screenshot of the Components options.](../media/timeline.png)

After you select the timeline control once, it will be disabled from the control list to prevent further selection on the same form. However, if a table has multiple main forms, it's possible to add a timeline in all the forms.

## Configure the timeline control

The timeline component has several features and functionality that can be configured and tailored to support specific business needs.

There are primarily three **record types** to show in the timeline: activities, notes, and posts. All of them are enabled by default.

- **Activities** can have many customizable subactivities to support business needs. Depending on what you have installed, the administrator can create, add, and display several different customized subactivities under the **Activity** section of the menu on the timeline.

- **Notes** allow you to capture details related to the table record. For example, you can use notes to capture thoughts, summarize information, and provide feedback on a case, and then update the case details later.

- There are two types of **posts**: auto and user. Auto posts are system-generated posts that notify the activity that has occurred. User posts allow you to leave a message for another user on a record.

The **Quick entry record** **type** provides you with quick access to create either a **Note** or a **Post**. 

In the **Sort default** property, you can define the default sort order of the activities within the timeline control.

**Records shown on page** property can display the defined number of records at a time in the timeline control.

The **Enable filter pane** checkbox allows you to enable or disable filter functionality on a timeline. It's enabled by default.

> [!div class="mx-imgBorder"]
> [![Screenshot of a Timeline filter.](../media/filter.png)](../media/filter.png#lightbox)

In the above diagram, you can review the different filter categories and decide which to use. The following is a complete list:

- Record type

- Activity type

- Activity status

- Activity status reason

- Activity due date (active)

- Posted by

- Modified by

The search timeline option shown in the preceding diagram can be enabled by checking the **Enable search bar** property

**Expand all records by default** displays all activities in an expanded view in timeline.

You can configure the default filters that are applied when a form loads or is refreshed by using **Edit filter pane**. Remove filter groups by turning off the setting. Users can remove the default filters to see all the records unless **Enable filter pane** is disabled.

> [!div class="mx-imgBorder"]
> ![Screenshot of the Edit filter pane.](../media/filter-pane.png)

**Enable** "**What you've missed" summary** helps you stay on top of updates and changes made to records by displaying updates at the top of the timeline when you access a record.

Based on the selection you have in the **Record types to show** property, in the **Record settings**, you'll find the list of **Activity types**.

> [!div class="mx-imgBorder"]
> ![Screenshot of Activity types in Record setting.](../media/task.png)

If you select each activity type, a dialog box will appear. You can enable the activity types as per your business need by using the **Enable** checkbox.

To allow users to create activity types directly from the timeline, select the **Create directly from timeline** property.

If you need to create a new activity or open an existing activity, you can do it in various types of forms. **Create Task using** and **Open Task using** are the two properties that control the type of form used for individual activities.

For each activity, the default form is likely to be different. It often shows the most relevant items in context of the selected activity. You can choose which of the items to show on the activity card or whether the titles are shown, among other configurations. To do this, select the default form under **Configure form**.

> [!div class="mx-imgBorder"]
> [![Screenshot of the Configure form for Task dialog box.](../media/configure.png)](../media/configure.png#lightbox)

The **Label** and **Display** options in the preceding dialog box can be configured based on the activity type. For some activity types, the **Status** tag might not be necessary. You can configure the property values accordingly. Instead of using a default form, you can create an activity-specific custom form by selecting **Select form** at the top.

The **Sort activity by** property allows you to control how data is sorted in timeline. It displays the list of the date fields in the activity table. You can select a date based on your requirement. Some dates can only exist on specific types of activities. If you select a date that doesn't exist for a specific activity type, the sort order of that activity type will be impacted.

**Create activities using** lets you choose which type of form users will use to create a new activity. It has three possible values: quick create form, main form, and main form dialog. You can select according to your business need.

**Open activities using** lets you choose which type of form users will use to open an existing activity. It has two possible values you can select, depending on your business needs: main form and main form dialog.

The following unit elaborates on how to create a report in a model-driven app.
