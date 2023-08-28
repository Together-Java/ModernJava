# Conditional Operator

When the only operation being performed inside of an `if` and `else` pair
is setting the initial value of a variable, you can use the "conditional operator"[^ternary]
to perform that assignment instead.

```java
int age = 22;

String message = age < 25
    ? "You cannot rent a car!"
    : "You might be able to rent a car";
```

You write a condition followed by a `?`, a value to use when that condition evaluates to `true`, a `:`,
and then a value to use when that condition evaluates to `false`.

```java
CONDITION ? WHEN_TRUE : WHEN_FALSE
```

[^ternary]:
    Some people will call this a ternary expression. Ternary meaning "three things."
    Same idea as tres leches.
