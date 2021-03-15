**Views** carry fields, mainly **Dimensions and Measures**, which are the basic building blocks for Looker queries.

In Looker, a Dimension is a Categorical field and can be used to filter query results. 
It can be:
   + A Feature, which has a direct link to a column in an underlying table.
   + A Fact or numerical value.
   + A Derived value, calculated based on the values of other fields in a single row.

For example, **Dimensions** for a *Products view* might include features or columns like product name, product model, product color, product price, product created date, and product end-of-life date.

A **Measure** is a field that uses a SQL aggregate function, like COUNT, SUM, AVG, MIN, or MAX. Any field calculated based on the values of other measure values is also a measure. Measures can be used to filter grouped values. For example, measures for a *Sales view* might include total items sold (a count), total sale price (a sum), and average sale price (an average).

The behavior and expected values for a field depend on its declared type, such as string, number, or time. For measures, types include aggregate functions, such as sum and percent_of_previous. 

In Looker, **Dimensions and Measures** fields are listed on the *Explore* page when building and running queries:

<img src="/Images/LookML_Views-Dimensions&Measures.png" width=800 hieght=700>

As per protocol, fields are declared as part of the view they belong to, stored in a view file.

Below is the example declarations of dimensions and measures:

<img src="/Images/LookML_Dim&Meas_DeclarationEg.png" width=450 hieght=500>

