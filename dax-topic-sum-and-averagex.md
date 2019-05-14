# DAX Topic: SUM\(\) and AVERAGEX\(\)

### Using SUMX\(\)

```text
Total Sales Including Tax SUMX Version = SUMX(Sales,Sales[ExtendedAmount]+Sales[TaxAmt])
```

![](.gitbook/assets/image%20%2817%29.png)

* Total Sales SUMX Version

```text
Total Sales SUMX Version = sumx(Sales,Sales[SalesAmount])
```

* Total Sales Including Tax SUMX Version 

```text
TotalSales Including Tax SUMX Version = SUMX(sales,Sales[TaxAmt]+Sales[SalesAmount])
```

* Total Sales Including Freight

```text
Total Sales Including Freight = SUMX(Sales,Sales[SalesAmount]+Sales[Freight])
```

![](.gitbook/assets/image%20%2832%29.png)

Filters 

![](.gitbook/assets/image%20%2825%29.png)

### Dealer Margin

```text
Dealer Margin = SUMX(Products,Products[ListPrice]-Products[DealerPrice])
```

### AVERAGEX\(\)

* Average Sell Price per Item

```text
Average Sell Price per Item = AVERAGEX(Sales,Sales[UnitPrice])
```

* Average Tax Paid

```text
Average Tax Paid= AVERAGEX(Sales,Sales[TaxAmt])
```

* Average Safety Stock

```text
Average Safety Stock = AVERAGEX(Products,Products[SafetyStockLevel])
```

![](.gitbook/assets/image%20%2834%29.png)



