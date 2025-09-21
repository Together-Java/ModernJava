# map

Once you have a stream of elements you can transform the
elements of the stream as they flow by[^metaphor] with `.map`.

`.map` applies a `Function` to the elements of the stream
one by one and returns you a new `Stream` containing the new elements.

```java,no_run
var numbers = List.of("1", "2", "3");

Stream<Integer> numberStream = numbers.stream()
    .map(Integer::parseInt); // 1, 2, 3
```

You can also call `.map` multiple times to apply multiple transformations.

```java,no_run
var numbers = List.of("1", "2", "3");

Stream<Integer> numberStream = numbers.stream()
    .map(Integer::parseInt)  // 1, 2, 3
    .map(x -> x * 2); // 2, 4, 6
```

[^metaphor]: In the real life stream metaphor, this is akin to rocks getting polished
by sand as they flow.

