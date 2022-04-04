You'll now explore the **Capture report views** showcase. This showcase demonstrates using the client APIs to apply and create bookmarks.

In the playground menu, select the **Capture report views** showcase.

> [!div class="mx-imgBorder"]
> ![Image shows the Capture report views showcase highlighted.](../media/playground-capture-report-views-showcase.png)

In the embedded Power BI report, at the top left, select the **Saved views** button.

> [!div class="mx-imgBorder"]
> ![Image highlights the Saved views button.](../media/playground-capture-report-views-saved-views-button.png)

Notice the list of *views*, which are really bookmarks. The `bookmarksManager.getBookmarks` function retrieved the report's bookmark collection.

Select any bookmark to apply it to the report, and notice that the page updates with new state. The `bookmarksManager.apply` function applied the bookmark to the report.

In the **Manufacturer** slicer, select the first manufacture, **Abbas**.

> [!div class="mx-imgBorder"]
> ![Image shows the Manufacturer slicer with Abbas selected.](../media/playground-capture-report-views-set-manufacturer-slicer.png)

Select the **Capture view** button.

> [!div class="mx-imgBorder"]
> ![Image highlights the Capture view button.](../media/playground-capture-report-views-capture-view-button.png)

In the dialog window, beneath **Enter a name for this view**, enter **Abbas**.

> [!div class="mx-imgBorder"]
> ![Image shows the name Abbas entered.](../media/playground-capture-report-views-capture-view-enter-name.png)

Select **Save**. The `bookmarksManager.capture` function created a personal bookmark.

Return to the saved views, and notice that the Abbas bookmark appears at the bottom of the list.

> [!div class="mx-imgBorder"]
> ![Image highlights the Abbas bookmark in the save views list.](../media/playground-capture-report-views-saved-views-abbas.png)

For a more detailed explanation, including access to the code, see [Capture report views showcase](/javascript/api/overview/powerbi/showcase-bookmarks/?azure-portal=true).
