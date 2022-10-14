In situations where you don't want the standard evaluation behavior in Power BI, you can use the CALCULATE and/or USERELATIONSHIP functions. However, more circumstances exist where you don't want the standard behavior. One of those situations is when you have a semi-additive problem to resolve. Standard measures are simple concepts, where they might use the SUM, AVERAGE, MIN, and MAX functions. Thus far, you've been using SUM for the **Total Sales** measure.

Occasionally, summing a measure doesn't make sense, such as when you are performing inventory counts in a warehouse. For example, if on Monday, you have 100 mountain bikes, and on Tuesday you have 125 mountain bikes, you wouldn't want to add those together to indicate that you had 225 mountain bikes between those two days. In this circumstance, if you want to know your stock levels for March, you would need to tell Power BI not to add the measure but instead take the last value for the month of March and assign it to any visual.

You can use the CALCULATE function to complete this action, along with the LastDate function, as shown in the following example:

```
Last Inventory Count =
CALCULATE (
    SUM ( 'Warehouse'[Inventory Count] ),
    LASTDATE ( 'Date'[Date] ))
```

This approach will stop the SUM from crossing all dates. Instead, you will only use the SUM function on the last date of the time period, thus effectively creating a semi-additive measure.
