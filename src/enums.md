# Enums

While you can use `String`, `int`, `boolean`, and friends
alongside your own custom classes to represent many situations,
that is not always enough.

Consider a stop light. At any given time it is either red,
yellow, or green. 

The tool we use to model that kind of thing is enums.

```java,no_run
enum StopLight {
    RED,
    YELLOW,
    GREEN
}
```

We call them enums because they enumerate multiple different possibilities.