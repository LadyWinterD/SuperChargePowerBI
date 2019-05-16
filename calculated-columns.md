# Calculated Columns

### Creating a day type calculated column

Open the Calendar Table from the right side of Power BI, create a new column. Type the code as below in the formula bar:

```text
Day Type = if('Calendar'[DayNumberOfWeek]=1||'Calendar'[DayNumberOfWeek]=7,
"Weekend","Weekday"
)
```

![](.gitbook/assets/image%20%2868%29.png)

### Practice 

* Creating a half-year column

```text
Half-Year = IF('Calendar'[MonthNumberOfYear]>6||'Calendar'[MonthNumberOfYear]<6,
"H2","H1"
)
```



