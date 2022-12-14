In Power Apps portals, you can search for rows across multiple tables by using the portal’s global search functionality. You can also search within rows of lists by using the list search functionality.

Portal search now uses Dataverse's search capability to deliver results from multiple tables and columns for new portals. For existing portals, Dataverse search can be enabled by setting the value for the site setting **Search/EnableDataverseSearch** to **true**.

> [!NOTE]
> Portal search needs the Dataverse search feature to be enabled on the Dataverse environment settings.

To enable Dataverse search:

1. In the [Power Platform admin center](https://admin.powerplatform.microsoft.com/?azure-portal=true), select an environment.

1. Select **Settings > Product > Features**.

1. Under **Search**, set **Dataverse search** to **On**.

1. Select **Save**.

## Global search

Global search of Power Apps portals allows you to search for rows across multiple tables. It also allows you to search across multiple columns and configure what columns of a table would be searchable.

Among the benefits of global search is its ability to:

- Find matches to any word in the search term in any column in the table. Matches can include inflectional words like stream, streaming, or streamed.
- Return results from all searchable tables in a single list, sorted by relevance, based on factors like the number of words matched or their proximity to each other in the text.
- Highlight matches in the search results.
- Provide facet options that can be used to further filter search results.

### Searchable tables

The aim of global search is to locate information within the site content. All content is located within the tables that are installed with Dynamics 365 Portals solutions and, depending on the starter portal that has been selected, the following tables can be searched: **Web Page**, **Web File**, **Knowledge Article**, **Forums**, **Blogs**, **Ideas**, **Incident (Case)**. Directly related tables are also searched, for example, a *blog* search also includes the **Blog Post** and **Blog Comment** tables.

Each of the mentioned tables includes a **Portal Search** view that defines a set of columns that are searchable within the table. You can change the columns that are defined in these views and publish the changes to modify the scope of the search. The name of the view is defined by the site setting `Search/IndexQueryName` and can be changed.

> [!NOTE]
> After changing the views or the view name, you need to rebuild the index as documented in the [Rebuild full search index](/power-apps/maker/portals/configure/search?azure-portal=true#rebuild-full-search-index) article.

Knowledge articles have a feature that allows you to mark an article as **Internal Only**. Articles are searchable only if they are published, and their **Internal Only** column is set to **false**.

Notes and attachments on knowledge articles and web files are searched as well. For more information, see [Search within file attachment content](/power-apps/maker/portals/configure/search-file-attachment/?azure-portal=true).

In addition to the system tables preconfigured for search, you can now include additional tables. For more information, read [configuring additional tables for search](/power-apps/maker/portals/configure/search-additional-entities/?azure-portal=true).

## Faceted search

Portal content can be searched by using filters based on the characteristics of the content. The filters that are implemented by a faceted portal search allow customers to find the content that they want quicker than a traditional search.

Faceted search enables portals to have search filters that allow you to choose between items like forums, blogs, pages, and knowledge articles. More filters are available for specific search types. For example, knowledge articles can be filtered by row Type, Modified Date, Rating, and Products to help customers find the content they need.

> [!div class="mx-imgBorder"]
> [![Screenshot of faceted content search using filters.](../media/content-search.png)](../media/content-search.png#lightbox)

Faceted search can be enabled or disabled by using the `Search/FacetedView` site setting. Individual parts of faceted search can be disabled by deactivating specific table views in Dynamics 365. Similar tables can be grouped together. For example, the search result type **Documents** describes both knowledge article attachments and web files.

For more information, see [Use faceted search to improve portal search](/power-apps/maker/portals/configure/improve-portal-search-faceted-search/?azure-portal=true).

## Configuration

Global search is highly configurable, and configuration is available for both functionality and user interface for the search results.

### Related site settings

Every aspect of the global search functionality can be configured by using the site settings that are described in detail in [Related site settings](/power-apps/maker/portals/configure/search?azure-portal=true#related-site-settings).

### Content snippets

The visual aspects of the global search functionality can be configured by using relevant content snippets, which define elements of the search user interface, including faceted search. The configurable elements include captions, titles, tooltips, buttons, and others. Because content snippets are language-aware, you can adapt the appearance and behavior of the search for a multilingual audience.

For more information, see [Related content snippets](/power-apps/maker/portals/configure/search?azure-portal=true#related-content-snippets).

### Attachment search

Power Apps portals allow you to index and search knowledge article and web file attachments. By default, this search is switched off but can be enabled by using site settings.

> [!IMPORTANT]
> **Dataverse Search** must be enabled for attachment search. For more information, see [Dataverse Search](/power-apps/user/relevance-search/?azure-portal=true).

You can exclude individual web files from the search by setting the **Exclude From Search** column to **Yes**.

Other aspects of attachment search can be modified by using additional site settings or templates. For more information, see [Search within file attachment content](/power-apps/maker/portals/configure/search-file-attachment/?azure-portal=true).
