# Disconnected Tables

### What-if

![Don&apos;t forget to click &apos;add slicer to this page&apos;](.gitbook/assets/image%20%2852%29.png)

![](.gitbook/assets/image%20%2817%29.png)

![](.gitbook/assets/image%20%2840%29.png)

```text
Total Margin with Selected Increase = 
[Total Margin $]* (100 + Increase[Increase Value])/100
```

![](.gitbook/assets/image%20%2846%29.png)

![](.gitbook/assets/image%20%2836%29.png)

{% hint style="info" %}
Once you create a new table by the parameter button in the Fields list, you will have a new table with GENERATESERIES\(\)
{% endhint %}

### GENERATESERIS\(\) 

Generateseris\(\) can be used anytime you want to create a new table of values with a constant increment between values.

### The new Measure 

```text
Increase Value = SELECTEDVALUE('Increase'[Increase])
```

![](.gitbook/assets/image%20%2833%29.png)

* Total Customers Born Before Selected Year

```text
Total Customer Born Before Selected Year = 
CALCULATE([Total Number of Customers],
FILTER(Customers,Customers[BirthDate]<DATE('Year'[Year Value],1,1)))
```

![Cannot use calculate\(\)](.gitbook/assets/image%20%2826%29.png)

{% hint style="info" %}
CULCULATE\(\) doesn't work at here
{% endhint %}



![](.gitbook/assets/image%20%2873%29.png)

![](.gitbook/assets/image%20%2810%29.png)

### Harvester Measure

![](.gitbook/assets/image%20%2869%29.png)

* Create a new table and click Enter Data as above.

{% hint style="info" %}
Same technique used with what-if earlier, It checks to see if there is a single value selected for DisplayMeasure\[Measure ID\] and if so it returns that value, otherwise it returns BLANK.

It 'harvests' the selection from the user when used with a slicer.
{% endhint %}

* add DisplayMeasure\[Measure\] to the card.

![](.gitbook/assets/image%20%2825%29.png)

![Add a slicer](.gitbook/assets/image%20%2816%29.png)

Then create a new measure at Sales table

```text
Measure to Display = 
SWITCH([Selected Measure],1,[Total Sales],2,[Total Cost],3,[Total Margin $])
```

![](.gitbook/assets/image%20%2853%29.png)

Add a new Column Chart to the report as above, place calendar\[Year\] on the Axis and \[Measure to display \]as the value.

{% hint style="info" %}
If you have read this book, you will find out the formula of Measure to Display should be like this:
{% endhint %}



![](.gitbook/assets/image%20%2822%29.png)

{% hint style="info" %}
But it is not correct, it is not gonna work, you should change the formula from \[Selected value\] to \[Selected Measure\].
{% endhint %}



```text
Measure to Display = 
SWITCH([Selected Measure],1,[Total Sales],2,[Total Cost],3,[Total Margin $])
```



