# Switch II

A common thing to do is have a `switch` statement which assigns a value
to a variable in each branch.

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

    Action action = null; // Delayed assignment rules are funky here.
    switch (light) {
        case RED -> {
            action = Action.STOP;
        }
        case YELLOW -> {
            action = Action.SLOW_DOWN;
        }
        case GREEN -> {
            action = Action.GO;
        }
    }

    IO.println(action);
}
```

For this purpose, you can instead use a switch "as an expression."