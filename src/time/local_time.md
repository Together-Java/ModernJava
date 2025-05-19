# LocalTime

In the same way a local date leaves off context about where
it was and what time it was, a local time just stores the time.

This means it will hold the exact time during the day, down to the nanoseconds.

You can make a `LocalTime` with `LocalTime.of` giving it the hours, minutes, and
seconds into the day.

```java
import java.time.LocalTime;

void main() {
    var tenTwentyFour = LocalTime.of(10, 24, 0);
    IO.println(tenTwentyFour);
}
```

And similarly you can get the current time your computer thinks it is with `LocalName.now()`

```java
import java.time.LocalTime;

void main() {
    var now = LocalTime.now();
    IO.println(now);
}
```