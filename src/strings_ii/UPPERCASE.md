# UPPERCASE

Similarly, if you have a `String` which potentially contains lower-cased letters, you can get a new `String` with everything
transformed into lower-case using the `.toUpperCase()` method.

```java
void main() {
    String message = "Happy Valentines Day";

    String upperCased = message.toUpperCase();
    IO.println(upperCased);
}
```

This does not change the original `String` in place. It just makes a new `String` with all upper-case letters.