In the previous section, you learned how to implement the Navigate and Back() functions using a Control. When implementing these functions, like any other function in Power Apps, there are certain arguments that need to be defined.

Navigate function
---------------------

Here's a breakdown of the syntax for the navigation function:

**Navigate**(*Screen*, *Transition* [, *UpdateContextRecord* ] )

-   **Screen** - Required. The name of the screen to display.

-   **ScreenTransition** - Required. The visual transition to use
    between the current screen and the next screen. 

-   **UpdateContextRecord** - Optional. A record that contains the
    name of at least one column and a value for each column. This record
    updates the context variables of the new screen. For more information, see
    [UpdateContext function in Power Apps](/power-apps/maker/canvas-apps/functions/function-updatecontext/?azure-portal=true).

In the first argument, you specify the name of the screen to display. In
the second argument, you specify how the old screen changes to the new
screen. In the third argument, you have the option to specify a Context
variable. Looking back to the second argument, ScreenTransition,
there are a number of different ScreenTransitions you could apply. Each
ScreenTransition produces a slightly different visual experience for the
user.

Screen transitions
------------------

 **ScreenTransition.Cover** - The new screen slides into view,
    covering the current screen.

**ScreenTransition.Fade** - The old screen fades away to reveal the
    new screen.

**ScreenTransition.None** - The old screen is quickly replaced with
    the new screen.

**ScreenTransition.UnCover** - The old screen slides out of view,
    uncovering the new screen.

Here are some examples using ScreenTransitions.


| **Formula**                     | **Description**                  | **Result**          |
| :------------------- | :------------------- |:----------------|
| **Navigate(Details, ScreenTransition.None)**   | Displays the **Details** screen with no transition or change in value for a context variable. | The **Details** screen appears quickly. |
|  **Navigate(Details, ScreenTransition.Fade)**                  | Displays the **Details** screen with a **Fade** transition. No value of a context variable is changed.                   | The current screen fades away to show the **Details** screen.            |
|  **Navigate(Details, ScreenTransition.Fade, {ID: 12})**                   | Displays the **Details** screen with a **Fade** transition, and updates the value of the **ID** context variable to **12**.                  | The current screen fades away to show the **Details** screen, and the context variable **ID** on the screen is set to **12**.            |
                                                                                                                                                               
                                            
The **Back ()** function has an optional argument
for ScreenTransition.

Back () function
--------------------

When using the **Back()** function it should be noted, this will take
you back to the previous screen that you navigated from, the key word being
"navigated". To elaborate, this does not mean the screen you or the user
was just on, you need to use the **Navigate** function to navigate
away from the screen to then use the **Back()** function to get back
there. This can be a little confusing, so here's an example of how this works. 

In the previous example, there are three screens. Update the **OnSelect**
property of the Next button on Screen1 from
**Navigate(Screen2,ScreenTransition.Cover)** to
**Navigate(Screen3,ScreenTransition.Cover)** and the **text** property
to **Jump to Screen 3**. Now, when the user selects the button, the app
will navigate to Screen3. Then when they select the Back button on
Screen3, they will navigate back to Screen1 and skip Screen2 entirely.
This is by design in Power Apps and is an important concept to ensure the navigation in your app is configured properly.

Before moving on to the next section, add one more screen to the example
app and rename the screen **Documentation**. With no Navigation pointing to this screen, it is not accessible to your end users. The purpose of this screen is to give the App creator a location in the app to make notes or add documentation about certain aspects of how the app functions. The App creator can also provide instructions for other editors of the app so they can quickly and easily identify what the previous creator did.

In this simple four screen app example, you can see how easy it is to
navigate screens by setting the **OnSelect** property of a control.
There are several additional ways to navigate through your app covered
in the next section.
