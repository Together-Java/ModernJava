# Integer from a Base 16 String

If you have a `String` which contains text that can be interpreted as a base 16 integer, you can convert it into an `int` by using `parseInt` and giving the
number `16` as an extra argument.

```java
~void main() {
String text = "C";

int twelve = Integer.parseInt(text, 16);

IO.println(twelve);
~}
```

This will not work if the number is prefixed by `0x` like it would be in your code.

```java,panics
~void main() {
Integer.parseInt("0xC", 16);
~}
```

If you want to handle both hexadecimal numbers and regular base 10 numbers you should instead use `Integer.decode`.

```java
~void main() {
IO.println(Integer.decode("0xC"));
IO.println(Integer.decode("0x19"));
IO.println(Integer.decode("19"));
~}
```