# Return

Anywhere inside of a method you can write `return` to immediately exit that method.

```java
void willReturnEarly() {
    for (int i = 0; i < 10; i++) {
        System.out.println(i);
        if (i == 5) {
            // Will stop at 5 because we exit the method
            return;
        }
    }

    System.out.println("THIS WONT RUN");
}

void main() {
    willReturnEarly();
}
```

This will break out of any loops and skip running any other code in the method.

```java
void escapeFromLoops() {
    while (true) {
        for (;;) {
            for (;;) {
                while (true) {
                    // Escape!
                    return;
                }
            }
        }
    }
}

void main() {
    escapeFromLoops();
}
```
