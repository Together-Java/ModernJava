# Nested Ifs

The code inside of the `{` and `}` can be anything, including more `if` statments.

```java
~void main() {
int age = 5; // 👶
if (age < 25) {
    System.out.println("You are too young to rent a car!");
    if (age == 24) {
        System.out.println("(but it was close)");
    }
}
~}
```

When an `if` is inside another `if` we say that it is "nested".

If you find yourself nesting more than a few `if`s that might be a sign that
you should reach out for help.

```java,no_run
if (...) {
    if (...) {
        if (...) {
            if (...) {
                // Seek professional help
            }
        }
    }
}
```
