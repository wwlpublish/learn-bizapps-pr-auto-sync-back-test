As previously mentioned, one of the most common ways to move from screen to screen is by setting the OnSelect property of a control. There are also several other ways to trigger the Navigate or Back functions.

Navigating screens by setting the OnChange property of a drop-down control
-------------------------------------------------------------------------

One option is to use a **DropDown** control and an If statement.
With this solution, depending on the choice selected in the drop-down menu, the
app navigates to a specific screen. If you would like to try this now, you can follow along with the example below.

1. Start an app in Power Apps Studio and add two blank screens. There should be a total of three blank screens.

1. On Screen1, add a **Dropdown** control.

1. Set the **Items** property for the **Dropdown** control to

    ```
    [" ", "Active","Inactive"]
    ```

1. Set the **OnChange** property for the **Dropdown** control to the following

    ```
    If(Dropdown1.Selected.Value ="Active",Navigate(Screen2,ScreenTransition.Cover),
    If(Dropdown1.Selected.Value = "Inactive",Navigate(Screen3,ScreenTransition.Fade)))
    ```

On your keyboard, hold the Alt key (or enter app *Play* mode) to test the new functionality.
When you select **Active** from the drop-down menu, the app should navigate
to Screen2. Likewise, if you select **Inactive** from the same drop-down menu, the app navigates to Screen3. Finally, if you select the blank (" ") option, the app shouldn't navigate to another screen.

Using variables and the Timer control to navigate screens
---------------------------------------------------------

You can also use a variable and an If statement to set navigation. Depending
on what the app sets the variable value as sends the user to a specific screen. For example, if you have the question "Do you have additional feedback to provide regarding this incident?" If the user selects "Yes", then you
want to send the user to the **Additional Information** screen. If the user selects, "No", then you want to navigate to the **Form Completed** screen.

Another option is to use a timer control. When the time runs out, the
app navigates to a different screen. For example, maybe you only want to
allow a users 30 seconds to answer the questions on a screen before
navigating to the next set of questions.

The following example builds off the previous example and incorporates variables and a Timer control.

1. On Screen1, add a **Timer** control.

1. Set the **Duration** property to 10000 (in milliseconds)

1. Set the **Auto start** to **On**.

1. Set the **OnTimerEnd** property to

    ```
    If(Dropdown1.Selected.Value = " ",Navigate(Screen2))
    ```

1. Select the drop-down control and change the **OnChange** property to

    ```
    If(Dropdown1.Selected.Value =
    "Active",Set(varStatus,1),If(Dropdown1.Selected.Value =
    "Inactive",Set(varStatus,2),Set(varStatus,0)))
    ```

1. Add a **Button** control under the drop-down menu, and set the **Text**
    property to "Next".

1. Set the **OnSelect** property for the "Next" button to

    ```
    If(varStatus = 1,Navigate(Screen2,ScreenTransition.Cover),
    If(varStatus = 2,Navigate(Screen3,ScreenTransition.Fade)))
    ```

There are now two ways to navigate to other screens from Screen1. Put your app in play mode to test it out. If you select your Timer control to start it and wait for 10 seconds (1 second = 1000 milliseconds) the timer ends, and the app automatically navigates to Screen2. Alternatively, if you select **Active** from the drop-down menu, your variable named varStatus is set to 1. Then when you select the "Next" button, you'll land on Screen2. If you select **Inactive** from the same drop-down, varStatus becomes 2, and then pressing the "Next' button navigates you to Screen3.

Documentation Screen
---------------------
Before moving on to the exercise in the next section, let's discuss the Documentation screen. You can do this by adding a screen to your app and rename the screen **Documentation**. With no Navigation pointing to this screen, it isn't accessible to your end-users. The purpose of this screen is to give the App creator or co-editors a location in the app to make notes or add documentation about certain aspects of how the app functions. It can be a place to keep track of settings, such as formatting or colors. Using a Documentation screen is a great technique to provide instructions to other developers of the app.

Summary
---------

There are different and flexible ways to configure navigation in your app. In the first example, the navigation dynamically changed with user input to the drop-down control. In the second example, we used navigation in two different ways: via the timer reaching zero, or by selecting a button. The variable allowed you to control which screen your user navigated to, based on the drop-down value selected, and triggered when the user selected a button control. A Documentation screen in your app that users can't navigate to provides developers a location to add notes on the app. Power Apps provides the flexibility to choose what works best for your solution!
