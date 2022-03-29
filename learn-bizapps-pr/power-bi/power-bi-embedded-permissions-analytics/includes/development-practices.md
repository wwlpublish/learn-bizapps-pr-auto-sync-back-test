It's critical that your solution enforces data permissions correctly and efficiently. The following bulleted list provides you with good development practices to apply.

-   Strive to enforce data permissions by using roles instead of app logic. Client-side filtering, achieved with the Power BI client APIs, shouldn't be used to enforce data permissions. Client-side filtering is intended to temporarily filter a subset of the data the user can see.

-   Strive to define fewer datasets (models) with well-designed roles.

-   Strive to create fewer roles by using dynamic rules. A data-driven solution is easier to maintain.

-   When possible, create rules on dimension tables instead of fact tables. It will help to deliver faster query performance.

-   Validate that the model design, including its relationships and relationship properties, are correctly configured.

-   Use the USERPRINCIPALNAME function instead of USERNAME function. It provides consistency when validating the roles in Power BI Desktop and the Power BI service.

-   Rigorously validate model RLS by testing all roles and expected username values. Test what happens when unexpected values are passed as the username, and in those instances, ensure that no table rows are returned.

-   Ensure that the Power BI Desktop data source connection uses the same credentials that will be applied when set up in the Power BI service.

-   Request data modelers document roles, their purpose, and expected username values for handover to the app developers.
