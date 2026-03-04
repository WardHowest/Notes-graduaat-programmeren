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

- [Chapter 4.0](/Databases/All-notes.md)
- [Chapter 4.5](/Databases/Chapter-4.5.md)
- [Chapter 4.6](/Databases/Chapter-4.6.md)
- [Chapter 4.7](/Databases/Chapter-4.7.md)
- [All notes](/Databases/All-notes.md)