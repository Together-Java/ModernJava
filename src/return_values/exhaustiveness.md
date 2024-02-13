# Exhaustiveness


When a method returns data, Java needs to know that no matter what happens
in the method there will be some `return` line reached.


```java,no_run,does_not_compile
int compute(int x) {
    if (x < 0) {
        return 5;
    }
    // Error! No return if x >= 0
}
```

```java,no_run
int compute(int x) {
    // Both "branches" have returns, so all is well
    if (x < 0) {
        return 5;
    }
    else {
        return 1;
    }
}
```

We call this property, whether in every situation a method will return a value, "exhaustiveness."
If there could be cases where no return statement is reached, that is "non-exhaustive" and Java
won't accept your code.
