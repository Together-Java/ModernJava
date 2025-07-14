# Exhaustiveness

Switches are considered exhaustive if they have a case label for every possible value
of the type of thing they are switching over.

This is important if you try to return from a function within a switch. Since you need to
return a value from every possible branch the function may take, you either need to add an
extra return after the switch expression or have an exhaustive switch.

```java,no_run
String describe(int number) {
    switch (number) {
        case 1 -> {
            return "loneliest";
        }
        case 2 -> {
            return "loneliest since 1";
        }
    }

    // Since no default, need a return here
    return "Its a number";
}
```

When you have something like an enum you don't need a `default` case
because you can handle every variant explicitly.

```java,no_run
enum Bird {
    TURKEY,
    EAGLE,
    WOODPECKER
}

boolean isScary(Bird bird) {
    switch (bird) {
        case TURKEY -> {
            return true;
        }
        case EAGLE -> {
            return true;
        }
        case WOODPECKER -> {
            return false;
        }
    }
    return false;
}
```