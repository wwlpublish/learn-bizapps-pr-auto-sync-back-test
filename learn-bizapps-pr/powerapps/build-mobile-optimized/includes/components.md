In this lesson, we'll look at the specific components within a Power Apps app that can be used to make a responsive app.

- Canvas app creation

- Application display settings

- New screen form additions

- Control and form additions

- Offline capabilities

- Notifications to a Power Apps app when there's no connectivity

## Canvas app creation

When creating a canvas app, the Power Apps designer contains the option to create a blank app or app from a template in a Phone Layout or Tablet Layout.

Both layouts can be used on a mobile phone or tablet but will have different experiences. For example, when creating a phone layout, the application will assume a vertical orientation and include up and down scrolling by the user in a narrow window. In tablet mode, the layout on that same phone will assume the phone will operate in a landscape mode and be held horizontally by default. The best application will vary by use case.

> [!div class="mx-imgBorder"]
> [![Screenshot of the Power Apps canvas page displaying the ability to create a blank Power Apps app or with a template for Phone or Tablet layouts.](../media/layout.png)](../media/layout.png#lightbox)

## Application display settings

Within the canvas app, a user can navigate to **Settings > Display** and view several important application display settings.

- Orientation

    -   The orientation of the application will be the default presentation layout of your app. It can either be in the longer portrait orientation or the wider landscape orientation.

- Scale to fit

    -   For a responsive design, the recommendation is to set this option to **No**. It's set to **Yes** by default.

- Lock aspect ratio

	- This option is enabled only if the **Scale to fit** option is set to **Yes**.

	- If this option is set to **No**, the designer is no longer designing a canvas app for a specific screen dimension.

- Lock orientation

	- If this option is set to **Yes**, the setting in Orientation is locked. For example, if an application is in portrait mode and Lock Orientation is **Yes**, the canvas app will never allow the user to enter a landscape orientation by the user.

	- If this option is set to **No**, the mobile app will allow the user to switch the application between landscape and portrait by moving the mobile device's orientation.

> [!div class="mx-imgBorder"]
> [![Screenshot of the Display settings for a canvas application, specifically the orientation, Scale to fit, Lock aspect ratio, and Lock orientation fields.](../media/settings.png)](../media/settings.png#lightbox)

## Create new responsive forms

When you create a new screen or form within a Power Apps app, there are several predefined responsive layouts for a phone or tablet that adhere to a responsive design by default. The following image displays the responsive layouts for a phone.

> [!div class="mx-imgBorder"]
> [![Screenshot showing the different screen layouts that are mobile-optimized.](../media/mobile-layout.png)](../media/mobile-layout.png#lightbox)

In the event one of the responsive layouts won't meet the business requirements, you can create your own responsive layout by using formulas and conditions. For more information about creating your own responsive layout, see the following documentation: [Create responsive layouts](/power-apps/maker/canvas-apps/create-responsive-layout/?azure-portal=true)

## Control and form design considerations

Buttons should be easy for users to locate and select. Consider placing them at the top or bottom of a form that spans the application from edge to edge. If it's an action such as a delete action, place the button to the side of the record where users are likely to be holding the device (right hand or left hand).

> [!div class="mx-imgBorder"]
> [![Screenshot of a canvas app that has buttons and icons displayed in a mobile-optimized design.](../media/button-positionpng)](../media/button-position.png#lightbox)

When you include fields on a form, add enough of a spacing buffer between fields and the edge of the phone to be forgiving of inaccurate screen touch selections. Users will likely inconsistently touch directly in the middle of a field and the experience shouldn't accidentally move the focus to another unintentional field. Buffers between the edge of a field and the edge of the form will help users avoid accidentally triggering phone swipe actions such as navigating back to a previous form by accident. If there are mandatory fields, try to prioritize those as the first fields.

> [!div class="mx-imgBorder"]
> [![Screenshot of a canvas app with fields that are organized by importance with a buffer between the edges of the field and the edge of the canvas app.](../media/field-considerations.png)](../media/field-considerations.png#lightbox)

Grids with data should span from edge to edge of the form and only scroll in one direction, vertically or horizontally. If other fields on a form are needed, include those below the primary field of the record, not in other columns to the right or left of the record. When you use multiple forms, scrolling should be a uniform experience across the application unless it really isn't possible.

> [!div class="mx-imgBorder"]
> [![Screenshot of a canvas app that has a horizontal scrolling grid that is mobile-optimized.](../media/scroll-position.png)](../media/scroll-position.png#lightbox)

## Containers

For more complex layouts, such as a mobile tablet that has more than one component on a screen but need a responsive design, containers should be used. In Unit 4, you'll see how containers can be used to optimize the experience of a canvas app on various mobile devices.

## Add offline capabilities

A user can add offline capabilities to an application for business cases where data needs to be used or stored offline until an application reconnects to the internet. The enabling of these capabilities can be complex with many design factors to consider. It's recommended to involve a developer and determine the best approach to implement offline capabilities. For more information about implementing offline capabilities into your power app, see the article [Develop offline-capable canvas apps](/power-apps/maker/canvas-apps/offline-apps/?azure-portal=true).

## Add a notification to a Power App when there's no connectivity

If you wish to alert a user that the canvas app is offline when accessing a specific page or conducting a specific action, the Notify function can be called to alert the user that the function may not be available at the current time. The notification by default will appear for 10 seconds and then disappear, or until the user dismissed the alert manually.

For more information about the notify function, see the article [Notify function in Power Apps](/power-apps/maker/canvas-apps/functions/function-showerror/?azure-portal=true).
