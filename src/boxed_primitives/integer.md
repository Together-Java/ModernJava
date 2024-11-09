# Integer

The type to use for an `int` that might be null is `Integer`.

```java
~void main() {
Integer i = null;
System.out.println(i);
i = 5;
System.out.println(i);
~}
```

If you try to do any math on an `Integer` which holds `null` you will
get a `NullPointerException`.

```java,panics
~void main() {
Integer i = null;
System.out.println(i * 5);
~}
```