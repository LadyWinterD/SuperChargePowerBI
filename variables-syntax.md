# Variables Syntax

VAR is always accompanied by a second keyword, RETURN. 

```text
Age Group = 
VAR AgeInDays = 
ROUNDDOWN (( DATE(2003,1,1) - Customers[BirthDate]),0)
VAR Age = AgeInDays/365
VAR BandsTable = 
FILTER(AgeBands,Age<=AgeBands[High] && Age > AgeBands[Low])
RETURN 
 CALCULATE(VALUES(AgeBands[Band]),BandsTable)
```

![](.gitbook/assets/image%20%284%29.png)

