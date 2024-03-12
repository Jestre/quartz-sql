---
title: Insert Data
draft: false
---
Now it is time to start populating your data. We will use the [[INSERT]] statement to begin populating our tables with data.  While doing this, remember to populate the tables which have keys which will function as foreign keys in other tables, *assuming you normalized your stuff*.

The SQL insert statement looks like this:

![[INSERT#Insert Statement]]

Don't worry about all of that, we'll only be using a small part for this class.

### Examples

#### Simple Example

```SQL
INSERT 
	INTO tablename 
		(field1, field2, field3, ...) 
	VALUES 
		(field1_value, field2_value, ...)
```


> [!info] Note
> Remember that any field marked as **not null** must be included in the list,  You may exclude fields which allow nulls and for which no data is being inserted at this point.


**TABLE: people**

| id (int not null) | name_last (varchar(50) not null) | name_first (varchar(25) null) |
| ----------------- | -------------------------------- | ----------------------------- |
| 1                 | Smith                            | Juan                          |
| 2                 | Jones                            | Bury                          |

```SQL
INSERT INTO people (id, name_last, name_first) VALUES (NULL, 'Smith', 'Juan')
INSERT INTO people VALUES (NULL, 'Jones', 'Bury')
```

> [!tip] A Tip
> If you will be inserting values for all fields, then the list of fields may be excluded, but it is good form to include them in case you change the schema of this table at a later point (or some other goof does it for you).


**TABLE: people (as modified by aforementioned `goof`)

| id (int not null) | salutation [char(3) null] | name_last [varchar(50) not null] | name_first [varchar(25) null] |     |
| ----------------- | ------------------------- | -------------------------------- | ----------------------------- | --- |
| 1                 |                           | Smith                            | Juan                          |     |
| 2                 |                           | Jones                            | Bury                          |     |

### Multi-Inserts

The same as the simple insert above, but if we have multiple rows of data to insert, we can specify multiple value sets (tuples) at once:

```SQL
INSERT 
	INTO tablename 
		(field1, field2, field3, ...) 
	VALUES 
		(field1_value, field2_value, ...),
		(field1_value, field2_value, ...),
		(field1_value, field2_value, ...),
		(field1_value, field2_value, ...)
```

```SQL
INSERT 
	INTO people 
		(id, name_last, name_first) 
	VALUES 
		(NULL, 'Smith', 'Juan'),
		(NULL, 'Jones', 'Bury'),
		(NULL, 'Cuervo', 'Johann'),
		etc.
```


---
Back to [[Class 2 Contents]]