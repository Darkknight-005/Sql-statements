 NOTE: `
    sql is not case sensitive 
    and after ever perticular statement semicolon is compulsory
`
                create 
*   
*       *To create a database or table
*   create database [name of database];
*   create tables [table name](fields);
*   
*       *To use a perticular database
*   use [name of database];

            show 
*       *To check list of databases / tables 
*   show databases;
*   show tables;
*   
*       *To check list of fields in tables
*   show fields from [table name];
*   

             select
*       *To see table data of all field 
*   select * from [table name];
*
*       *To see table of particular field or column
*   select [column name] from [table name];
*
*       *To select unique values of all / certain field
*   select distinct * from [table name];
*   select distinct [column name] from [table name];
*
*       *To select all the enter of particular field data 
*   select * form [table name] where [field name='value to search'];
*
*    *To the limited amount data from field of table
*   select * from [table name] limit [input number] ;
*   

         ' and , or , not ' 
*
*       *To these are used for multiple condition for checking data
*   select * from [table name] where [field name='value to search] and [field name = 'value to search];
*
*   select * from [table name] where [field name='value to search] or [field name = 'value to search];
*
*   select * from [table name] where [field name='value to search] and not [field name = 'value to search];
*       
*      note :- here and will check both the condition in a row
*              and or will give result of both as well as only one if another one is not there
*              at last "not" is used with "and" not with or 
*
*       {ascending | descending}
*
*       *To sort the result in ascending or descending order use "order by". 
*   select * from [table name] order by [field name] asc|desc;
*       *for multiple.
*   select * from [table name] order by [field name],[field name] asc|desc;
*
*       {insert into}
*
*       *To insert data for a particular field in a table
*   insert into [table name]( "field_name_1","field_name_2" ) values("value_for_field_name_1","value_for_field_name_2");
*
*       *To insert data to all the field no need to specify field_name
*   insert into [table name] values("values","should","be","inside_invert_comma");
*
*   note:- remember the order when adding data at all field without
*