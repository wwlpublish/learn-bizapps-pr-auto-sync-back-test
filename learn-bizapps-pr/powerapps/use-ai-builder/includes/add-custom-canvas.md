AI Builder custom model components can provide a rich user experience in your applications. The referenced model must be published before it can be used in a canvas app. For this unit, you learn about *object detection*, which allows the reader to detect recognizable objects in an image and use this information in the app.

## Add the object detector

The object detector is the AI Builder component that allows use of the object detection custom model in a canvas screen. Follow these steps:

1. In the top menu for a selected screen in the canvas app studio, select the **Insert** tab.

1. In the **AI Builder** group, select **Object detector**.

> [!div class="mx-imgBorder"]
> [![Screenshot of Power Apps with the Insert tab selected and A I Builder dropped down to show Object detector.](../media/object-detector.png)](../media/object-detector.png#lightbox)

## Configure the object detector

After you select the object detector you want to add to the screen, the following component properties are available to capture the results of the reader:

- **GroupedResults**: list of distinct recognized images with a count. This can help with inventory management.

- **Results**: list of all recognized images with a confidence score. This can help determine which of the images are considered valid (if confidence level is at a level determined as valid for the business scenario).

In the following video, you walk through the configuration steps by using two galleries to display the properties you use when you process an image with the object detector.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/]
