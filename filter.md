# FILTER\(\)

* Total number of Customers

```text
Total Customers with Income of $80,000 or above = 
COUNTROWS(FILTER(Customers,Customers[YearlyIncome]>=80000))
```

![](.gitbook/assets/image%20%2880%29.png)

```text
Customers with sales Greater Than $5,000 Version2 =
 CALCULATE(COUNTROWS(Customers),
 FILTER(Customers,CALCULATE(SUM(Sales[ExtendedAmount])>= 5000)))
```

```text
Customers with Sales Greater Than $5,000 = 
CALCULATE(COUNTROWS(Customers),FILTER(Customers,[Total Sales]>=5000))
```

```text
Total Sales of Products That Have Some Sales but Less Than $10,000 =
 CALCULATE([Total Sales],FILTER(Products,[Total Sales]<10000 && [Total Sales] > 0))
```

```text
Count of Products That Have Some Sales but Less Than $10,000 = 
CALCULATE(COUNTROWS(Products),FILTER(Products,[Total Sales]<= 10000 && [Total Sales] > 0))
```

![](.gitbook/assets/image%20%2824%29.png)



