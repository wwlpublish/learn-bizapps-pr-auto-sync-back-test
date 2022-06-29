When using Microsoft Power Apps, you don't have to write complicated application code the way that a traditional developer does. However, you must express logic in an app and control its navigation, filtering, sorting, and other functionalities. This is where formulas come in.

If you've used Microsoft Excel functions, you should recognize the approach that Power Apps takes. This unit shows a couple of basic formulas for text formatting and then describes three of the formulas that Power Apps includes when it generates an app. With this information, you'll have a better idea of what formulas can do, and then you can also start to write your own.

## Get started with formulas and properties

The previous unit explored controls in all three screens of an app that Power Apps generated. In this section, you’ll use the properties of the label control to format the price in the gallery.

By default, the price appears as a plain number without a currency symbol. Suppose that you want to add a dollar sign and change the text color based on the item's cost (for example, red if it's more than $5 but green otherwise). The following graphic shows the expected result.

![Screenshot of text formatting for color and currency in gallery.](../media/conditional-format.png)

By default, Power Apps pulls in a price value for each item. This value is set as the **Text** property of the label that shows the price.

> [!NOTE]
> Be sure to complete the steps in unit 1 of this module as the description field is changed to price as reflected in the next steps.

1. In **BrowseScreen1**, select the price of the first item.

   ![Screenshot of select price of the first item in browse screen.](../media/select-price.png)

1. In the drop-down list of properties, select **Text**.

1. To add the currency symbol for US dollars, set the **Text** property to this formula:

   ```powerappsfl
   Text(ThisItem.Price, "$ ##.00")
   ```

> [!NOTE]
   > If your formula returns an error, then please note that the language setting of your Power Apps environment can affect some separators and operators. For example, the above formula is expressed in a language and region that uses dot or period as the decimal separator, such as Japan or the United Kingdom. However, this same formula in a language and region where a comma is used for the decimal separator, such as France or Spain, the formula will need to be: `Text(ThisItem.Price; "$ ##,00")`
   > 
   > The property selection operator . (dot or period) in ThisItem.Price is always the same, no matter what the decimal separator is, but notice that the decimal separator and the chaining operation separator changed to a comma and semicolon respectively. Internally the formula doesn't change, all that changes is how it's displayed and edited by the author. See [Formula separators and chaining operator](/power-apps/maker/canvas-apps/global-apps?azure-portal=true#formula-separators-and-chaining-operator) for more information.

The **Text** function specifies how to format the number. The formula is like an Excel function, but Power Apps formulas refer to controls and other app elements instead of cells in a workbook.

If you select a control and then open the property drop-down list, a list of properties that are relevant to the control appears. For example, the following is a partial list of the properties for a **Label** control. Some properties are relevant across a wide range of controls, but others are relevant only for a specific control.

![Screenshot of setting properties fpr the drop-down list.](../media/powerapps-formulas4.png)

To conditionally format the price's color, select the price **Label** and choose the **Color** property and set it to this formula: 

```powerappsfl
If(ThisItem.Price > 5, Color.Red, Color.Green)
```

![Screenshot of the formula for the color property screen.](../media/power-apps-color.png)

## Formulas included in the generated app

Power Apps uses a couple of formulas in every app that it generates. Both examples are from the browse screen and work with the **OnSelect** property. This property defines what happens when a user selects a control.

* The first formula is associated with the **IconNewItem1** control ![New item icon](../media/powerapps-icon-add-item.png). Select this control to open the edit/create screen where you can create an item. To view the formula, select the ![New item icon](../media/powerapps-icon-add-item.png) and then select it in the formula bar. The formula is as follows:

  ```powerappsfl
  NewForm(EditForm1);Navigate(EditScreen1, ScreenTransition.None)
  ```

  The formula instantiates an edit page on the edit/create screen so that users can create an item. A value of `ScreenTransition.None` means that there's no transition, such as a fade, between screens.

* The second formula is associated with the **IconSortUpDown1** control ![Screenshot of the formula for the sort gallery icon items.](../media/powerapps-icon-sort.png). Select this control to sort the items in the gallery. The formula is as follows:

  ```powerappsfl
  UpdateContext({SortDescending1: !SortDescending1})
  ```

  The formula uses `UpdateContext` to update a variable called `SortDescending1`. The exclamation "!" symbol in the formula is a shortcut for the Not function. The value of the variable switches back and forth as you select the control. This variable tells the gallery on this screen how to sort the items.

The app contains many other formulas, so take some time to select controls and determine what formulas are set for various properties.

For more information about these and other functions, refer to [formula reference for Power Apps](/power-apps/maker/canvas-apps/formula-reference/?azure-portal=true) page.

For additional information on customizing a canvas app, refer to the Use the UI and controls in a canvas app in Power Apps learning path and the Use basic formulas to make a better canvas app in Power Apps learning path.
