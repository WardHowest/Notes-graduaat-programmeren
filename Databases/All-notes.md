| Chapter: 4.0 | syntax            | note                                                 |
| ------------ | ----------------- | ---------------------------------------------------- |
| C 4.0        | use libary        | select database                                      |
| C 4.2        | SELECT-clausule   | specify what collums to use                          |
| C 4.2        | FROM-clausule     | specify tabble                                       |
| C 4.2        | WHERE-clausule    | Filter rows                                          |
| C 4.2        | GROUP BY-clausule | Groups rows together                                 |
| C 4.2        | HAVING-clausule   | Specify a search condition mostly used with GROUP BY |
| C 4.2        | ORDER BY-clausule | Sort rows                                            |
| C 4.2        | ASC/DESC          | Used with ORDER BY to sort asending or decending     |

| Chapter: none | syntax                                   | note                                                                  |
| ------------- | ---------------------------------------- | --------------------------------------------------------------------- |
| None          | CREATE TABLE                             | Creates a table                                                       |
| None          | INSERT INTO [table] VALUES ( )           | Insert data into table                                                |
| None          | CREATE DATABASE                          | Creates a database                                                    |
| None          | IDENTITY                                 | Automaticly fills in row (not requiered to fill in when creating row) |
| None          | NOT NULL                                 | Requires collum to to be filled in                                    |
| None          | DELETE FROM [database] WHERE-clausule    | Deletes specified row(s)                                              |
| None          | DELETE FROM [database]                   | Deletes all data in database                                          |
| None          | PRIMARY KEY                              | Marks primary key oppon table creation                                |
| None          | SECUNDAIRY KEY                           | Marks secundairy key oppon table creation                             |
| None          | FOREIGN KEY                              | Refers to primary key                                                 |
| None          | PRIMARY KEY([collum], [collum])          | combination of 2 or more variables to for the primary key             |
| None          | DROP [database]                          | Deletes database                                                      |
| None          | DISTINCT                                 | Removes duplicates querry                                             |
| None          | OFFSET [n] ROWS FETCH NEXT [n] ROWS ONLY | Start from n row and skip n after that                                |
| None          | SELECT TOP([n])                          | Gives the first [n] rows                                              |
| None          | SELECT TOP([n]) WITH TIES                | Gives the first [n] rows and all rows that match last row             |


[comment]: <> (4.5)
| Chapter 4.5 | syntax                        | note                                                      |
| ----------- | ----------------------------- | --------------------------------------------------------- |
| 4.5         | =                             | Is equal to                                               |
| 4.5         | <>                            | between                                                   |
| 4.5         | !=                            | Is different than                                         |
| 4.5         | >                             | Is bigger than                                            |
| 4.5         | >=                            | Is bigger or equal than                                   |
| 4.5         | !>                            | Is not bigger than                                        |
| 4.5         | <                             | Is smaller than                                           |
| 4.5         | <=                            | Is smaller or equal than                                  |
| 4.5         | !<                            | Is not smaller than                                       |
| 4.5         | IS NULL                       | Expression is empty                                       |
| 4.5         | IS NOT NULL                   | Expression is not empty                                   |
| 4.5         | LIKE('[%char(s)]')            | Only get data that ends with char(s)                      |
| 4.5         | LIKE('%[char(s)]%')           | Only get data that contains pattern from included char(s) |
| 4.5         | LIKE('_[char(s)]')            | Skip First Letter than only give exact macht from char(s) |
| 4.5         | LIKE('[char(s)]__[char(s)]%') | Only get data that contains pattern from included char(s) |




[comment]: <> (4.6)
| Chapter: 4.6 | syntax                                              | note                                                            |
| ------------ | --------------------------------------------------- | --------------------------------------------------------------- |
| C 4.6.1      | GETDATE()                                           | Gets the current date in format (yyyy-mm-dd)                    |
| C 4.6.1      | DATEPART([dateformat], [date])                      | Returns specified time format of a date in an integer           |
| C 4.6.1      | DATEDIFF([dateformat], [startdate], [enddate])      | Returns the difference between 2 dates in specified time format |
| C 4.6.1      | DATEADD([dateformat], [n], [date])                  | Adds n to specified time format                                 |
| C 4.6.2      | REPLACE([string], [what to replace], [replacement]) | Replaces character(s)                                           |
| C 4.6.2      | CHARINDEX([search], [string])                       | Returns position of character in an integer if not found = 0    |
| C 4.6.2      | RIGHT([string], [n])                                | returs n character(s) starting from the right                   |
| C 4.6.2      | LEFT([string], [n])                                 | returs n character(s) starting from the left                    |
| C 4.6.2      | CONCAT([string1], [string2], )                      | Adds 2 or more strings together                                 |
| C 4.6.2      | UPPER[string]                                       | Sets string to uppercase                                        |
| C 4.6.2      | LOWER[string]                                       | Sets string to lowercase                                        |
| C 4.6.2      | LTRIM[string]                                       | trims all the spaces from the left side of the string           |
| C 4.6.2      | RTRIM[string]                                       | trims all the spaces from the right side of the string          |
| C 4.6.2      | TRIM[string]                                        | trims all the spaces from the left and right side of the string |
| C 4.6.3      | SOUNDEX([string], [string])                         | Evaluate 2 similar strings and returns a 4 character code       |
| C 4.6.3      | DIFFERENCE([string], [string])                      | Compares two soundex values and returns an integer 0-4          |
| C 4.6.4      | CAST([value] AS [datatype])                         | Casts a value into a specified datatype                         |
| C 4.6.4      | CONVERT([datatype], [value], [style])               | Convert value to specified datatype style is optional           |


[comment]: <> (C4.7)
| Chapter: 4.7 | syntax                                         | note                                                |
| ------------ | ---------------------------------------------- | --------------------------------------------------- |
| C 4.7        | COUNT(*)                                       | Count amount of rows in querry                      |
| C 4.7        | COUNT([collum]) FROM [table] WHERE [condition] | Count amount of rows that matches specific criteria |
| C 4.7        | COUNT(DISTINCT [expression])                   | Count unique rows                                   |
| C 4.7        | MIN([[expression]])                            | Return lowest value in set of values                |
| C 4.7        | MAX([[expression]])                            | Return higest value in set of values                |
| C 4.7        | SUM("[distinct]" ,[expression])                | Calculate sum                                       |
| C 4.7        | AVG("[distinct]"), [expression]                | Calculate average                                   |