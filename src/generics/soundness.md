# Soundness

Even though every `String` is assignable to `Object`, 
a `Box<String>` is not assignable to `Box<Object>`.

If that was allowed then you could do something like the following.

```java,no_run,does_not_compile
Box<String> stringBox = new Box<>();
// This might feel innocent
Box<Object> objectBox = stringBox;
// But now we can put anything,
// like an Integer, in the Box
objectBox.data = 123;
// Which is a problem since that affects
// stringBox as well
String s = stringBox.data; // But its actually an Integer! Crash!
```

We call this property - that the types don't let you accidentally make
silly situations - soundness. Java isn't _fully_ sound, but its sound enough
for most people.