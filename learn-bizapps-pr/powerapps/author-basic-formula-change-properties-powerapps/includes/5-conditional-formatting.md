Applying conditional formatting to your app is a great way to enhance
the look and feel as well as user experience. Remember, each control
has slightly different properties, which means that the conditional formatting
for one control might not be the same for another. Examples of how you
can use conditional formatting include setting the **Visible** property of
an **Image** control to hide it when certain users are signed in or to
change the **DisplayMode** of a button to **Disabled** until all of the
fields in a **Form** control have data entered in them. Conditional
formatting can greatly enhance the user experience with visual
indicators and modified functionality based on the condition.

Continuing with the previous example, the following formula shows how to apply
conditional formatting to the **Label6 Color** property.

```powerappsfl
If(Sum(Value(TextInput2.Text),Value(TextInput3.Text)) >50,Color.DarkGreen,Color.DarkRed)
```

The **Color** property defines the color of the text in the **Label**
control. For this example, if the sum of the two **TextInput** controls
is greater than 50, then the color will be DarkGreen, if not then the
color will be DarkRed.

When setting the Color property in Power Apps, there are a few options.
You can provide a color object, as shown in the example, by using
Color.Orange or any of the predefined colors in Power Apps. There is also
a ColorValue and an RGBA function available. For more information, see
[Power Apps Color enumeration and functions](/power-apps/maker/canvas-apps/functions/function-colors/?azure-portal=true).

Another concept that can be applied is to reference the **Text**
property to determine the **Color** property. If your app needs to always show PASS in DarkGreen and FAIL in DarkRed, then you can use the
following logic. Instead of repeating the same **If** logic in both
properties you can reference one property in another. Try replacing the
formula in the **Color** property.

```
If(Label6.Text = "PASS", Color.DarkGreen,Color.DarkRed)
```

This will get you the same result as before but now if you change your
criteria for determining pass or fail you can update the logic in the
Text property and the Color property will not need to be updated.

This was a simple example, but it demonstrates how you can quickly
add conditional formatting to your canvas app to enhance the experience.
Try to incorporate conditional formatting in your app, when possible, to
enhance user experience and functionality.
