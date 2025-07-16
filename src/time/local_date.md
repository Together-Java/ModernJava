# LocalDate

A local date is something like "January 10th, 2024."

This just records a day, month, and year. It doesn't know
in what part of the world it was January 10th 2024, just
that somewhere the "local" date was that.

You can make a `LocalDate` with `LocalDate.of`.

```java
import java.time.LocalDate;

void main() {
    var jan10 = LocalDate.of(2024, 1, 10);
    IO.println(jan10);
}
```

And you can get the current `LocalDate` in whatever timezone
your computer is programmed to be in with `LocalDate.now();`

```java
import java.time.LocalDate;

void main() {
    var now = LocalDate.now();
    IO.println(now);
}
```