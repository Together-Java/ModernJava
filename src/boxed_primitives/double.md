# Double

The type to use for a `double` that might be null is `Double`.

```java
~void main() {
Double d = null;
IO.println(d);
d = 3.14;
IO.println(d);
~}
```

If you try to do any math on a `Double` which holds `null` you will
get a `NullPointerException`.

```java,panics
~void main() {
Double d = null;
IO.println(d + 1);
~}
```