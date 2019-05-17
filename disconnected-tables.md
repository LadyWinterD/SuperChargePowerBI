# Disconnected Tables

### What-if

![Don&apos;t forget to click &apos;add slicer to this page&apos;](.gitbook/assets/image%20%2849%29.png)

![](.gitbook/assets/image%20%2816%29.png)

![](.gitbook/assets/image%20%2837%29.png)

```text
Total Margin with Selected Increase = 
[Total Margin $]* (100 + Increase[Increase Value])/100
```

![](.gitbook/assets/image%20%2843%29.png)

![](.gitbook/assets/image%20%2833%29.png)

{% hint style="info" %}
Once you create a new table by the parameter button in the Fields list, you will have a new table with GENERATESERIES\(\)
{% endhint %}

### GENERATESERIS\(\) 

Generateseris\(\) can be used anytime you want to create a new table of values with a constant increment between values.

### The new Measure 

```text
Increase Value = SELECTEDVALUE('Increase'[Increase])
```

![](.gitbook/assets/image%20%2830%29.png)

* Total Customers Born Before Selected Year

```text
Total Customer Born Before Selected Year = 
CALCULATE([Total Number of Customers],
FILTER(Customers,Customers[BirthDate]<DATE('Year'[Year Value],1,1)))
```

![Cannot use calculate\(\)](.gitbook/assets/image%20%2823%29.png)

{% hint style="info" %}
CULCULATE\(\) doesn't work at here
{% endhint %}



![](.gitbook/assets/image%20%2868%29.png)

![](.gitbook/assets/image%20%2810%29.png)

### SWITCH\(\)



