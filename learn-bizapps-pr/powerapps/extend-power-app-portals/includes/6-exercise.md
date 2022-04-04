The purpose of this hands-on lab is to demonstrate how to add JavaScript code to a page to render data from Microsoft Dataverse as a chart by using another charting library. The data has been retrieved from Dataverse by using a web template that acts as a REST API endpoint.

The exercises work best when you have sample data to work with. Depending on the environment that you are working with, you might want to install some sample data to assist with the exercises. Microsoft Power Platform does provide the ability to add sample data as needed. If the environment that you are working in doesn't have sample data installed, follow the steps in the [Add or remove sample data](/power-platform/admin/add-remove-sample-data/?azure-portal=true) documentation to install the sample data into your environment.

## Learning objectives

At the end of these exercises, you will be able to:

- Build a webpage that acts as a REST endpoint that returns data from Dataverse.
- Add inline code to a content webpage to retrieve the data by using the endpoint.
- Use an external JavaScript library to consume the retrieved data.

**Estimated time to complete this exercise**: 15 to 20 minutes


### Prerequisites

For this exercise, make sure that the following parameters are set up in your environment:

- A Power Apps portal that is provisioned. If you do not have a Power Apps portal available, follow the [Create Portal](/power-apps/maker/portals/create-portal/?azure-portal=true) instructions to create one.
- Access to the Power Apps maker portal.

### High-level steps

To finish the exercise, complete the following tasks:

1. Create a web template with Liquid code to retrieve data about accounts in Dataverse and then return the data in JSON format.
1. Add **Page Template** and **Web Page** records that use the web template that you created.
1. Open a content page and add JavaScript code that retrieves the data.
1. Add a charting library to the page and JavaScript code by using the library to build a graph with the retrieved data.


#### Create a web template

To create a web template, follow these steps:

1. Go to [Power Apps maker portal](https://make.powerapps.com/?azure-portal=true) and confirm you have selected the correct environment in the upper right.
1. Select **Apps**.
1. Select the Portals Management app.

    > [![Screenshot of the portal management app highlighted.](../media/portal-management-app.png)](../media/portal-management-app.png#lightbox)

1. Select **Web Templates**.
1. Select **+ New**.
1. Enter the following values:
   - **Name** - getAccounts
   - **Website** - Select your current website
   - **Source** - Enter the following content
   - **MIME Type** - application/json

    ```twig
    {% fetchxml accounts %}
    <fetch>
      <entity name="account">
        <attribute name="name" />
        <attribute name="numberofemployees" />
        <attribute name="revenue" />
      </entity>
    </fetch>
    {% endfetchxml %}
    [
    {% for account in accounts.results.entities -%}
      {
        "x": {{ account.numberofemployees }},
        "y": {{ account.revenue }},
        "z": {{ account.revenue | divided_by: account.numberofemployees }},
        "name": "{{ account.name }}"
      }{% unless forloop.last %},{% endunless %}
    {% endfor -%}
    ]
    ```

1. Press **Save & Close**.

This Liquid code retrieves the list of accounts and then generates a data structure in JSON format. The data structure is already prepared for plotting by assigning appropriate labels to data points:

- **name** - Company name
- **x** - Number of employees
- **y** - Company revenue in thousands
- **z** - Revenue for each employee (calculated)

#### Create a page template and a webpage

To create a page template and a webpage, follow these steps:

1. Select **Page Templates**.
1. Select **+ New**.
1. Enter the following values:
    - **Name** - getAccounts
    - **Website** - Select your current website
    - **Type** - Select **Web Template**
    - **Web Template** - Select **getAccounts**
    - **Use Website Header and Footer** - Clear the check box
1. Select **Save & Close**.
1. Select **Web Pages**.
1. Select **+ New**.
1. Enter the following values:
    - **Name** - getAccounts
    - **Website** - Select your current website
    - **Parent Page** - Select **Home**
    - **Partial URL** - getAccounts
    - **Page Template** - getAccounts
    - **Publishing State** - Published
1. Select **Save & Close**.

> [!IMPORTANT]
> If you have not previously configured table permissions for the account table, your API page will return an empty array. Complete the next task to set up the permissions if you have not done so previously.

#### Add table permissions

To add table permissions, follow these steps:

1. Switch to the Portal Management app.
1. Select **Table Permissions**.
1. Select **+ New**.
1. Enter the following values:
    - **Name** - Account Directory
    - **Table Name** - Select account table
    - **Website** - Select your current website
    - **Access Type** - Select **Global**
    - **Privileges** - Select **Read**
1. Select **Save**.
1. Scroll to the **Web Roles** subgrid.
1. Select **Add Existing Web Role**.
1. Locate and select **Anonymous users** and **Authenticated users**.
1. Select **Add**.

#### Test the REST webpage

Go to `https://yourportal.powerappsportals.com/getAccounts`.

Your output should look like the following example:

   > [!div class="mx-imgBorder"]
   > [![Screenshot example of the REST webpage output.](../media/rest-data.png)](../media/rest-data.png#lightbox)

#### Add code to retrieve the data

To add code to retrieve the data, follow these steps:

1. Open Power Apps portals Studio in a new browser tab and then follow these steps:
    1. Go to [Power Apps maker portal](https://make.powerapps.com/?azure-portal=true).
    1. Select the target environment by using the environment selector in the upper-right corner.
    1. From the **Apps** list, select the application of type **Portal**.
    1. Select the **Edit** menu.
1. Select the **Pages** icon on the tool belt on the left side.
1. Select an existing page from the hierarchy, for example **Product B** located under the **Services** page.
    > [!NOTE]
    > The names and hierarchy of pages on your portal might differ.
1. Select the **Page Copy** area on the page.
1. Select **Components** on the tool belt.
1. Select **One-column section**.
1. Select **Added section** and then select the **source code editor** icon.
1. Insert the following code as the content of the innermost **div** element:

    ```html
    <script>
    function makeChart(rData) {
      console.log(rData);
    }

    $(document).ready(function() {
      $.get('/getAccounts', makeChart, 'json');
    });
    </script>
    ```

1. Select **Save**.
1. Select **Browse website**.
1. When the page is displayed, press the **F12** key to display browser developer tools.
1. Verify that the console output contains the same data as previously retrieved by the REST API page.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of the console output with the same data as the previously retrieved REST API page.](../media/console-output.png)](../media/console-output.png#lightbox)

> [!IMPORTANT]
> If you have not previously configured table permissions for the account table, your API call will return an empty array. Make sure that you have completed the **Add table permissions** task.

#### Add external library functionality

This exercise uses Highcharts.js library (free for personal or non-profit use) to create a bubble chart based on the data.

1. Switch to portals Studio.
1. Locate and open the content page that you previously modified.
1. Select the section that you previously modified.
1. Insert the following code either above or below the previous code:

    ```html
      <script src="https://code.highcharts.com/highcharts.js"></script>
      <script src="https://code.highcharts.com/highcharts-more.js"></script>
      <figure>
        <div class="mychart"></div>
      </figure>
    ```

1. Modify the **makeChart** function as follows:

    ```javascript
    function makeChart(rData) {
      console.log(rData);
      Highcharts.chart($('.mychart')[0], {
        title: {
          text: "Customers efficiency"
        },
        legend: {
          enabled: false
        },
        xAxis: {
          title: {
            text: "Number of employees"
          }
        },
        yAxis: {
          title: {
            text: "Turnover ($K)"
          }
        },
        tooltip: {
          pointFormat: '<strong>{point.name}</strong><br/>Employed: {point.x}<br>Turnover ($K): ${point.y}',
          headerFormat: ''
        },
        series: [{
          type: 'bubble',
          data: rData
        }]
      });
    }
    ```

1. Select **Save**.
1. Select **Browse website**.
1. The output should now include the bubble chart. Hover over the bubbles to verify the data.

> [!div class="mx-imgBorder"]
> [![Screenshot of the output with the bubble chart now included.](../media/chart.png)](../media/chart.png#lightbox)
