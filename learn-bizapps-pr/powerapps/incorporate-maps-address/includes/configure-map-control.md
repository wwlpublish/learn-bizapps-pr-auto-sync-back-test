You can use the following two methods to add maps to your canvas apps. Both methods have their strengths and weaknesses.

-   Interactive map control (premium)

-   Static map APIs

The map control is a premium control that takes full advantage of the native geospatial capabilities within Power Apps. It contains many properties that allow you to zoom, tilt, navigate, rotate, and interact with a map in an all-in-one experience. You don't need to add complex formulas or manually created controls to the app to achieve this functionality.

> [!div class="mx-imgBorder"]
> [![Screenshot of the map control for a canvas app.](../media/map-control.png)](../media/map-control.png#lightbox)

The static map API approach uses an image control and several formulas and controls to interact with the image control. This approach takes more effort to build but doesn't require other user licensing like the map control does. Map controls, such as zooming and navigation, require the use of separately added controls and advanced formulas that consume map web services to interact with the map image. This module doesn't cover static map APIs, but you might find many tutorials and documentation that explain how to build them. The process isn't the same as it is for the interactive map controls, and it's a much more intensive and technical process.

After adding the map control to the canvas app, you'll have access to many properties that you can interact with through the **Properties** menu or through Microsoft Power Fx. In this lesson, you'll learn about several of these fields and their setup.

The following screenshot is an example map control that's added to a canvas app by using the configurable options.

> [!div class="mx-imgBorder"]
> [![Screenshot of the interactive map control and the fields that are available to use.](../media/map-control-properties.png)](../media/map-control-properties.png#lightbox)

When you enable the **Use default location** feature, the map will automatically start at a certain location when it first loads, which provides a consistent user experience. When enabled, the map will always render at the location that's specified in the default latitude and longitude fields with the default zoom level.

> [!div class="mx-imgBorder"]
> [![Screenshot of the default location properties of the interactive map for an app.](../media/default-location-properties.png)](../media/default-location-properties.png#lightbox)

The map can automatically show the user's current location on the interactive map when you set the **CurrentLocation** field to **true** and use the **Location.Latitude** and **Location.Longitude** settings in the respective **CurrentLocationLatitude** and **CurrentLocationLongitude** properties.

> [!div class="mx-imgBorder"]
> [![Screenshot of the current location properties of the interactive map for an app.](../media/current-location-properties.png)](../media/current-location-properties.png#lightbox)

Depending on the application's requirements, or where it will be used, the map control can display the picture in different views. For instance, you can use a satellite view to see the actual buildings and roads as they appear either with or without street and building information applied. Alternatively, the map can show a digitally rendered version in dark or light modes with three different types of roads. Some views might be better for navigation while others might be more optimal for accessibility or research purposes. 

> [!div class="mx-imgBorder"]
> [![Screenshot of the different styles for an interactive map and how they appear in the application.](../media/map-styles.png)](../media/map-styles.png#lightbox)

The map control also has embedded controls, such as **Zoom**, **Compass**, and **Pitch**, that you can enable so that users of the canvas app can view the location from different perspectives.

> [!div class="mx-imgBorder"]
> [![Screenshot of the Zoom, Compass, and Pitch controls for an interactive map and how each can change the appearance of the map.](../media/map-zoom-compass-pitch.png)](../media/map-zoom-compass-pitch.png#lightbox)

You can assign data sources to the maps, which will allow you to insert pins on the map. You can use this feature for business use cases such as delivery locations, customer locations, and more.

For more information, see [Use a data source to insert pins](/power-apps/maker/canvas-apps/geospatial-map-excel/?azure-portal=true).

When you select icons for the different pins in a data source, you can select from any Microsoft Azure pins. To review all available image templates, see the [List of image templates](/azure/azure-maps/how-to-use-image-templates-web-sdk?azure-portal=true#list-of-image-templates).

> [!div class="mx-imgBorder"]
> [![Screenshot of the data source selection for a map control.](../media/map-data-source.png)](../media/map-data-source.png#lightbox)

For pins that are placed on a map, you can view associated information for that pin to provide canvas-specific information. To do so, point to the pins or select them, depending on the configuration in the **Show info cards** and the fields that are selected to display. You can set the color of the pins for the entire control in the properties or from the data source for each individual pin.

> [!div class="mx-imgBorder"]
> [![Screenshot of the Cluster pins, Show info cards, and Pin color configurations for an interactive map.](../media/cluster-information-cards.png)](../media/cluster-information-cards.png#lightbox)

If multiple pins are located closely together, you can use the **Cluster pins** configuration to group all pins together until users adjust their zoom to have a better view of those pins.

> [!div class="mx-imgBorder"]
> [![Screenshot example of the Cluster pins feature on a map control.](../media/cluster-pins.png)](../media/cluster-pins.png#lightbox)

For more information, see [Add informational cards to pins on a map](/power-apps/maker/canvas-apps/geospatial-map-infocards/?azure-portal=true).
