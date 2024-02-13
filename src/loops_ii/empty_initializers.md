# Empty Initializers

You are allowed to leave the initializer part of a `for` loop blank
so long as you still have the `;`.

```java
~void main() {
int number = 0;
for (;number < 5; number++) {
    System.out.println(number);
}
~}
```

You might choose to do this for the same reasons you might choose to split the declaration
and assignment of the "loop variable." So that the variable will be accessible after the end of the loop.

This way its initialization and declaration can be on the same line, which might be desirable.

```java
~void main() {
int number = 0;
for (;number < 5; number++) {
    System.out.println(number);
}
System.out.println("Still have number: " + number);
~}
```
