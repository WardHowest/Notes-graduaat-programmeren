| Chapter: 4.0 | syntax            | example                                                                         | note                                                          |
| ------------ | ----------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------- |
| C 4.0        | USE libary        | USE pubs                                                                        | select database                                               |
| C 4.2        | SELECT-clausule   | SELECT price, pub_id                                                            | specify what collums to use                                   |
| C 4.2        | FROM-clausule     | SELECT * FROM authors                                                           | specify tabble                                                |
| C 4.2        | WHERE-clausule    | SELECT * FROM authors WHERE                                                     | Filter rows                                                   |
| C 4.2        | GROUP BY-clausule | SELECT price FROM titles GROUP BY price                                         | Groups rows together                                          |
| C 4.2        | HAVING-clausule   | SELECT price, COUNT(*) AS number FROM titles GROUP BY price HAVING COUNT(*) > 2 | Specify a search condition mostly used with GROUP BY          |
| C 4.2        | ORDER BY-clausule | SELECT * from titles ORDER BY price                                             | Sort rows                                                     |
| C 4.2        | ASC/DESC          | SELECT * from titles ORDER BY price DESC                                        | Used with ORDER BY to sort asending or decending default: ASC |



| Order of execution |
| ------------------ |
| FROM-clausule      |
| WHERE-clausule     |
| GROUP BY-clausule  |
| HAVING-clausule    |
| SELECT-clausule    |
| ORDER BY-clausule  |



| Chapter: none | syntax                                   | example                                                                          | note                                                      |
| ------------- | ---------------------------------------- | -------------------------------------------------------------------------------- | --------------------------------------------------------- |
| None          | CREATE TABLE                             | CREATE TABLE authors                                                             | Creates a table                                           |
| None          | INSERT [table] VALUES ( )                | INSERT authors values()                                                          | Insert data into table                                    |
| None          | CREATE DATABASE                          | CREATE DATABASE pubs                                                             | Creates a database                                        |
| None          | IDENTITY                                 | job_id smallint IDENTITY(1,1)                                                    | Automaticly fills in row, begins with 1 steps up with 1   |
| None          | NOT NULL                                 | job_desc varchar(50) NOT NULL                                                    | Requires collum to to be filled in                        |
| None          | DELETE FROM [database] WHERE-clausule    | DELETE FROM authors WHERE au_id = 172-32-1176                                    | Deletes specified row(s)                                  |
| None          | DELETE FROM [database]                   | DELETE FROM authors                                                              | Deletes all data in database                              |
| None          | PRIMARY KEY                              | job_id smallint IDENTITY(1,1) PRIMARY KEY CLUSTERED                              | Marks primary key oppon table creation                    |
| None          | SECUNDAIRY KEY                           |                                                                                  | Marks secundairy key oppon table creation                 |
| None          | FOREIGN KEY                              |                                                                                  | Refers to primary key                                     |
| None          | PRIMARY KEY([collum], [collum])          | UPKCL_taind PRIMARY KEY (au_id, title_id)                                        | combination of 2 or more variables to for the primary key |
| None          | DROP [database]                          | DROP database pubs                                                               | Deletes database                                          |
| None          | DISTINCT                                 | SELECT DISTINCT city FROM authors                                                | Removes duplicates querry                                 |
| None          | OFFSET [n] ROWS FETCH NEXT [n] ROWS ONLY | SELECT * FROM authors OFFSET ORDER BY au_id OFFSET 2 ROWS FETCH NEXT 5 ROWS ONLY | Start from n row and skip n after that                    |
| None          | SELECT TOP [n]                           | SELECT TOP 5 * FROM authors                                                      | Gives the first [n] rows                                  |
| None          | SELECT TOP([n]) WITH TIES                | SELECT TOP 3 WITH TIES * FROM titles ORDER BY price                              | Gives the first [n] rows and all rows that match last row |



| Chapter 4.5 | syntax                        | example                                                   | note                                                      |
| ----------- | ----------------------------- | --------------------------------------------------------- | --------------------------------------------------------- |
| 4.5         | =                             | SELECT * FROM titles WHERE [type] = 'business'            | Is equal to                                               |
| 4.5         | between [value] AND [value]   | SELECT * FROM titles WHERE price BETWEEN 10 AND 20        | between                                                   |
| 4.5         | !=                            | SELECT * FROM authors WHERE type != 'business'            | Is different than                                         |
| 4.5         | >                             | SELECT * FROM titles WHERE price > 19.99                  | Is bigger than                                            |
| 4.5         | >=                            | SELECT * FROM titles WHERE price >= 19.99                 | Is bigger or equal than                                   |
| 4.5         | !>                            | SELECT * FROM titles WHERE price !> 19.99                 | Is not bigger than                                        |
| 4.5         | <                             | SELECT * FROM titles WHERE price < 19.99                  | Is smaller than                                           |
| 4.5         | <=                            | SELECT * FROM titles WHERE price <= 19.99                 | Is smaller or equal than                                  |
| 4.5         | !<                            | SELECT * FROM titles WHERE price != 19.99                 | Is not smaller than                                       |
| 4.5         | IS NULL                       | SELECT * FROM titles WHERE ytd_sales IS NULL              | Expression is empty                                       |
| 4.5         | IS NOT NULL                   | SELECT * FROM titles WHERE ytd_sales IS NOT NULL          | Expression is not empty                                   |
| 4.5         | LIKE('[%char(s)]')            | SELECT * FROM titles WHERE [type] LIKE('%ess')            | Only get data that ends with char(s)                      |
| 4.5         | LIKE('%[char(s)]%')           | SELECT * FROM titles WHERE [type] LIKE('%o%')             | Only get data that contains pattern FROM included char(s) |
| 4.5         | LIKE('_[char(s)]')            | SELECT * FROM jobs WHERE job_desc LIKE('__naging Editor') | Skip n Letter(s) than only give exact macht FROM char(s)  |
| 4.5         | LIKE('_[char(s)]%')           | SELECT * FROM jobs WHERE job_desc LIKE('_a%')             | Skip First Letter than only give pattern FROM char(s)     |
| 4.5         | LIKE('[char(s)]__[char(s)]')  | SELECT * FROM jobs WHERE min_lvl LIKE('1_0')              | Only get data that contains exact pattern                 |
| 4.5         | LIKE('[char(s)]__[char(s)]%') | SELECT * FROM titleauthor WHERE title_id LIKE('BU__3%')   | Only get data that contains pattern FROM included char(s) |



| Chapter: 4.6 | syntax                                              | example                                                       | note                                                            |
| ------------ | --------------------------------------------------- | ------------------------------------------------------------- | --------------------------------------------------------------- |
| C 4.6.1      | GETDATE()                                           |                                                               | Gets the current date in format (yyyy-mm-dd)                    |
| C 4.6.1      | DATEPART([dateformat], [date])                      | SELECT DATEPART(YEAR, pubdate) AS date from titles            | Returns specified time format of a date in an integer           |
| C 4.6.1      | DATEDIFF([dateformat], [startdate], [enddate])      | SELECT DATEDIFF(YEAR, pubdate, GETDATE()) AS date from titles | Returns the difference between 2 dates in specified time format |
| C 4.6.1      | DATEADD([dateformat], [n], [date])                  | SELECT DATEADD(DAY, 1, pubdate ) AS date from titles          | Adds n to specified time format                                 |
| C 4.6.2      | REPLACE([string], [what to replace], [replacement]) | SELECT REPLACE('Net Etiquette', 't', 'm')                     | Replaces character(s)                                           |
| C 4.6.2      | CHARINDEX([search], [string])                       | SELECT CHARINDEX('x', 'example')                              | Returns position of character in an integer if not found = 0    |
| C 4.6.2      | RIGHT([string], [n])                                | SELECT RIGHT('example', 3)                                    | returs n character(s) starting from the right                   |
| C 4.6.2      | LEFT([string], [n])                                 | SELECT LEFT('example', 3)                                     | returs n character(s) starting from the left                    |
| C 4.6.2      | CONCAT([string1], [string2])                        | SELECT CONCAT(au_lname,' ', au_fname) AS name FROM authors    | Adds 2 or more strings together                                 |
| C 4.6.2      | UPPER[string]                                       | SELECT UPPER(au_lname) FROM authors                           | Sets string to uppercase                                        |
| C 4.6.2      | LOWER[string]                                       | SELECT LOWER(au_lname) FROM authors                           | Sets string to lowercase                                        |
| C 4.6.2      | LTRIM[string]                                       | SELECT LTRIM('   example   ')                                 | trims all the spaces from the left side of the string           |
| C 4.6.2      | RTRIM[string]                                       | SELECT RTRIM('   example   ')                                 | trims all the spaces from the right side of the string          |
| C 4.6.2      | TRIM[string]                                        | SELECT TRIM('   example   ')                                  | trims all the spaces from the left and right side of the string |
| C 4.6.3      | SOUNDEX([string], [string])                         | SELECT SOUNDEX('Juice'), SOUNDEX('Banana')                    | Evaluate 2 similar strings and returns a 4 character code       |
| C 4.6.3      | DIFFERENCE([string], [string])                      | SELECT DIFFERENCE('Juice','Jucy')                             | Compares two soundex values and returns an integer 0-4          |
| C 4.6.4      | CAST([value] AS [datatype])                         | SELECT CAST(25.65 AS int)                                     | Casts a value into a specified datatype                         |
| C 4.6.4      | CONVERT([datatype], [value], [style])               | SELECT CONVERT(varchar, pubdate, 107) FROM titles             | Convert value to specified datatype style is optional           |




| Chapter: 4.7 | syntax                          | example                                     | note                                 |
| ------------ | ------------------------------- | ------------------------------------------- | ------------------------------------ |
| C 4.7        | COUNT(*)                        | SELECT COUNT(*) FROM authors                | Count amount of rows in querry       |
| C 4.7        | COUNT(DISTINCT [expression])    | SELECT COUNT(DISTINCT [state]) FROM authors | Count unique rows                    |
| C 4.7        | MIN([[expression]])             | SELECT MIN(price) FROM titles               | Return lowest value in set of values |
| C 4.7        | MAX([[expression]])             | SELECT MAX(price) FROM titles               | Return higest value in set of values |
| C 4.7        | SUM("[distinct]" ,[expression]) | SELECT SUM(price) FROM titles               | Calculate sum                        |
| C 4.7        | AVG("[distinct]"), [expression] | SELECT AVG(price) FROM titles               | Calculate average                    |

| Chapter: 4.8 | syntax            | example                                                                         | note                                                 |
| ------------ | ----------------- | ------------------------------------------------------------------------------- | ---------------------------------------------------- |
| C 4.8        | GROUP BY-clausule | SELECT price FROM titles GROUP BY price                                         | Groups rows together                                 |
| C 4.8        | HAVING-clausule   | SELECT price, COUNT(*) AS number FROM titles GROUP BY price HAVING COUNT(*) > 2 | Specify a search condition mostly used with GROUP BY |



| Chapter: 4.9 + 4.10 | syntax                                | example                                                                                        | note                                                        |
| ------------------- | ------------------------------------- | ---------------------------------------------------------------------------------------------- | ----------------------------------------------------------- |
| C 4.9               | JOIN[table2] ON [collum2] = [collum1] | SELECT employee.job_id, jobs.job_desc FROM employee JOIN jobs ON jobs.job_id = employee.job_id | Inner joins or combines 2 tables. More tables can be joined |



- [Chapter 4.0](/Databases/All-notes.md)
- [Chapter 4.5](/Databases/Chapter-4.5.md)
- [Chapter 4.6](/Databases/Chapter-4.6.md)
- [Chapter 4.7](/Databases/Chapter-4.7.md)
- [Chapter 4.8](/Databases/Chapter-4.8.md)
- [Chapter 4.9 + 4.10](/Databases/Chapter-4.9+4.10.md)
- [All notes](/Databases/All-notes.md)