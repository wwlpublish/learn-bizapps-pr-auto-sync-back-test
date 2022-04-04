Power Apps portals does not support client-side business rules or custom JavaScript processes that are available on model-driven forms. However, custom JavaScript can be added directly to a portal page in the Power Apps portals Studio source code editor and to web templates.

> [!div class="mx-imgBorder"]
> [![Screenshot of custom JavaScript added in Portals Studio source code editor.](../media/javascript-template.png)](../media/javascript-template.png#lightbox)

In addition, the **Table Lists**, **Table Forms**, and **Web Forms** features include a custom JavaScript column that allows developers to add scripts that implement the required functionality.

The functionality can range from hiding controls, to replacing input controls with user-friendly equivalents, to invoking external web services and implementing sophisticated integration scenarios.

Out of the box, Power Apps portals includes the [jQuery](https://jquery.com/?azure-portal=true) library that makes manipulation of page content and appearance a reasonably simple task.

### Controls and columns

A default **Contact Us** form that creates a lead in Microsoft Dataverse includes a mandatory **Topic** column. This column could be confusing to site visitors. You can't use CSS to hide the control because it leaves the red asterisk that indicates that the column is mandatory. JavaScript helps make your job of hiding the column relatively simple. To set this column to a predefined value and then hide it from view, go to portals Studio and add the following script to the source code of the page that contains the **Contact Us** form:

```html
<script>
$(document).ready
(
  function()
  {
    $("#subject").val('Submitted from contact us form'); // sets the value
    $("#subject").closest('tr').hide(); // hide the row containing the column
  }
);
</script>
```

> [!div class="mx-imgBorder"]
> [![Screenshot of script added to the source code of the page.](../media/javascript-page.png)](../media/javascript-page.png#lightbox)

JavaScript is a simple way to add supplementary behavior or functionality to your Power Apps portal. It can be added directly to a page or added to the **Table Form** configuration (through the Portal Management app) or as part of a web template, depending on your scoping needs. Script can be used on the form to:

* Implement business rules.
* Add dependencies between elements like dependent option sets.
* Perform additional form validation.

These options provide reasonable alternatives to client-side business rules and scripting in model-driven forms.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4AmL6]

For more information, see [Add custom JavaScript](/power-apps/maker/portals/configure/add-custom-javascript/?azure-portal=true).
