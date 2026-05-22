# Conditional Operator

When the only operation being performed inside of an `if` and `else` pair
is setting the initial value of a variable, you can use the "conditional operator"[^ternary]
to perform that assignment instead.

```java
~void main() {
int age = 22;

String message = age < 25
    ? "You cannot rent a car!"
    : "You might be able to rent a car";

IO.println(message);
~}
```

You write a condition followed by a `?`, a value to use when that condition evaluates to `true`, a `:`,
and then a value to use when that condition evaluates to `false`.

```java,no_run
CONDITION ? WHEN_TRUE : WHEN_FALSE
```

Just like multiple if else statements, we have the concept to "chain" ternary operators. If the first condition is not true, it goes to the next condition and so on.

```java
~void main() {
int age = 22;

String message = age <= 0
    ? "You do not exist yet"
    : age > 100
    ? "Sorry, you are too old."
    : age < 25
    ? "You cannot rent a car!"
    : "You might be able to rent a car";

IO.println(message);
~}
```

It is same as before, you write a condition followed by a `?`, a value to use when that condition evaluates to `true`, a `:`,
and then _chain_ another condition to use when that condition evaluates to `false`.

Finally, if no condition was true, it matches the value after the final `:`.

```java,no_run
CONDITION ? WHEN_TRUE : CONDITION ? WHEN_TRUE : CONDITION ? WHEN_TRUE ... : WHEN_ALL_FALSE
```

[^ternary]: Some people will call this a ternary expression. Ternary meaning "three things." Same idea as tres leches.
