# Disconnected Tables

### What-if

![Don&apos;t forget to click &apos;add slicer to this page&apos;](.gitbook/assets/image%20%2856%29.png)

![](.gitbook/assets/image%20%2819%29.png)

![](.gitbook/assets/image%20%2843%29.png)

```text
Total Margin with Selected Increase = 
[Total Margin $]* (100 + Increase[Increase Value])/100
```

![](.gitbook/assets/image%20%2849%29.png)

![](.gitbook/assets/image%20%2838%29.png)

{% hint style="info" %}
Once you create a new table by the parameter button in the Fields list, you will have a new table with GENERATESERIES\(\)
{% endhint %}

### GENERATESERIS\(\) 

Generateseris\(\) can be used anytime you want to create a new table of values with a constant increment between values.

### The new Measure 

```text
Increase Value = SELECTEDVALUE('Increase'[Increase])
```

![](.gitbook/assets/image%20%2835%29.png)

* Total Customers Born Before Selected Year

```text
Total Customer Born Before Selected Year = 
CALCULATE([Total Number of Customers],
FILTER(Customers,Customers[BirthDate]<DATE('Year'[Year Value],1,1)))
```

![Cannot use calculate\(\)](.gitbook/assets/image%20%2828%29.png)

{% hint style="info" %}
CULCULATE\(\) doesn't work at here
{% endhint %}



![](.gitbook/assets/image%20%2877%29.png)

![](.gitbook/assets/image%20%2812%29.png)

### Harvester Measure

![](.gitbook/assets/image%20%2873%29.png)

* Create a new table and click Enter Data as above.

{% hint style="info" %}
Same technique used with what-if earlier, It checks to see if there is a single value selected for DisplayMeasure\[Measure ID\] and if so it returns that value, otherwise it returns BLANK.

It 'harvests' the selection from the user when used with a slicer.
{% endhint %}

* add DisplayMeasure\[Measure\] to the card.

![](.gitbook/assets/image%20%2827%29.png)

![Add a slicer](.gitbook/assets/image%20%2818%29.png)

Then create a new measure at Sales table

```text
Measure to Display = 
SWITCH([Selected Measure],1,[Total Sales],2,[Total Cost],3,[Total Margin $])
```

![](.gitbook/assets/image%20%2857%29.png)

Add a new Column Chart to the report as above, place calendar\[Year\] on the Axis and \[Measure to display \]as the value.

{% hint style="info" %}
If you have read this book, you will find out the formula of Measure to Display should be like this:
{% endhint %}



![](.gitbook/assets/image%20%2824%29.png)

{% hint style="info" %}
But it is not correct, it is not gonna work, you should change the formula from \[Selected value\] to \[Selected Measure\].
{% endhint %}



```text
Measure to Display = 
SWITCH([Selected Measure],1,[Total Sales],2,[Total Cost],3,[Total Margin $]*)
```

![](.gitbook/assets/image%20%2851%29.png)

* Create a new table
* Create 2 new column

![](.gitbook/assets/image%20%2839%29.png)

```text
Age = ROUNDDOWN((DATE(2003,1,1)-Customers[BirthDate])/365,0)
```

```text
Age Group = CALCULATE(VALUES(AgeBands[Band]),
FILTER(AgeBands,Customers[Age] >= AgeBands[Low] && Customers[Age] < Agebands[High]))
```

### Variables Syntax

VAR is always accompanied by a second keyword, RETURN.

```text
Age Group = 
VAR Age = ROUNDDOWN (( DATE(2003,1,1) - Customers[BirthDate] ) / 365,0)
RETURN 
 CALCULATE(VALUES(AgeBands[Band]),FILTER(AgeBands,Customers[Age]<=AgeBands[High] && customers[age] > AgeBands[Low]))
```

It also can be wrote like this:

```text
Age Group =
VAR AgeInDays =
ROUNDDOWN((DATE(2003,1,1)-Customers[BirthDate]),0)
VAR Age = AgeInDays / 365
RETURN
CALCULATE(
    VALUES(AgeBands[Band]),FILTER(AgeBands, Age >= AgeBands[Low] && Age<AgeBands[High]))
```

Include a table as below:

```text
Age Group =
VAR AgeInDays = 
ROUNDDOWN (( DATE(2003,1,1) - Customers[BirthDate]),0)
VAR Age = AgeInDays/365
VAR BandsTable = 
FILTER(AgeBands,Customers[Age]<=AgeBands[High] && customers[age] > AgeBands[Low])
RETURN 
 CALCULATE(VALUES(AgeBands[Band]),BandsTable)
```

### 

