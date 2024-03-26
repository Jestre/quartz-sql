---
title: Grouping Data - Answers
draft: false
---

### Grouping - Answers

1. How many of each gender are in sws.people?

```SQL
SELECT gender, COUNT(*) AS cnt
FROM people
GROUP BY gender
```

2. Create a query to show the number of years employed, and how many people are in that group.

```SQL
SELECT DATEDIFF(year, hire_date, CURRENT_TIMESTAMP) AS years, COUNT(*) AS cnt
FROM people
GROUP BY DATEDIFF(year, hire_date, CURRENT_TIMESTAMP)
ORDER BY years
```


### Having - Answers

1. How many occurrences of people having the same last name?

```SQL
SELECT last_name, COUNT(*) AS cnt
FROM people
GROUP BY last_name
HAVING COUNT(*) > 1
```


2. How many genders have more than 100 people of that type?

```SQL
SELECT gender, COUNT(*) AS cnt
FROM people
GROUP BY gender
HAVING COUNT(*) > 100
```


---
Back to [[Class 4 Contents]]