# Types

When a variable is declared, it is given a type.

```java,no_run
String color = "green";
```

In this case, the variable `color` is declared to have the type `String`.
After this declaration, `color` cannot be assigned to a value that is not a `String`.

```java,no_run
// A number is not a String!
String color = 8;
```

This applies to all situations where a variable might be given a value,
including delayed assignment and reassignment.

One mental model is that types are like shapes. If the type of something is a circle,
you can only put circles into it.

```java,no_run
◯ thing = ◯;
```

You cannot put square pegs in that round hole.

```java,no_run
// If Java actually functioned in terms of shapes, this
// would not work since a Square is not the same "type"
// of thing as a Circle.
◯ thing = ▢;
```
