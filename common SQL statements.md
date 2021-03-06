
![mysql](https://i0.wp.com/learn.onemonth.com/wp-content/uploads/2019/07/image2-1.png?fit=600%2C315&ssl=1)

### `NOTE` : sql is not case sensitive and after ever perticular statement semicolon is compulsory

1.  create
***
```
        *To create a database or table.

        create database [name of database];
        create tables [table name](fields);

        *To use a perticular database

        use [name of database];

```
***
2.  show
***
```
        *To check list of databases / tables

        show databases;
        show tables;

        *To check list of fields in tables.

        show fields from [table name];

```
***
3.  select
***
```
        *To see table data of all field.

        select * from [table name];

        *To see table data of particular field or column.

        select [column name] from [table name];
```

#### Distinct
```
        *To select unique values of all / certain field.

        select distinct * from [table name];
        select distinct [column name] from [table name];

        *To select all the enter of particular field data

        select * form [table name] where [field name='value to search'];

        *To the limited amount data from field of table

        select * from [table name] limit [input number] ;

```
***
4.  and, or, not
***
```
        *To these are used for multiple condition for checking data.

        select * from [table name] where [field name='value to search] and [field name = 'value to search];
        select * from [table name] where [field name='value to search] or [field name = 'value to search];
        select * from [table name] where [field name='value to search] and not [field name = 'value to search];

    `NOTE` :- here and will check both the condition in a row
    and or will give result of both as well as only one if another one is not there
    at last "not" is used with "and" not with 'or'.

```
***
5.  ASCENDING | DESCENDING
***
```
        *To sort the result in ascending or descending order use "order by".

        select * from [table name] order by [field name] asc|desc;

        *for multiple.

        select \* from [table name] order by [field name],[field name] asc|desc;

```
***
6.  INSERT INTO
***
```
        *To insert data for a particular field in a table.

        insert into [table name]("field_name_1","field_name_2") values("value_for_field_name_1","value_for_field_name_2");

        *To insert data to all the field no need to specify field_name.

        insert into [table name] values("values","should","be","inside_invert_comma");

```
`NOTE` :- remember the order when adding data at all field without defining the table structure of pre defined table.

***
7.  UPDATE
***
```
        *To update or modify the existing record in a tabe.

        update [table name]
        set [field_name = value]
        where [field name = "value to search"];
```

`NOTE` :- if you specify a field which is common in all rows of a table it will update that all.


`WARNING` :- If you don't use the where clause all rows of that certain field will updated and your responsible for that
messed-up data.


***
8.  DELETE
***
```
        *To delete a particular record.

        delete from [field_name]
        where [field name = "value to search"];

    `WARNING` :- Always specify the where clause unless you want to delete whole data from a particular table.

```
***
9.  SQL TOP, LIMIT and [ FETCH FIRST or ROWNUM ]
***
```
        => This is for sql server / access.
        select top 3 * from [table_name];

        => This is for MySql

        select * from table
        limit 20 or [you want to see how many rows];

        => This is for Oracle.

        select * from [ table name ]
        fetch first 3 rows only;

```
***
10. Min and Max
***
```
        To check the smallest value use min().

        select min(Field_name)
        from table_name;

        To check the largest value use max().

        select max(Field_name)
        from table_name;

    `NOTE` :- You can use "where" clause to check "min | max" value for specific.

```
***
11. Count(), Avg(), Sum()
***
```
        To count rows in the field use count()

        select count(field_name)
        from table_name
        where field_name='value to search';

        To get Average floats | int use avg()

        select avg(field_name)
        from table_name
        where field_name='value to search';

        To get addition of floats | int use sum()

        select sum(field_name)
        from table_name
        where field_name='value to search';

    `NOTE` :- Count() function works for both string and floats because it count rows not data inside fields.???

```
***
12. Like
***
```
        Like operator is used with where clause

        To select string start with an alphabet

        select * from table_name
        where field_name like 'a%';

        To select string end with an alphabet

        select * from table_name
        where field_name like '%a';

        To select string with an alphabet in any position

        select * from table_name
        where field_name like '%a%';

        To select the string with an alphbet in second position

        select * from table_name
        where field_name like '_a%';

        To select the string starts with an alphabet and are at least 3 characters in length

        select * from table_name
        where field_name like 'a__%';

        To select with string with an alphabet and end with an alphabet

        select * from table_name
        where field_name like 'a%d';

        there is NOT LIKE

    `NOTE` :- if you use "NOT" operator with "LIKE" operator means "NOT LIKE" you will get the alternate result of the above written statment's.

```
***
13. Wildcards
***
```
    The WILDCARD characters used in with LIKE operator and LIKE operator is used with WHERE clause.
    Wildcard used in ms access
```

|Sr No.|Symbol|Description|Example|
|--- |--- |--- |--- |
|1|     * 	|Represents zero or more characters       	                    |bl* finds bl, black, blue, and blob.|
|2|     ? 	|Represents a single character 	                                |h?t finds hot, hat, and hit.|
|3|     [] 	|Represents any single character within the brackets 	        |h[oa]t finds hot and hat, but not hit.|
|4|     ! 	|Represents any character not in the brackets                   h[!oa]t finds hit, but not hot and hat.|
|5|     - 	|Represents any single character within the specified range 	|c[a-b]t finds cat and cbt.|
|6|     # 	|Represents any single numeric character 	                    |2#5 finds 205, 215, 225, 235, 245, 255,|
|7|         |                                                               |265, 275, 285, and 295  Wildcard used |
|8|         |                                                               |in sql server.|
|9|     % 	|Represents zero or more characters 	                        |bl% finds bl, black, blue, and blob.|
|10|     _ 	|Represents a single character 	                                |h_t finds hot, hat, and hit.|
|11|     [] 	|Represents any single character within the brackets 	        |h[oa]t finds hot and hat, but not hit.|
|12|     ^ 	|Represents any character not in the brackets 	                |h[^oa]t finds hit, but not hot and hat.|
|13|     - 	|Represents any single character within the specified range 	|c[a-b]t finds cat and cbt.|


***
14. IN
***
```
The IN operator allows you to specify multiple values in a WHERE clause.The IN operator is a shorthand for multiple OR conditions.

        IN syntax:

        SELECT column_name(s)
        FROM table_name
        WHERE column_name IN (value1, value2, ...);

        OR:

        SELECT column_name(s)
        FROM table_name
        WHERE column_name IN (SELECT STATEMENT);

```
***
15. Between
***
```
        The BETWEEN operator selects values within a given range.

        SELECT column_name(s)
        FROM table_name
        WHERE column_name BETWEEN value1 AND value2;

```
***
16. Aliases
***
```
        An alias only exists for the duration of that query.
        An alias is created with the AS keyword.
        it is a temporary name.

        Alias Column Syntax

        SELECT column_name AS alias_name
        FROM table_name;

        Alias Table Syntax

        SELECT column_name(s)
        FROM table_name AS alias_name;

```
***
17. Inner join
***
```
        The INNER JOIN keyword selects records that have matching values in both tables.

    Two table join

        SELECT column_name(s)
        FROM table1
        INNER JOIN table2
        ON table1.column_name = table2.column_name;

    Three table join

        SELECT Orders.OrderID, Customers.CustomerName, Shippers.ShipperName
        FROM ((Orders
        INNER JOIN Customers ON Orders.CustomerID = Customers.CustomerID)
        INNER JOIN Shippers ON Orders.ShipperID = Shippers.ShipperID);

```
***
18. left join
***
```
        The LEFT JOIN keyword returns all records from the left table (table1), and the matching records from the right table (table2). The result is 0 records from the right side, if there is no match.

        SELECT column_name(s)
        FROM table1
        LEFT JOIN table2
        ON table1.column_name = table2.column_name;

    `Note`: The LEFT JOIN keyword returns all records from the left table (Customers), even if there are no matches in the right table (Orders).

```
***
19. right join
***
```
        The RIGHT JOIN keyword returns all records from the right table (table2), and the matching records from the left table (table1).SELECT column_name(s)

        FROM table1
        RIGHT JOIN table2
        ON table1.column_name = table2.column_name;

```
***
20. Full join
***
```
        The FULL OUTER JOIN keyword returns all records when there is a match in left (table1) or right (table2) table records.
        Tip: FULL OUTER JOIN and FULL JOIN are the same.

        SELECT column_name(s)
        FROM table1
        FULL OUTER JOIN table2
        ON table1.column_name = table2.column_name
        WHERE condition;

```
***
21. Self join
***
```
        A self join is a regular join, but the table is joined with itself.

        SELECT column_name(s)
        FROM table1 T1, table1 T2
        WHERE condition;

    T1 and T2 are different table aliases for the same table.

```
***
22. UNION
***
```
        The UNION operator is used to combine the result-set of two or more SELECT statements.

            Every SELECT statement within UNION must have the same number of columns
            The columns must also have similar data types
            The columns in every SELECT statement must also be in the same order

        SELECT column_name(s) FROM table1
        UNION
        SELECT column_name(s) FROM table2;

        To allow duplicates use UNION ALL.

```
***
23. Group by
***
```
        The GROUP BY statement groups rows that have the same values into summary rows, like "find the number of customers in each country".
        The GROUP BY statement is often used with aggregate functions (COUNT(), MAX(), MIN(), SUM(), AVG()) to group the result-set by one or more columns.

        SELECT column_name(s)
        FROM table_name
        WHERE condition
        GROUP BY column_name(s)
        ORDER BY column_name(s);

```
***
24. Having
***
```
        The HAVING clause was added to SQL because the WHERE keyword cannot be used with aggregate functions.

        SELECT column_name(s)
        FROM table_name
        WHERE condition
        GROUP BY column_name(s)
        HAVING condition
        ORDER BY column_name(s);

```
***
25. Exists
***
```
        The EXISTS operator is used to test for the existence of any record in a subquery.

        The EXISTS operator returns TRUE if the subquery returns one or more records.

        SELECT column_name(s)
        FROM table_name
        WHERE EXISTS
        (SELECT column_name FROM table_name WHERE condition);

```
***
26. Any
***
```
        The ANY operator:

        returns a boolean value as a result
        returns TRUE if ANY of the subquery values meet the condition

        ANY means that the condition will be true if the operation is true for any of the values in the range.

        SELECT column_name(s)
        FROM table_name
        WHERE column_name operator ANY
        (SELECT column_name
        FROM table_name
        WHERE condition);

```
***
27. All
***
```
         The ALL operator:

         returns a boolean value as a result
         returns TRUE if ALL of the subquery values meet the condition
         is used with SELECT, WHERE and HAVING statements

         ALL means that the condition will be true only if the operation is true for all values in the range.

         SELECT ALL column_name(s)
         FROM table_name
         WHERE condition;

         ALL Syntax With WHERE or HAVING

         SELECT column_name(s)
         FROM table_name
         WHERE column_name operator ALL
         (SELECT column_name
         FROM table_name
         WHERE condition);

    `NOTE` :- there is an another operator which is "ANY" same as "ALL"

```
***
28. Select into
***
```
        The SELECT INTO statement copies data from one table into a new table.

        Copy all columns into a new table:

        SELECT *
        INTO newtable [IN externaldb]
        FROM oldtable
        WHERE condition;

```
***
29. insert into
***
```
        The INSERT INTO SELECT statement copies data from one table and inserts it into another table.

        The INSERT INTO SELECT statement requires that the data types in source and target tables match.

     `Note`: The existing records in the target table are unaffected.

        INSERT INTO SELECT Syntax

        Copy all columns from one table to another table:

        INSERT INTO table2
        SELECT * FROM table1
        WHERE condition;

        Copy only some columns from one table into another table:

        INSERT INTO table2 (column1, column2, column3, ...)
        SELECT column1, column2, column3, ...
        FROM table1
        WHERE condition;

```
***
30. Case
***
```
        The SQL CASE Statement

        The CASE statement goes through conditions and returns a value when the first condition is met (like an if-then-else statement). So, once a condition is true, it will stop reading and return the result. If no conditions are true, it returns the value in the ELSE clause.

        If there is no ELSE part and no conditions are true, it returns NULL.
        CASE Syntax
        CASE
            WHEN condition1 THEN result1
            WHEN condition2 THEN result2
            WHEN conditionN THEN resultN
            ELSE result
        END;

```
***
31. Null function
***
```
        Suppose that the "UnitsOnOrder" column is optional, and may contain NULL values.

        Look at the following SELECT statement:
        SELECT ProductName, UnitPrice * (UnitsInStock + UnitsOnOrder)
        FROM Products;

        if any of the "UnitsOnOrder" values are NULL, the result will be NULL.
        Solutions

        MySQL

        The MySQL IFNULL() function lets you return an alternative value if an expression is NULL:
        SELECT ProductName, UnitPrice * (UnitsInStock + IFNULL(UnitsOnOrder, 0))
        FROM Products;

        or we can use the COALESCE() function, like this:
        SELECT ProductName, UnitPrice * (UnitsInStock + COALESCE(UnitsOnOrder, 0))
        FROM Products;

        SQL Server

        The SQL Server ISNULL() function lets you return an alternative value when an expression is NULL:
        SELECT ProductName, UnitPrice * (UnitsInStock + ISNULL(UnitsOnOrder, 0))
        FROM Products;

        MS Access

        The MS Access IsNull() function returns TRUE (-1) if the expression is a null value, otherwise FALSE (0):
        SELECT ProductName, UnitPrice * (UnitsInStock + IIF(IsNull(UnitsOnOrder), 0, UnitsOnOrder))
        FROM Products;

        Oracle

        The Oracle NVL() function achieves the same result:
        SELECT ProductName, UnitPrice * (UnitsInStock + NVL(UnitsOnOrder, 0))
        FROM Products;

```
***
32. stored procedure
***
```
        What is a Stored Procedure?

        A stored procedure is a prepared SQL code that you can save, so the code can be reused over and over again.

        So if you have an SQL query that you write over and over again, save it as a stored procedure, and then just call it to execute it.

        You can also pass parameters to a stored procedure, so that the stored procedure can act based on the parameter value(s) that is passed.
        Stored Procedure Syntax
        CREATE PROCEDURE procedure_name
        AS
        sql_statement
        GO;
        Execute a Stored Procedure
        EXEC procedure_name;

        Stored Procedure Example

        The following SQL statement creates a stored procedure named "SelectAllCustomers" that selects all records from the "Customers" table:
        Example
        CREATE PROCEDURE SelectAllCustomers
        AS
        SELECT * FROM Customers
        GO;

        Execute the stored procedure above as follows:
        Example
        EXEC SelectAllCustomers;
        Stored Procedure With One Parameter

        The following SQL statement creates a stored procedure that selects Customers from a particular City from the "Customers" table:
        Example
        CREATE PROCEDURE SelectAllCustomers @City nvarchar(30)
        AS
        SELECT * FROM Customers WHERE City = @City
        GO;

        Execute the stored procedure above as follows:
        Example
        EXEC SelectAllCustomers @City = 'London';
        Stored Procedure With Multiple Parameters

        Setting up multiple parameters is very easy. Just list each parameter and the data type separated by a comma as shown below.

        The following SQL statement creates a stored procedure that selects Customers from a particular City with a particular PostalCode from the "Customers" table:
        Example
        CREATE PROCEDURE SelectAllCustomers @City nvarchar(30), @PostalCode nvarchar(10)
        AS
        SELECT * FROM Customers WHERE City = @City AND PostalCode = @PostalCode
        GO;

        Execute the stored procedure above as follows:
        Example
        EXEC SelectAllCustomers @City = 'London', @PostalCode = 'WA1 1DP';

 ```
 ***
