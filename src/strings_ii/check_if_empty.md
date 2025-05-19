# Check if empty

You can check if a `String` is empty in a few ways.

The one you should already have been able to figure out[^noshame] is that you can get the `.length` of a `String`
and see if that is zero.

```java
void main() {
    String textMessages = "";
    IO.println(
        textMessages.length() == 0
    );
}
```

But another is to use the explicitly defined `.isEmpty()` method.

```java
void main() {
    String textMessages = "";
    IO.println(
        textMessages.isEmpty()
    );
}
```

This can be more convenient. Both to write, as it is fewer characters to type, and to read later on.

[^noshame]: Again, no shame if not. I didn't exactly call attention to it.