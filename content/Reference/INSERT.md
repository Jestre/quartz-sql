---
title: INSERT statement
---
### Insert Statement

```sql
-- Syntax for SQL Server and Azure SQL Database 
[ WITH <common_table_expression> [ ,...n ] ] 
INSERT 
{ 
	[ TOP ( expression ) [ PERCENT ] ] 
	[ INTO ] 
	{ <object> | rowset_function_limited 
		[ WITH ( <Table_Hint_Limited> [ ...n ] ) ] 
	} 
  { 
	  [ ( column_list ) ] 
	  [ <OUTPUT Clause> ] 
	  { VALUES ( { DEFAULT | NULL | expression } [ ,...n ] ) [ ,...n ] 
	  | derived_table 
	  | execute_statement 
	  | <dml_table_source> 
	  | DEFAULT VALUES 
	  } 
  } 
} 
[;]
```


---
Back to [[References]]