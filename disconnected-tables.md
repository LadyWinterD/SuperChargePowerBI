# Disconnected Tables

### What-if

![Don&apos;t forget to click &apos;add slicer to this page&apos;](.gitbook/assets/image%20%2848%29.png)

![](.gitbook/assets/image%20%2815%29.png)

![](.gitbook/assets/image%20%2836%29.png)

```text
Total Margin with Selected Increase = 
[Total Margin $]* (100 + Increase[Increase Value])/100
```

![](.gitbook/assets/image%20%2842%29.png)

![](.gitbook/assets/image%20%2832%29.png)

{% hint style="info" %}
Once you create a new table by the parameter button in the Fields list, you will have a new table with GENERATESERIES\(\)
{% endhint %}

### GENERATESERIS\(\) 

Generateseris\(\) can be used anytime you want to create a new table of values with a constant increment between values.

### The new Measure 

```text
Increase Value = SELECTEDVALUE('Increase'[Increase])
```

![](.gitbook/assets/image%20%2829%29.png)

* Total Customers Born Before Selected Year

```text
Total Customers Born Before Selected Year = 
CALCULATE([Total Number of Customers],
FILTER(Customers,Customers[BirthDate]<DATE([Customers'age Value],1,1)))
```

![Cannot use calculate\(\)](.gitbook/assets/image%20%2822%29.png)



