A **LookML project** is a group of LookML files which tells about a set of connected models, views, Explores, and (optionally) LookML dashboards.
We will generally find this hierarchy in a LookML project ::
      
   A **Model** contains information about which tables to use and how they should be joined together. Here we’ll normally define the Model, its Explores, and its Joins.

   A **View** contains information about how to access or calculate information from each table (or across multiple joined tables). Here we’ll usually define the View, its        dimensions and measures, and its field sets.

   An **Explore** is often defined within a Model file, but sometimes we need a separate Explore file for a derived table, or to extend or refine an Explore across models.

   A **Join** lets us combine data from multiple views.

   A **Manifest file** can contain instructions for using files imported from another project or for our project’s localization settings.

**In Looker**, we can access our projects under the Develop menu in the tool.

+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
**Where Do LookML Projects and Files Come From ??**
      
   When we create a new **Project**, Looker’s project generator creates a baseline set of files that we
   use as a template for building out the project. Very rarely, if ever, we will write a LookML file from scratch.
   
   Multiple **View** files, one file for every table in the database.
   
   One **Model** file. The model file declares an Explore for every view. 
   
   Each **Explore** declaration includes **Join** logic to join any view that Looker can control which is related to the Explore.
   
From here, we can filter the project by removing unwanted views and Explores and by adding custom dimensions and measures.
