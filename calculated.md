# CALCULATED\(\)

```text
Total Sales to Females = CALCULATE([Total Sales],Customers[Gender]="F")
```

### CALCULATE\(\) WITH A SINGLE TABLE

* Total Male Customers

```text
Total Customers Males = CALCULATE([Total Number of Customers],Customers[Gender]="M")
```

* Total Customers Bron Before 1950

```text
Total Customers Bron Before 1950 = CALCULATE([Total Number of Customers],
Customers[BirthDate]<DATE(1950,01,01))
```

* Total Customers Born in January

```text
Total Customers Born in January = CALCULATE([Total Number of Customers],MONTH(Customers[BirthDate])=1)
```

* Customers Earning at Least $100,000 per year

```text
Customers Earning at Least $100,000 per year = CALCULATE([Total Number of Customers],Customers[YearlyIncome]>=100000)
```

![](.gitbook/assets/image%20%2841%29.png)

### Using CALCULATE\(\) over Multiple Tables

```text
Total Sales = SUMX(Sales,Sales[OrderQuantity]*Sales[UnitPrice])
```

* Total Sales of Clothing

```text
Sales of Bikes to Married Men = CALCULATE([Total Sales],Products[Category]="Bikes",
Customers[MaritalStatus]="M",Customers[Gender]="M")
```

![](.gitbook/assets/image%20%288%29.png)



