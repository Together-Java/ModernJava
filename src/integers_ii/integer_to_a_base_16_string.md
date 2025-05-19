# Integer to a Base 16 String

If you have an integer you want to turn into a `String` in base 16
integer you can use the `toHexString` method on `Integer`.

```java
~void main() {
int x = 29411;
String xStr = Integer.toHexString(x);

// 72e3
IO.println(xStr);
~}
```