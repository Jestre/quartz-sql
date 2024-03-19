---
title: Answers - Class 3
draft: true
---
Let's tack some functionality on now and try to answer some queries:

#### Who has been employed the longest?

```SQL
SELECT TOP 1 last_name, first_name, hire_date
FROM people
ORDER BY hire_date DESC
```

#### Who has been employed the shortest?

```SQL
SELECT TOP 1 last_name, first_name, hire_date
FROM people
ORDER BY hire_date
```

#### Which people do not have email addresses listed?

```SQL
SELECT last_name, first_name, email
FROM people
WHERE email IS NULL
```
#### How many entries in the people table?

```SQL
SELECT COUNT(*) FROM people
```

####  Who is vested in the insurance plan (assume 20 years)?

```SQL
SELECT last_name, first_name, DATEADD(year, 20, hire_date) AS vested
FROM people
WHERE  DATEADD(year, 20, hire_date) <= CURRENT_TIMESTAMP
ORDER BY vested DESC, hire_date
```

> DATEADD(interval, number, date)
> [Reference](https://learn.microsoft.com/en-us/sql/t-sql/functions/dateadd-transact-sql?view=sql-server-ver16)
#### Was anyone hired today?

```SQL
SELECT TOP 30 last_name, first_name, hire_date
FROM people
WHERE hire_date = CAST(CURRENT_TIMESTAMP AS DATE)
```

> CAST(field AS type)
#### Does anyone have a work anniversary today?  If so, how long?

```SQL
SELECT TOP 30 id, last_name, first_name, hire_date, DATEDIFF(year, hire_date, CURRENT_TIMESTAMP) AS years
FROM people
WHERE DATEPART(d, hire_date) = DATEPART(d, GetDate()) 
  AND DATEPART(m, hire_date) = DATEPART(m, GetDate())
ORDER BY years
```

> DATEDIFF(part, start_date, end_date)
> [Reference](https://learn.microsoft.com/en-us/sql/t-sql/functions/datediff-transact-sql?view=sql-server-ver16)


> DATEPART(part, field) 
> 	where part is d = day, m = month, y = year, etc.
> [Reference](https://learn.microsoft.com/en-us/sql/t-sql/functions/datepart-transact-sql?view=sql-server-ver16)


---
Back to [[Class 3 Contents]]