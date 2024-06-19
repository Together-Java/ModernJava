# Instances

To make an instance of an inner class you can use `new` to invoke its constructor
like any other class.

```java,no_run
class Car {
    class Speedometer {

    }

    Speedometer getSpeedometer() {
        return new Speedometer();
    }
}
```

The restriction is that an inner class can only be constructed from an instance
method of the containing class.

This means that, in the example above, you cannot make an instance of `Speedometer`
unless you first have an instance of `Car`.

```java
class Main {
    void main() {
        var car = new Car();
        var speedometer = car.getSpeedometer();

        System.out.println(speedometer);

        // But this will not work
        // var speedometer = new Car.Speedometer();
    }
}
~
~class Car {
~    class Speedometer {
~
~    }
~
~    Speedometer getSpeedometer() {
~        return new Speedometer();
~    }
~}
```