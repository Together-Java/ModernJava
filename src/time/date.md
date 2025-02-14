# Date

There is one class related to time that isn't much like the others: `java.util.Date`.

Java did not originally come with the `java.time` classes. At first it just had `Date`.

```java
import java.util.Date;

class Main {
    void main() {
        Date date = new Date();
        System.out.println(date);
    }
}
```

`Date` is somewhat of a chimera between `Instant` and `ZonedDateTime`. It represents an instant in time but specifically in the UTC timezone.[^gmt]

It is important to know about because a lot of code, including code that comes with Java, makes use of it.

Whenever you see `Date` in the wild you should usually turn it into an `Instant` by
calling `.toInstant()`.

```java
import java.time.Instant;
import java.util.Date;

class Main {
    void main() {
        Date date = new Date();
        System.out.println(date);

        Instant instant = date.toInstant();
        System.out.println(instant);
    }
}
```

You can also construct a `Date` from an `Instant` using `Date.from`. This is useful if there is some code that wants a `Date` as an argument.

```java
import java.time.Instant;
import java.util.Date;

class Main {
    void main() {
        var instant = Instant.now();
        System.out.println(instant);
        
        Date date = Date.from(instant);
        System.out.println(date);
    }
}
```

To be clear though, `Date` has problems. We aren't ready to explain all of them yet. Just treat `Date` as haunted, as in by ghosts, and use the `java.time` alternatives when you can.

[^gmt]: You will notice that when we print out the date we get GMT. GMT is basically the same as UTC, though [the documentation for `Date`](https://docs.oracle.com/en/java/javase/21/docs/api/java.base/java/util/Date.html) explains the difference.