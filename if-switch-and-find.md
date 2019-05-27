# IF\(\),SWITCH\(\),and FIND\(\)

### FIND\(\)

```text
Mountain Products = FIND("Mountain",Products[ModelName],1,0)
```

![](.gitbook/assets/image.png)

### IF\(\)

```text
Mountain Products = if(FIND("Mountain",Products[ModelName],1,0)>0,TRUE(),FALSE())
```

![](.gitbook/assets/image%20%289%29.png)



