An **Explore** is a view that users can query. We can imagine of the **Explore** as a starting point for a query, or in SQL terms, as the FROM in a SQL statement. 
Not all views are Explores, because not all views express an entity of importance. 

For instance, a *States view* should get in touch to a lookup table for *state names* which doesn’t permit an Explore, because business users never need to query it directly. On the other hand, business users likely want a way to query an *Orders view*, and so defining an Explore for Orders makes sense.

An explore declaration identifies the join connections to other views. Continuing with the previous instance , the *Orders view* might join the *States view*, knowing the state in which a sale occurred. Dig into **Joins** for more detail.

In Looker, users can see Explores listed in the Explore menu:

<img src="/Images/LookML_Explore_inTool.png" width=200 height=300>

Based on protocol, **Explores** are declared in the model file. The example below shows the declaration for an **orders** Explore for an e-commerce database. The views *orders* and *customers* are defined away, in their own view files.

Example **Explore** declaration:

<img src="/Images/LookML_Explore_Declaration.png">

**"Explore" attach an existing view to the Explore menu of Looker. Even though an explore can be written inside of a view file, it is practically best practice to write it within a model file instead.**
