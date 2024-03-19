---
title: Creating Tables
draft: false
---
### Creating Tables

To create a table you can either execute a SQL query containing the schema for the new table, or you can use the built-in table editor in SSMS.

### SQL Query

```SQL
CREATE TABLE sws.people ( 
	id INT PRIMARY KEY IDENTITY (1, 1), 
	name_last NCHAR (25) NOT NULL, 
	name_last NCHAR (15) NOT NULL, 
	name_middle NCHAR (15),
	start_date DATETIME NOT NULL, 
	phone_home CHAR (10), 
	phone_mobile CHAR (10),
	agency_id INT NOT NULL, 
	FOREIGN KEY (agency_id) REFERENCES sws.agencies (agancy_id) 
);
```

### SSMS Table Editor

1. Browse to your database
2. Click the '+' sign to expand it
3. R-click on Tables and choose New > Table
4. Add the fields for the table, and define their data types, etc.
	1. Don't forget the identity and primary key
5. When complete, R-Click the tab of the designer and choose Save Table (name it here)
6. Add any additional tables

##### Step 3
![[new-table.png]]

##### Step 4

Set Identity, will cause SQL Server to increment the counter in this field automatically.

![[table-fields.png]]

Now Right-Click on the little triangle, and choose "Set Primary Key"

![[set-primary-key.png]]

##### Step 5

Finally, right-click on the tab and choose Save Table.  It will ask you to name it at this point.


---
Back to [[Class 2 Contents]]