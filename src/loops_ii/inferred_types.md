# Inferred Types

The initializer of a `for` loop works the same as any variable assignment, so
you still are allowed to use `var` so that the type of the declared variable is inferred.

```java
for (var i = 0; i < 10; i++) {
    System.out.println(i);
}
```

`var` is the same number of letters as `int` so you aren't gaining much when your `for` loop
is just counting over numbers.

But if your `for` loop is doing something more exotic, it might make sense.

```java
for (var repeated = ""; repeated.length() < 5; repeated = repeated + "a") {
    System.out.println(repeated);
}

// a
// aa
// aaa
// aaaa
```
