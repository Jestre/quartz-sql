---
title: UPDATE statement
---
### UPDATE Statement

```sql
-- Syntax for SQL Server and Azure SQL Database
[ WITH <common_table_expression> [...n] ] 
UPDATE 
	[ TOP ( expression ) [ PERCENT ] ] 
	{ { table_alias | <object> | rowset_function_limited 
		[ WITH ( <Table_Hint_Limited> [ ...n ] ) ] 
	  } 
	  | @table_variable 
	} 
	SET 
		{ column_name = { expression | DEFAULT | NULL } 
		  | { udt_column_name.{ { property_name = expression 
							    | field_name = expression } 
							    | method_name ( argument [ ,...n ] ) 
							  } 
		  } 
		  | column_name { .WRITE ( expression , @Offset , @Length ) } 
		  | @variable = expression 
		  | @variable = column = expression 
		  | column_name { += | -= | *= | /= | %= | &= | ^= | |= } expression 
		  | @variable { += | -= | *= | /= | %= | &= | ^= | |= } expression 
		  | @variable = column { += | -= | *= | /= | %= | &= | ^= | |= } expression 
		} [ ,...n ] 
	[ <OUTPUT Clause> ] 
	[ FROM{ <table_source> } [ ,...n ] ] 
	[ WHERE { <search_condition> 
			| { [ CURRENT OF 
				  { { [ GLOBAL ] cursor_name } 
					  | cursor_variable_name 
				  } 
				] 
			} 
		} 
	] 
	[ OPTION ( <query_hint> [ ,...n ] ) ] 
[ ; ]
```


---
Back to [[References]]