---
title: Numeric Data
---
### Exact Numeric Data Types

|**Data Type**|**Lower limit**|**Upper limit**|**Memory**|
|---|---|---|---|
|bigint|−2^63 (−9,223,372, 036,854,775,808)|2^63−1 (−9,223,372, 036,854,775,807)|8 bytes|
|int|−2^31 (−2,147, 483,648)|2^31−1 (−2,147, 483,647)|4 bytes|
|smallint|−2^15 (−32,767)|2^15 (−32,768)|2 bytes|
|tinyint|0|255|1 byte|
|bit|0|1|1 byte/8bit column|
|decimal (p,s) |−10^38+1|10^381−1|5 to 17 bytes|
|numeric|−10^38+1|10^381−1|5 to 17 bytes|
|money|−922,337, 203, 685,477.5808|+922,337, 203, 685,477.5807|8 bytes|
|smallmoney|−214,478.3648|+214,478.3647|4 bytes|
For decimal and numeric, one may specify both "precision" and "scale," that is, how long can the number be (including digits after the decimal, the scale)?  


### Approximate numeric data types

The approximate numeric data type stores floating point numeric data. They are often used in scientific calculations.

|**Data Type**|**Lower limit**|**Upper limit**|**Memory**|**Precision**|
|---|---|---|---|---|
|float(n)|−1.79E+308|1.79E+308|Depends on the value of n|7 Digit|
|real|−3.40E+38|3.40E+38|4 bytes|15 Digit|

---

Back to [[Data Types]]