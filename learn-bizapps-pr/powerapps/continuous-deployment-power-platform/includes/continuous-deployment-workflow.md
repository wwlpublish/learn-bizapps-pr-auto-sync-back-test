We discussed the challenges with common patterns when deploying a new unmanaged solution with each sprint earlier in this learning path. Eventually, things just fall apart in production with things becoming a mess of hundreds of solutions.

> [!div class="mx-imgBorder"]
> [![Diagram that shows the common challenges where production becomes a mess.](../media/mess.png)](../media/mess.png#lightbox)

A modern approach to solution development will include layering and support deployments that are deterministic. **Deployments are deterministic** simply means that once an import order is established, the impact on runtime behavior should be more clearly understood.

> [!div class="mx-imgBorder"]
> [![Diagram that shows a modern approach with layering and deterministic deployments.](../media/layering.png)](../media/layering.png#lightbox)

## Continuous delivery workflow example

In this example, we have condensed our CI flow to the left to focus on our release stage (Continuous Delivery).

> [!VIDEO https://www.microsoft.com/videoplayer/embed/]
