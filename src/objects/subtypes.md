# Subtypes

We consider most everything to be a "subtype"
of `Object`.

This means that if you have a variable or field that holds an `Object`
you can assign any data you want into it.

```java
~void main() {
String oak = "oak";
Object tree = oak;
System.out.println(tree);
~}
```

If something is a subtype of `Object`, we would call `Object`
its "supertype."[^super]

[^super]: Super meaning above and Sub meaning below. God how I feel for people who learn
english as a second language.