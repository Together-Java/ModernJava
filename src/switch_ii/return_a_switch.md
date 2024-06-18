# Return a Switch

If you choose to, you do not need to assign the result of a switch expression into a variable. You can directly return the result from a method.

```java,no_run
enum Bird {
    TURKEY,
    EAGLE,
    WOODPECKER
}

boolean isScary(Bird bird) {
    return switch (bird) {
        case TURKEY -> true;
        case EAGLE -> true;
        case WOODPECKER -> false;
    };
}
```