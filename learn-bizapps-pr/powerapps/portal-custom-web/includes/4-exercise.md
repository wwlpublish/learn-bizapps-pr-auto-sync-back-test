The purpose of this hands-on lab is to introduce the concept of building and extending Liquid templates.

The exercises work best when you have sample data to work with. Depending on the environment that you are working with, you might want to install some sample data to assist with the exercises. Microsoft Dataverse does provide the ability to add sample data as needed. If the environment that you are working in does not have sample data installed, follow the steps in the [Add or remove sample data](/power-platform/admin/add-remove-sample-data/?azure-portal=true) documentation to install the sample data into your environment.

## Learning objectives

At the end of these exercises, you will be able to:

- Extend Liquid templates by using `extends` and `block` tags.
- Reuse Liquid templates by using the `include` tag.
- Apply table permissions to the results of the new template.

### Prerequisites

For this exercise, you will need to have the following parameters set up in your environment:

- A Power Apps portal that is provisioned. If you do not have a Power Apps portal available, follow the [Create Portal](/power-apps/maker/portals/create-portal/?azure-portal=true) instructions to create one.
- Access to the Power Apps maker portal.

## High-level steps

To finish the exercise, you need to complete the following high-level tasks:

- Create a partial template by accessing Dataverse data to use as a layout block.
- Create a new template that extends a two-column layout web template.
- Overwrite the side panel to include the partial template.
- Change the template of an existing webpage.
- Configure table permissions to display data to anonymous users.

## Detailed steps

To complete the exercise, you will build a new page template that includes a side panel that lists all accounts in Dataverse.  

### Create a partial template

Your first task is to create a partial template that will not be used to render a page but will instead be inserted into another template.

1. Open [https://make.powerapps.com](https://make.powerapps.com/?azure-portal=true).
2. Select the Portals Management app.
3. Select **Page Templates**.
4. Select **New**.
5. Enter the following values:
   - **Name** - Directory 
   - **Website** - Select your current website
   - **Source** - Enter the following content:

    ```twig
    {% fetchxml accounts %}
    <fetch>
      <entity name="account">
        <attribute name="name" />
      </entity>
    </fetch>
    {% endfetchxml %}
    
    {% if accounts.global_permission_granted %}
      <ul>
        {% for account in accounts.results.entities %} 
        <li>{{ account.name }}</li>
        {%- endfor -%}
      </ul>
    {% else %}
      <div class="alert alert-warning">You do not have permissions to access the directory.</div>
    {% endif %}
    ```

6. Select **Save & Close**.

### Extend an existing template

Next, you will create a new template that extends an existing Liquid template and then insert the template that you previously created.

1. Select **Web Templates**.
2. Select **New**.
3. Enter the following values:
   - **Name** - Directory Template
   - **Website** - Select your current website
   - **Source** - Enter the following content:

    ```twig
    {% extends "Layout 2 Column Wide Left" %}
    
    {% block aside %}
      <h2>Directory</h2>
      {% include 'Directory' %}
    {% endblock %}
    ```

6. Select **Save & Close**.

### Create a page template and associate with that page

In this exercise, you will create a page template that will use your new web template and will include the Directory output.

1. Select **Page Templates**.
2. Select **New**.
3. Enter the following values:
   - **Name** - Directory Page Template
   - **Website** - Select the current website
   - **Type** - Select **Web Template**
   - **Web Template** - Select **Directory Template**
   - **Table Name** - Select **Web Page**
4. Select **Save & Close**.

### Test

Your next step is to test that your new template works:

1. Open Power Apps portals Studio in a new browser tab. Then, follow these steps:
   1. Go to the Power Apps maker portal at https://make.powerapps.com.
   2. Select the target environment by using the environment selector in the upper-right corner.
   3. From the **Apps** list, select the application of type **Portal**.
   4. Select the **Edit** menu.
2. On the toolbelt, select the **Pages** icon.
3. Select an existing page, for example, **Product A** under **Services**. Note: names and hierarchy of pages on your portal might differ.
4. Locate the **Template** property in the **Component** panel on the right side.
5. Select **Directory Page Template** as the new template.
   The list of accounts should be displayed because portals Studio runs under the maker account and uses Dataverse security instead of table permissions to filter the data.
6. Select **Browse website**.
   The message "You do not have permissions to access the directory" should be displayed.

### Add table permissions

Follow these steps to add table permissions:

1. Return to the Portal Management app.
2. Select **Table Permissions**.
3. Select **+ New**.
4. Enter the following values:
   - **Name** - Account Directory
   - **Table Name** - Select the account table
   - **Website** - Select your current website
   - **Scope** - Select **Global**
   - **Privileges** - Select **Read**
5. Select **Save**.
6. Scroll to the **Web Roles** subgrid.
7. Select **Add Existing Web Role**.
8. Locate and select **Anonymous users** and **Authenticated users**.
9. Select **Add**.

### Test

Your final task is to test your new template:

1. Switch to portals Studio.
2. Select **Browse website**.

This command rebuilds the site cache. A simple browser page refresh will not be sufficient to update the data.

The page should now be displayed and include the list of accounts.

   ![Site cache rebuilt with page displayed and list of accounts.](../media/build-template.png)
