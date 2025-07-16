# Yield

To use a "switch expression" you put the entire switch to the right hand side of an equals sign[^context] and, instead of assigning to a variable, you "`yield`" the value you want to assign.

```java
enum StopLight {
    RED,
    YELLOW,
    GREEN
}

enum Action {
    STOP,
    SLOW_DOWN,
    GO
}

void main() {
    StopLight light = StopLight.GREEN;

    Action action = switch (light) {
        case RED -> {
            yield Action.STOP;
        }
        case YELLOW -> {
            yield Action.SLOW_DOWN;
        }
        case GREEN -> {
            yield Action.GO;
        }
    };

    IO.println(action);
}
```

`yield` is very similar to `return`. The difference is that `return` will exit the entire method. `yield` just decides what the switch evaluates to.

[^context]: Technically we are talking about an "expression context." Meaning a place where you are allowed to put an expression. The right hand side of an equals sign is one, but there are many others.