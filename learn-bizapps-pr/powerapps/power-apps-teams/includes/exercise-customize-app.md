Now that the data model has been created in Dataverse, you can customize the app that employees will use to submit their swag asset requests. Customizing the app in this exercise will involve editing the fields available on the asset request submission form, and changing formatting, such as colors and font.

## Task: Edit the app form 

1.  Select the save icon to save your app.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of save app button.](../media/save.png)](../media/save.png#lightbox)

1.  From your app canvas, select the **Tree view** icon on the left side of the screen. Within the tree view underneath RightContainer1, select **EditForm1**, and select **Edit fields**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the edit form fields button.](../media/edit-fields.png)](../media/edit-fields.png#lightbox)

1.  Select **+ Add field** and add the **Asset** and **Asset Category** fields.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the add field with asset and asset category.](../media/add-field.png)](../media/add-field.png#lightbox)

1. Select the **Edit fields** button located in the **Properties** pane.

	> [!div class="mx-imgBorder"]
	> [![Screenshot showing the edit fields button.](../media/properties-edit-fields.png)](../media/properties-edit-fields.png#lightbox)

1. Select and drag each field from the area shown below to rearrange the order. The order should appear as shown below. If you're missing any of the fields, you can add them in.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the field order.](../media/field-order.png)](../media/field-order.png#lightbox)

1. Select on the **Approval status** field to expand it. Set the Control type to **View option set single-select**. You can then close the Fields menu.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the control type set as view option set single select.](../media/control-type.png)](../media/control-type.png#lightbox)

1. With EditForm1 selected, change the column value to **1** as shown below.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the column value set to one.](../media/column-value.png)](../media/column-value.png#lightbox)

1. **Save** your app.

## Task: Import data

1.  With your app saved, select on the **Build** tab.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the build tab.](../media/build.png)](../media/build.png#lightbox)

1.  Select the **Asset** table.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the asset table selected.](../media/asset.png)](../media/asset.png#lightbox)

1.  Select **Import** > **Import Data**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the import data option selected.](../media/import-data.png)](../media/import-data.png#lightbox)

1.  Select the **Excel workbook** option.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the Excel workbook option selected.](../media/excel-workbook.png)](../media/excel-workbook.png#lightbox)

1.  Select the **Upload file** option. Select **Browse**, and navigate to the Excel **Contoso Coffee Asset List.xlsx** file found in your lab documents. Check that the **Authentication kind** is set to **Organizational** account, and select **Sign in**.

    *If you get an error when trying to upload the file, refresh the page and try again.*

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the sign in button.](../media/sign-in.png)](../media/sign-in.png#lightbox)

    In the pop-up, confirm your account to sign in.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the select account window.](../media/account.png)](../media/account.png#lightbox)

1.  Select **Next**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the connect data source details.](../media/connect-data-source.png)](../media/connect-data-source.png#lightbox)

1.  Tick the checkbox next to **Sheet1** and select **Next**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of Power Query.](../media/power-query.png)](../media/power-query.png#lightbox)

1.  In the **Price** column header, select the 123 icon and change it to **Currency**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of price column changed to currency.](../media/currency.png)](../media/currency.png#lightbox)

1.  When asked to confirm the change, select **Replace current**.

1. Select **Next**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the next button.](../media/next-button.png)](../media/next-button.png#lightbox)

1. In the Load Settings, select **Load to existing table**. You'll need to select your **Asset** table as the destination table. Your table will look something like crf7d_Asset. However, it likely won't be exactly the same as the example shown here, your prefix may be different.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of load to existing table selected.](../media/load-existing-table.png)](../media/load-existing-table.png#lightbox)

1. Map the source column to the destination column as shown below then select **Publish**.

	|     Source column    |     Destination column    |
	|----------------------|---------------------------|
	|     Image            |     Image                 |
	|     Asset Name       |     Name                  |
	|     Price            |     Price                 |

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the publish button.](../media/publish.png)](../media/publish.png#lightbox)

1. Wait approximately 2 minutes, then refresh your browser. Navigate back to the Asset table in the Build tab, and you should see your list of assets populated.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the asset table on the build tab.](../media/build-asset-table.png)](../media/build-asset-table.png#lightbox)

1. Select **Edit**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the edit button.](../media/edit.png)](../media/edit.png#lightbox)

1. Select the **+more** button to show the other columns. The other columns you should show are Category, Image and Price.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the existing columns.](../media/existing-columns.png)](../media/existing-columns.png#lightbox)

1. You'll need to populate the category column. Select the correct category for each of the assets.

	|     Asset Name                             |     Category     |
	|--------------------------------------------|------------------|
	|     Cappuccino Cup w/ Saucer               |     Accessory    |
	|     Contoso Logo Beanie                    |     Apparel      |
	|     Contoso Logo Cap                       |     Apparel      |
	|     Hope is brewing Long Sleeve (heart)    |     Apparel      |
	|     Hope is brewing Long Sleeve (logo)     |     Apparel      |
	|     Hope is brewing T-Shirt (heart)        |     Apparel      |
	|     Hope is brewing T-Shirt (logo)         |     Apparel      |
	|     Latte Glass                            |     Accessory    |
	|     Travel Mug                             |     Accessory    |

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the category list.](../media/category-list.png)](../media/category-list.png#lightbox)

1. Select the **Build** tab and select your **Swag Request App**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the swag request app on the build tab.](../media/swag-request-app-build.png)](../media/swag-request-app-build.png#lightbox)

## Task: Configure app form

1.  In our form, we would like the Asset field to be filtered based on the selected Asset Category. On your canvas, select the **Asset** field, and then select again just under the label to select the **DataCardValue**.
    
    You've selected the right spot when you see the panel on the right display a COMBO BOX for DataCardValueX (you might have a different number, if you added the columns to the form in a different order, that's fine).

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the modify properties on Data Card Value.](../media/data-card-value.png)](../media/data-card-value.png#lightbox)

1.  Select the Advanced tab and **Unlock to change properties**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the unlock to change properties button.](../media/unlock.png)](../media/unlock.png#lightbox)

1.  Now select back on the **Properties** tab and select **Depends on** ... This allows us to set a formula that will apply a filter to the Asset choices based on the Asset Category chosen.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the properties depends on button.](../media/properties-dependency.png)](../media/properties-dependency.png#lightbox)

1.  Select the following options:
    
    Make your selections in the bottom half of the form first:

    **Matching field:** **Assets**, **Category**

    Then select values in the top half for Parent control.

    **Parent control:**	**DataCardValue6** (see note below), **Name**

    > [!NOTE]
    > It's important to do the selections in this order - if you select the parent control first, when you select the Asset table in the Matching field, it resets your selections in the top half. If you do it in the wrong order, just change the Parent control back to what it should be so that it matches the screenshot below.
    >
    > You may have a different number for DataCardValue6 if you added your columns in a different order. There are only two options available to select here - in one, the only dropdown in the second option is "Value". Use the one, which allows you to select "Name" in the dropdown list.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the modified properties on Data Card Value.](../media/modify-properties.png)](../media/modify-properties.png#lightbox)

1.  Then select **Apply**.

    You'll see a formula in the formula bar, and you'll also get a warning icon on your canvas and an error flag on your app checker. We need to manually add one more thing (which couldn't be chosen from the Depends on selections) to the formula to correct this

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the warning icon.](../media/warning.png)](../media/warning.png#lightbox)

1.  Edit the formula. Select at the end of the word Category, type a dot (period/full stop) and type the letter **N**. Select Name from the list of options that appears.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of name selected from list of options.](../media/name.png)](../media/name.png#lightbox)

Your final formula will look like this, and the error and warning messages will be cleared.

	`Filter(Assets, Category.Name = DataCardValue6.Selected.Name)`

> [!div class="mx-imgBorder"]
> [![Screenshot of the final formula.](../media/final-formula.png)](../media/final-formula.png#lightbox)

### Locale differences

If your computer has its regional settings set to use the comma ',' for its decimal separator (like in much of Europe) your formulas will use a semicolon ';' instead of a comma. Your formula will appear as shown below instead. If you are in the en-us locale, you can ignore this.

`Filter(Assets; Category.Name = DataCardValue6.Selected.Name)`

1.  **Save** then select to **preview** the app.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the save and preview buttons.](../media/save-preview.png)](../media/save-preview.png#lightbox)

1.  When you preview the app for the first time, there's no data in the requests table, so you'll get this blank "No item to display" message.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the preview app.](../media/preview.png)](../media/preview.png#lightbox)

1.  While in preview mode, select the **+New record** button, enter request details, and select the checkmark to submit your request. Repeat this so that you have three requests in your app. Your dependant dropdown menus are working (you get different Asset choices based on Asset category chosen) and the Approval Status and Request Number are read only.

	When submitting requests, try to use a variation of options, as this data will be used to build a Power BI report later in another lab in this Learning Path.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of Power App- preview app submitting request.](../media/submit-request.png)](../media/submit-request.png#lightbox)

1.  Once you've submitted at least three requests, close the preview.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of close preview button.](../media/close-preview.png)](../media/close-preview.png#lightbox)

## Task: Add image to the form

1.  Within EditForm1, select **Asset_DataCard1**.

	> [!div class="mx-imgBorder"]
	> [![Screeshot of the asset data card selected.](../media/asset-data-card.png)](../media/asset-data-card.png#lightbox)

1. From the ribbon, select **Insert** > **Media** > **Image**. This will add a blank image inside Asset_DataCard1.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the insert image option.](../media/insert-image.png)](../media/insert-image.png#lightbox)

1. Select **Asset_DataCard1** and drag the bottom border from the canvas to increase the size of the cell, until it appears as shown below.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the resized border.](../media/border-size.png)](../media/border-size.png#lightbox)

1. Select the image that you previously added (**Image2**). Reposition it and resize it so that it appears on your screen as shown below.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of positioning and sizing image.](../media/position-size.png)](../media/position-size.png#lightbox)

1. With Image2 selected, type the following formula into the formula bar. Ensure the dropdown/property next to the formula bar is set to **Image**.

	`DataCardValue5.Selected.Image`

	> [!div class="mx-imgBorder"]
	> [![Screenshot of enter formula in formula bar.](../media/enter-formula.png)](../media/enter-formula.png#lightbox)

	*In the formula, DataCardValue5 refers to the DataCardValue for the Asset field. If your form is in a different order, your number may not be 5.*

1. Select **BrowseGallery1** from under LeftContainer1. When you select the gallery, you'll see a pen icon appears. Select the pen icon.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the pen icon.](../media/pen.png)](../media/pen.png#lightbox)

1. This will select the first cell of the gallery. Select the image (**Image1**) within the cell.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the gallery image.](../media/gallery-image.png)](../media/gallery-image.png#lightbox)

1. With Image1 selected, type the following formula into the formula bar. Ensure the dropdown/property next to the formula bar is set to Image.

	`ThisItem.Asset.Image`

	> [!div class="mx-imgBorder"]
	> [![Screenshot of modify image of Browse Gallery 1.](../media/modify-image.png)](../media/modify-image.png#lightbox)

1. **Save** and **preview** the app. Test it out by creating a new request. As you select an Asset in the form, the image will update. Close the preview when you're done.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of Power App in preview mode.](../media/preview-mode.png)](../media/preview-mode.png#lightbox)

## Task: Configure app design 

When creating an app, you have full control of the design of the screens. In this case, we'll be using colors to match with the overall theme of Microsoft Teams.

1.  From the tree view (menu on the left of the app canvas), select **Screen1**. On the properties pane for Screen1, change the **Fill** to the custom value **E1DFDD** as shown below.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the change color fill icon.](../media/change-color.png)](../media/change-color.png#lightbox)

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the color selection screen.](../media/color-selection.png)](../media/color-selection.png#lightbox)

1.  From the tree view, select **TopBar_RightContainer1**, then select its color property from the properties pane.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the color property.](../media/color-property.png)](../media/color-property.png#lightbox)

1.  Change the color of **TopBar_RightContainer1** to the light purple shown selected below.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the color changed to light purple.](../media/purple.png)](../media/purple.png#lightbox)

1.  From the tree view, expand **LeftContainer1** and select **TopBar_LeftContainer1** and change the color property to match the color shown in step 3 above. Your app should now appear as below.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of modify color to match.](../media/match-color.png)](../media/match-color.png#lightbox)

1.  Expand **TopBar_LeftContainer1** and select **AppNameLabel1**. In the properties pane, set the Text value to **Swag Requests** and change the Font size to **20**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the text value set as swag requests.](../media/swag-requests.png)](../media/swag-requests.png#lightbox)

1.  Select **LeftControlContainer1**. Change the color property to the purple as shown below.

	> [!div class="mx-imgBorder"]
	> [![Screenshot ofAppNameLabel1 color changed to purple.](../media/purple-color-property.png)](../media/purple-color-property.png#lightbox)

1.  Expand **LeftControlContainer1** and then expand the **IconButton_Add1.** Select the **IconButton_Add_Label1.** Change the Text property to **New request** and set the font size as **14**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of modify IconButton_Add_Label1 properties.](../media/icon-button-modify-properties.png)](../media/icon-button-modify-properties.png#lightbox)

1.  Change the text color of **IconButton_Add_Label1** to white.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the text color changed to white.](../media/white-text.png)](../media/white-text.png#lightbox)

1.  Select **BrowseGallery1**. Within the gallery, select the first text box that appears with the title. Go to the formula bar and change the **FontSize** to **12**. You can drag the textbox to readjust the size so that the text is displayed in full.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the text box font size adjusted.](../media/text-font-size.png)](../media/text-font-size.png#lightbox)

1. Select the **Subtitle1** field, that is, the other text label, within the gallery. Change the **FontSize** property to **10**.

1. In the formula bar at the top of the screen, change the property dropdown to **Text**, and type in the following formula.

	`ThisItem.'Created By'.'Full Name'& " - "& ThisItem.'Created On'`

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the formula added.](../media/formula-added.png)](../media/formula-added.png#lightbox)

1.  From the tree view, select **BrowseGallery1**, then select the pen icon that appears on the top left corner of the gallery.

1.  Selecting the pen icon will allow you to readjust the cell of the gallery. Resize it so that there's increased space between the cells.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the cell resized to increase space.](../media/increase-space.png)](../media/increase-space.png#lightbox)

1. Increase the size of **Image1** then move it slightly to the right, as shown below.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the image moved slightly.](../media/move-image.png)](../media/move-image.png#lightbox)

1. Resize and reposition **Title1** and **Subtitle1** so that they appear as shown below. Increase the space of both of them so that they each take up two line spaces. This is so that text can overflow into the next line if necessary. You may need to reposition the image and increase the size of the cell so that it sits nicely.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the title and subtitle size and position changed.](../media/size-position.png)](../media/size-position.png#lightbox)

1. **Save** your app.

1. We're now going to add a colored bar to each item to show the approval status. Select **BrowseGallery1** then select the pen icon as shown earlier, so that the first cell of the gallery is selected. Then, select on the **Insert** from the ribbon and select **rectangle**. A rectangle should now appear in each cell of the gallery.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of insert rectangle.](../media/rectangle.png)](../media/rectangle.png#lightbox)

1. Resize and move the rectangle, so that it appears as shown below.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the rectangle resized and moved.](../media/move-rectangle.png)](../media/move-rectangle.png#lightbox)

1. With the rectangle selected, change the property dropdown next to the formula bar to **Fill**, then enter in the following formula. You'll see all the rectangles change to gold.

	`Switch(Text(ThisItem.'Approval Status'),"Approved", Green,"Rejected",OrangeRed,Gold)`

	> [!div class="mx-imgBorder"]
	> [![Screenshot of formula for rectangle.](../media/rectangle-formula.png)](../media/rectangle-formula.png#lightbox)

### Locale differences

If your computer has its regional settings set to use the comma ',' for its decimal separator (like in much of Europe) your formulas will need to use a semicolon ';' instead of a comma. Use the formula below instead. If you are in the en-us locale, you can ignore this.

`Switch(Text(ThisItem.'Approval Status');"Approved"; Green;"Rejected";OrangeRed;Gold)`

1. Go to view your data sources, then select **Edit data** on the **Requests** table.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the edit data button on the requests table.](../media/edit-table-data.png)](../media/edit-table-data.png#lightbox)

1.  In the **Requests** table, set the value of the **Approval Status** column for 1 row to **Approved**. For the next row, set it to **Rejected**. Leave the third row (and any extra rows you may have) blank. Close the table.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the approval status.](../media/approval-status.png)](../media/approval-status.png#lightbox)

1.  You can now see the conditional formatting of the rectangle appear based on the Approval Status field for each row.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the conditional formatting of the rectangle.](../media/conditional-formatting.png)](../media/conditional-formatting.png#lightbox)

1.  On the form, select the Data Card Key for the Name card (that is, **DataCardKeyX**). From the properties pane, change the **FontSize** to **12**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of a label font size.](../media/font-size.png)](../media/font-size.png#lightbox)

1.  Set the color to the **purple** as shown below. Set the Font weight to **bold**.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the color set to purple and the font weight set to bold.](../media/purple-bold.png)](../media/purple-bold.png#lightbox)

1.  Repeat the formatting changes in the step above to the **DataCardKey** for **Asset Category**, **Asset**, and **Comment** cards of the form.

1.  On the Data Card Key of both the **Approval Status** and **Request Number.** cards, set the Font size to **12** and the color of the font to **dark grey**. Resize the cards to ensure the text is fully visible.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the font size set and the color set.](../media/font-size-color.png)](../media/font-size-color.png#lightbox)

1.  Select **Image2** from Asset_DataCard1 (that is, the image of the asset within the form). Move it to the left as shown below.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the image moved to the left.](../media/image-moved.png)](../media/image-moved.png#lightbox)

1.  **Save** and **preview** the app. From the app, you can also select a past request to view or edit it from the form.

1. Your app should now appear as below.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the finished app.](../media/finished-app.png)](../media/finished-app.png#lightbox)
	
