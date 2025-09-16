# Remainder

To get the remainder of the division between two integers you can use the `%` operator.
This is called the "modulo operator."

With `int`s `7 / 2` will give you `3`. That `3` is the "quotient" from the division
and is the number of times `2` can be taken out of `7`. This leaves a "remainder" of `1`.

The modulo operator gives you that remainder.

```java
~void main() {
int x = 5;
// 5 / 2 is 2 with a remainder of 1
// y will be 1
int y = x % 2;
// 5 / 3 is 1 with a remainder of 2
// z will be 2
int z = x % 3;

IO.println(x);
IO.println(y);
IO.println(z);
~}
```

A common use for this is to make numbers "go in a circle."

For instance, say you wanted to count from 0 up to 3 and then go back to 0.

```java
~void main() {
int value = 0;
IO.println(value);

// the remainder of (0 + 1) divided by 3 is 1
// value will be 1
value = (value + 1) % 3;
IO.println(value);


// the remainder of (1 + 1) divided by 3 is 2
// value will be 2
value = (value + 1) % 3;
IO.println(value);


// the remainder of (2 + 1) divided by 3 is 0
// value will again be 0.
//
// We never reach 3 because 3 divided by 3
// always has a remainder of zero.
value = (value + 1) % 3;
IO.println(value);

// the remainder of (0 + 1) divided by 3 is 1
// value will be 1
value = (value + 1) % 3;
IO.println(value);

// and so on.
// 
// If you did this process with 5 you would go
// 0, 1, 2, 3, 4, 0, 1, ...
//
// If you did this process with 7 you would go
// 0, 1, 2, 3, 4, 5, 6, 0, 1, ...
//
// You always go back to the start just before you reach
// the number you are getting the remainder by.
~}
```

The fact that all the reassignments of value look identical is something that will be useful in tandem
with loops.
