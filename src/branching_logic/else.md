# Else

When you want to do one thing when a condition evaluates to `true`
and another when that same condition evaluates to `false` you can use `else`.

```java
int age = 30; // 🙎‍♀️
if (age < 25) {
    System.out.println("You cannot rent a car!");
}
else {
    System.out.println("You might be able to rent a car.");
}
```

You write the word `else` immediately after the `}` at the end of an `if` statement, then
some code inside of a new `{` and `}`.

```java
if (CONDITION) {
    <CODE TO RUN>
}
else {
    <CODE TO RUN>
}
```

When the condition evaluates to `false`, the code inside of `else`'s `{` and `}` will run.

`else` cannot exist without a matching `if`, so this code does not work.

```java
else {
    System.out.println("No if.");
}
```
