NOTE: ` sql is not case sensitive and after ever perticular statement semicolon is compulsory`

1.  create

        *To create a database or table.

        create database [name of database];
        create tables [table name](fields);

        *To use a perticular database

        use [name of database];

2.  show

        *To check list of databases / tables

        show databases;
        show tables;

        *To check list of fields in tables.

        show fields from [table name];

3.  select

        *To see table data of all field.

        select * from [table name];

        *To see table data of particular field or column.

        select [column name] from [table name];

    Distinct

        *To select unique values of all / certain field.

        select distinct * from [table name];
        select distinct [column name] from [table name];

        *To select all the enter of particular field data

        select * form [table name] where [field name='value to search'];

        *To the limited amount data from field of table

        select * from [table name] limit [input number] ;

4.  `and, or, not`

        *To these are used for multiple condition for checking data.

        select * from [table name] where [field name='value to search] and [field name = 'value to search];
        select * from [table name] where [field name='value to search] or [field name = 'value to search];
        select * from [table name] where [field name='value to search] and not [field name = 'value to search];

    NOTE :- here and will check both the condition in a row
    and or will give result of both as well as only one if another one is not there
    at last "not" is used with "and" not with 'or'.

5.  ASCENDING | DESCENDING

        *To sort the result in ascending or descending order use "order by".

        select * from [table name] order by [field name] asc|desc;

        *for multiple.

        select \* from [table name] order by [field name],[field name] asc|desc;

6.  INSERT INTO

        *To insert data for a particular field in a table.

        insert into [table name]("field_name_1","field_name_2") values("value_for_field_name_1","value_for_field_name_2");

        *To insert data to all the field no need to specify field_name.

        insert into [table name] values("values","should","be","inside_invert_comma");

    NOTE :- remember the order when adding data at all field without defining the table structure of pre defined table.

7.  UPDATE

        *To update or modify the existing record in a tabe.

        update [table name]
        set [field_name = value]
        where [field name = "value to search"];

    NOTE :- if you specify a field which is common in all rows of a table it will update that all.

    WARNING :- If you don't use the where clause all rows of that certain field will updated and your responsible for that messed-up data.

8.  DELETE

        *To delete a particular record.

        delete from [field_name]
        where [field name = "value to search"];

    WARNING :- Always specify the where clause unless you want to delete whole data from a particular table.

9.  SQL TOP, LIMIT and [ FETCH FIRST or ROWNUM ]

        => This is for sql server / access.
        select top 3 * from [table_name];

        => This is for MySql

        select * from table
        limit 20 or [you want to see how many rows];

        => This is for Oracle.

        select * from [ table name ]
        fetch first 3 rows only;

10. Min and Max
        
        To check the smallest value use min().

        select min(Field_name) 
        from table_name;

        To check the largest value use max().

        select max(Field_name)
        from table_name;

    NOTE :- You can use "where" clause to check "min | max" value for specific.

11. Count(), Avg(), Sum()

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

    NOTE :- Count() function works for both string and floats because it count rows not data inside fields.✌

12. Like
        
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
    NOTE :- if you use "NOT" operator with "LIKE" operator means "NOT LIKE" you will get the alternate result of the above written statment's.

13. Wildcards
        
        The WILDCARD characters used in with LIKE operator and LIKE operator is used with WHERE clause.
    Wildcard used in ms access            
*       * 	Represents zero or more characters       	                   bl* finds bl, black, blue, and blob
*       ? 	Represents a single character 	                               h?t finds hot, hat, and hit
*       [] 	Represents any single character within the brackets 	       h[oa]t finds hot and hat, but not hit
*       ! 	Represents any character not in the brackets                   h[!oa]t finds hit, but not hot and hat
*       - 	Represents any single character within the specified range 	   c[a-b]t finds cat and cbt
*       # 	Represents any single numeric character 	                   2#5 finds 205, 215, 225, 235, 245, 255, 265, 275, 285, and 295
    Wildcard used in sql server
*       % 	Represents zero or more characters 	                                bl% finds bl, black, blue, and blob
*       _ 	Represents a single character 	                                    h_t finds hot, hat, and hit
*       [] 	Represents any single character within the brackets 	            h[oa]t finds hot and hat, but not hit
*       ^ 	Represents any character not in the brackets 	                    h[^oa]t finds hit, but not hot and hat
*       - 	Represents any single character within the specified range 	        c[a-b]t finds cat and cbt

14. IN 

        The IN operator allows you to specify multiple values in a WHERE clause.
        The IN operator is a shorthand for multiple OR conditions.

        IN syntax:

        SELECT column_name(s)
        FROM table_name
        WHERE column_name IN (value1, value2, ...);

        OR:

        SELECT column_name(s)
        FROM table_name
        WHERE column_name IN (SELECT STATEMENT); 

15. Between

        The BETWEEN operator selects values within a given range.

        SELECT column_name(s)
        FROM table_name
        WHERE column_name BETWEEN value1 AND value2;
16. Aliases

        An alias only exists for the duration of that query.
        An alias is created with the AS keyword.
        it is a temporary name.

        Alias Column Syntax

        SELECT column_name AS alias_name
        FROM table_name;

        Alias Table Syntax
        
        SELECT column_name(s)
        FROM table_name AS alias_name;
17. Inner join

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
18. left join

        The LEFT JOIN keyword returns all records from the left table (table1), and the matching records from the right table (table2). The result is 0 records from the right side, if there is no match.

        SELECT column_name(s)
        FROM table1
        LEFT JOIN table2
        ON table1.column_name = table2.column_name;

    Note: The LEFT JOIN keyword returns all records from the left table (Customers), even if there are no matches in the right table (Orders).

19. right join

        The RIGHT JOIN keyword returns all records from the right table (table2), and the matching records from the left table (table1).SELECT column_name(s)
        
        FROM table1
        RIGHT JOIN table2
        ON table1.column_name = table2.column_name;

20. full join

        The FULL OUTER JOIN keyword returns all records when there is a match in left (table1) or right (table2) table records.
        Tip: FULL OUTER JOIN and FULL JOIN are the same.

        SELECT column_name(s)
        FROM table1
        FULL OUTER JOIN table2
        ON table1.column_name = table2.column_name
        WHERE condition;
21. self join

        A self join is a regular join, but the table is joined with itself.
        
        SELECT column_name(s)
        FROM table1 T1, table1 T2
        WHERE condition;
    T1 and T2 are different table aliases for the same table.

22. UNION

        The UNION operator is used to combine the result-set of two or more SELECT statements.

            Every SELECT statement within UNION must have the same number of columns
            The columns must also have similar data types
            The columns in every SELECT statement must also be in the same order

        SELECT column_name(s) FROM table1
        UNION
        SELECT column_name(s) FROM table2; 

        To allow duplicates use UNION ALL.
