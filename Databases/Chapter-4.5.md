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

- [Chapter 4.0](/Databases/All-notes.md)
- [Chapter 4.5](/Databases/Chapter-4.5.md)
- [Chapter 4.6](/Databases/Chapter-4.6.md)
- [Chapter 4.7](/Databases/Chapter-4.7.md)
- [All notes](/Databases/All-notes.md)