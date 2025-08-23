# Enums


<img src="/enums/header.png" height="200px"/>

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

Enums are types with fixed sets of allowed values. We call them enums because they enumerate multiple different possibilities.