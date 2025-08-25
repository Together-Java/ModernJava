# filter

With a stream of elements you can also drop the
elements of the stream as they flow by[^metaphor] with `.filter`.

`.filter` will test each element with a predicate. If the
predicate returns `true` the element will be retained.
If it returns `false` the element will be dropped.


```java,no_run
var numbers = List.of("1", "2", "3");

Stream<Integer> numberStream = numbers.stream()
    .map(Integer::parseInt) // 1, 2, 3
    .filter(x -> x % 2 == 1); // 1, 3
```

[^metaphor]: In the real life stream metaphor, this is akin to rocks stuck along the way and not
continuing to go with the flow of water.
