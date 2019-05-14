# Time Intelligence

Turn off auto date/time

![](.gitbook/assets/image%20%2836%29.png)

```text
Total Sales LY = 
CALCULATE([Total Sales],SAMEPERIODLASTYEAR('Calendar'[Date]))
```

```text
Total Sales YTD = TOTALYTD([Total Sales],'Calendar'[Date])
```

![](.gitbook/assets/image%20%2845%29.png)

* Total Sales Month to Date

```text
Total Sales Month to Date = TOTALMTD([Total Sales],'Calendar'[Date])
```

```text
Total Sales FYTD 30 June = TOTALYTD([Total Sales],'Calendar'[Date],"30/6")
```

The year end date- 6/30

```text
Total Sales FYTD 31 March = TOTALYTD([Total Sales],'Calendar'[Date],"31/3")
```

* Total Sales Previous Month 

```text
Total Sales Previous Month = CALCULATE([Total Sales],PREVIOUSMONTH('Calendar'[Date]))
```

* Total Sales Previous Day

```text
Total Sales Previous Day = 
CALCULATE([Total Sales],PREVIOUSDAY('Calendar'[Date]))

Total Sales Previous Quarter 
= CALCULATE([Total Sales],PREVIOUSQUARTER('Calendar'[Date]))
```

![](.gitbook/assets/image%20%281%29.png)

![](.gitbook/assets/image%20%2855%29.png)

![](.gitbook/assets/image%20%2830%29.png)

```text
Total Sales YTD Manual =
CALCULATE (
    [Total Sales],
    FILTER (
        ALL ( 'Calendar' ),
        'Calendar'[CalendarYear] = MAX ( 'Calendar'[CalendarYear] )
            && 'Calendar'[Date] <= MAX ( 'calendar'[Date] )
    )
)

```

![](.gitbook/assets/image%20%2813%29.png)

```text
Total Sales YTD Doesn't Work = 
CALCULATE(
    [Total Sales],
        FILTER(
            'Calendar',
                'Calendar'[CalendarYear] = MAX('Calendar'[CalendarYear])
                    && 'Calendar'[Date] = MAX('Calendar'[Date])
                )
)
```

```text
Total Sales YTD Manual ID =
CALCULATE (
    [Total Sales],
    FILTER (
        ALL ( 'Calendar' ),
        'Calendar'[CalendarYear] = MAX ( 'Calendar'[CalendarYear] )
            && 'Calendar'[ID] <= 'Calendar'[ID]
    )
)

```

```text
Total Sales LY ID = 
CALCULATE([Total Sales],FILTER(ALL('Calendar'),
'Calendar'[ID] >= MIN('Calendar'[ID]) -365
&& 'Calendar'[ID] <= MAX('Calendar'[ID])-365 ))

```

![](.gitbook/assets/image%20%2848%29.png)

October 31 2003, it has an ID of 853, so it can be thought of as:

```text
'Çalendar'ID >= 823 && 'Calendar'[ID] <= 853
```

* Total Sales Moving Annual Total



```text
Total Sales Moving Annual Total = 
CALCULATE (
    [Total Sales],
    FILTER (
        ALL ( 'Calendar' ),
        'Calendar'[ID] <= MAX ( 'Calendar'[ID] )
            && 'Calendar'[ID]
                > MAX ( 'Calendar'[ID]) - 365 )
    )


```

Total Sales Rolling 90 Days

```text
Total Rolling 90 Days =
IF (
    MAX ( 'Calendar'[ID] ) >= 90,
    CALCULATE (
        [Total Sales],
        FILTER (
            ALL ( 'Calendar' ),
            'Calendar'[ID]
                >= MAX ( 'Calendar'[ID] ) - 90
                && 'Calendar'[ID] <= MAX ( 'Calendar'[ID] )
        )
    )
)



```

![](.gitbook/assets/image%20%2838%29.png)

![](.gitbook/assets/image%20%287%29.png)

It should be same if your formula is correct.

