# Delayed Assignment

The initializer of a `for` loop can give an initial value to a variable
declared outside of the loop.

```java
~void main() {
int number;
for (number = 0; number < 5; number++) {
    IO.println("At: " + number);
}
~}
```

You might choose to do this so that after the loop is finished, you can still access the variable.

```java
~void main() {
int number;
for (number = 0; number < 5; number++) {
    IO.println("At: " + number);
}

// This will work, we can access the variable still.
IO.println("Ended at: " + number);
~}
```

If you had put both the declaration and initial value inside the initializer, you won't be able
to use that variable after the loop

```java
~void main() {
for (int number = 0; number < 5; number++) {
    IO.println("At: " + number);
}

// This will not work. number is no longer available
IO.println("Ended at: " + number);
~}
```
