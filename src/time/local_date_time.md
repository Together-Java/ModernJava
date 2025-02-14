# LocalDateTime

What do you get if you combine a `LocalDate` and a `LocalTime`? A `LocalDateTime`!

A `LocalDateTime` stores dates and times.

If you have both a `LocalDate` and a `LocalTime` you can combine them
with `LocalDateTime.of`.

```java
import java.time.LocalDate;
import java.time.LocalTime;
import java.time.LocalDateTime;

class Main {
    void main() {
        var jan10 = LocalDate.of(2024, 1, 10);
        var tenTwentyFour = LocalTime.of(10, 24, 0);
        System.out.println(LocalDateTime.of(jan10, tenTwentyFour));
    }
}
```