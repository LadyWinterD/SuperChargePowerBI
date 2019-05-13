# ALL\(\), ALLEXCEPT\(\), and ALLSELECTED\(\)

### ALL\(\)

```text
Total ALL Products = COUNTROWS(ALL(Products))
```

![](.gitbook/assets/image%20%2814%29.png)

```text
Total Global Sales = CALCULATE([Total Sales],ALL(Territories))
```

![](.gitbook/assets/image%20%2834%29.png)

* % of Global Sales 

```text
% of Global Sales = DIVIDE([Total Sales],[Total Global Sales])
```

![](.gitbook/assets/image%20%2825%29.png)

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

![](.gitbook/assets/image%20%2840%29.png)

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

![](.gitbook/assets/image%20%2819%29.png)

{% hint style="info" %}
ALLSELECTED\(\) Removes the filters from the matrix but respect the filters in the slicer.
{% endhint %}

* Total Sales for All Days Selected Dates



