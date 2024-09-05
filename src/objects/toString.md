# toString

All `Object`s have a `toString` method. 

This is intended to be a suitable representation for debugging,
although one may choose to favor different concerns.

For built-in classes the result of their `toString` method is likely
what you'd expect.

```java
~class Apple {}
~void main() {
Object o = "123";

// If its already a String, toString() doesn't
// have to do much work
System.out.println(o.toString());

o = 123;
// Integers, Longs, etc. all have a representation
// which looks the same as they do in literal form.
System.out.println(o.toString());

o = new Apple();
// And custom classes will, by default, just have the
// class name followed by gibberish
System.out.println(o.toString());
~}
```

