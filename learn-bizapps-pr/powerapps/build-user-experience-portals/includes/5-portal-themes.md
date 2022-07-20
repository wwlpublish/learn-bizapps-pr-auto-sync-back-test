Portals use the [Bootstrap front-end framework](http://getbootstrap.com/?azure-portal=true) to control the design and layout of the website. Bootstrap is a package of HTML and Cascading Style Sheets (CSS) design templates for typography, forms, buttons, navigation, and other elements, in addition to optional JavaScript extensions. One of the many appealing features of Bootstrap is that it offers a responsive layout out of the box; it automatically adjusts your website to have an aesthetically pleasing appearance on all devices, from small phones to large desktops.

## Theme fundamentals

A theme determines the appearance of all webpages in your portal to ensure visual consistency. The theme controls navigational structure, the banner, colors and fonts, and other visual elements of a webpage.

The web templates that are included in a starter portal are implemented by using standard Bootstrap components with minimal additional custom styles. Consequently, the starter portal can take advantage of the customization options that are provided by Bootstrap; the theme can be customized in a way that's applied consistently to the entire portal.

### CSS on webpages

Cascading Style Sheets (CSS) is a language that determines the style of a webpage by describing how its HTML elements are to be displayed, including text, fonts, colors, backgrounds, borders, and margins.

Making changes to the style of your portal pages can be as simple as applying CSS statements directly to a page in the **Custom CSS** column. For example, if you need to increase the height of the navigation bar at the top of a particular page to fit a logo, you can simply edit the page and then add a custom CSS statement.

```css
.navbar-static-top.navbar { min-height: 100px; background-color:gold; }
```

> [!NOTE]
> CSS statements that are added directly to a webpage will apply to that webpage only.

This process works for small adjustments on a single page, but the better approach is to record customizations in one or more CSS files and then apply them to the entire portal or parts of it.

## Apply customizations

In Power Apps portals, the **Enable basic theme** feature controls how CSS customizations are applied to the portal.

### Themes

When you turn on the **Enable basic theme** feature, you can use default themes called **Presets**. You can also create copies of the preset themes for additional customization.

![Screenshot of a selection of themes in portals Studio.](../media/theme-selection.png)

Themes create an overall look and feel for the site by defining a number of colors for different areas. 

If the site requires additional customizations, then the **Edit CSS** feature can be used. It is available regardless of whether the basic theme is enabled.

### Edit CSS

When the **Enable basic theme** feature is off, you can only apply customizations by editing existing or adding new CSS files. 

Any starter portal has a number of files that are already included as child web files on the home page: `bootstrap.min.css` and `theme.css`. These files define default styles and a theme for your entire portal. Additional stylesheets can be uploaded and edited.

> [!div class="mx-imgBorder"]
> [![Screenshot of themes editing options from toolbelt for CSS code.](../media/css-edit.png)](../media/css-edit.png#lightbox)

For additional information, see [Edit CSS](/power-apps/maker/portals/edit-css/?azure-portal=true).

You need to consider how to approach style modifications for your portal:

- Create complete styling for the entire site and then replace the content of the CSS file. This process works well if you have access to good designers who can ensure that all relevant elements are defined. This approach creates centrally controlled styling and ensures consistency throughout the portal.
- Redefine only the elements that require modifications, for example, colors and font size. Create and upload the CSS file that contains only these incremental adjustments. This process works well if your target design is close to the starter portal design and only minor styling modifications are required. This approach allows incremental modifications that can be easily undone.

> [!WARNING]
> If you decide to overwrite `bootstrap.min.css` or `theme.css` files, make sure that you download a backup copy of these files prior to replacing them. If your replacement CSS is invalid or incomplete, you might not be able to undo the replacement and will have to restore the content of these files if the portal is rendered non-functional.

### Localized CSS modifications

Instead of applying CSS to the entire site, it is possible to upload CSS as web files using the Portal Management app. The CSS that is contained in the web file applies to the file's parent page and all descendants of that page, which makes it possible for you to build fully customized sections of your site.

For example, if you want to apply different styling to your **News** section and all the new articles underneath it, go to **News**, create a child web file with a **.css** extension, upload your CSS file (the name does not matter), and the style will be applied to the **News** section and its content only.

> [!IMPORTANT]
> The partial URL must end in **.css** for the portal to recognize it and apply it to the webpage and its child pages.

### Customize bootstrap

The standard way to create a custom version of Bootstrap is [through the official Bootstrap site](http://getbootstrap.com/customize/#less-variables/?azure-portal=true). However, due to the popularity of Bootstrap, many other source sites have also been created for this purpose. These sites might provide a more user-friendly interface for Bootstrap customization or predesigned versions of Bootstrap for you to download. [The official Bootstrap customize](http://getbootstrap.com/customize/?azure-portal=true) site has more information about Bootstrap customization.

> [!TIP]
> When you are customizing Bootstrap, only select elements that require modifications. For example, if you only want to replace the fonts with your corporate standard fonts, then select the typography components of Bootstrap, which will reduce the chances of accidentally rewriting other CSS elements.

After you have configured Bootstrap, it will generate one or more files that you would want to upload as web files. Unless your intent is to completely *replace* the original styles, make sure that you don't use `bootstrap.css`, `bootstrap.min.css`, `theme.css`, or `theme.min.css` in your partial URLs because of how the portal handles multiple CSS files.

### Background images

When people start portal customizations, one of the most common requests that they have is to replace the background images. These images are often applied by using CSS but can easily be replaced without changing CSS. Look for the web files under the portal's **Home** page, for example, `homehero.jpg`.

![Screenshot of the list of available web files under Home page.](../media/web-files-root.png) 

You can replace the attachments of these web files with your own images, and that process is all that's required. Make sure that the size of the new images is compatible to maintain consistent layout.
