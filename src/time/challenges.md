# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1.

Print out every day from January 1st to December 31st. When the program reaches your birthday
make it print out "Happy Birthday \<your name\>" instead of the date.

```java,editable
class Main {
    void main() {
        // CODE HERE
    }
}
```

## Challenge 2.

Make a `Poison` class which has a `Duration` field which stores how long
the poison will be potent for as well as an `Instant` at which the
poison was brewed.

Implement a method that takes an `Instant` and returns if the `Poison`
will be expired by that point.

```java,editable
import java.time.Duration;
import java.time.Instant;

class Poison {
    // CODE HERE
}

class Main {
    void main() {
        var hemlock = new Poison(Instant.now(), Duration.ofDays(365 * 3));

        IO.println(hemlock.isPotentAt(Instant.now())); // true
        IO.println(hemlock.isPotentAt(Instant.now().plus(Duration.ofDays(5))); // true
        IO.println(hemlock.isPotentAt(Instant.now().plus(Duration.ofDays(365 * 10)))); // false
    }
}
```

## Challenge 3.

Get as input using `IO.readln` a `day`, `month`, `year`, and UTC offset.

Interpret that input as an `OffsetDateTime` then print how many seconds will have
passed between that offset date time and midnight of January 1st 1983 GMT.

```java,editable
class Main {
    void main() {
        // CODE HERE
    }
}
```

## Challenge 4.

A train leaves Boston at 12:50pm EDT on August 23rd 2025 and arrives in Chicago
at 10:12am CDT August 24th 2025.

How many minutes long was that train ride? Use the Java's time classes to figure out the answer.

```java,editable
class Main {
    void main() {
        // CODE HERE
    }
}
```

As a small hint, you will first want to represent those events as `ZonedDateTime`s, convert the `ZonedDateTime`s to `Instant`s, and then get the `Duration` between those `Instant`s. Then get the number
of minutes in that `Duration`.



