The following procedures will show you how to create a Document processing model in AI Builder. This guided experience will walk through each step of the model creation process. You can save your work and return at any time. Progress will be saved automatically when you go between steps.

## Sign in to AI Builder

Follow these steps to sign in to AI Builder:

1. Go to Power Automate or Power Apps and sign in with your organizational account.
1. In the left pane, select AI Builder > Explore.
1. Select Document processing.
1. If you want to create your model by using your own documents, make sure that you have at least five examples that use the same layout. Otherwise, you can use sample data we will be using in this guided experience. You can download the sample data in [English version](https://go.microsoft.com/fwlink/?linkid=2128080) or in [Japanese version](https://go.microsoft.com/fwlink/?linkid=2186887)
1. Select **Create**.

## Choose document type

In this step you select the type of document you want to build an AI model to automate data extraction. There are two options:

- **Structured and semi-structured documents**. Structured and semi-structured documents are those where for a given layout, the fields, tables, checkboxes, and other items can be found in similar places. Examples of structured and semi-structured documents are invoices, purchase orders, delivery orders, tax documents, etc.

- **Unstructured and free-form documents**. Unstructured documents are those where there is no set structure, usually free documents with a varying number of paragraphs. Examples of unstructured documents are contracts, statements of work, letters, etc.

![Screenshot of the AI Builder Choose document type page where to choose between structured or unstructured documents.](../media/document-processing-choose-document-type.png)

## Choose information to extract

In this step you define the fields and tables you want to teach your model how to extract.

The provided sample data in [English version](https://go.microsoft.com/fwlink/?linkid=2128080) or in [Japanese version](https://go.microsoft.com/fwlink/?linkid=2186887) are invoices from two different providers. Define the following fields to extract:

- Invoice number
- Due date
- Total amount
- Customer ID

Select **+ Add** and then select **Field**.

![Screenshot of the Power Automate Choose information to extract page adding four fields on the Fields tab.](../media/add-field.jpg)

Enter the field name **Invoice Number** and click **Done**, repeat this step for **Due Date**, **Total amount**, and **Customer ID**.

![Screenshot of Define Field.](../media/define-field.jpg)

These are the fields that the model will learn how to extract from the document.

![Screenshot of Define Field 2.](../media/define-field-02.jpg)

We also want to extract the description and total amount for each line item present on the invoice. Define a table names **Items** and with the columns **Description** and **Item total**.

Select **Add** + and then **Add Single page table**, and then **Next**.

![Screenshot of Single Page Table.](../media/single-page-table-01.jpg)

Define as table name **Items** and define the columns **Description** and **Item total**. 
Select **Column1** and then rename **Column1 by Description**.
Select **+ New column**, enter the column name **Item total**.

![Screenshot of Single Page Table 2.](../media/single-page-table-02.jpg)

![Screenshot of Single Page Table 3.](../media/single-page-table-03.jpg)


## Define collections and upload documents

A collection is a group of documents that share the same layout. Create as many collections as documents with different layout that you want your model to process. In this guided experience, since we have two invoice providers, and each invoice provider uses a different invoice template we define two collections.

Select **New Collection** and change the name of the first collection to **Adatum**.  

Name the first collection **Adatum** and the second collection **Contoso**.

![Screenshot of New Collection.](../media/new-collection.jpg)

![Screenshot of New Collection 1.](../media/new-collection-01.jpg)

![Screenshot of New Collection 2.](../media/new-collection-02.jpg)

Now that we have created our two collections we will need to upload at least five samples for each collection.

For the collection named **Adatum**, upload the five documents you will find on the **AI Builder Document processing Sample Data/Adatum/Train** folder.

Select the **+** icon in each collection.

![Screenshot of Adatum Add Documents 1.](../media/adatum-add-documents-01.jpg)

Select **Add documents**, and select **My device** as a data source.

![Screenshot of Adatum Add Documents 2.](../media/adatum-add-documents-02.jpg)

![Screenshot of Adatum Add Documents 3.](../media/adatum-add-documents-03.jpg)

Select 5 documents from your local device and select upload documents. Those 5 uploaded documents will be used to train your model.

![Screenshot of Adatum Add Documents 4.](../media/adatum-add-documents-04.jpg)

![Screenshot of Adatum Add Documents 5.](../media/adatum-add-documents-05.jpg)

![Screenshot of Adatum Add Documents 6.](../media/adatum-add-documents-06.jpg)

Once the 5 documents are uploaded to your collection Adatum, you can repeat these steps above for the collection Contoso.

For the collection names **Contoso**, upload the five documents you will find on the **AI Builder Document processing Sample Data/Contoso/Train** folder.

Once you have uploaded the sample documents to each collection click **Next** to continue.

## Tag documents

Now is the time to teach your AI model how to extract the fields and tables you have defined. You do this by tagging the sample documents you have uploaded.

To start the tagging process, select a collection on the right panel.

### Tag fields

Let’s start by tagging our defined fields **Invoice number**, **Due date**, **Total amount**, and **Customer ID**. To tag a field, simply draw a rectangle around the field on the document and select the field name it corresponds to.

![Screenshot of Tag Field 1.](../media/tag-field-01.jpg)

![Screenshot of Tag Field 2.](../media/tag-field-02.jpg)

![Screenshot of Tag Field 3.](../media/tag-field-03.jpg)

At anytime you can resize to adjust your selection.

When you hover over different words in your documents, light blue boxes appear. These indicate that you can draw a rectangle around those words to select a field.

![Screenshot of address with number selected.](../media/forms-address.png)

### Field or table not in document

Not all defined fields and tables need to necessarily be in all documents. If you have started by tagging the Contoso collection, you will see that the field Customer ID is not present. For fields not present in documents, just tell the AI model that this is the case by going to the field or table on the right panel and selecting **‘Not available in the document’** in the three dotted menu.

![Screenshot of Tag Field 4.](../media/tag-field-04.jpg)

### Tag tables

To tag a table: 

1.	Draw a rectangle around the table in the document you are interested in, and then select the table name that it corresponds to. 

![Screenshot of New Tag Table 1.](../media/new-tag-table-01.jpg)

The content of the panel on the right will change.

![Screenshot of New Tag Table 2.](../media/new-tag-table-02.jpg)

2.	Draw rows by left clicking between row separators.

![Screenshot of New Tag Table 3.](../media/new-tag-table-03.jpg)

![Screenshot of New Tag Table 4.](../media/new-tag-table-04.jpg)

3.	Draw columns by pressing Ctrl + left-click (or ⌘  leff-click on MacOS) .

![Screenshot of New Tag Table 5.](../media/new-tag-table-05.jpg)

4.	Once the rows and columns have been set, assign the headers to extract by selecting the header column and mapping it to the desired one.

![Screenshot of New Tag Table 6.](../media/new-tag-table-06.jpg)

![Screenshot of New Tag Table 7.](../media/new-tag-table-07.jpg)

5.	A preview of how the table will be extracted appears on the panel on the right.

![Screenshot of New Tag Table 8.](../media/new-tag-table-08.jpg)

6.	If the header of the table has been tagged, select Ignore first row so the header of the table isn't extracted as the table content.

![Screenshot of New Tag Table 9.](../media/new-tag-table-09.jpg)

![Screenshot of New Tag Table 10.](../media/new-tag-table-10.jpg)


### Tag all documents

Once you have finished tagging one document, move to the next one to tag by clicking the navigation arrows bellow the document preview on the top right.

Once you have finished tagging one collection, navigate back to the collection list to tag the second collection.

![Screenshot of Tag Table 5.](../media/tag-table-05.jpg)

## Summary and train

After you have tagged all documents across all collections, follow these steps:

1. Select **Next**.
2. Review the summary of your model's details. If everything looks acceptable, select **Train**.

## Next steps

Now that you've created a Document processing model in AI Builder, you'll learn how to test your model and use it in Power Apps and Power Automate.

