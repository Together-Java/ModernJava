# Controversy

Static fields are culturally controversial. Specifically static fields
which can change.

```java
class Counter {
    static int value = 0;
}
```

In the example above, any part of the code can change the value at any time by writing to `Counter.value`.

This is "fine" in small to mid-sized programs, but once you have a hundred thousand lines
it can become difficult to reason about what code changes that field and when.

For this reason[^and] you will probably get a lot of mean comments if you share code that uses a static field you can change.

Using static fields for constants is less controverial.

```java
class Constants {
    static final int DAYS_IN_A_WEEK = 7;
}
```

[^and]: Well, in addition to the generally rampant immaturity of programmers.