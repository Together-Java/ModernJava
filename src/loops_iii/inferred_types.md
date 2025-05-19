# Inferred Types

A variable declaration in a for-each loop can make use of `var` to infer its type.

```java
~class Main {
~   void main() {
String[] chairMaterials = { "wicker", "wood", "plastic" }
for (var chairMaterial : chairMaterials) {
    IO.println(chairMaterial);
}
~   }
~}
```

And this is good to know for the same reasons you would use `var` other places in Java.
Writing `Book book` can be a drain on the soul.
