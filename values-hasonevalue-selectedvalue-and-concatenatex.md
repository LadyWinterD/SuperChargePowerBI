# VALUES\(\),HASONEVALUE\(\),SELECTEDVALUE\(\),and CONCATENATEX\(\)

### VALUES\(\)

```text
Total Months in Calendar = COUNTROWS(
VALUES('Calendar'[MonthName])
)
```

```text
Month Name(Values) = IF(
HASONEVALUE('Calendar'[MonthName]),VALUES('Calendar'[MonthName])
)
```

```text
=IF(Logical Test, Result if True,[Result if False])
```

![](.gitbook/assets/image%20%2824%29.png)

### SELECTEDVALUE\(\)

![](.gitbook/assets/image%20%289%29.png)

```text
Month Name Alternate = 
SELECTEDVALUE('Calendar'[MonthName])
```

### CONCATENATEX\(\)

![](.gitbook/assets/image%20%2822%29.png)

```text
Month Name(Values) = CONCATENATEX(VALUES('Calendar'[MonthName]),[MonthName],",")
```

* Number of Color Variants

```text
Numver of Color Variants = COUNTROWS(VALUES(Products[Color]))
```

* Number of Sub Categories

```text
Number of Size Ranges = COUNTROWS(VALUES(Products[SizeRange]))
Number of Sub Categories = COUNTROWS(VALUES(Products[ProductSubcategoryKey]))
```

![](.gitbook/assets/image%20%2842%29.png)

* Product Category 

```text
Product category = 
IF(HASONEVALUE(Products[Category]),VALUES(Products[Category]))
```

* Product Subcategory 

```text
Product subcategory = 
IF(HASONEVALUE(Products[subCategory]),VALUES(Products[subCategory]))
```

![](.gitbook/assets/image%20%2827%29.png)



