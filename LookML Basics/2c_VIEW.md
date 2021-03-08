A **View** file defines a list of fields (dimensions or measures) and their relationship to an underlying table or derived table. In LookML a view generally mention an underlying database table, but it can also represent a derived table.

A **View** likely join to other views. The relation between views is typically defined as part of an Explore declaration in a model file.

In Looker, view names appear at the front of dimension and measure names in the data table. This makes it clear which view the field belongs to in the tool as shown below ::

<img src="/Images/LookML_View_Names.png">

A **View** is stored in a **" .view.lkml "** file. 

The **Common Form** of a **View** declaration is shown below ::

<img src="/Images/LookML_View_Declaration.png">
