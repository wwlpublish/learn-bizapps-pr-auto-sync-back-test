Dataverse supports an auditing capability where table and column data changes within an organization can be recorded over time for use in analysis and reporting purposes. Auditing is supported on all custom and most customizable tables and columns. Auditing is not supported on table or column definition changes, retrieve operations, export operations, or during authentication. 

## Key concepts

The following bullets identify some key auditing concepts:

- You can enable or disable auditing at the organization, table, and column levels. If auditing is not enabled at the organization level, auditing of tables and columns, even if it is enabled, does not occur. By default, auditing is enabled on all auditable table columns, but is disabled at the table and organization level.

- The ability to retrieve and display the audit history is restricted to users who have certain security privileges: View Audit History, and View Audit Summary. There are also privileges specific to partitions: View Audit Partitions, and Delete Audit Partitions. See the specific message request documentation for information about the required privileges for each message.

- Audited data changes are stored in records of the audit table.

### Configure tables and columns for auditing

There are three levels where auditing can be configured: organization, table, and column. The organization level is the highest level, followed by the table level, and finally the column level. For column auditing to take place, auditing must be enabled at the column, table, and organization levels. For table auditing to take place, auditing must be enabled at the table and organization levels.

There is a slight difference in how auditing is enabled or disable for an organization compared to a table or column. You enable or disable auditing at the organization level by setting a particular column value of the organization record. However, for tables and columns, you set a property value of the table or column definition.

A user must be assigned the System Administrator or System Customizer role to enable or disable auditing.

### Enabling auditing

**By setting the IsAuditEnabled property of a table’s definition and the IsAuditEnabled property** of each desired column’s definition to true, data changes to records of those tables can be logged by the platform. However, when enabling auditing on a table, all of the table’s columns are enabled for auditing by default. You can explicitly disable auditing on any or all of the columns as needed. The IsAuditEnabled property can be set when the table or column definition is created or updated through the following requests: CreateEntityRequest, UpdateEntityRequest, CreateAttributeRequest, UpdateAttributeRequest.

In addition, auditing is enabled at the organization level by setting the IsAuditEnabled column value of the target organization record to true.

### Disabling auditing 

To disable auditing, set IsAuditEnabled, as described previously, to false. Publish the table customizations if you have disabled auditing on any columns. You can disable auditing for a whole organization by setting the IsAuditEnabled column to false in the target organization’s record.