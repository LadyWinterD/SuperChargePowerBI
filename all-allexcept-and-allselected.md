# ALL\(\), ALLEXCEPT\(\), and ALLSELECTED\(\)

### ALL\(\)

```text
Total ALL Products = COUNTROWS(ALL(Products))
```

![](.gitbook/assets/image%20%2821%29.png)

```text
Total Global Sales = CALCULATE([Total Sales],ALL(Territories))
```

![](.gitbook/assets/image%20%2846%29.png)

* % of Global Sales 

```text
% of Global Sales = DIVIDE([Total Sales],[Total Global Sales])
```

![](.gitbook/assets/image%20%2834%29.png)

### Quick Measures Option

```text
Total Sales total for Country = 
CALCULATE([Total Sales], ALLSELECTED('Territories'[Country]))
```

### ALLEXCEPT\(\)

```text
Total Sales total for Country = 
CALCULATE([Total Sales], ALL('Territories'[Country]))
Total Sales total for Country 2 = 
CALCULATE([Total Sales], ALLEXCEPT(Territories,Territories[Group])
```

### ALLSELECTED\(\)

Removes the filters from the matrix but respect the filters in the slicer.

```text
Total Slected Territories = 
CALCULATE([Total Sales],ALLSELECTED(Territories))
```

```text
% of Selected Territorries = 
DIVIDE([Total Sales],[Total Selected Territories])
```

```text
% of Selected Territories ONE STEP =
 DIVIDE(
 [Total Sales],
 CALCULATE([Total Sales],ALLSELECTED(Territories)
 ))
```

![](.gitbook/assets/image%20%2855%29.png)

### Practice Exercises

```text
Total Sales to All Customers = CALCULATE([Total Sales],ALL(Customers))
```

```text
% of All Customer Sales = DIVIDE([Total Sales],[Total Sales to All Customers])
```

```text
% Sales of Selected Customers = 
DIVIDE([Total Sales],
(CALCULATE([Total Sales],ALLSELECTED(Customers))))
```

![](.gitbook/assets/image%20%2826%29.png)

{% hint style="info" %}
ALLSELECTED\(\) Removes the filters from the matrix but respect the filters in the slicer.
{% endhint %}

* Total Sales for All Days Selected Dates

```text
Total Sales for All Days Selected Dates = 
CALCULATE([Total Sales],ALLSELECTED('Calendar'))

% Sales for ALL Days Selected Dates = 
DIVIDE([Total Sales],[Total Sales for All Days Selected Dates])
```

### ALLEXCEPT\(\)

![](.gitbook/assets/image%20%2842%29.png)

![](.gitbook/assets/image%20%2861%29.png)

```text
Total Orders ALL Customers = CALCULATE([Total Order Quantity],all(Customers))
```

```text
Baseline order of All customer orders = CALCULATE([Total Order Quantity],
ALLEXCEPT(Customers,Customers[Occupation]))
```

```text
% Baseline % this Occupation is of All customer orders =
 DIVIDE([Baseline order of All customer orders],[Total Orders ALL Customers])

```

```text
Total Orders Selected Customers =
 CALCULATE([Total Order Quantity],ALLSELECTED(Customers))
```

```text
Occupation % of Selected Customers = DIVIDE([Total Order Quantity],[Total Orders Selected Customers])

```

```text
Percentage Point Variation to Baseline = 
[Occupation % of Selected Customers] -[Baseline % this Occupation is of All customer orders]
```

![](.gitbook/assets/image%20%2820%29.png)

