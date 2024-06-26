# lowercase

In English[^otherlangs] letters can be either lower-cased (`a`, `b`, `c`) or upper-cased (`A`, `B`, `C`).

If you have a `String` which potentially contains upper-cased letters, you can get a new `String` with everything
transformed into lower-case using the `.toLowerCase()` method.

```java
void main() {
    String message = "Happy Valentines Day";

    String lowerCased = message.toLowerCase();
    System.out.println(lowerCased);
}
```

This does not change the original `String` in place. It just makes a new `String` with all lower-case letters.


[^otherlangs]: Other languages also have a notion of case. I am not a polyglot though, so I'm not qualified
to talk about them.