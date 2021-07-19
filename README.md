# murach_php_and_mysql_ch16 #
Murach's PHP and MYSQL (3rd Edition), Chapter 16 Exercises

## Exercise 16-1 Create a database diagram from a SQL script ##
In this exercise, you can use MySQL Workbench to create a database diagram for the my_guitar_shop2 database.

1. If necessary, install MySQL Workbench.
2.  Start MySQL Workbench.
3. Start a new model and a new diagram within that model.
4. Use the Reverse Engineer MySQL Create Script command to reverse engineer a diagram from this SQL script file.
**htdocs/book_apps/_create_db/my_guitar_shop2.sql**
5. Look on the left side of the window until you find the seven tables that were created. Drag all seven tables from the catalog tree to the diagram.
6. Double-click the Products table to display a pane across the bottom of the window. Click the Columns tab to review the column definitions for that table. Then, click the close button on the Products tab to close the pane.
7. Add the arrows that show these relationships, arranging the tables as necessary.

    |Primary key|Foreign key|
    |-|-|
    |customerID (customers)|customerID (orders)|
    |customerID (customers)|customerID (address)|
    |orderID (orders)|orderID (orderItems)|
    |productID (products)|productID (orderItems)|
    |categoryID (orderItems)|categoryID (products)|

    To do that, click the "Place a relationship using existing columns" button, click the column for the foreign key, and click the column for the primary key. Note how this identifies the foreign keys in the tables. If you make a mistake, you can right-click on the relationship arrow to delete it, but be sure not to delete the foreign key columns when you're asked if you want to do that.
8. Save the diagram with a name of my_guitar_shop3.mwb.
9. When you're done, review the diagram. There should be a one-to-many relationship between six of the tables. However, the administrators table is a supporting table that isn't related to any of the other tables.

## Exercise 16-2 Create some simple database designs ##
In this exercise, you can use your preferred database design tool. If you don't already have a preference, we recommend using MySQL Workbench.

1. Create a diagram for a database of music albums created by music artists. Each artist may have one or more albums, and each album may have one or more tracks. Keep track of this data: artist name, album name, album release date, track name, and track time.
2. Create a diagram for a database of members of groups within an association. Assume that each member can belong to any number of groups and that each group can have any number of members. Keep track of this data: member name, member email address, member phone number, group name, and group description.
