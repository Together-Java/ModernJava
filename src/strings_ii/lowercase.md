# lowercase

In English, letters can be either lower-cased (`a`, `b`, `c`) or upper-cased (`A`, `B`, `C`).

If you have a `String` which potentially contains upper-cased letters, you can get a new `String` with everything
transformed into lower-case using the `.toLowerCase()` method.

```java
void main() {
    String message = "Happy Valentines Day";

    String lowerCased = message.toLowerCase();
    IO.println(lowerCased);
}
```

This does not change the original `String` in place. It just makes a new `String` with all lower-case letters.

What about other languages? Many of them also have a distinction between uppercase and lowercase, and usually, `.toLowerCase()` does the right thing for them too:

```java,no_run
~void main() {
// Cyrillic
IO.println("ПРИВЕТ".toLowerCase()); // prints "привет"
~}
```

However, in different languages, the mapping between uppercase and lowercase characters can differ. For example, in Turkish, the lowercase form of the letter `I` is `ı` without a dot. By default, Java uses the rules for the language of the operating system, so `"I".toLowerCase()` will return `"i"` on an English system and `"ı"` on a Turkish one.