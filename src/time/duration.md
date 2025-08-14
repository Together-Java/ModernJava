# Duration

A `Duration` stores a duration of time. 

You can make these with `Duration.ofMinutes`, `Duration.ofMillis`
and other similarly named methods.

```java
import java.time.Duration;

void main() {
    var fiveMinutes = Duration.ofMinutes(5);
    IO.println(fiveMinutes);

    var twelveMilliSeconds = Duration.ofMillis(12);
    IO.println(twelveMilliSeconds);
}
```

You can use these to get the duration between two `Instant`s with
`Duration.between`.

```java
import java.time.Instant;
import java.time.Duration;

void main() {
    var january2nd = Instant.ofEpochMilli(86400000);
    IO.println(january2nd);

    var january3rd = Instant.ofEpochMilli(86400000 * 2);
    IO.println(january3rd);

    Duration twentyFourHours = Duration.between(january2nd, january3rd);
    IO.println(twentyFourHours);
}
```

And you can move `Instant`s by a given `Duration` of time using its `.plus` and `.minus`
methods.

```java
import java.time.Instant;
import java.time.Duration;

void main() {
    var january1st = Instant.ofEpochMilli(0);
    IO.println(january1st);

    IO.println(
        january1st.plus(Duration.ofHours(45))
    );

    IO.println(
        january1st.minus(Duration.ofHours(1))
    );
}
```
