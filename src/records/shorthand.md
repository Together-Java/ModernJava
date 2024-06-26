# Shorthand

One way to think about records is that they are "shorthand"[^nonnative]
for a regular class.

So the following record

```java,no_run
public record Cat(boolean spayed, int weight) {}
```

is shorthand for a regular class that looks like this.

```java,no_run
// There are a few parts that I left off here
// so this isn't 100% accurate.
public class Cat {
    private final boolean spayed;
    private final int weight;

    public Cat(boolean spayed, int weight) {
        this.spayed = spayed;
        this.weight = weight;
    }

    public boolean spayed() {
        return this.spayed;
    }

    public int weight() {
        return this.weight;
    }

    // + the magic that makes it print nicer
    // + the magic that lets you use .equals
    // + a little more that will be relevant later
}
```

[^nonnative]: For you non-native English speakers, a shorthand is a shortened form of something. TTYL is "shorthand" for "Talk to you later." 