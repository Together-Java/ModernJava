# Unboxing Conversion

If you try to use a boxed primitive in a context where
the normal type is expected, it will be implicitly "unboxed."

This means you can use `Integer`s directly in math expressions.

```java, no_run
void main() {
    Integer x = 5;
    int y = 3;
    int z = x * y;

    System.out.println(z);
}
```

As well as `Boolean`s in logical expressions.

```java, no_run
void main() {
    Boolean hasHat = true;
    if (hasHat) {
        System.out.println("You have a hat!");
    }
}
```

And so on for `Double`, `Character`, etc.

But if you use one of these types like this and they happen to be `null` you will
get a `NullPointerException`.

```java, panics
void main() {
    Integer x = null;
    // Bool
    int y = x;
}
```