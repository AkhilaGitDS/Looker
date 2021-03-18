**+Sets: +**

In Looker, a set is a list which means one category of fields that are used at once. Usually sets are used to specify which fields to show after a user drills down into data. Drill sets are specified on a field-by-field basis, so we get complete control over what data is displayed when a user clicks a value in a table or dashboard. Sets can also be used as a security feature to define groups of fields visible only to specific users.

Below illustration shows a set declaration in a view order_items, defining fields that list relevant details about a purchased item. *Note that the set references fields from other views by specifying scope.*

<img src="/Images/LookML_Set_DeclarationEg.png">


**+Drill Down: +**

In Looker, we can drill down on any fields that are set up that way when writing LookML. The fields to display for the new drill query are defined by a *Set*.
Drilling works in both query results tables and dashboards. Drilling starts a new query that is limited only to the value we clicked on. Drill actions is different for dimensions and measures:
+ When drilling on a *Dimension*, the new query filters on the drilled value. 
  Such as , if we click on a particular date in a query of customer orders by date, the new query will show orders only for that particular date.
+ When drilling on a *Measure*, the new query will show the dataset that contributed to the measure. 
  Such as, when drilling on a count, the new query will show the rows to calculate that count. When drilling on max, min, and average measures, drilling still shows all the rows     that contributed to that measure. This means that drilling on a max measure, for example, shows all the rows that were used to calculate the max value, not just a single row for   the max value.

