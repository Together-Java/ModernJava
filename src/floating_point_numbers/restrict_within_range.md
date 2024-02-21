# Restrict within range

When doing some calculations you might want to enforce that the result falls within a certain range.

In Java 21 `java.lang.Math` got expanded with a clamp function for `double`, `float`, `clamp` and `long` in the form of: `clamp(value, min, max)`

So if we were to do:
`double result = Math.clamp(100*100, 2, 50)` the result would be 50.

In older versions we'd have to use a function like the following to handle this:

```java
public int clamp(int value, int min, int max) {
  if (value > max) {
    return max;
  } else if (value < min) {
    return min;
  } else {
    return value;
  }
}
```