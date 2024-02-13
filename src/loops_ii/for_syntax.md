# For Syntax

A `for` loop has three distinct parts.

1. An initializer.

2. An expression which evaluates to a `boolean`.

3. A statement.

```java,no_run
for (<INITIALIZER> ; <EXPRESSION> ; <STATEMENT>) {
    <CODE HERE>
}
```

The initializer is a statement which declares and initializes a variable
like `int number = 0`.

The expression is some check like `number < 5` that is checked each iteration
to know if the loop should continue.

The statement is ran at the end of every iteration, generally updating the variable tracked by the
initializer and expression.

These can be thought of as being the same as a `while` loop written like so.

```java,no_run
<INITIALIZER>;
while (<EXPRESSION>) {
    <CODE HERE>

    <STATEMENT>;
}
```
