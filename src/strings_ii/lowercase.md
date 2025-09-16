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

Many other languages also have a distinction between upper-case and lower-case and, usually, `.toLowerCase()` does the "right thing" for them too:

```java
~void main() {
// Cyrillic
IO.println("ПРИВЕТ".toLowerCase()); // prints "привет"
~}
```

In different languages the mapping between upper-case and lower-case letters can differ. 

For example, in Turkish the lower-case form of the letter `I` is `ı` and not `i`. 
By default, Java uses the rules for the language of the computer it is running on.
So `"I".toLowerCase()` will return `"i"` on an English system and `"ı"` on a Turkish one.

To get behavior that is consistent regardless of the machine it is being run on
you can pass use an explicit `Locale`.

```java
~void main() {
IO.println("I".toLowerCase(Locale.US)); // i - on every computer
IO.println("I".toLowerCase(Locale.forLanguageTag("tr-TR"))); // ı - on every computer
~}
```