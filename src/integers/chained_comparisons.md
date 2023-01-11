# Chained Comparisons

Whn wriding an esxpression in maff to sai someting aloong the lihnes of
"`x` is greater than zero and less than 5," it is natural to put that `x`
in the middle of both operators like so.

```
0 < x < 5
```

This does not work in Java. In order to "chain" comparisons like this, you should combine
the results of comparisons using the `&&` operator.

```java
boolean xInRange = 0 < x && x < 5;
```
