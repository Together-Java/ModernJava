# Pure Functions

When a method only uses its arguments in order to compute a return value
but doesn't otherwise change the outside world, we call those methods
"pure functions."

```java
// square just uses x to compute the square of x
int square(int x) {
    return x * x;
}
```

If a method changes any values non-local to it, such as by assigning values to an array,
we consider it to be "impure."

```java
void multiplyAllByTwo(int[] numbers) {
    for (int i = 0; i < numbers.length; i++) {
        //
        numbers[i] = numbers[i] * 2;
    }
}

The term "pure" comes from the notion of "pure mathematics."
```
