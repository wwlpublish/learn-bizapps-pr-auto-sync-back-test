Formulas are designed to enhance functionality, performance, and user
experience in your Power Apps canvas app. Like Excel, in Microsoft Power Apps you can create
single function formulas or combine multiple functions and elements in
the same formula. In Power Apps, you also can modify the way controls
behave and display by defining the control's properties with a formula.
To view all the Power Apps functions, see more information in the
[formula reference for Power Apps](/power-apps/maker/canvas-apps/formula-reference/?azure-portal=true).
The following screenshot shows the controls that are available in Power Apps. To view
the full list of controls, see more information in the
[controls and properties in Power Apps](/power-apps/maker/canvas-apps/reference-properties/?azure-portal=true).
This documentation also describes the list of properties available
for each control.

![Screenshot of Input dropdown menu item control.](../media/controls.png)

## Control properties

Each control has a specific set of properties. The properties available
are different based on the control type. This is because each control
has a slightly different use case and look and feel when users
interact with the app. However, there are a few control properties, such
as Visible, X, Y, and a few others that are present for all controls. The
exception is the **screen** control, which does not have an X or Y property.
Before developing your app, first try to determine what functionality
you're looking for and then select the control that best fits those needs.

In some cases, depending on the app requirements you can use different controls
interchangeably to get the same results. For example,
**Dropdown** and **Combo box** are similar controls. One key
difference between the two is a **Combo Box** allows you to
search for items and select multiple items. The **Dropdown**
control does not support this functionality.

## Localization

Power Apps is used to build apps that are used around the globe. Apps can
be written so the user experience is completely in their native language
and regional settings. The portal and other web interfaces
will also reflect your local language.

To help you in your building experience, **Power Apps formulas adapt to
your local language**. For example, you might see the following formula:

```powerappsfl
Filter(DataSource, Price > 12.50)
```

This is the default for languages where the decimal (.) is used to as the decimal
separator. If your language uses the comma (,) as the decimal separator then the
syntax of the formula adapts. The previous formula becomes this.

```powerappsfl
Filter(DataSource; Price > 12,50)
```

Keep this in mind as you start work with formulas and functions. All of
the formulas found in this learning content assume a decimal (.)
separator.

If you need to build apps that support different languages and regions,
see [Build global support into canvas apps](/power-apps/maker/canvas-apps/global-apps/?azure-portal=true).
