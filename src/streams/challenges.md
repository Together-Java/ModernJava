# Challenges


Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1.

Translate the following code using a for-loop to code using streams.

```java,editable
import module java.base;

class Main {
    void main() {
        for (int i = 0; i < 10; i++) {
            IO.println(i);
        }
    }
}
```

## Challenge 2.

Translate the following code using a for-loop to code using streams.

```java,editable
import module java.base;

class Main {
    void main() {
        List<Integer> timestamps = List.of(1, 1756137441);

        Set<Instant> instants = new HashSet<>();
        for (int timestamp : timestamps) {
            instants.add(Instant.ofEpochSecond(timestamp));
        }

        IO.println(instants);
    }
}
```

## Challenge 3.

Read the documentation on [`Collector`](https://docs.oracle.com/en/java/javase/24/docs/api/java.base/java/util/stream/Collector.html) and [`Collectors`](https://docs.oracle.com/en/java/javase/24/docs/api/java.base/java/util/stream/Collector.html).

Make an implementation of `Collector` that can collect elements into `MySpecialList`.

```java,editable
import module java.base;

class MySpecialList<T> extends ArrayList<T> {}

class Main {
    // CODE HERE

    void main() {
        MySpecialList<Integer> l = Stream.of(1, 2, 3)
            .collect(/* CODE HERE */);
    }
}
```