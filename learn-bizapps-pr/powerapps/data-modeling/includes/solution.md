Microsoft Dataverse is a flexible data repository that can solve business problems in multiple ways. There is not a single right way to data model this solution. What follows is an example of how you might approach solving this set of requirements. Compare the example data model to what you designed and review the differences.

<insert data model solution video>

In addition to the proposed data model, our architects suggested the following options:
Upon evaluation and additional information from Fabrikam, Visits might be a custom activity table.

· Not every Visitor should be a Contact record. If the Visitor has low probability as a customer (just her to see the robots), then keep the Contact table data cleaner without the additional Visitor records. Keep the Contacts dedicated to the sales process.

· IoT devices such as the tracker mentioned in the requirements can quickly produces massive amounts of data. We are basing our model on the assumption that the provided API allows us to use the data relevant to our purposes. If that is not the case, a much deeper discussion will be required.

Even when it seems like the requirements lend themselves to a certain path, it is likely there is not a single right way to meet a those requirements. As solution architects it is important to evaluate the requirements with an eye on offering the simplest solution that meets, or exceeds, the requirements while providing a secure environment that users are delighted to use.