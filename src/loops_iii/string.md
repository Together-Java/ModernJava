# String

One thing that feels like it _should_ implement the `Iterable` interface but does not is `String`.

```java,does_not_compile
~class Main {
~   void main() {
String letters = "abc";
for (char letter : letters) {
    System.out.println(letter);
}
~   }
~}
```

To loop over all the characters in a `String`, you have to use a regular loop.

```java,does_not_compile
~class Main {
~   void main() {
String letters = "abc";
for (int i = 0; i < letters.length(); i++) {
    char letter = letters.charAt(i);
    System.out.println(letter);
}
~   }
~}
```