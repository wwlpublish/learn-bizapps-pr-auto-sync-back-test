In this exercise, you'll create a storage account and a container. Furthermore, you'll upload the sample data input files (which are stored in the Microsoft Learn repository for this exercise) that you’ll use to generate data insights for the customer by using the Retail churn model.

## Task 1: Create storage account
To create a storage account, follow these steps:
1.  Go to the [Microsoft Azure portal](https://ms.portal.azure.com/?azure-portal=true) and sign in with the credentials that you're using for the lab.

1.  Select **Create a resource** and then select **Storage account**.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the Create a resource page with Storage account selected.](../media/storage-account.png)

1.  Select the subscription that you want to use for this lab. For the resource group, select **Create new** to create a new resource group.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the Subscription and Resource group fields.](../media/subscription-resource-group.png)

1.  Provide a storage account name, such as **retailchurnmodel**, and then select **Review + create**. (Note this storage account name because you’ll need it later in the exercise).

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the storage account name with the Review and create button.](../media/account-name.png)

## Task 2: Upload sample data input files to a container in a storage account
Follow these steps to upload sample data input files to a container in a storage account:
1.  After you’ve created the storage account, create a container in the storage account by selecting **+ Container**.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the add Container button.](../media/new-container.png)

1.  In the **Name** dropdown menu, select **retailgrocery**, and in the **Public access level** dropdown menu, select **Container (anonymous read access for containers and blobs)**.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the new container details.](../media/container-details.png)]

1. Download two compressed files and extract the CSV files to your local computer for use in the next step:
    1. [grocery_msrc_session.zip](https://github.com/MicrosoftDocs/mslearn-developer-tools-power-platform/raw/master/retail-cloud/Grocery_msrc_session.zip)
    1. [grocery_contact.zip](https://github.com/MicrosoftDocs/mslearn-developer-tools-power-platform/raw/master/retail-cloud/grocery_contact.zip)
   
1. Upload all three files you downloaded in the previous step to the container: **Grocery\_contact.csv**, **Grocery\_msrc\_session.csv**, and **Grocery\_msrc\_session.csv**.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the Upload blob dialog, showing a file to upload.](../media/upload.png)

1.  When the files have been uploaded to the blob, it will resemble the following screenshot.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the list of files that have been uploaded.](../media/upload-list.png)

Congratulations, you’ve successfully created a storage account and have uploaded the sample data input files to the storage account.
