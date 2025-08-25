# Inference

If Java cannot figure out exactly what functional interface you want
to use it will not allow you to use a lambda or a method reference.

```java,does_not_compile
class Main {
    void main() {
        // Does not know what type the "var" should be
        var ride = () -> IO.println("cruisin'");
    }
}
```

To resolve this you need to give Java a hint as to what
interface it should resolve to. In addition to simply
giving explicit types to variables and fields
you can do this by "casting" the expression
to a functional interface.

```java
@FunctionalInterface
interface Trip {
    void takeOff();
}

class Main {
    void main() {
        var ride = (Trip) () -> IO.println("cruisin'");
        ride.takeOff();
    }
}
```