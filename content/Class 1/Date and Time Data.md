---
title: Date and Time Data
---

### Date & Time data types

The date and time data types store data and time data, and the date time offset.

|**Data Type**|**Storage size**|**Accuracy**|**Lower Range**|**Upper Range**|
|---|---|---|---|---|
|datetime|8 bytes|Rounded to increments of .000, .003, .007|1753-01-01|9999-12-31|
|smalldatetime|4 bytes, fixed|1 minute|1900-01-01|2079-06-06|
|date|3 bytes, fixed|1 day|0001-01-01|9999-12-31|
|time|5 bytes|100 nanoseconds|00:00:00.0000000|23:59:59.9999999|
|datetimeoffset|10 bytes|100 nanoseconds|0001-01-01|9999-12-31|
|datetime2|6 bytes|100 nanoseconds|0001-01-01|9999-12-31|

---

Back to [[Data Types]]