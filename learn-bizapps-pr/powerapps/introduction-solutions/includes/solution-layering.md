Solution layering is implemented at a component level. The video below gives an overview of the two distinct layers, managed and unmanaged solutions. They exist at different layers within a Microsoft Dataverse environment.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/]

In Dataverse, there are two distinct layers.

## Managed layers

-   At the base of the managed layers level is the system layer.

    -   The system layer contains the entities and components that are required for the platform to function.

-   All imported, managed solutions and the system solution exist at this level.

-   When multiple managed solutions are installed, the last one installed is above the managed solution installed previously.

    -   This means that the second solution installed can customize the one installed before it.

-   When two managed solutions have conflicting definitions, the runtime behavior is either "Last one wins" or a merge logic is implemented.

-   If you uninstall a managed solution, the managed solution below it takes effect.

-   If you uninstall all managed solutions, the default behavior defined within the system solution is applied. 

## Unmanaged layer

All imported unmanaged solutions and ad-hoc customizations exist at this layer. All unmanaged solutions share a single unmanaged layer.

There are components that have a merge behavior such as sitemaps and forms. Meaning each layer is merged to produce the runtime behavior as opposed to last layer wins.