# Ragged Arrays

In relatively unique circumstances[^alreadyunique] you might want to make a "ragged array". That is, a multi-dimensional
array where each array might be of a different size.

You can do this by making the number of elements in nested initializers be different
```java
boolean[][] triangle = {
    { false },
    { false, false, false},
    { false, false, false, false, false },
    { false, false, false},
    { false }
}
```

Or by using arrays initialized with `new` inside of an initializer.

```java,no_run
boolean[][] triangle = {
    new boolean[1],
    new boolean[3],
    new boolean[5],
    new boolean[3],
    new boolean[1]
};
```

Or even by omitting the trailing dimensions on when initializing with new and later filling in each row.

```java,no_run
boolean[][] triangle = new boolean[5][];
triangle[0] = new boolean[1];
triangle[1] = new boolean[3];
triangle[2] = new boolean[5];
triangle[3] = new boolean[3];
triangle[4] = new boolean[1];
```



[^alreadyunique]: And if you are using a multi-dimensional array, you are already doing something interesting.