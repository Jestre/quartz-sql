---
title: Other and etc.
---

## Other Considerations

- Normalization of tables
- Indexes and Keys

## Normalization

| Name | Address | Phone | Class |
| ---- | ---- | ---- | ---- |
| Steven Diego | 330 S. Sanitary Street, Raleigh, NC 27529 | 919-555-1212 | SQL 101 |
| James Smith | 320 Some Street, Garner, NC 27602 | 919-121-5555 | SQL 101 |
| Dante Aligheri | 201 Venice Street, Venice, 999 | 97-222-222-2342 | SQL 101 |
| Adam Jones | 3488 Some Town, Wendell, NC 27888 | 919-256-12334 | SQL 101 |
| Adam Jones | 1212 Home on the Range, Salisbury, NC 22321 | 984-555-1212 | SQL 101 |
| Tom Jones | 3488 Some Town, Wendell, NC 27888 | 984-123-8474 | SQL 101 |
#### First Normal Form

1. Does the combination of all columns make a unique row every single time?
2. What field can be used to uniquely identify the row?
#### Second Normal Form

1. Fulfill the requirements of first normal form
2. Each non-key attribute must be functionally dependent on the primary key


## Keys

#### Primary Keys

A primary key in a table is a field that uniquely identifies each row and column or set of columns in the table. The primary key is an attribute or a set of attributes that help to uniquely identify the tuples(records) in the table. The primary key provides the means to distinguish one tuple from all the others in the relation. It helps the user to identify the location and also the database system to identify, locate, and refer to one particular tuple in the relation.
#### Foreign Keys

A foreign key is a column in one table that refers to the primary key in another table

**Which way around?**

Does table1 have many table2s, or does a table2 have many table1s?

If it’s the first, then table1 ID goes into table 2, and if it’s the second then table2 ID goes into table1.

## Indexes

Indexes are data structures that can increase a database’s efficiency in accessing tables. Indexes are not required; the database can function properly without them, but query response time can be slower.

Every index is associated with a table and has a key, which is formed by one or more table columns. When a query needs to access a table that has an index, the database can decide to use the index to retrieve records faster.

---
Back to [[Class 1 Contents]]