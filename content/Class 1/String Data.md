---
title: String Data
---
### Character strings data types

Character strings data types allow you to store either fixed-length (char) or variable-length data (varchar). The text data type can store non-Unicode data in the code page of the server.

|**Data Type**|**Lower limit**|**Upper limit**|**Memory**|
|---|---|---|---|
|char|0 chars|8000 chars|n bytes|
|varchar|0 chars|8000 chars|n bytes + 2 bytes|
|varchar (max)|0 chars|2^31 chars|n bytes + 2 bytes|
|text|0 chars|2,147,483,647 chars|n bytes + 4 bytes|

### Unicode character string data types

Unicode character string data types store either fixed-length (nchar) or variable-length (nvarchar) Unicode character data.

|**Data Type**|**Lower limit**|**Upper limit**|**Memory**|
|---|---|---|---|
|nchar|0 chars|4000 chars|2 times n bytes|
|nvarchar|0 chars|4000 chars|2 times n bytes + 2 bytes|
|ntext|0 chars|1,073,741,823 char|2 times the string length|

### Binary string data types

The binary data types stores fixed and variable length binary data.

| **Data Type** | **Lower limit** | **Upper limit** | **Memory** |
| ---- | ---- | ---- | ---- |
| binary | 0 bytes | 8000 bytes | n bytes |
| varbinary | 0 bytes | 8000 bytes | The actual length of data entered + 2 bytes |
| image | 0 bytes | 2,147,483,647 bytes |  |

---

Back to [[Data Types]]