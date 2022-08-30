Another way to make your App more dynamic and intuitive to the user is
to use functions including **IsBlank**, **IsBlankOrError**, **IsEmpty**, **IsNumeric**, **IsToday**, and **IsMatch**. These functions allow for validation of thecondition of a field, control, variable, or table. All these functions return boolean *true* or *false* based on the results of their evaluation. This can allow for the creation of solutions where you don't allow the user to submit a form if a field is blank or if the field's data doesn't match the evaluation. The following is an overview of some of these functions.

-   **IsBlank** -- This function checks a field, property, or variable
    to see if the result is *blank* or an empty string. The return value for **IsBlank** is a boolean *true* or *false*.

-   **IsBlankOrError** -- This function checks whether an expression is blank or results in an error, and returns *true* or *false*.

-   **IsEmpty** -- This function checks a table of data to see if it
    contains any records. If the table is empty, then the function returns
    *true*.

-   **IsMatch** -- This function checks a text string to determine if the      result matches the specified pattern. If the pattern is a match the function returns *true*. For details about the various matching patterns, see    [IsMatch function in Power Apps](/power-apps/maker/canvas-apps/functions/function-ismatch/?azure-portal=true).

-   **IsNumeric** -- This function checks a field, property, or variable
    to determine if the value is numeric. If the object is numeric, then the
    function returns *true*.

-   **IsToday** -- This function checks if a date or time value is
    between midnight today and midnight tomorrow. If the date or time
    value is within that range, the function returns *true*.

You can test this functionality by using the following example to disable a button if the **Text Input** control is not a valid email address.

1.  Add a **Text Input** control to your canvas. Make the **Default** property blank by deleting *"Text Input"*.

2.  Add a **Button** control to the canvas.

3.  Modify the **DisplayMode** property of the **Button** control to the
    following formula. (Make sure you rename the control to reference the text input control you just added if it is not *TextInput4.Text*.)
    ```powerappsfl
    If(IsMatch(TextInput4.Text, Email), DisplayMode.Edit,DisplayMode.Disabled)
    ```

4.  Preview the app by selecting the **Play** button in the upper-right corner.

5.  If the field is blank or has an incomplete email address, the button
    will be disabled and display in a grey color. When you enter a valid
    formatted email address, the button will turn to blue and become clickable.

The data validating functions are very helpful tools for shaping the data entered by your users. Employing them can help eliminate data-entry errors and further enhance the user experience.
