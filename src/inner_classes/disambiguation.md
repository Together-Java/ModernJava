# Disambiguation

If you are within an inner class and want to use a field
from the instance it was created in but that field has the same
name as a field in the inner class - like the following.

```java,no_run
class Car {
    int speed = 0;

    class Speedometer {
        // Speed is declared here, but it is
        // a different field
        int speed = 5; 
    }
}
```

You can disambiguate between the fields by using the name of the containing class
followed by `.this`. 

```java,no_run
class Car {
    int speed = 0;

    class Speedometer {
        // Speed is declared here, but it is
        // a different field
        int speed = 5; 

        void saySpeed() {
            System.out.println(speed); // 5
            System.out.println(this.speed); // 5
            System.out.println(Car.this.speed); // 0
        }
    }
}
```

```java
~class Car {
~    int speed = 0;
~
~    class Speedometer {
~        // Speed is declared here, but it is
~        // a different field
~        int speed = 5; 
~
~        void saySpeed() {
~            System.out.println(speed); // 5
~            System.out.println(this.speed); // 5
~            System.out.println(Car.this.speed); // 0
~        }
~    }
~}
class Main {
    void main() {
        var car = new Car();
        var speedometer = car.new Speedometer();
        speedometer.saySpeed();
    }
}
```