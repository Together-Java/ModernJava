# Integer from a String

If you have a `String` which contains text that can be interpreted
as an integer you can convert it to an `int` using the `parseInt`
static method on `Integer`.[^already]

```java
~void main() {
String text = "123";

int oneTwoThree = Integer.parseInt(text);

IO.println(oneTwoThree);
~}
```

If what is in the `String` cannot be converted to an `int` that method
will throw a `NumberFormatException`.

```java,panics
~void main() {
String word = "music";

int value = Integer.parseInt(word);
~}
```

If you want to handle input from a user that might not be interpretable
as an integer, you can use `try`/`catch` alongside delayed assignment.

```java
~void main() {
String word = "seltzer";

int value;
try {
    value = Integer.parseInt(word);
} catch (NumberFormatException e) {
    value = 8; // Default value
}
~}
```

[^already]: You should actually already know this. I just never explained explicitly that parseInt was a static method or showed that you could catch _only_ the `NumberFormatException`. In my defense, `IO.readln`
at one point came far later in the book.