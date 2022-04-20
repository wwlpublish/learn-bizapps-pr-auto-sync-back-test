In Power Apps like Excel, you can create formulas to calculate and
return values. The following are a few common functions that you can use when working with
numbers and calculating values:

-   **Average** - Calculates the average, or arithmetic mean, of its
    arguments.

-   **Max** - Finds the maximum value.

-   **Min** - Finds the minimum value.

-   **Sum** - Calculates the sum of its arguments.

-   **StdevP** - Calculates the standard deviation of its arguments.

-   **VarP** - Calculates the variance of its arguments.

You can incorporate controls into your calculations by referencing
the function name.

The following example shows how to calculate the sum of goods and services.

> [!NOTE]
   > If your formula returns an error, then please note that the language setting of your Power Apps environment can affect some separators and operators. For example, the above formula is expressed in a language and region that uses dot or period as the decimal separator, such as Japan or the United Kingdom. However, this same formula in a language and region where a comma is used for the decimal separator, such as France or Spain, the formula will need to be: `Text(ThisItem.Price; "$ ##,00")`
   > 
   > The property selection operator . (dot or period) in ThisItem.Price is always the same, no matter what the decimal separator is, but notice that the decimal separator and the chaining operation separator changed to a comma and semicolon respectively. Internally the formula doesn't change, all that changes is how it's displayed and edited by the author. See [Formula separators and chaining operator](/power-apps/maker/canvas-apps/global-apps?azure-portal=true#formula-separators-and-chaining-operator) for more information.

1. Navigate to [Power Apps](https://make.powerapps.com/).

1. Select **+ New App** and **Canvas**.

1. At the bottom, under **Blank app**, select **Tablet layout**.

1. Select the **Insert** tab and add a **Label**.

1. Change the **Text** property to *Product*.

1. Add three more **Labels** and change the **Text** properties to *Quantity*, *Cost*, and *Total*, respectively.

1. Select the **Insert** tab, then the **Text** dropdown, and insert three **Text Inputs** to your canvas app,
   and arrange them as shown in the following screenshot.

   ![Screenshot of Power Apps Treeview Screen1 text inputs.](../media/calculation-update.png)

1. Insert another **Label** to the right of *Total*. Name it **Label6**.

1. Change the **Text** property to the following.

   ```powerappsfl
   Sum(TextInput2 * TextInput3)
   ```

   (In this example, TextInput2 is the Quantity purchased and TextInput3 is the Cost per item.)

1. Now preview the app by selecting the **Play** button in the
   upper-right corner. Test the formula by entering some numbers for the quantity and price.

1. Next, format the formula to display the value as a Currency. Update
   the formula as follows.
   ```powerappsfl
   Text(Sum(TextInput2 * TextInput3),"$#,###0.00")
   ```
   
   ![Screenshot of Power Apps Treeview Screen1 values.](../media/calculation-update-2.png)

For more information, see [Power Apps Aggregate Functions](/power-apps/maker/canvas-apps/functions/function-aggregates/?azure-portal=true).
