# Declaration

To declare a record you write the word `record` followed by a
class name, a list of "record components" in parentheses, and a pair of `{}`.

The list of record components should be reminiscent of function arguments.

```java
record Person(String name, int age) {}
```

Having an empty list of record components is also allowed.[^astowhy]

```java
record Pants() {}
```

[^astowhy]: As to why you might want to give an empty list of record components,
it's nuanced. For now it's just for fun.