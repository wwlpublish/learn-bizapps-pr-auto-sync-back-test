Every canvas app you build will incorporate and utilize controls.
Remember, there are several different types of controls to choose from,
and each control has a slightly different set of **Properties**. When
developing your app, you can create formulas to dynamically change and
update different control properties, such as:

- Format

- Text

- Color

- Position (X and Y)

Here's a detailed look at the **Date picker** control,
including a simple example.

The Date picker control has a few key properties:

- **DefaultDate** -- The initial value of a date control unless the
    user changes it.

- **SelectedDate** -- The date currently selected in a date control.

- **Format** -- The text format in which the control shows the date
    and the user specifies the date.

- **Language** -- Determines the language used to format dates,
    including names of months. If this property isn't specified, the
    user's device setting determines the language.

Use the following steps to add the **Date picker** control and modify
the displayed format.

1. In Power Apps Studio, select the **Insert** tab.

1. In the ribbon, select **Input**.

1. From the drop-down menu, select **Date picker**. By default, when
    you add the **Date picker** control, the **DefaultDate** is set to
    **Today().**

1. Select the **Properties** drop-down menu, for the **Date picker** control.

1. From the drop-down, select **Format**. By default, the **Format**
    property is set to **DateTimeFormat.ShortDate**.

1. Update the Format property to be **DateTimeFormat.LongDate**. This
    will change the display from the format of 6/30/2020 to Sunday, June
    30, 2020.

Another common request is to change the date format property from the
format of month/day/year to day/month/year. This can be accomplished by
manually setting the **Format** property of the control to "dd/mm/yyyy".
For more information about how to format the Text function, see
[Power Apps Text function](/power-apps/maker/canvas-apps/functions/function-text/?azure-portal=true).
