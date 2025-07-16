# Functional Interfaces

If an interface has only a one method that needs to be implemented we would call that a "functional interface."[^SAM]

```java
interface Runner {
    // Only one method to implement
    // "single abstract method"
    void run();
}
```


Any other methods on the interface must be `default` or `static`.

```java
interface Runner {
    void run();

    // Neither the default or static method are considered
    default void runTwice() {
        this.run();
        this.run();
    }

    static double milesToKilometers(double distance) {
        return distance * 1.609;
    }
}
```

Functions take input and return an output. We call them functional interfaces because with you can treat them as being functions whose input and output are the same as that one method to be implemented.


[^SAM]: You might also see these referred to as SAM interfaces. SAM for Single Abstract Method.