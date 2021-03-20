**+Derived Tables: +**

A **Derived table** is a table containing values from other tables; it is retrieved as though it has a physical table with its own set of columns. A derived table is exposed as its own view using the derived_table parameter, and defines dimensions and measures in the same manner as conventional views. The view for a derived table can be queried and joined into other views, just like any other view.

Derived tables are created by using the *derived_table* parameter in a *view* declaration.

*+Using Derived Tables for Facts Tables: +*

In Looker, a common use for derived tables is to present a facts table, which calculates facts about an entity based on values derived from other views. For example, a common need is to analyze user traits based on past orders or actions, and then report, sort, and filter those traits like any other facet of a user.

Case: A Derived Table for User Order Facts

Consider an *e-commerce dataset* with a *users table* holding customer data and an *orders table* holding details about customer orders. A derived table can be used to create a *user_orders_facts table*, containing user-centric facts such as lifetime total revenue for a user, which doesn’t physically exist in the underlying tables. More example columns are number of lifetime orders, latest order date, whether the user placed multiple orders, and so on. See the picture below.

<img src="/Images/LookML_DRTbls&FCTbls.png">

Since the primary key for the fact table(user_orders_facts table) is user_id, the view can be joined one-to-one with the users Explore(users table), allowing rich query possibilities. An example is shown below:

<img src="/Images/LookML_user_order_factsEg.png" width=500 hieght=600>

*+Persistent Derived Tables: +*

There are repeated cases where calculating a derived table takes a significant amount of time. To avoid running an costly derived-table calculation more often than required, Looker can cache (or “persist”) the data in a derived table. **A persistent derived table (PDT) is simply a derived table that is automatically regenerated.** 

Persistent derived tables use a scratch table in the database to save results, which requires additional database configuration depending on the type of database.
