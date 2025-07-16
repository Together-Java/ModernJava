# Labeled Break

Labeled breaks work the same with `for` loops as they do with `while` loops.

```java,no_run
outerLoop:
for (;;) {
    for (;;) {
        break outerLoop;
    }
}
```

This applies also to when `while` loops are nested within `for` loops or the other way around.

```java
~void main() {
outerForLoop:
for (int i = 0; i < 10; i++) {
    IO.println(i);
    while (i < 100) {
        if (i == 5) {
            break outerForLoop;
        }
        i++;
    }
    IO.println(i);
}

// 0
~}
```
