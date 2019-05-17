# Disconnected Tables

### What-if

![Don&apos;t forget to click &apos;add slicer to this page&apos;](.gitbook/assets/image%20%2851%29.png)

![](.gitbook/assets/image%20%2817%29.png)

![](.gitbook/assets/image%20%2839%29.png)

```text
Total Margin with Selected Increase = 
[Total Margin $]* (100 + Increase[Increase Value])/100
```

![](.gitbook/assets/image%20%2845%29.png)

![](.gitbook/assets/image%20%2835%29.png)

{% hint style="info" %}
Once you create a new table by the parameter button in the Fields list, you will have a new table with GENERATESERIES\(\)
{% endhint %}

### GENERATESERIS\(\) 

Generateseris\(\) can be used anytime you want to create a new table of values with a constant increment between values.

### The new Measure 

```text
Increase Value = SELECTEDVALUE('Increase'[Increase])
```

![](.gitbook/assets/image%20%2832%29.png)

* Total Customers Born Before Selected Year

```text
Total Customer Born Before Selected Year = 
CALCULATE([Total Number of Customers],
FILTER(Customers,Customers[BirthDate]<DATE('Year'[Year Value],1,1)))
```

![Cannot use calculate\(\)](.gitbook/assets/image%20%2825%29.png)

{% hint style="info" %}
CULCULATE\(\) doesn't work at here
{% endhint %}



![](.gitbook/assets/image%20%2871%29.png)

![](.gitbook/assets/image%20%2810%29.png)

### Harvester Measure

![](.gitbook/assets/image%20%2867%29.png)

* Create a new table and click Enter Data as above.

{% hint style="info" %}
Same technique used with what-if earlier, It checks to see if there is a single value selected for DisplayMeasure\[Measure ID\] and if so it returns that value, otherwise it returns BLANK.

It 'harvests' the selection from the user when used with a slicer.
{% endhint %}

* add DisplayMeasure\[Measure\] to the card.

![](.gitbook/assets/image%20%2824%29.png)

![Add a slicer](.gitbook/assets/image%20%2816%29.png)



