Business intelligence involves collaboration, and sharing datasets across workspaces is a powerful way to collaborate within your organization. However, if your organization has many different datasets that can be accessed by many users, you might want to take measures to manage those datasets. For instance, you might want to direct your users to the most up-to-date and highest-quality datasets in your workspaces, or you might want to restrict the reuse of datasets across your workspaces.

To ensure that your organization has consistent data for making decisions and a healthy data culture, it's important to create and share optimized datasets and then endorse those datasets as the *one source of truth*. Report creators can then reuse those endorsed datasets to build accurate, standardized reports.

Power BI provides two ways to endorse your datasets:

-   **Promotion** - Promote your datasets when they're ready for broad usage. Power BI Admins have permissions to promote datasets.

-   **Certification** - Request certification for a promoted dataset from an admin user that is defined in the Dataset Certification tenant admin setting. This certification adds another layer of security for your datasets. Certification can be a highly selective process, so only the truly reliable and authoritative datasets are used across the organization.

In this example, you and the other teams are using a workspace in Power BI service to organize all your reports and dashboards. However, you begin to receive emails from confused users who expected to see a sales report and are now looking at a product report instead. You need to make some changes to direct your users to the datasets that they should be accessing, and you can accomplish this task with the endorsing capability in Power BI.

In this example, the certification type of endorsement is best suited for the Sales team because it will require users to have special access before they can view the Sales dashboards. By implementing the certification, you'll lead your users to the most appropriate reports and dashboards, avoiding the inevitable confusion that might arise with building and sharing a diversity of reports.

Though you'll soon learn how to certify the dataset, you'll first learn how to promote a dataset, in case you prefer to use that method.

## Promote a dataset 

You can only promote a dataset if you're a Power BI admin user or the owner of that dataset.

To promote a dataset, go to your workspace in Power BI service, and then open the settings page for the dataset that you want to promote. In this example, you want to promote the Tailwind Traders dataset.

Select the **Endorsement** setting.

> [!div class="mx-imgBorder"]
> [![Select endorsement option](../media/7-select-endorsement-option-ssm.png)](../media/7-select-endorsement-option-ssm.png#lightbox)

In the **Endorsement** settings, select the **Promoted** option, and then select **Apply**.

> [!div class="mx-imgBorder"]
> [![Select endorsement settings](../media/7-select-endorsement-settings-ss.png)](../media/7-select-endorsement-settings-ss.png#lightbox)

When you return to your workspace, a badge in the **Endorsement** column for that dataset will appear, indicating that it's ready for viewing by all of your users.

> [!div class="mx-imgBorder"]
> [![View promoted dataset badge](../media/7-promoted-dataset-badge-ssm.png)](../media/7-promoted-dataset-badge-ssm.png#lightbox)

## Certify a dataset 

You can only certify a dataset if you've been listed as a user in the tenant settings. The certification option will appear dimmed for other users.

To certify a dataset, you would start the same way as you did to promote the dataset. This time, however, you will select the **Certified** option in the **Endorsement** settings.

> [!div class="mx-imgBorder"]
> [![Select certified option](../media/7-select-certified-option-ssm.png)](../media/7-select-certified-option-ssm.png#lightbox)

When you apply your change, the **Certified** setting will update to display a message regarding who certified the dataset and when they did so.

> [!div class="mx-imgBorder"]
> [![View certified message details](../media/7-view-certified-details-ss.png)](../media/7-view-certified-details-ss.png#lightbox)

For more information, see [Promote your dataset](/power-bi/service-datasets-promote/?azure-portal=true) or [Certify datasets](/power-bi/service-datasets-certify/?azure-portal=true).
