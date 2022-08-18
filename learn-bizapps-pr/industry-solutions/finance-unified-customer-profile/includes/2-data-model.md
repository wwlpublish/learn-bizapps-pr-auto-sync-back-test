In this exercise, you'll learn about the Unified customer profile data tables.

The Unified customer profile data model is built atop the **FinancialServiceCommon** and **RetailBankingCoreDataModel** layers in Microsoft Dataverse. For more information, see [Overview of Microsoft Cloud for Financial Services entities](/common-data-model/schema/core/industrycommon/financialservices/overview/?azure-portal=true).

## Task 1: Explore customer and bank data and relationships

In this task, you'll explore the main tables that are related to Unified customer profile. Select each table name to navigate to the Microsoft Docs page that provides details about each table.

### Unified customer profile table definitions  

Definitions for the Unified customer profile table are as follows:

- [Contact](/common-data-model/schema/core/industrycommon/financialservices/financialservicescommondatamodel/contact/?azure-portal=true) (customer) - Person with whom a business unit has a relationship, such as customer, supplier, and colleague.

- [Account](/common-data-model/schema/core/industrycommon/financialservices/financialservicescommondatamodel/account/?azure-portal=true) - Business that represents a customer or potential customer. The company that is billed in business transactions.

- [Bank](/common-data-model/schema/core/industrycommon/financialservices/financialservicescommondatamodel/bank/?azure-portal=true) - The bank that the branch is associated with.

- [Branch](/common-data-model/schema/core/industrycommon/financialservices/financialservicescommondatamodel/branch/?azure-portal=true) - The branch of the main bank, when  the borrower applies for a loan at a branch.


> [!div class="mx-imgBorder"]
> [![Screenshot of the Unified customer profile tables.](../media/tables.png)](../media/tables.png#lightbox)

## Task 2: Discover life event data tables and relationships

In this task, you'll learn about the main tables that are related to life event data. Select each table name to navigate to the Microsoft Docs page that provides details about each table.

### Life event data table definitions

[Life Moment](/common-data-model/schema/core/industrycommon/financialservices/retailbankingcoredatamodel/lifemoment/?azure-portal=true) tables show significant milestones in a customer's personal life that can impact their financial situation, such as attending college, marriage, having a child, retirement, and so on.  


> [!div class="mx-imgBorder"]
> [![Screenshot of the life event tables.](../media/life-event.png)](../media/life-event.png#lightbox)

## Task 3: Learn about financial data tables and relationships

In this task, you'll learn about the main tables that are related to customer financial data, including different types of financial holdings, financial instruments, and customer financial holdings. Select each table name to navigate to the Microsoft Docs page that provides details about each table.

### Financial data table definitions

Definitions for the Financial data table are as follows:

- [Financial holding](/common-data-model/schema/core/industrycommon/financialservices/retailbankingcoredatamodel/financialholding) - Accounts, loans, investments, credit lines, and savings accounts that are held by a customer.

- [FH loan](/common-data-model/schema/core/industrycommon/financialservices/retailbankingcoredatamodel/fh_loan) - Loans that are held by the customer with the financial institution.
  
- [FH saving](/common-data-model/schema/core/industrycommon/financialservices/retailbankingcoredatamodel/fh_saving) - Savings accounts that are held by the customer at the financial institution.
  
- [FH line of credit](/common-data-model/schema/core/industrycommon/financialservices/retailbankingcoredatamodel/fh_creditline) - A deposit account holding that allows the holder to make deposits and withdrawals through financial holding instruments. An account can be interest bearing.
  
- [FH investment](/common-data-model/schema/core/industrycommon/financialservices/retailbankingcoredatamodel/fh_investment) - A deposit account holding that allows the holder to make deposits and withdrawals through financial holding instruments. An account can be interest bearing.
  
- [FH account](/common-data-model/schema/core/industrycommon/financialservices/retailbankingcoredatamodel/fh_account) - A deposit account holding that allows the holder to make deposits and withdrawals through financial holding instruments. An account can be interest bearing.
  
- [Financial holding instrument](/common-data-model/schema/core/industrycommon/financialservices/retailbankingcoredatamodel/financialholdinginstrument) - A deposit account holding that allows the holder to make deposits and withdrawals through financial holding instruments. An account can be interest bearing.
  
- [FI direct debit](/common-data-model/schema/core/industrycommon/financialservices/retailbankingcoredatamodel/fi_directdebit) - An automated payment system whereby an account holder authorizes a creditor to debit the customer's bank account at regular intervals.
  
- [FI standing order](/common-data-model/schema/core/industrycommon/financialservices/retailbankingcoredatamodel/fi_standingorder) - An instruction order from an account holder for a set amount of money to be removed from an account at regular intervals and then paid to or transferred to another account.
  
- [FI card](/common-data-model/schema/core/industrycommon/financialservices/retailbankingcoredatamodel/fi_card) - An instruction order from an account holder for a set amount of money to be removed from an account at regular intervals and then paid to or transferred to another account.
  
- [FI overdraft](/common-data-model/schema/core/industrycommon/financialservices/retailbankingcoredatamodel/fi_overdraft) - An extension of credit that is associated with a checking account, allowing the account holder to continue withdrawing funds when an account reaches zero.
  
- [Customer financial holding](/common-data-model/schema/core/industrycommon/financialservices/retailbankingcoredatamodel/customerfinancialholding) - Financial holdings that are owned by the customer.


> [!div class="mx-imgBorder"]
> [![Screenshot of the financial data tables.](../media/financial-data.png)](../media/financial-data.png#lightbox)

## Task 4: Explore connections data tables and relationships

In this task, you'll explore the main tables that are related to customer connections, including groups (such as households) and relationships. Select each table name to navigate to the Microsoft Docs page that provides details about each table.

### Connections data table definitions

Definitions for the Connections data table are as follows:

- [Group](/common-data-model/schema/core/industrycommon/financialservices/retailbankingcoredatamodel/group/?azure-portal=true) - An association of several customers that allows, for example, the representation of households.

- [Group member](/common-data-model/schema/core/industrycommon/financialservices/retailbankingcoredatamodel/groupmember/?azure-portal=true) - An association between a customer and a group.
  
- [Group Financial Holding](/common-data-model/schema/core/industrycommon/financialservices/retailbankingcoredatamodel/groupfinancialholding/?azure-portal=true) - Financial holdings that are associated with a group that are to be included in the group's total assets and liabilities.
  
- [Relationship](/common-data-model/schema/core/industrycommon/financialservices/retailbankingcoredatamodel/relationship/?azure-portal=true) - Denotes an association between one contact to another (not as part of the larger group) where a direct association of finances doesn't necessarily exist, such as a spouse, lawyer, child, or grandparent.


> [!div class="mx-imgBorder"]
> [![Screenshot of the connections data tables.](../media/connections.png)](../media/connections.png#lightbox)