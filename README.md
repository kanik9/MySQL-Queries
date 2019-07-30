# MySQL-Queries
In this files all types of MySQL Queries are present


If Nested Queries came than solve first those queries which are present in brackets
https://www.w3resource.com/mysql/subqueries/index.php







MySQL data type

"""
Properly defining the fields in a table is important to the overall optimization of your database. You should use only the type and size of field you really need to use. For example, do not define a field 10 characters wide, if you know you are only going to use 2 characters. These type of fields (or columns) are also referred to as data types, after the type of data you will be storing in those fields.

MySQL uses many different data types broken into three categories −

Numeric
Date and Time
String Types.
Let us now discuss them in detail.

Numeric Data Types
MySQL uses all the standard ANSI SQL numeric data types, so if you're coming to MySQL from a different database system, these definitions will look familiar to you.

The following list shows the common numeric data types and their descriptions −

INT − A normal-sized integer that can be signed or unsigned. If signed, the allowable range is from -2147483648 to 2147483647. If unsigned, the allowable range is from 0 to 4294967295. You can specify a width of up to 11 digits.

TINYINT − A very small integer that can be signed or unsigned. If signed, the allowable range is from -128 to 127. If unsigned, the allowable range is from 0 to 255. You can specify a width of up to 4 digits.

SMALLINT − A small integer that can be signed or unsigned. If signed, the allowable range is from -32768 to 32767. If unsigned, the allowable range is from 0 to 65535. You can specify a width of up to 5 digits.

MEDIUMINT − A medium-sized integer that can be signed or unsigned. If signed, the allowable range is from -8388608 to 8388607. If unsigned, the allowable range is from 0 to 16777215. You can specify a width of up to 9 digits.

BIGINT − A large integer that can be signed or unsigned. If signed, the allowable range is from -9223372036854775808 to 9223372036854775807. If unsigned, the allowable range is from 0 to 18446744073709551615. You can specify a width of up to 20 digits.

FLOAT(M,D) − A floating-point number that cannot be unsigned. You can define the display length (M) and the number of decimals (D). This is not required and will default to 10,2, where 2 is the number of decimals and 10 is the total number of digits (including decimals). Decimal precision can go to 24 places for a FLOAT.

DOUBLE(M,D) − A double precision floating-point number that cannot be unsigned. You can define the display length (M) and the number of decimals (D). This is not required and will default to 16,4, where 4 is the number of decimals. Decimal precision can go to 53 places for a DOUBLE. REAL is a synonym for DOUBLE.

DECIMAL(M,D) − An unpacked floating-point number that cannot be unsigned. In the unpacked decimals, each decimal corresponds to one byte. Defining the display length (M) and the number of decimals (D) is required. NUMERIC is a synonym for DECIMAL.

Date and Time Types
The MySQL date and time datatypes are as follows −

DATE − A date in YYYY-MM-DD format, between 1000-01-01 and 9999-12-31. For example, December 30th, 1973 would be stored as 1973-12-30.

DATETIME − A date and time combination in YYYY-MM-DD HH:MM:SS format, between 1000-01-01 00:00:00 and 9999-12-31 23:59:59. For example, 3:30 in the afternoon on December 30th, 1973 would be stored as 1973-12-30 15:30:00.

TIMESTAMP − A timestamp between midnight, January 1st, 1970 and sometime in 2037. This looks like the previous DATETIME format, only without the hyphens between numbers; 3:30 in the afternoon on December 30th, 1973 would be stored as 19731230153000 ( YYYYMMDDHHMMSS ).

TIME − Stores the time in a HH:MM:SS format.

YEAR(M) − Stores a year in a 2-digit or a 4-digit format. If the length is specified as 2 (for example YEAR(2)), YEAR can be between 1970 to 2069 (70 to 69). If the length is specified as 4, then YEAR can be 1901 to 2155. The default length is 4.

String Types
Although the numeric and date types are fun, most data you'll store will be in a string format. This list describes the common string datatypes in MySQL.

CHAR(M) − A fixed-length string between 1 and 255 characters in length (for example CHAR(5)), right-padded with spaces to the specified length when stored. Defining a length is not required, but the default is 1.

VARCHAR(M) − A variable-length string between 1 and 255 characters in length. For example, VARCHAR(25). You must define a length when creating a VARCHAR field.

BLOB or TEXT − A field with a maximum length of 65535 characters. BLOBs are "Binary Large Objects" and are used to store large amounts of binary data, such as images or other types of files. Fields defined as TEXT also hold large amounts of data. The difference between the two is that the sorts and comparisons on the stored data are case sensitive on BLOBs and are not case sensitive in TEXT fields. You do not specify a length with BLOB or TEXT.

TINYBLOB or TINYTEXT − A BLOB or TEXT column with a maximum length of 255 characters. You do not specify a length with TINYBLOB or TINYTEXT.

MEDIUMBLOB or MEDIUMTEXT − A BLOB or TEXT column with a maximum length of 16777215 characters. You do not specify a length with MEDIUMBLOB or MEDIUMTEXT.

LONGBLOB or LONGTEXT − A BLOB or TEXT column with a maximum length of 4294967295 characters. You do not specify a length with LONGBLOB or LONGTEXT.

ENUM − An enumeration, which is a fancy term for list. When defining an ENUM, you are creating a list of items from which the value must be selected (or it can be NULL). For example, if you wanted your field to contain "A" or "B" or "C", you would define your ENUM as ENUM ('A', 'B', 'C') and only those values (or NULL) could ever populate that field.
"""





MySQL WHERE clause

"""
We have seen the SQL SELECT command to fetch data from a MySQL table. We can use a conditional clause called the WHERE Clause to filter out the results. Using this WHERE clause, we can specify a selection criteria to select the required records from a table.

Syntax
The following code block has a generic SQL syntax of the SELECT command with the WHERE clause to fetch data from the MySQL table −

SELECT field1, field2,...fieldN table_name1, table_name2...
[WHERE condition1 [AND [OR]] condition2.....
You can use one or more tables separated by a comma to include various conditions using a WHERE clause, but the WHERE clause is an optional part of the SELECT command.

You can specify any condition using the WHERE clause.

You can specify more than one condition using the AND or the OR operators.

A WHERE clause can be used along with DELETE or UPDATE SQL command also to specify a condition.

The WHERE clause works like an if condition in any programming language. This clause is used to compare the given value with the field value available in a MySQL table. If the given value from outside is equal to the available field value in the MySQL table, then it returns that row.

Here is the list of operators, which can be used with the WHERE clause.

Assume field A holds 10 and field B holds 20, then −

Operator	Description	Example
=	Checks if the values of the two operands are equal or not, if yes, then the condition becomes true.	(A = B) is not true.
!=	Checks if the values of the two operands are equal or not, if the values are not equal then the condition becomes true.	(A != B) is true.
>	Checks if the value of the left operand is greater than the value of the right operand, if yes, then the condition becomes true.	(A > B) is not true.
<	Checks if the value of the left operand is less than the value of the right operand, if yes then the condition becomes true.	(A < B) is true.
>=	Checks if the value of the left operand is greater than or equal to the value of the right operand, if yes, then the condition becomes true.	(A >= B) is not true.
<=	Checks if the value of the left operand is less than or equal to the value of the right operand, if yes, then the condition becomes true.	(A <= B) is true.
The WHERE clause is very useful when you want to fetch the selected rows from a table, especially when you use the MySQL Join. Joins are discussed in another chapter.

It is a common practice to search for records using the Primary Key to make the search faster.

If the given condition does not match any record in the table, then the query would not return any row.
"""







MySQL Function 
""" 
Here is the list of all important MySQL functions. Each function has been explained along with suitable example.

MySQL Group By Clause − The MySQL GROUP BY statement is used along with the SQL aggregate functions like SUM to provide means of grouping the result dataset by certain database table column(s).

MySQL IN Clause − This is a clause, which can be used along with any MySQL query to specify a condition.

MySQL BETWEEN Clause − This is a clause, which can be used along with any MySQL query to specify a condition.

MySQL UNION Keyword − Use a UNION operation to combine multiple result sets into one.

MySQL COUNT Function − The MySQL COUNT aggregate function is used to count the number of rows in a database table.

MySQL MAX Function − The MySQL MAX aggregate function allows us to select the highest (maximum) value for a certain column.

MySQL MIN Function − The MySQL MIN aggregate function allows us to select the lowest (minimum) value for a certain column.

MySQL AVG Function − The MySQL AVG aggregate function selects the average value for certain table column.

MySQL SUM Function − The MySQL SUM aggregate function allows selecting the total for a numeric column.

MySQL SQRT Functions − This is used to generate a square root of a given number.

MySQL RAND Function − This is used to generate a random number using MySQL command.

MySQL CONCAT Function − This is used to concatenate any string inside any MySQL command.

MySQL DATE and Time Functions − Complete list of MySQL Date and Time related functions.

MySQL Numeric Functions − Complete list of MySQL functions required to manipulate numbers in MySQL.

MySQL String Functions − Complete list of MySQL functions required to manipulate strings in MySQL.

"""
