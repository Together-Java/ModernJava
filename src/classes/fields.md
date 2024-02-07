# Fields

Classes contain zero or more fields.

Fields are like variables except they don't live in a method,
they are attached to instances of the class they are a part of.

To declare a field in a class you say the type of the field, a name for the field,
and then a `;`.

```java
class Muppet {
    String name;
}
```

One way to think about it is that when you say `new Muppet()`, Java makes a box big enough to hold
all of the fields that a muppet needs.[^box]

[^box]: This "box" metaphor is part of where the name "boxed primitives" comes from.
