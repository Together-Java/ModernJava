# Return in void methods

In `void` methods, you can still exit early with a `return` statement, but you do not give any
value after it.

```java
void doStuff() {
    int i = 0;
    while (true) {
        if (i == 8) {
            return;
        }

        System.out.println(i);
    }
}
```

