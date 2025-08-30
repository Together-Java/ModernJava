# OffsetDateTime

An `OffsetDateTime` is similar to a `ZonedDateTime` but with the key difference
that an `OffsetDateTime` doesn't record a moment in a specific time zone, but instead
as an offset from the [UTC](https://en.wikipedia.org/wiki/Coordinated_Universal_Time)[^utc] timezone.

This is useful because timezones change their rules frequently. If you had to pick a representation
of dates and times to store, this is a good default.

```java
import java.time.LocalDate;
import java.time.LocalTime;
import java.time.LocalDateTime;
import java.time.ZonedDateTime;
import java.time.ZoneId;

class Main {
    void main() {
        var feb14 = LocalDate.of(2025, 2, 14);
        var fiveTwentyThree = LocalTime.of(5, 23, 0);
        var est = ZoneId.of("US/Eastern");

        LocalDateTime localDateTime = LocalDateTime.of(feb14, fiveTwentyThree);
        ZonedDateTime zonedDateTime = ZonedDateTime.of(localDateTime, est);
        OffsetDateTime offsetDateTime = zonedDateTime.toOffsetDateTime();

        IO.println(offsetDateTime);
    }
}
```

You can get the current `OffsetDateTime` for the time zone your computer is running in
with `OffsetDateTime.now()`.

```java
import java.time.OffsetDateTime;

class Main {
    void main() {
        var now = OffsetDateTime.now();

        IO.println(now);
    }
}
```

And you can do the same for an arbitrary time zone by giving a `ZoneId` to
`now`. Java knows the UTC offset for every time zone.

```java
import java.time.OffsetDateTime;
import java.time.ZoneId;

class Main {
    void main() {
        var now = OffsetDateTime.now(ZoneId.of("US/Eastern"));

        IO.println(now);
    }
}
```

[^utc]: UTC stands for "Coordinated Universal Time" in English and "Temps Universel Coordonné" in French. The specific letter order of "UTC" (rather than "CUT" or "TUC") was chosen as a compromise between the two languages.