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

When you have something like an enum you might think you don't need a `default` case
because you can handle every variant explicitly.[^sometimes]

```java,no_run,does_not_compile
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
}
```

This is, unfortunately, not the case for a switch statement. 
You either need a `default` case or to have an explicit `case null` to handle the
possibility that the enum value is `null`.[^lies]

```java,no_run,does_not_compile
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
        // Need to handle the possibility of null
        // or give a "default ->"
        case null -> {
            // You might want to return a value or just crash
            return false;
        }
    }
}
```

[^sometimes]: This is sometimes the case! It is really just this specific form of switch that has this restriction.

[^lies]: Remember at the very start when I said I was going to lie to you? This is one of those lies. The real reason for this restriction has to do with how Java compiles switch statements and a concept called "separate compilation." Basically
even though we know you covered all the enum variants, Java still makes you account for if a new enum variant was added later on. It doesn't do this for all forms of `switch` though.