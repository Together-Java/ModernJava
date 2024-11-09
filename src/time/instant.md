# Instant

A `java.time.Instant` stores information on a particular moment in time.

You can get the current "instant" with `Instant.now`.

```java
import java.time.Instant;

void main() {
    var now = Instant.now();
    System.out.println(now);
}
```

But if you happen to know a number milliseconds after January 1, 1970 UTC[^epoch] you
can get an `Instant` which represents that point in time with `Instant.ofEpochMilli`.

```java
import java.time.Instant;

void main() {
    var january2nd = Instant.ofEpochMilli(86400000);
    System.out.println(january2nd);
}
```

[^epoch]: https://en.wikipedia.org/wiki/Unix_time

