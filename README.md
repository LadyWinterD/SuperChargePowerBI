# Introduction

## Reading Notes -Super Charge Power BI

There are some reading notes I have been done through I read this book, I hope It could be helpful for you .

![](.gitbook/assets/image%20%2863%29.png)



### The error I found in this book:

* Chapter 17:Creating a Morphing Switch Measure 



{% hint style="info" %}
If you have read this book, you will find out the formula of Measure to Display should be like this:
{% endhint %}



![](.gitbook/assets/image%20%2824%29.png)

{% hint style="info" %}
But it is not correct, it is not gonna work, you should change the formula from \[Selected value\] to \[Selected Measure\].
{% endhint %}



```text
Measure to Display = 
SWITCH([Selected Measure],1,[Total Sales],2,[Total Cost],3,[Total Margin $])
```





## Useful Link:

#### A Free Quick Reference Guide

{% embed url="https://exceleratorbi.com.au/shop/" %}

#### DAX Formatter

{% embed url="http://www.daxformatter.com/" caption="DAX Formatter" %}

![](.gitbook/assets/image%20%2815%29.png)

#### Reference DAX

{% embed url="https://exceleratorbi.com.au/exceleratorblog/" caption="" %}







