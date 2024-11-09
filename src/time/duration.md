# Duration

A `Duration` stores a duration of time. 

You can make these with `Duration.ofMinutes`, `Duration.ofMillis`
and other similarly named methods.

```java
import java.time.Duration;

void main() {
    var fiveMinutes = Duration.ofMinutes(5);
    System.out.println(fiveMinutes);

    var twelveMilliSeconds = Duration.ofMillis(12);
    System.out.println(twelveMilliSeconds);
}
```

You can use these get the duration between two `Instant`s with
`Duration.between`.

```java
import java.time.Instant;
import java.time.Duration;

void main() {
    var january2nd = Instant.ofEpochMilli(86400000);
    System.out.println(january2nd);

    var january3rd = Instant.ofEpochMilli(86400000 * 2);
    System.out.println(january3rd);

    Duration twentyFourHours = Duration.between(january2nd, january3rd);
    System.out.println(twentyFourHours);
}
```

And you can move `Instant`s by a given `Duration` of time using its `.plus` and `.minus`
methods.

```java
import java.time.Instant;
import java.time.Duration;

void main() {
    var january1st = Instant.ofEpochMilli(0);
    System.out.println(january1st);

    System.out.println(
        january1st.plus(Duration.ofHours(45))
    );

    System.out.println(
        january1st.minus(Duration.ofHours(1))
    );
}
```
