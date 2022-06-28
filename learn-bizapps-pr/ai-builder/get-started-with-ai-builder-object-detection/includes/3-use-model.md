Learn how to use your Object detection model in Power Apps.

### Quick test

After your model has completed training, you can view important details about your newly trained model on a details page.

To see your model in action, select **Quick test**.

Drag and drop or upload an image from your device to test. If
using sample data, you can go to the **AIBuilder\_Lab\\Lab
Images\\ObjectDetection\_Green Tea\\Test** folder for a test image.

You will now be able to view the detected objects that you chose and the associated confidence scores.

### Publish your model

Your model can't be used until you publish it. If you're satisfied with your model, select **Publish** to make it available for use.

### Use your model in Power Apps

Now that your model is published, you can use your Object detection model in a canvas app. A special component is available for you to add that analyzes any image and detects objects based on your trained object detection model.

1. Select **Use model**.

2. Select **Build intelligent apps** to begin the canvas app creation experience.

3. Within your canvas app, an object detection component is automatically added and linked to your published Object detection model.
Going forward, you can select **Insert > AI Builder** to view the list of AI Builder components and then select **Object detector** to add an object detector component. Make sure that you select the correct model; only published models will appear in the drop-down list.

    ![Power Apps Screen1 contains an object detector component.](../media/build-intelligent-apps.jpg)

4. Select **Insert** and then add a **Data table** component.

5. To bind the **Object detector** component to one of the data tables, select the **Data table component** and replace the formula bar value with **ObjectDetector1.GroupedResults**.

    ![Power Apps Screen1 has a Data Table component below the object detector. The table shows three types of green tea.](../media/bind-object-detector.jpg)

    This action will auto populate the data table with the list of objects that the model can recognize and their count in the image.

6. Select **Play** in the upper right of the Power Apps studio to preview the app.

7. Select **Detect** and then select the image that you used to quick test previously.

A preview of your image shows the recognized objects and updates the counts accordingly.
