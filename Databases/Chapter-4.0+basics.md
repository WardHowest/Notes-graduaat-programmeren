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

- [Chapter 4.0](/Databases/All-notes.md)
- [Chapter 4.5](/Databases/Chapter-4.5.md)
- [Chapter 4.6](/Databases/Chapter-4.6.md)
- [Chapter 4.7](/Databases/Chapter-4.7.md)
- [Chapter 4.8](/Databases/Chapter-4.8.md)
- [All notes](/Databases/All-notes.md)