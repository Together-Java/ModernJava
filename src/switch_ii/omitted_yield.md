# Omitted Yield

If a branch of a switch just yields a value but does nothing else interesting you can
omit the `yield` along with the surrounding `{` and `}`.

```java
~enum StopLight {
~    RED,
~    YELLOW,
~    GREEN
~}
~
~enum Action {
~    STOP,
~    SLOW_DOWN,
~    GO
~}
~
~void main() {
StopLight light = StopLight.GREEN;

Action action = switch (light) {
    case RED -> Action.STOP;
    case YELLOW -> Action.SLOW_DOWN;
    case GREEN -> Action.GO;
};

IO.println(action);
~}
```

Which can be mixed with cases that have explicit `yield`s and might do other things.

```java
~enum StopLight {
~    RED,
~    YELLOW,
~    GREEN
~}
~
~enum Action {
~    STOP,
~    SLOW_DOWN,
~    GO
~}
~
void main() {
    StopLight light = StopLight.GREEN;

    Action action = switch (light) {
        case RED -> Action.STOP;
        case YELLOW -> {
            IO.println("Lemon Light!");
            yield Action.SLOW_DOWN;
        }
        case GREEN -> Action.GO;
    };

    IO.println(action);
}
```