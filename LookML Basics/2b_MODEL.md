A **Model** is a customized portal within the database, designed to provide *very meaningful* data exploration for particular business users. Many models can exist for the same database connection in a single LookML project. Each model can reveal different data to different users. 
For example, sales agents need different data than company executives, so we would likely to develop 2 models to provide outlook of the database applicable for each user.

In Looker, queries are grouped by the model to which they belong. We see models listed under the **Explore** menu in the tool.

A **Model** file defines the database to connect and also defines a group of Explores for that connection. By agreement each file declares exactly one model and, in new LookML, model filenames end in **" .model.lkml. "** The name of the model file controls the name that displays in Looker.

The **Common Form** of a model declaration in LookML is shown below::

<img src="/Images/LookML_Model_Declaration.png" width="350" height="300">
