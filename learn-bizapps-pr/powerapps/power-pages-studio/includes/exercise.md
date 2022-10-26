The purpose of this hands-on-lab is to create a web page and edit source code by using Power Pages design studio.

At the end of these exercises, you'll be able to:

- Open Power Pages design studio to edit your portal.
- Create new page using a standard template.
- View the source code of the page.
- Add custom HTML code directly to a page.

For this exercise, you'll need to have the following :

- A provisioned Power Pages site in your environment. If you don't have a Power Pages site available, follow the [Create and manage Power Pages sites](/power-pages/getting-started/create-manage) instructions to create one.

## Scenario

To enhance website experience for visitors sometimes it's necessary to add custom HTML content to a page. In this exercise, you'll add HTML code that creates a dismissable alert. The code will also include a small fragment in [Liquid language](/power-apps/maker/portals/liquid/liquid-overview) creating a dynamic greeting for the visitor.

### High-level steps

1. Open your portal in Power Pages design studio.
2. Create a new landing webpage.
3. Edit page, add a spacer and content placeholder then add HTML code.
4. Save the page and browse the site to view the results.

## Detailed steps

### Launch Power Pages design studio

1. Sign in to [Power Pages](https://make.powerpages.microsoft.com/?azure-portal=true).

1. Select a target environment by using the environment selector in the upper-right corner.

1. Select your site then select **Edit** to launch the design studio.

1. Make sure **Pages** workspace is selected.

   ![Screenshot of Power Pages design studio with a site in edit mode.](../media/exercise-launch-studio.png)

### Create a web page

1. Select **+ Page** button.
6. Enter a page name.
3. Select **Landing Page** standard layout, then press **Add**.
   ![Screenshot of page created with the landing page layout.](../media/exercise-create-page.png)

### Edit page

1. Select the first button on the page. Press the plus sign (**+**), then select **Spacer** element. That will add small space before our custom content.

2. Select the spacer, press the plus sign (**+**), then select **Text** element. That will add a placeholder for our custom content.

3. Select the **Source code editor** (**</>**) icon in the top command bar. Your page should look like this:

   ![Screenshot of the placeholder text for custom content and open source code editor.](../media/exercise-placeholder.png)

4. Copy the following code and paste it into the page source replacing `<p>Enter text</p>` content:

    ```html
    <div role="alert" class="alert alert-info alert-dismissible">
      <button type="button" data-dismiss="alert" aria-label="Close" class="close"><span aria-hidden="true">×</span></button>
      <strong>Happy <span>{{ now | date: 'MMMM' }}</span>!</strong>
      Get your unlimited free education at 
      <a href="https://learn.microsoft.com/">Microsoft Learn</a>
    </div>
    ```

5. Press **Save** button then press **Preview** button in the top right corner. 

6. Your custom page with a dismissable alert will open.

    ![Screenshot of a Power Pages page rendering miscellaneous bootstrap content.](../media/exercise-page.png)

7. Check that the greeting includes current month.

8. Press cross (x) icon to dismiss the alert.
