# If

The way to represent a branching path in Java is by using an `if` statement.

```java
~void main() {
int age = 5; // 👶
if (age < 25) {
    IO.println("You are too young to rent a car!");
}
~}
```

You write the word `if` followed by an expression which evaluates to a `boolean` inside of `(` and `)`.
This expression is the "condition". Then you write some code inside
of `{` and `}`.

```java,no_run
if (CONDITION) {
    <CODE HERE>
}
```

When the condition evaluates to `true`, the code inside of the `{` and `}` will run.
If it evaluates to `false` that code will not run.

In this example the condition is `age < 25`. When `age` is less than 25 it will evaluate to `true`
and you will be told that you cannot rent a car.

```java
~void main() {
int age = 80; // 👵
if (age < 25) {
    IO.println("You are too young to rent a car!");
}
~}
```

If this condition evaluates to `false`, then the code inside of `{` and `}`
will not run.
