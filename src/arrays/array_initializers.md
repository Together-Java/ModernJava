# Array Initializers

To give an initial value to an array you can use an array initializer.

After the equals sign you write `{` followed by a comma separated list of elements and a final `}`.

```java
int[] numbers = { 1, 2, 3 }
             // |---------|
             // this part is
             // the initializer
```

The elements in an initializer do not have to be literals and can also be variables or expressions.

```java
int two = 2;
// Will hold 1, 2, 3 just like the array above
int[] numbers = { 1, two, two + 1 }
```

We call them array initializers because you use them to give an initial value to an array.[^pattern]

[^pattern]: You may be noticing a pattern. Confusing sounding names are often kinda "obvious" with enough context.
