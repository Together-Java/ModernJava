# Strip extra whitespace

If you have a `String` which might contains some extra "trailing" whitespace or extra "leading"
whitespace, you can remove that by using the `.strip` method.

This will give a new `String` with both the leading and trailing whitespace removed.

```java
void main() {
    String message = "   Happy Valentines Day.   ";

    System.out.print(message.strip());
    IO.println("|");
}
```

If you want to just remove the leading whitespace, you can use `.stripLeading`.

```java
void main() {
    String message = "   Happy Valentines Day.   ";

    System.out.print(message.stripLeading());
    IO.println("|");
}
```

And to remove only trailing whitespace, `.stripTrailing`.

```java
void main() {
    String message = "   Happy Valentines Day.   ";

    System.out.print(message.stripTrailing());
    IO.println("|");
}
```

All of these methods are useful when you get input from human beings. Humans are generally pretty bad at seeing if they hit the spacebar one too many times.