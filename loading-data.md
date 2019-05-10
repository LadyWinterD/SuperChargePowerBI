# Loading Data

## Download the sample Database

{% embed url="https://exceleratorbi.com.au/learn-to-write-dax/" caption="Sample database" %}

You will have 5 tables after you unzip it. 

* Sales
* Products
* Territory
* Calendar
* Customers

You can import it in Power BI Desktop.

![](.gitbook/assets/image%20%287%29.png)

![](.gitbook/assets/image%20%285%29.png)



{% hint style="info" %}
It is possible for things to go wrong, especially the first time you load data from access. The most common cause of problems is that you have 32-bit Microsoft office installed on your PC and 64-bit Power BI ,In that case you need to download the 64-bit version of the access database.

[https://www.microsoft.com/en-nz/p/access/cfq7ttc0k7q8?activetab=pivot%3aoverviewtab](https://www.microsoft.com/en-nz/p/access/cfq7ttc0k7q8?activetab=pivot%3aoverviewtab)
{% endhint %}

You will see the tables as below:

![Change the Territory to Territories\(Double-Click the Territory table on the right ,and rename it\)](.gitbook/assets/image%20%281%29.png)

### Relationships

Click the left side , you can see the relationships between the tables.

![](.gitbook/assets/image%20%283%29.png)

Power BI guessing which relationships should be used, these automatically created relationships may or may not be correct.In this case, it is correct.

### Joining tables

![](.gitbook/assets/image%20%2814%29.png)

### Editing Query

![](.gitbook/assets/image%20%2811%29.png)

### Remove the three fiscal solumns

![](.gitbook/assets/image%20%2823%29.png)

### Click Close & Apply and save the pbix workbook.

### Remove the steps in a Query

![](.gitbook/assets/image.png)

### Importing new tables 

![](.gitbook/assets/image%20%2810%29.png)

![](.gitbook/assets/image%20%289%29.png)

### Changing the name to SubCategory

![](.gitbook/assets/image%20%2812%29.png)

### It has been connected automatically , you can see the relationships as below, but we don't need SubCategory table any more, just DELETED it.

![](.gitbook/assets/image%20%2824%29.png)



