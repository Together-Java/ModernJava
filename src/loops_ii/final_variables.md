# Final Variables

The initializer of a `for` loop can also declare `final` variables.

```java
~void main() {
int i = 0;
for (final String name = "Bob"; i < 5; i++) {
    IO.println(name + ": " + i);
}
~}
```

This doesn't have much use with loops that track `int`s and `String`s, but if you
are feeling clever you can use this ability along with arrays or other things you
can change without reassigning a variable.

```java
~void main() {
for (final char[] letters = { 'I', 'O', 'U' }; letters[0] != 'A';) {
    for (int i = 0; i < letters.length; i++) {
        letters[i] -= 1;
        System.out.print(letters[i]);
    }
    IO.println();
}

// HNT
// GMS
// FLR
// EKQ
// DJP
// CIO
// BHN
// AGM
~}
```

There aren't many reasons to do this, but it is in fact not against the law and I cannot stop you.
