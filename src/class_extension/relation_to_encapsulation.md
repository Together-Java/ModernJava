# Relation to Encapsulation

It takes deliberate effort to properly encapsulate implementation details
in the presence of inheritance.

Say there was a class which tracked passengers who booked flights.

```java
class Airplane {
    private final List<String> passengers = new ArrayList<>();

    void bookOne(String passenger) {
        this.passengers.add(passenger);
    }

    void bookMany(List<String> passengers) {
        for (var passenger : passengers) {
            bookOne(passenger);
        }
    }
}
```

A reasonable extension to this class would be to print a message every time someone books a flight.[^well]

```java
class Airplane {
    private final List<String> passengers = new ArrayList<>();

    void bookOne(String passenger) {
        this.passengers.add(passenger);
    }

    void bookMany(List<String> passengers) {
        for (var passenger : passengers) {
            bookOne(passenger);
        }
    }
}

class PrintingAirplane extends Airplane {
    @Override
    void bookOne(String passenger) {
        IO.println(passenger);
        super.bookOne(passenger);
    }
}

class Main {
    void main() {
        var airplane = new PrintingAirplane();
        airplane.bookOne("Ned Ludd");
        airplane.bookMany(List.of("Robin Hood", "Friar Tuck"));
    }
}
```

But a subtle problem with this is that in Airplane `bookMany` is defined in terms of `bookOne`.
So in our subclass when we override `bookOne` we get the behavior we want. Every time someone is booked
we print their name.

But a small innocuous change in `Airplane` could break this. If `bookMany` was redefined to not
use `bookOne` then you would miss names.

```java
class Airplane {
    private final List<String> passengers = new ArrayList<>();

    void bookOne(String passenger) {
        this.passengers.add(passenger);
    }

    void bookMany(List<String> passengers) {
        for (var passenger : passengers) {
            // Only change
            this.passengers.add(passenger);
        }
    }
}
```

A reasonable extension to this class would be to print a message every time someone books a flight.[^well]

```java
class Airplane {
    private final List<String> passengers = new ArrayList<>();

    void bookOne(String passenger) {
        this.passengers.add(passenger);
    }

    void bookMany(List<String> passengers) {
        for (var passenger : passengers) {
            // Only change
            this.passengers.add(passenger);
        }
    }
}

class PrintingAirplane extends Airplane {
    @Override
    void bookOne(String passenger) {
        IO.println(passenger);
        super.bookOne(passenger);
    }
}

class Main {
    void main() {
        var airplane = new PrintingAirplane();
        airplane.bookOne("Ned Ludd");
        airplane.bookMany(List.of("Robin Hood", "Friar Tuck"));
    }
}
```

This can be adjusted for by overriding both `bookOne` and `bookMany` in `PrintingAirplane`, but you are equally vulnerable to the opposite change.

```java
class PrintingAirplane extends Airplane {
    @Override
    void bookOne(String passenger) {
        IO.println(passenger);
        super.bookOne(passenger);
    }

    @Override
    void bookMany(List<String> passengers) {
        for (var passenger : passengers) {
            IO.println(passenger);
        }
        super.bookMany(passengers);
    }
}
```

As a general rule, changing a class which may have been extended by other classes requires more effort than if doing so were not an option. This is because in a few ways "inheritance breaks encapsulation."
At least in the sense of there being an interplay between mechanics you wouldn't otherwise have to consider.

If you don't want to deal with these issues, you can disallow extending a class.

[^well]: Well, reasonable in the world of contrived programming examples.