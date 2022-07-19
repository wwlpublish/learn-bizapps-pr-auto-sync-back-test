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

![Animated screenshot of the Power Automate Choose information to extract page adding four fields on the Fields tab.](../media/forms-choose-information.gif)

We also want to extract the description and total amount for each line item present on the invoice. Define a table names **Items** and with the columns **Description** and **Item total**.

![Animated screenshot of the Power Automate Choose information to extract page adding two columns on the Tables tab.](../media/forms-choose-information-2.gif)

## Define collections and upload documents

A collection is a group of documents that share the same layout. Create as many collections as documents with different layout that you want your model to process. In this guided experience, since we have two invoice providers, and each invoice provider uses a different invoice template we define two collections.

Name the first collection **Adatum** and the second collection **Contoso**.

![Animated screenshot of the Power Automate Add collections of documents page adding two document collections.](../media/form-processing-add-collections.gif)

Now that we have created our two collections we will need to upload at least five samples for each collection.

For the collection named **Adatum**, upload the five documents you will find on the **AI Builder Document processing Sample Data/Adatum/Train** folder.

For the collection names **Contoso**, upload the five documents you will find on the **AI Builder Document processing Sample Data/Contoso/Train** folder.

![Animated screenshot of the Power Automate Add collections of documents page uploading five documents to each collection.](../media/form-processing-add-collections-2.gif)

Once you have uploaded the sample documents to each collection click **Next** to continue.

## Tag documents

Now is the time to teach your AI model how to extract the fields and tables you have defined. You do this by tagging the sample documents you have uploaded.

To start the tagging process, select a collection on the right panel.

### Tag fields

Let’s start by tagging our defined fields **Invoice number**, **Due date**, **Total amount**, and **Customer ID**. To tag a field, simply draw a rectangle around the field on the document and select to which field name it corresponds to.

![Animated screenshot of the Power Automate Tag documents step selecting fields on the invoice and then connecting them with data fields.](../media/forms-tag-fields.gif)

At anytime you can resize to adjust your selection.

When you hover over different words in your documents, light blue boxes appear. These indicate that you can draw a rectangle around those words to select a field.

![Screenshot of address with number selected.](../media/forms-address.png)

### Field or table not in document

Not all defined fields and tables need to necessarily be in all documents. If you have started by tagging the Contoso collection, you will see that the field Customer ID is not present. For fields not present in documents, just tell the AI model that this is the case by going to the field or table on the right panel and selecting **‘Not available in the document’** in the three dotted menu.

![Animated screenshot of the Customer ID field that was detected, but when you click the ellipsis button next to it, it's Unavailable in document.](../media/forms-not-available-in-document.gif)

### Tag tables

To tag a table: 

1. Draw a rectangle around the table in the document you are interested in, and then select the table name that it corresponds to. The content of the panel on the right will change. 
1. Select a cell from the table on the right panel, and then tag it on the document. 
1. Once you have tagged one cell, come back to the right panel, and select another cell to tag. 
1. Repeat this process until you have tagged all rows for all the columns you are interested in. 

The following animation illustrates the process: 

![Animated screenshot of invoice opening the table menu and selecting Tag table, then selecting items for each field.](../media/form-processing-tag-table.gif)

### Tag all documents

Once you have finished tagging one document, move to the next one to tag by clicking the navigation arrows bellow the document preview on the top right.

Once you have finished tagging one collection, navigate back to the collection list to tag the second collection.

![Animated screenshot of the Tag documents step, going through the documents and assigning fields.](../media/forms-tag-tables-2.gif)

## Summary and train

After you have tagged all documents across all collections, follow these steps:

1. Select **Next**.
2. Review the summary of your model's details. If everything looks acceptable, select **Train**.

## Next steps

Now that you've created a Document processing model in AI Builder, you'll learn how to test your model and use it in Power Apps and Power Automate.

