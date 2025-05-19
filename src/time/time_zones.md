# Time Zones

Partially because of how day night cycles work
and sometimes because of arcane rules made up
to help out farmers, we have time zones.

This means that while it might be 9am in Boston
it would simultaneously be 10pm in Tokyo. Boston and Tokyo
are in different time zones.

You can get access to the time zone your computer
is using with `ZoneId.systemDefault()`. This gives you
a `ZoneId` which identifies a time zone.

```java
import java.time.ZoneId;

class Main {
    void main() {
        ZoneId tz = ZoneId.systemDefault();

        IO.println(tz);
    }
}
```

If you want to get the identifier for a different time zone
you use `ZoneId.of` and give it a `String` identifying
the time zone. These come from [a big list](https://www.iana.org/time-zones)
published by the Internet Assigned Numbers Authority (IANA).


```java
import java.time.ZoneId;

class Main {
    void main() {
        // Eastern Standard Time
        ZoneId tz = ZoneId.of("US/Eastern");

        IO.println(tz);
    }
}
```

While you won't be using this directly, every `ZoneId` 
has the information needed to determine what time it would
be accessible via `getRules()`.

```java
import java.time.ZoneId;

class Main {
    void main() {
        // Eastern Standard Time
        ZoneId tz = ZoneId.of("US/Eastern");

        IO.println(tz.getRules());
    }
}
```

And it is this machinery used by the parts of the time API which
determine the exact time it would be in a given time zone.
