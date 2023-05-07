# Empty Expressions

You are also allowed to leave the expression part of a `for` loop blank.

```java
for (int i = 0;;i++) {
    System.out.println(i);
}
// 0
// 1
// 2
// 3
// ... and so on
```

This means that each time through there is no check to see if the loop will exit.
The loop will only exit if there is an explicit `break` somewhere.

```java
for (int i = 0;;i++) {
    if (i == 5) {
        break;
    }
    System.out.println(i);
}
// 0
// 1
// 2
// 3
// 4
```