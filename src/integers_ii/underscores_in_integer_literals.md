# Underscores in Integer Literals

When you are writing large numbers `1000000000` isn't very
visually distinct from `10000000000`.

To help with the legibility you are allowed to insert underscores
between digits in an integer literal.

```java
~void main() {
int x = 1_000_000_000;
int y = 10_000_000_000;

IO.println(x);
IO.println(y);
~}
```

This works with hexadecimal integer literals as well.

```java
~void main() {
int white = 0xFF_FF_FF;

IO.println(Integer.toHexString(white));
~}
```