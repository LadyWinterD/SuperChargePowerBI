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

![](.gitbook/assets/image%20%2821%29.png)

### SELECTEDVALUE\(\)

![](.gitbook/assets/image%20%289%29.png)

```text
Month Name Alternate = 
SELECTEDVALUE('Calendar'[MonthName])
```

### CONCATENATEX\(\)

![](.gitbook/assets/image%20%2819%29.png)

```text
Month Name(Values) = CONCATENATEX(VALUES('Calendar'[MonthName]),[MonthName],",")
```

* Number of Color Variants

```text
Numver of Color Variants = COUNTROWS(VALUES(Products[Color]))
```

* Number of Sub Categories



