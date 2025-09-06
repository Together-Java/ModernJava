# Functional Interfaces

If an interface has only one method that needs to be implemented we would call that a "functional interface."[^SAM]

```java
interface Band {
    // Only one method to implement
    // "single abstract method"
    void playHitSong();
}
```


Any other methods on the interface must be `default` or `static`.

```java
interface Band {
    void playHitSong();

    // Neither the default or static method are considered
    default void encore() {
        this.playHitSong();
        this.playHitSong();
    }

    static int turnDial(int level) {
        if (level == 10) {
            return 11;
        }
        else {
            return level;
        }
    }
}
```

Functions take input and return an output. We call them functional interfaces because with you can treat them as being functions whose input and output are the same as that one method to be implemented.


[^SAM]: You might also see these referred to as SAM interfaces. SAM for Single Abstract Method.