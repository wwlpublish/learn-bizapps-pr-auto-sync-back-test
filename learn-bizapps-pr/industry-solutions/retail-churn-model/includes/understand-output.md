In this exercise, you'll review the output of the Retail Churn model.

1.  Open the Retail churn model to view its contents. Here you'll find three main areas:

	- **Training model performance** will display a letter grade of how well the model has performed.
	
	- **Likelihood to churn (number of customers)** that can be read as X customers are Y% likely to churn.
	
	- **Most influential factors** considered by the AI in predicting the model. This will vary depending on the data set.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the Retail Churn Model view with training model performance, likelihood to churn, and most influential factors.](../media/retain-churn-model-view.png)

1.  To view a customer's full profile in Dynamics 365 Customer Insights, navigate to Customers and open any of the sample records.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the customers records view.](../media/customers.png)](../media/customers.png#lightbox)

	> [!div class="mx-imgBorder"]
	> ![Screenshot of a customer record details.](../media/customer-record.png)

1.  To view the calculated churn scores, navigate to **Data** and then under **Entities**, open the msfsiRetailBankingChurn entity that was created when you ran the churn model.

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the entities view.](../media/entities.png)

1.  On the Attributes tab, you'll find various new columns created by the model that factor into the score. Here's a breakdown of some of these attributes:

	- ExpFeature1 = Contact related factors
	
	- ExpFeature2 = Digital transaction factors
	
	- ExpFeature3 = Physical transaction factors
	
	- ExpFeature4 = Digital session factors
	
	- ExpFeature5 = Physical session factors

	> [!div class="mx-imgBorder"]
	> ![Screenshot of the attributes list.](../media/attributes.png)

1.  Select the **Data** tab to see the calculated churn score for each of the **CustomerIDs** in the dataset.

	> [!div class="mx-imgBorder"]
	> [![Screenshot of the data tab with calculated churn scores for each customer.](../media/data.png)](../media/data.png#lightbox)

**Congratulations!** You have successfully run the Retail Churn Model in Dynamics 365 Customer Insights.
