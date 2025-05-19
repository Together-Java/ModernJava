# StringBuilder

When you add `String`s together, the result is a new `String`.

```java
void main() {
    String a = "a";
    String b = "b";
    String ab = a + b;

    IO.println(ab);
}
```

This is perfectly fine and what you would expect, but if you are adding strings
together in a loop it can become an issue.

```java
```