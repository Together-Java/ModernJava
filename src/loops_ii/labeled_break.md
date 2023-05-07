# Labeled Break

Labeled breaks work the same with `for` loops as they do with `while` loops.

```java
outerLoop:
for (;;) {
    for (;;) {
        break outerLoop;
    }
}
```

This applies also to when `while` loops are nested within `for` loops or the other way around.

```java
outerForLoop:
for (int i = 0; i < 10; i++) {
    System.out.println(i);
    while (i < 100) {
        if (i == 5) {
            break outerForLoop;
        }
        i++;
    }
    System.out.println(i);
}

// 0
```