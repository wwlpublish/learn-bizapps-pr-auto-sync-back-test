Advanced forms are configured in the Portal Management app, and not through Power Apps portals Studio.

> [!div class="mx-imgBorder"]
> [![Diagram of the Advanced form overview in Portal Management.](../media/web-form-overview.png)](../media/web-form-overview.png#lightbox)

### Advanced form properties

Unlike a list or basic form, an advanced form is not linked to any particular Microsoft Dataverse table. Instead, an advanced form organizes advanced form steps and persists a history of a user's steps as advanced form session rows. Options on the advanced form control top-level preferences for the multi-step process:

- **Start step** - Controls the initialization of the form within the portal.

- **Authentication** - Associates a form session with a portal user. Authenticated advanced forms capture portal user information and provide the **Save** and **Resume** capabilities by using sessions.

- **Expiration** - Defines how to handle stale saved sessions and expire them.

- **Progress indicator** - Is supported where the advanced form includes multiple steps.

![Screenshot of Advanced form properties in Portal Management app.](../media/advanced-form-properties.png)

### Advanced form steps

Advanced form steps provide the flow logic of the form’s user experience, such as steps and conditional branching. They also provide details regarding the rendering of a form and additional behavior.

> [!IMPORTANT]
> If advanced form steps are modified, previously created history data could now be stale. Whenever steps are changed, we recommend that you delete all advanced form session rows to eliminate a mismatch between the sequence of steps that are logged in the history and the current sequence.

Each advanced form that is presented on the portal has one or more steps. These steps share some common properties:

- **Target table** - The Dataverse table that is selected for the step defines available columns and how step data is related to the previous and next steps in the sequence.

- **Next Step** - Each step contains a pointer (a lookup) to the next step, with the exception of terminal steps. Terminal steps do not have a next step and are the last step of the advanced form. With conditional branching, you can have multiple terminal steps.

- **Move Previous Permitted** - This property defines whether the step allows users to return to the previous step. Depending on the logic and the data that is captured, some steps are irreversible, while others (typically during the information capture sequence) allow navigation back and forth through the steps.

The following step types are available: **Load Form/Load Tab**, **Redirect**, and **Condition**.

> [!NOTE]
> The **Condition** step can't be selected as the start step for an advanced form.

#### Load Form and Load Tab steps

The **Load Form** and **Load Tab** step types allow the step to act as a basic form within the overall advanced form process. These steps load a model-driven form with a similar set of available options as a basic form. For more details about configuring individual **Load Form** and **Load Tab** steps, see [Define a load form and load tab step type](/power-apps/maker/portals/configure/load-form-step/?azure-portal=true).

Similar to the basic form configuration, the related advanced form metadata rows contain additional behavior modification logic to change or override the functionality of form columns when they are rendered on the portal. You can use the advanced form metadata to redefine the behavior of individual columns, sections, tabs, subgrids, notes, and timelines.

#### Redirect step

The **Redirect** step type allows for a redirect of the user's browser session to another page in the portal or to an external URL. This step is useful for seamlessly directing the process flow. Configuration is similar to the basic form's **On Success** settings. For more information, see [Add a redirect step type](/power-apps/maker/portals/configure/add-redirect-step/?azure-portal=true).

#### Condition step

The **Condition** step type evaluates an expression. If the expression evaluates to true, then the next step is displayed. If the expression evaluates to false, and if the **Next Step If Condition Fails** is specified, that step is displayed. Combining the **Condition** and **Redirect** steps allows the creation of data-driven process flows.

> [!IMPORTANT]
> Design-time validation does not exist for expressions. If a specified logical expression is invalid, for example, if it refers to a non-existent table column, the step fails to run, and a generic portal error message is displayed to the user. Keep expressions simple and make sure that the syntax and column references are correct.

For more information about configuring **Condition** steps and expression syntax, see [Add a conditional step type](/power-apps/maker/portals/configure/add-conditional-step/?azure-portal=true).

## Add an advanced form to your portal

An advanced form defines required behavior but does not contain information regarding how and where on the website to render the form. The advanced form contains relationships to web pages and a start step to control the initialization of the form within the portal.

> [!NOTE]
> An advanced form can't be selected as an action target; it can only be displayed on a web page.

The advanced form is not listed as a component in portals Studio, but a maker can add the following Liquid tag to the page source code to display a pre-configured form in the Portal Management app.

```twig
{% webform name: 'advanced form name' %}
```

> [!div class="mx-imgBorder"]
> [![Screenshot of Advanced form added to web page in Portal Studio.](../media/web-form-portal-studio.png)](../media/web-form-portal-studio.png#lightbox)

You can also select an advanced form as the value for an **Advanced Web Form** lookup on a webpage. If the page template associated with the webpage supports this lookup value, it will use that form definition to render the form.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4AoG8]
