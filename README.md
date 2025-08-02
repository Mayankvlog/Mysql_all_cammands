# Mysql_all_cammands

1. Database Management

These commands are used for creating, selecting, and deleting entire databases.

    CREATE DATABASE [database_name];: Creates a new, empty database.

    DROP DATABASE [database_name];: Permanently deletes a database. Use with caution.

    SHOW DATABASES;: Lists all databases on the server.

    USE [database_name];: Selects a database to work with. All subsequent commands will apply to this database until you select another one.

2. Table Management

After selecting a database, these commands are used to create, modify, and delete tables.

    CREATE TABLE [table_name] (column1 datatype, column2 datatype, ...);: Creates a new table with specified columns and data types.

    ALTER TABLE [table_name] ADD [column_name] [datatype];: Adds a new column to an existing table.

    ALTER TABLE [table_name] DROP COLUMN [column_name];: Deletes a column from a table.

    DROP TABLE [table_name];: Permanently deletes a table and all its data.

    SHOW TABLES;: Lists all tables within the currently selected database.

    DESCRIBE [table_name];: Shows the structure of a table, including column names and data types.

3. Data Manipulation

These are the core commands for performing CRUD (Create, Read, Update, Delete) operations on data within your tables.

    INSERT INTO [table_name] (column1, column2, ...) VALUES (value1, value2, ...);: Inserts a new row of data into a table.

    SELECT [column1, column2, ...] FROM [table_name];: Retrieves data from a table.

        SELECT * FROM [table_name]; selects all columns.

    UPDATE [table_name] SET [column1] = [new_value] WHERE [condition];: Modifies existing data in a table. The WHERE clause is crucial to prevent updating all rows.

    DELETE FROM [table_name] WHERE [condition];: Deletes rows from a table. The WHERE clause is essential to avoid deleting all data.

4. Querying and Filtering

These commands are used to write more complex and specific SELECT statements.

    WHERE [condition]: Filters records based on a condition.

        Example: SELECT * FROM users WHERE age > 30;

    ORDER BY [column] ASC|DESC: Sorts the result set by a specific column in ascending or descending order.

        Example: SELECT name, age FROM users ORDER BY age DESC;

    GROUP BY [column]: Groups rows that have the same values into summary rows. Often used with aggregate functions like COUNT(), SUM(), AVG().

        Example: SELECT department, COUNT(*) FROM employees GROUP BY department;

    JOIN: Combines rows from two or more tables based on a related column.

        INNER JOIN: Returns records that have matching values in both tables.

        LEFT JOIN: Returns all records from the left table, and the matched records from the right table.

        Example: SELECT Orders.OrderID, Customers.CustomerName FROM Orders INNER JOIN Customers ON Orders.CustomerID = Customers.CustomerID;
