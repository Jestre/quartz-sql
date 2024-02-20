---
title: Homework - Class 1
---
For this class, we will be rebuilding parts of our asset module and a few other pieces.

The class decided on the following foundational tables to begin the project, though you certainly don't have to abide by these choices:

- Person table
- Vendor table
- Items table
- Assignment table
- Item types table (laptop, desktop, bwc)

And here are some question which were posed that the system needed to answer, at a minimum.  There will certainly be many more.

1. How many people have been assigned a particular item?
2. How many of an item do we have?
3. How many items does each vendor have?
4. How many items does each person have?

  
To begin, simply write out your choices for table name, attribute name, and the data type and other details of that attribute, e.g.

```
Persons_table (
	person_id_pk int not null, (primary key)
	person_name varchar(20),
	email varchar(50),
	vendor_id_fk int not null (foreign key to vendor_table)
)
```


---

Back to [[Class 1 Contents]]