---
title: Class 4 - Joining Tables
draft: false
---
### Joining Tables - Innies and Outies

### (INNER) JOIN

Joins two or more tables and returns only those rows with matching records in each.

```SQL
SELECT t1.field1, t1.field2, t2.field3
FROM tablename t1 INNER JOIN
	 othertable t2
		 ON t1.id = t2.id
```
![[venn-join-inner.png]]

### LEFT (OUTER) JOIN

Joins two (or more) tables and returns **ALL** tuples from the left (first) table, and those records with matching records from the right (second) table.

```SQL
SELECT t1.field1, t1.field2, t2.field3
FROM tableone t1 LEFT OUTER JOIN
     tabletwo t2
	     ON t1.id = t2.id
```

![[venn-join-left-outer.png]]

### RIGHT (OUTER) JOIN

Joins two (or more) tables and returns **ALL** tuples from the right (second) table, and those records with matching records from the left (first) table.

```SQL
SELECT t1.field1, t1.field2, t2.field3
FROM tableone t1 LEFT OUTER JOIN
     tabletwo t2
	     ON t1.id = t2.id
```

![[venn-join-right-outer.png]]



### FULL (OUTER) JOIN

Gimme all dem datas!  Pulls all tuples from all linked tables.

```SQL
SELECT t1.field1, t1.field2, t2.field3
FROM tableone t1 FULL OUTER JOIN
     tabletwo t2
	     ON t1.id = t2.id
```

![[venn-join-full-outer.png]]


## Steven's Syndrome

But what if I need to join more than two tables?


---
Back to [[Class 4 Contents]]