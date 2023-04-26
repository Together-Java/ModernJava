# Conversion

When a value is returned, Java will want to coerce it into
the type of value that the method says it returns.

If Java knows how to do that conversion, then it can happen automatically.

```java
// This method declares a return type of double.
double returnFive() {
    // x is an int
    int x = 5;
    // When it is returned, it will be turned into a double 
    return x;
}
```

But if that conversion might potentially be lossy, as with converting `double`s to `int`s,
you must do it yourself.

```java
double returnNine() {
    double nine = 9.0;
    // The (int) explicitly converts the double to an int
    return (int) nine;
}
```