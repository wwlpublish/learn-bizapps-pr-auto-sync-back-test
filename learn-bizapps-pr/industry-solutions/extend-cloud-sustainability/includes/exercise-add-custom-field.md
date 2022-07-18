You might want to add more descriptive details to your facility. You can add a custom field to the existing **Facility** form to achieve this objective. The following exercise demonstrates how to create a field in a table and how to add that field to an existing form.

1. Sign in to the application and find the existing form that you want to add the new field to. This example shows how to add a facility type field to the **Facility** form. 
2. Select **Company profile > Facilities**. 

    > [!div class="mx-imgBorder"]
    > [![Screenshot showing facilities under company profiles and edit/ delete option for facilities.](../media/facilities.png)](../media/facilities.png#lightbox)

3. Select the pencil icon next to the facility to which you want to add a field to open the **Facility** form.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of Facility form showing Contoso Factory general details.](../media/facility-form.png)](../media/facility-form.png#lightbox)

4. To find the table in the data model that will need to be edited, look in the application URL for the **ent** value.  In the URL, the **ent=msdyn_facility** value will display. 

5. Sign in to [Power Apps](https://make.preview.powerapps.com/environments/839eace6-59ab-4243-97ec-a5b8fcc104e4/home/?azure-portal=ture) and select the **Sustainability Trial** environment from the dropdown menu in the upper-right corner.
6. Expand **Data > Tables** in the left navigation pane.

    > [!div class="mx-imgBorder"]
    > [![Screenshot showing expanded data option in navigation panel and table is selected under data.](../media/data-tables.png)](../media/data-tables.png#lightbox)

7. Change the **Default** dropdown menu to **All**.
8. Search for the name of the table that you found in the URL. In this example, it’s **msdyn_facility**. This table allows for customization (the checkbox).
    
    > [!div class="mx-imgBorder"]
    > [![Screenshot showing facility as m s d y n underscore facility under Data tables.](../media/msdyn-facility.png)](../media/msdyn-facility.png#lightbox)

9. Select the pencil icon to edit the table.

10. Select + Add column and enter the display name of the column as you want it to appear on the form.

    > [!div class="mx-imgBorder"]
    > [![Screenshot showing columns of Table facility where you can add column.](../media/facility-column.png)](../media/facility-column.png#lightbox)

11. Select **Forms** from the top menu.
12.	Select the ellipsis (…) next to the **Main** and then select **Edit form> Edit form in new tab**

    > [!div class="mx-imgBorder"]
    > [![Screenshot of forms where you can edit form in new tab by clicking on ellipsis.](../media/edit-form.png)](../media/edit-form.png#lightbox)

13. Select the **+ Form field** option to view the list of fields that you can add to the form.
14. Select Type from the list and then drag it onto the form.
15.	Select **Save** and then **Publish** the change.
16.	Return to the application and refresh. The field should be added to the form.

    > [!div class="mx-imgBorder"]
    > [![Screenshot of Contoso factory facility where field is added to form after refresh.](../media/contoso-factory.png)](../media/contoso-factory.png#lightbox)

 

