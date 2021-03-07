LookML project made up of different concepts, starting from very top level:

LookML Project is collection of LookML files which describes the set of related **Models, Views, Explores** and optionally LookML dashboards.
    **Model** file specifies connection to a single database, multiple model can exist to a same database connection in a single LookML project.
    Each model can explore different data to different users. 
    For instance, Sales agent needs different data than company excecutives might, so we would develop 2 models to offer views of the database accordingly to each kind of user.

   Within **Models**, we define our **Explores** : Explores are interactive pages where users can build their own queries by choosing fields, applying filters and so on.
                Once an Explores are defined in the LookML, it can be seen in **Explore** menu. In Sql terms, Explore is the **From** clause of a query. 
                To Start building Explores, we first need to define some **Views**. 
                Once some Views has been established - we can use **Joins** which are defined in **Explores** to try multiple views to single explore.
                Joining views like this allows our users to explore data from multiple data tables at the same time.
   
   Within a **View**, most common types of fields are **Dimensions and Measures**.
                In Looker, Dimensions are appeared in the **Group BY** and **SELECT** clauses of the SQL that Looker generates.
                A **Dimension** can be either *COLUMN* in the underlying table or *COMPUTED VALUE* based on other fields.
                A **Measure** is where we define *AGGREGATES* like Max, Min, Sum, Count and any other SQL aggregate our database can perform.
                  *Measure* can also perform simple transformations on other measures. 
                In addition to *Dimensions* and *Measures* , we can also use LookML to specify other type of fields like *Time-Based Fields* or *Filters*.

   All fields defined in the LookML, will appear in the users *Field Picker* in the **Explore**, Once they pushed to production. 
   Users can use the fields to run their own queries without needing to know SQL. 
   Other file types we may see in our LookML project include *LookML Dashboards* and project *manifest*(manifest.lkml) files. 
       Project **Manifest** files are used for project level settings like listing files for other projects for import and specifying *Model* localization settings.
       Each Project can only have *One Manifest File*. When using Folders to organize LookML files, be sure that manifest file (*{} Manifest.lkml*) is kept at the *root level* at        the projects directory structure.
       LookML **Dashboard** files are stored as version controlled files associated with the Project. These *Dashboards* are YAML(Yet Another Markup Language / YAML Ain't Markup Language) based and defined inside the LookML by a developer.
       
**DERIVED TABLES**::
    As opposed to regular view, that pulls values directly from a database table, *Derived tables* pulls values from the results of a SQL query. 
    In Looker, Derived tables are comparable to SQL concepts of *Materialized Views, Common table expressions and Subqueries*. 
    A Derived table is exposed as its own views and defines *Dimensions* and *Measures* in same manner as conventional view.
    The View for the Derived table can be queried and joined into other views just like any other view.
