# Type

The type of an inner class, when used as a variable or as a field,
is the name of the containing class followed by a `.` and the
name of the inner class.

```java,no_run
class Car {
    class Speedometer {}
}
```

So a field containing an instance of `Speedometer` would have the type `Car.Speedometer`.

```java,no_run
Car.Speedometer speedometer = ...;
```

The exception is if the inner class is referenced within the class that declares it.
In that context you just need to write the name of the class;

```java
class Car {
    // Car.Speedometer is not required
    // (it will work though)
    Speedometer speedometer;

    class Speedometer {}
}
```