In the previous section, you learned how to implement the Navigate and Back functions using a Control. When employing these functions, like any other function in Power Apps, we need to define certain arguments.

Navigate function
---------------------

Here's a breakdown of the Navigate syntax:

**Navigate**(*Screen* [, *Transition* [, *UpdateContextRecord* ]])

- **Screen** - Required. The screen to display.

- **ScreenTransition** - Optional. The visual transition to use
    between the current screen and the next screen. The default value is **None**.

- **UpdateContextRecord** - Optional. A record that contains the
    name of at least one column and a value for each column. This record
    updates the context variables of the new screen as if passed by the  [UpdateContext](/power-apps/maker/canvas-apps/functions/function-updatecontext/?azure-portal=true) function.

In the first argument, you specify the name of the screen to navigate to. In
the second argument, you specify how the old screen visually changes to the new
screen. In the third argument, you can specify a Context
variable.

Let's take a closer look at the second argument, ScreenTransition.
Below is a list with descriptions of the different ScreenTransitions you could apply. Each ScreenTransition produces a slightly different visual experience for the user, and the transitions all occur in a split second.

Screen transitions
------------------

**ScreenTransition.Cover** - The new screen slides into view from right to
    left, covering the current screen.

**ScreenTransition.CoverRight** - The new screen slides into view from left to
    right, covering the current screen.

**ScreenTransition.Fade** - The current screen fades away to reveal the new
    screen.

**ScreenTransition.None** - (Default) - The new screen quickly replaces the
    old screen.

**ScreenTransition.UnCover** - The current screen slides out of view from
    right to left, uncovering the new screen.

**ScreenTransition.UnCoverRight** - The current screen slides out of view from
    left to right, uncovering the new screen.

Examples
--------

| **Formula**  | **Description**  | **Result**    |
| :------------------- | :------------------- |:----------------|
| **Navigate(Details)**   | Displays the **Details** screen with no transition or change in value for a context variable. | The **Details** screen appears quickly. |
|  **Navigate(Details, ScreenTransition.Fade)**                  | Displays the **Details** screen with a **Fade** transition. No value of a context variable is changed.                  | The current screen fades away to show the **Details** screen.           |
|  **Navigate(Details, ScreenTransition.Fade, {ID: 12})**                   | Displays the **Details** screen with a **Fade** transition and updates the value of the **ID** context variable to **12**.                 | The current screen fades away to show the **Details** screen, and the context variable **ID** on the screen is set to **12**.           |
|  **Navigate( Details, ScreenTransition.Fade, { ID: 12 , Shade: Color.Red } )** | Displays the **Details** screen with a **Fade** transition. Updates the value of the **ID** context variable to 12 and updates the value of the **Shade** context variable to **Color.Red.** | The current screen fades away to show the **Details** screen. The context variable **ID** on the **Details** screen is set to **12**, and the context variable **Shade** is set to **Color.Red**. If you set the **Fill** property of a control on the **Details** screen to **Shade**, that control would display as red. |

Back function
--------------------

The **Back** function returns to the screen that was most recently displayed. As the user navigates to other screens, the app tracks the path of the screens and the transition used. So, when the **Back** function runs, the inverse screen transition runs as well. Using **Back**, your user can return all the way to the screen that appeared when they started using the app.

Though **Back** normally returns **true**, if the user hasn't navigated to another screen since using the app, then invoking **Back** will return a **false** value and the user will stay on the current screen.

The **Back** function also has an optional argument for ScreenTransition.

Examples
----------

| **Formula**   | **Description**   | **Result**    |
| :------------------- | :------------------- |:----------------|
|**Back()**| Displays the previous screen with the default return transition. | Displays the previous screen through the inverse transition of the transition through which the current screen appeared.|
|**Back( ScreenTransition.Cover )** | Displays the previous screen with the **Cover** transition. | Displays the previous screen through the **Cover** transition, regardless of the transition through which the current screen appeared.|

Summary
--------

The Navigate and Back functions are customizable by taking advantage of their parameters. It's possible to simply switch to another screen with the Navigate function, but it's also possible to add a visual transition and even set context variables in the process. The Back function provides either the inverse of any transition that got your user to the current screen, or you can define a transition. It's up to you to determine the user experience!
