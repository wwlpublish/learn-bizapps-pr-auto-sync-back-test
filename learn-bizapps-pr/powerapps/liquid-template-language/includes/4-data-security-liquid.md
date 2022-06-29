Liquid extensions in Power Apps portals give portal makers access to Microsoft Dataverse. Table permissions govern all data that is accessed by Liquid objects and tags, and it's not possible to switch off this feature. It also makes the output dynamic because it varies with the current portal user, their web roles, and associated table permission records.

To improve rendering performance and alter the template in response to the current user's privileges, developers can assert particular access rights before implementing data retrieval. For example, instead of trying to access contact records, developers would check whether the user has Read privileges for the contact table and would then handle the response appropriately without retrieving the data.

Consider the following Liquid fragment:

```twig
{% if user %}
<p>
  {% assign account = entities.account[user.parentcustomerid.id] %}
  {% if account and account.permissions.can_read %}
    Company: {{account.name}}
  {% else %}
    Unknown company
  {% endif%}
</p>  
{% endif %}
```

In this example, the code:

- Displays data only if the user is signed in.
- Retrieves the parent account record.
- Checks that the account exists and that the user has permissions to read that record. The **Permissions** property of the **table** object returns the [Table Permissions](/power-apps/maker/portals/liquid/liquid-objects#table-permissions/?azure-portal=true) object that can be used to verify specific privileges.
- Displays the name of the account, if available; otherwise, it displays the "Unknown company" message.

You can test the code inside portals Studio and then browse to the site. Check the different values that are rendered by the code because of the maker privileges within portals Studio.

For more information, see [Work with Liquid templates](/power-apps/maker/portals/liquid/liquid-overview/?azure-portal=true).
