# Counting Up and Down

One of the easiest things to do with a `for` loop is count up to or down from
a given number.

```java
~void main() {
// Goes from 1 to 100
for (int currentNumber = 1; currentNumber <= 100; currentNumber++) {
    System.out.println(currentNumber);
}

// Goes from 100 to 1
for (int currentNumber = 100; currentNumber >= 1; currentNumber--) {
    System.out.println(currentNumber);
}
~}
```

You use the initializer to set some variable to a starting number like `int currentNumber = 1`,
have the expression check if the number is at the target end number like `currentNumber <= 100`,
and use the statement to change the number by one like `currentNumber++`.[^test]

[^test]: Very often, if you are given a test on `for` loops it will focus on doing all sorts of counting up, down, and around. Be prepared.
