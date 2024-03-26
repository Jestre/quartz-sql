---
title: Grouping Data
draft: false
---
### Grouping Data

To aggregate data, we tack the `GROUP BY` clause onto our [[SELECT]] statement.  To do so, we must also have some aggregation methodology, most typically `COUNT()`.

The format is simply:

```SQL
SELECT field1, COUNT(*)
FROM tablename
WHERE ...
GROUP BY field [,field, field]
```

#### Examples

1. How many of each gender are in sws.people?
2. Create a query to show the number of years employed, and how many people are in that group.


### Having

And then there was `HAVING`.   It's like WHERE, but different.

```SQL
SELECT field1, COUNT(*)
FROM tablename
GROUP BY field
HAVING expression = expression
```

#### Examples

1. How many occurrences of people having the same last name?
2. How many genders have more than 100 people of that type?


---
Back to [[Class 4 Contents]]
