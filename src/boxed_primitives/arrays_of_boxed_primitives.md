# Arrays of Boxed Primitives

If you have an array of the boxed version of a type, that is not
compatible with an array containing the unboxed version and vice-versa.[^interesting]

```java,does_not_compile,no_run
int[] numbersOne = { 1, 2, 3 };
Integer[] numbersTwo = { 4, 5, 6 };

// This line won't work
numbersOne = numbersTwo;
// And neither will this one
numbersTwo = numbersOne;
```

[^interesting]: The reasons for this are deeply interesting and have to do with the nitty gritty of how
Java is actually implemented. It might also change in the future.