# New Operator

If you want to make an instance of an inner class
without making a method on the class containing it,
you can use the "new operator."

Whereas you make an instance of a regular class by saying 
something like `new ClassName()`, you can make an instance of an
inner class by using `.new` on a variable that holds an instance
of the containing class.

Thats a confusing verbal description, but it kinda makes sense once you see it.

```java
class Car {
    class Speedometer {
    }
}
```

```java
~class Car {
~    class Speedometer {
~    }
~}
class Main {
    void main() {
        Car car = new Car();
        Car.Speedometer speedometer = car.new Speedometer();
        System.out.println(speedometer);
    }
}
```
