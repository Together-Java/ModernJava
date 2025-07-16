# Integer to a String

If you have an integer you want to turn into a `String` you have two options.

One is to "add it" to an empty string.

```java
~void main() {
int x = 4;
String xStr = "" + x;

IO.println(xStr);
~}
```

The other is to use the `toString` static method on `Integer`.


```java
~void main() {
int x = 4;
String xStr = Integer.toString(x);

IO.println(xStr);
~}
```

I personally find the second one more direct, but opinions can reasonably vary.