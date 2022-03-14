NOTE: ` sql is not case sensitive and after ever perticular statement semicolon is compulsory`

1.   create

         *To create a database or table.

          create database [name of database];
          create tables [table name](fields);

         *To use a perticular database

          use [name of database];

2.   show

         *To check list of databases / tables

          show databases;
          show tables;

         *To check list of fields in tables.

          show fields from [table name];

3.   select

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

4.   and, or, not 

            *To these are used for multiple condition for checking data.

            select * from [table name] where [field name='value to search] and [field name = 'value to search];
            select * from [table name] where [field name='value to search] or [field name = 'value to search];
            select * from [table name] where [field name='value to search] and not [field name = 'value to search];

    NOTE :- here and will check both the condition in a row
            and or will give result of both as well as only one if another one is not there
            at last "not" is used with "and" not with 'or'.

5.   ASCENDING | DESCENDING

         *To sort the result in ascending or descending order use "order by".

          select * from [table name] order by [field name] asc|desc;

         *for multiple.

          select \* from [table name] order by [field name],[field name] asc|desc;

6.   INSERT INTO

         *To insert data for a particular field in a table.

          insert into [table name]("field_name_1","field_name_2") values("value_for_field_name_1","value_for_field_name_2");

         *To insert data to all the field no need to specify field_name.

          insert into [table name] values("values","should","be","inside_invert_comma");

    NOTE :- remember the order when adding data at all field without defining the table structure of pre defined table.

7.   UPDATE

          *To update or modify the existing record in a tabe.

          update [table name]
          set [field_name = value]
          where [field name = "value to search"];

    NOTE :- if you specify a field which is common in all rows of a table it will update that all.

    WARNING :- If you don't use the where statment all rows of that certain field will updated and your responsible for that messed-up data.

8.   DELETE

          *To delete a particular record.
          
          delete from [field_name] 
          where [field name = "value to search"];

    WARNING :- Always specify the where statment unless you want to delete whole data from a particular table.

9.    *SQL TOP, LIMIT and [FETCH FIRST or ROWNUM]

          => This is for sql server / access 
          select top 3 * from [table_name];

          => This is for MySql
          select * from table
          limit 20 or [you want to see how many rows];

          => This is for Oracle.

     