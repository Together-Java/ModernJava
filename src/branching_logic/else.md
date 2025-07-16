# Else

When you want to do one thing when a condition evaluates to `true`
and another when that same condition evaluates to `false` you can use `else`.

```java
~void main() {
int age = 30; // 🙎‍♀️
if (age < 25) {
    IO.println("You cannot rent a car!");
}
else {
    IO.println("You might be able to rent a car.");
}
~}
```

You write the word `else` immediately after the `}` at the end of an `if` statement, then
some code inside of a new `{` and `}`.

```java,no_run
if (CONDITION) {
    <CODE TO RUN>
}
else {
    <CODE TO RUN>
}
```

When the condition evaluates to `false`, the code inside of `else`'s `{` and `}` will run.

`else` cannot exist without a matching `if`, so this code does not work.

```java,does_not_compile
~void main() {
else {
    IO.println("No if.");
}
~}
```
