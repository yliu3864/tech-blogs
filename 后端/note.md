### JPA

```java
    @Query("select t from MarketingHomePopup t where (t.startTime is null or t.startTime <= ?1) and (t.endTime is null or t.endTime >= ?1) and t.status = 'able' order by t.position ")
    @Query("SELECT new ca.core.product.model.ProductItem(t) FROM Product t WHERE t.productType = ?1 and t.status = 'able' and t.isInSaleList = true and t.productUseType is null order by t.weight, t.createTime")
```

### copy prop

```java
BeanUtils.copyProperties(source, dest);
```

### list 

```java
list.stream()
    .map(item:new)
    .filter(it->{
        //condition
        return 
    })
    .collect(Collectors.toList());
```

