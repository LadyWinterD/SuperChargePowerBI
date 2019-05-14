# Measures

## First Measure

![](.gitbook/assets/image%20%287%29.png)

* Create a new blank matrix and drop the column-Category to the Rows drop zone for matrix. 
* Right click the table-product , create a new Measure. Type as below.

```text
Total Sales = SUM(Sales[ExtendedAmount])

```

* Then drop this measure to the Values drop zone for matrix.
* Click back into the formula bar, and apply the formatting $, press enter again.

Then you can see the total sales in the matrix.

![](.gitbook/assets/image%20%2846%29.png)

### Practice Exercises-SUM\(\)

* \[Total Sales\]

```text
Total Sales = SUM(Sales[ExtendedAmount])
```

* \[Total Cost\]

```text
Total Cost = SUM(Sales[ExtendedAmount])
```

* \[Total Margin $\]

```text
Total Margin $ = [Total Sales]-[Total Cost]
```

* \[Total Margin %\]

```text
Total Margin % = [Total Margin $]/[Total Sales]
```

* \[Total Sales Tax Paid\]

```text
Total Sales Tax Paid = SUM(Sales[TaxAmt])
```

* \[Total Sales Including Tax\]

```text
Total Sales Including Tax = [Total Sales]+[Total Sales Tax Paid]
```

* \[Total Order Quantity\]

```text
Total Order Quantity = sum(Sales[OrderQuantity])
```

### Count of Occupation

![](.gitbook/assets/image%20%2845%29.png)

### 

### COUNT\(\)

* Total number of Products

```text
Total Number of Products = COUNT(Products[ProductName])
```

* Total Number of Customers

```text
Total Number of Customers = COUNT(Customers[Name])
```

![](.gitbook/assets/image%20%2857%29.png)

### COUNTROWS\(\)

* Total Number Of Products Countrows Version

```text
Total Number Of Products Countrows Version = COUNTROWS(Products)
```

* Total Number Of Customers Countrows Version 

```text
Total Number Of Customers Countrows Version = COUNTROWS(Products)
```

### DISTINCTCOUNT\(\)

* Total Number Of Customers DISTINCTCOUNT Version 

```text
Total Number Of Customers DISTINCTCOUNT Version = DISTINCTCOUNT(Customers[CustomerKey])
```

* Count of Occupation

```text
Count of Occupation = DISTINCTCOUNT(Customers[Occupation])
```

* Total Customers in Database DISTINCTCOUNT Version

![](.gitbook/assets/image%20%2843%29.png)

* Count of Country

```text
Count of Country = DISTINCTCOUNT(Territories[Country])
```

* Total Customer that have Purchased

```text
Total Customer that have Purchased = DISTINCTCOUNT(Sales[CustomerKey])
```

![](.gitbook/assets/image%20%2813%29.png)

![](.gitbook/assets/image%20%2834%29.png)

### MAX\(\),MIN\(\),AND AVERAGE\(\)

* Maximum Tax paid on A product

```text
Maximum Tax paid on A product = MAX(Sales[TaxAmt])
```

* Minimum Tax paid on A product 

```text
Minimum Tax paid on A product = Min(Sales[UnitPrice])
```

* Average Price Paid for a product

```text
Average Price Paid for a product = AVERAGE(Sales[UnitPrice])
```

### COUNTBLANK\(\)

* How many customers are missing address line 2 from the master data?
* How many products in the products table do not have a weight value stored in the master data?

```text
Coustomers Without Address Line 2 = COUNTBLANK(Customers[AddressLine2])
Products Without Weight Values = COUNTBLANK(Products[Weight])
```

### DIVIDE\(\)

```text
Total Margin % = DIVIDE([Total Margin $],[Total Sales])
```

* Markup %

```text
Markup % = DIVIDE([Total Margin $],[Total Cost])
```

* Tax % 

```text
Tax % = DIVIDE([Total Sales Tax Paid],[Total Sales])
```

![](.gitbook/assets/image%20%2840%29.png)



