---
title: Using SELECT
draft: false
---
The one every knows, but few should be using:

```SQL
SELECT * FROM tablename
```

This is fine, but if you do need to see all fields, do you really need to see them for every piece of data in the table?  If not, try just the TOP 10 or 20, e.g.

```SQL
SELECT TOP 10 * FROM tablename
```

But more likely, you'll just want to see certain fields:

```SQL
SELECT field1, field2, field3 FROM tablename 
-- or
SELECT TOP 10 field1, field2, field3 FROM tablename
```


> [!NOTE] A Comment
> As seen above, using two dashes "--" before any part of a query will "comment" out that bit of code, or allow you to make notes within your SQL.  Good way to explain to others (and yourself in a year or two) what you were thinking when you wrote the query the way you did.


## Filters

To filter the data returned from the [[SELECT]] statement, you can use the WHERE clause.

**TABLE: people**

| id (int not null) | name_last (varchar(50) not null) | name_first (varchar(25) null) |
| ----------------- | -------------------------------- | ----------------------------- |
| 1                 | Smith                            | Juan                          |
| 2                 | Jones                            | Bury                          |
| 3                 | Diggs                            | Steven                        |
| 4                 | Taylor                           | Kanisha                       |
| 5                 | Jones                            | Steven                        |

```SQL
SELECT name_last, name_first
FROM people

-- Last name is Smith
WHERE name_last = 'Smith'
-- Anyone whose last name is not Smith
WHERE name_last <> 'Smith' 
-- Both must match
WHERE name_last = 'Diggs' AND name_first = 'Steven'
-- Anyone whose last name is Diggs or whose first name is Steven
WHERE name_last = 'Jones' OR name_first = 'Steven' 
```

The options for WHERE include:

- '=' equal
- '<>' not equal
- '<', '>' less than or greater than
- IS NULL
- IS NOT NULL


## Sorting

To sort the returned data by a field or fields, use the ORDER BY clause:

```SQL
SELECT name_last, name_first
FROM people
ORDER BY name_last, name_first
```

You can also specify the sort order for each field using **ASC** (ascending, the default) or **DESC** (descending) 

```SQL
SELECT name_last, name_first
FROM people
ORDER BY name_last DESC, name_first
-- Last names will be sorted from Z..A, while first names will be sorted A..Z (for each last name)
-- TAYLOR, K
-- SMITH, ADAM
-- SMITH, JOHN
-- DIGGS, LUCKY
```

---
Back to [[Class 3 Contents]]