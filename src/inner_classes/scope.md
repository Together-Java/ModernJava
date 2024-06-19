# Scope

Within an inner class all fields and methods of the instance it was created in
are available.

```java,no_run
class Car {
    int speed = 0;

    class Speedometer {
        int getSpeed() {
            return speed;
        }
    }

    Speedometer getSpeedometer() {
        return new Speedometer();
    }
}
```
```java,no_run
~class Car {
~    int speed = 0;
~
~    class Speedometer {
~        int getSpeed() {
~            return speed;
~        }
~    }
~
~    Speedometer getSpeedometer() {
~        return new Speedometer();
~    }
~}
class Main {
    void main() {
        Car car = new Car();
        Car.Speedometer = car.getSpeedometer();
    }
}
```
One mental model for this is that