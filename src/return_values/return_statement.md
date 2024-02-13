# Return Statement

Whenever the code in a method reaches a line that looks like `return <VALUE>;`, that method
will immediately exit.

This will exit out of any loops, similarly to a `break`.

```java,no_run
int doMath() {
    int x = 0;
    while (true) {
        x++;

        if (x == 8) {
            return x;
        }
    }

    // Needed because Java isn't smart enough to know
    // that the while loop will always reach the return x;
    // line.
    return 0;
}
```

We call this kind of line a return statement.
