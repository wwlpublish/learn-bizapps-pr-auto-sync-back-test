You add a chart to a webpage by using the Liquid tag [chart](/power-apps/maker/portals/liquid/portals-entity-tags?azure-portal=true#chart). As with any Liquid code, you can add the `chart` tag directly into the page content, embed it inside a content snippet, or add it as part of a web template.

```twig
{% chart id:"EE3C733D-5693-DE11-97D4-00155DA3B01E" viewid:"00000000-0000-0000-00AA-000010001006" %}
```

### Parameters

Two parameters are available for you to provide with the `chart` tag:

- **id** - Visualization identifier of the chart. You can get this parameter by exporting the chart.

- **viewid** - Table view identifier when it is opened in the model-driven view editor. If it's not specified, the default view will be used.

Showing a model-driven chart in Power Apps portals doesn't require additional configuration. Only system charts and system views are supported in configuration.

- To obtain the `chart id`, export the chart definition from a model-driven app and then look for `visualizationid` in the exported chart file.
- To obtain the `viewid`, start customizing the view and then copy the view ID from the URL.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4Avkv]

To allow users to view the chart, ensure that the appropriate **Table Permission** records are created and assigned to applicable web roles to allow read data from the target table. If permission is not granted, the user will see an access denied message.

> [!NOTE]
> Different users might see different resulting charts based on their specific table permissions.

Some chart types and some out-of-the-box charts aren't supported. For more information, see [Unsupported charts and chart types](/power-apps/maker/portals/configure/add-chart?azure-portal=true#unsupported-charts-and-chart-types).

For more information and step-by-step instructions, see [Add a chart created in a model-driven app to a webpage in portal](/power-apps/maker/portals/configure/add-chart/?azure-portal=true).
