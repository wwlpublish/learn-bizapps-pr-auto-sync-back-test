Power Apps in the Microsoft Power Platform is made up of two major tools: Canvas app and Model-driven app. While model-driven apps can only have Dataverse as the backend database, canvas apps support over 400 data sources through the built-in or custom connectors.

Canvas apps are used for the mobile or tablet devices, where you need task-based applications. The development process is simple, where you're provided with a blank canvas. You can drag components on the blank canvas to form the user interface. You can develop formulas in the property pane of each component to add validation and other business logic.

You can bring the power of canvas apps into a model-driven app by embedding a canvas app. It enables creation of rich visual areas on a form and displays data from various sources, along with the data from Dataverse.

## Embed a canvas app using the classic experience

To embed a canvas app to a model-driven form by using the classic experience, you need to first open the main form and switch to the classic view. In the classic development platform, which is the original development platform for Dynamics CRM applications, you can automatically generate the canvas app to be embedded into the model-driven app.

> [!div class="mx-imgBorder"]
> [![Screenshot of the Switch to classic option.](../media/classic.png)](../media/classic.png#lightbox)

In the classic view, you need to select the column that will bind to the canvas app. Select **Change Properties** from the **Edit** group on the **Home** tab. Select the **Controls** tab in the **Field Properties** dialog box.

> [!div class="mx-imgBorder"]
> [![Screenshot of the Field Properties dialog box.](../media/controls.png)](../media/controls.png#lightbox)

You add a canvas app control by selecting **Add Control**. Select **Web** to allow the canvas app to be displayed in a web interface.

The following three properties are used for configuring the application properties of the embedded canvas app into the model-driven app:

- **Table (Entity) name:** Specifies the table that will provide data to the embedded canvas app. This will be prefilled based on the form data source. However, you can change the value by selecting the **Configure property** icon.

- **App name:** Specifies the name of the canvas app to embed. The model-driven form looks for the canvas app with the specified name in the current environment. If a canvas app with that name can't be found in the environment, the canvas app control will use the app ID to load the canvas app. Enter the app name for an existing canvas app.

- **App ID:** Specifies the app ID of the embedded canvas app. You can enter an app ID for an existing canvas app.

> [!div class="mx-imgBorder"]
> [![Screenshot of the Field Properties dialog box with Canvas app selected under Web.](../media/field-properties.png)](../media/field-properties.png#lightbox)

If you don't have an existing canvas app, you can keep the app name and app ID properties blank and select the **Customize** button in the **Field Properties** dialog box to create a new canvas app. This opens the Power Apps canvas app studio.

A new canvas app is created with the primary key field of the selected table on the host model-driven app in the user interface. The primary key is placed on the **Form1** form control, which is automatically created. The **Item** property of the form control references a special **ModelDrivenFormIntegration** control.

You'll also notice this special **ModelDrivenFormIntegration** control in the left pane of the canvas app studio. This control is responsible for bringing contextual data from the host model-driven form to the embedded canvas app.

You design the canvas app by adding more fields and controls. Remember to save and publish the canvas app after you complete your design. The app name and app ID property of the host model-driven app are automatically updated with the corresponding details of the newly created canvas app.

## Embed a canvas app using the modern experience

To embed a canvas app to a model-driven form by using the modern experience, you need to first open the main form, which is the host model-driven form. You need to select the column from the main form editor that will bind to the canvas app, followed by the **Canvas app** control under the **Related data** group from the **Components** list in the model-driven app.

> [!div class="mx-imgBorder"]
> [![Screenshot of the Add Canvas app area.](../media/add-canvas-app.png)](../media/add-canvas-app.png#lightbox)

A dialog box named **Add Canvas** app opens. This dialog box has three properties: **Entity name**, **App name**, and **App ID**. These properties are like those in the classic experience. You can create a blank canvas app and enter the app ID in the dialog box.

Alternatively, you can select the column that will bind to the canvas app and select the **Component** property in the column property pane at the right side of the form editor. From the **Add component** dialog box, select **Canvas app**.

> [!div class="mx-imgBorder"]
> [![Screenshot of the Component property.](../media/component.png)](../media/component.png#lightbox)

You'll be prompted by a dialog box in which you need to enter the three properties: **Entity name**, **App name**, and **App ID**. You can create a blank canvas app and enter the app ID in the dialog box.

The canvas app component will be embedded in the model-driven app, and the component property will look as follows.

> [!div class="mx-imgBorder"]
> ![Screenshot of the canvas app component embedded in the model-driven app.](../media/components.png)

## ModelDrivenFormIntegration control properties and actions

When a canvas app is embedded in a model-driven app, a special control named **ModelDrivenFormIntegration** is added in the canvas app. This control is responsible for bringing contextual data from the host model-driven app to the canvas app. This control has some important properties and actions, as follows:

**DataSource:** By default, the **DataSource** property value should be set to the data source connected to the parent table of the host model-driven form. When you embed an existing canvas app, the **ModelDrivenFormIntegration** data source can be configured from the canvas app tree view.

**OnDataRefresh:** The formula in this property is evaluated when the host model-driven form saves data. Use this property to refresh the data source connected to the parent table of the host model-driven form and to perform other actions like setting or updating variables.

**Item:** This is a read-only property that allows the embedded canvas app to access the columns of the host model-driven app. As an example, to get the value of a column with the name **departmentnumber** and display name **Department Number**, you can use **ModelDrivenFormIntegration.Item. departmentnumber** or **ModelDrivenFormIntegration.Item.'Department Number'**.

**SaveForm:** This is a predefined action that saves the data on the host model-driven form.

**RefreshForm:** This is a predefined action that refreshes the data on the host model-driven form. This comes with a single parameter:

- **showPrompt** - A required boolean parameter that indicates if a confirmation prompt should be displayed to the user before saving any unsaved data on the host model-driven form. Values should be "true" or "false".

**NavigateToMainForm:** This is a predefined action that navigates the host model-driven form to a main form and displays the specified row. This comes with three parameters:

- **entityName** - A required string parameter that specifies the parent table of the main form.

- **formName** - A required string parameter that specifies the name of the main form to navigate to.

- **recordId** - A required string parameter that specifies the ID of the row to display in the main form.

**NavigateToView:** This is a predefined action that navigates the host model-driven form to a view. This comes with two parameters:

- **entityName** - A required string parameter that specifies the parent table of the view.

- **viewName** - A required string parameter that specifies the name of the main form to navigate to.

**OpenQuickCreateForm:** This is a predefined action that can open the default quick create form for a table. This comes with a single parameter:

- **entityName** - A required string parameter that specifies the parent table of the quick create form.

In the next unit, you'll learn how to add a timeline component in a model-driven form.
