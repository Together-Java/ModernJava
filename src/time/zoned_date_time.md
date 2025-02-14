# ZonedDateTime

A `ZonedDateTime` has all the information of
a `LocalDateTime`, but with the addition of a time zone.

These are useful for recording the time that events took place
in a way that can be communicated.

```java
import java.time.LocalDate;
import java.time.LocalTime;
import java.time.LocalDateTime;
import java.time.ZonedDateTime;
import java.time.ZoneId;

class Main {
    void main() {
        var jan10 = LocalDate.of(2024, 1, 10);
        var tenTwentyFour = LocalTime.of(10, 24, 0);
        var est = ZoneId.of("US/Eastern");

        LocalDateTime localDateTime = LocalDateTime.of(jan10, tenTwentyFour);
        ZonedDateTime zonedDateTime = ZonedDateTime.of(localDateTime, est);

        System.out.println(zonedDateTime);
    }
}
```

You can get the current `ZonedDateTime` for the time zone your computer is running in
with `ZonedDateTime.now()`.

```java
import java.time.ZonedDateTime;

class Main {
    void main() {
        var now = ZonedDateTime.now();

        System.out.println(now);
    }
}
```

And you can do the same for an arbitrary time zone by giving a `ZoneId` to
`now`.

```java
import java.time.ZonedDateTime;
import java.time.ZoneId;

class Main {
    void main() {
        var now = ZonedDateTime.now(ZoneId.of("US/Eastern"));

        System.out.println(now);
    }
}
```
