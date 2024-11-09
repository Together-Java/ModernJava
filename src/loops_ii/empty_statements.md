# Empty Statements

You can even leave the statement part of a `for` loop blank. This means that at
the end of an iteration there is nothing guaranteed to run.

```java
~void main() {
for (int i = 6; i > 2;) {
    System.out.println(i);
    i--;
}

// 6
// 5
// 4
// 3
// 2
~}
```

If you leave both the initializer and statement blank, that will be functionally identical to a `while` loop.[^cry]

```java
~void main() {
int number = 1;
for (;number < 10;) {
    System.out.println(number);
    number *= 2;
}

// Same logic as above
int number2 = 1;
while (number2 < 10) {
    System.out.println(number2);
    number2 *= 2;
}
~}
```

If you leave the initializer, expression, and statement blank it will be the same as a `while (true)` loop.

```java,no_run
for (;;) {
    System.out.println("The people stated singing it...");
}
// Runs forever
```

The only difference is that `(;;)` looks somewhat like

- A spider
- The Pokémon Kabuto
- A person crying

And that can be fun.
