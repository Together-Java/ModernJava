# Static Inner Classes

If you mark an inner class as `static` then it becomes
much closer to a normal class.

```java,no_run
class Car {
    static class Speedometer {

    }
}
```

You can make instances of it directly without an instance of the outer class.

```java,no_run
Car.Speedometer speedometer = new Car.Speedometer();
```

And it cannot access fields of the instance it was made in, because it was not made in an instance.

```java,no_run
class Car {
    int speed; // Speedometer can't magically get this anymore

    static class Speedometer {

    }
}
```

I would wager that this is the most common kind of inner class to see
in real code, despite requiring more words to define[^theme].

[^theme]: A theme that will start to emerge is that the "best" code sometimes has
a few extra modifiers on it and the "default" behavior isn't what you want. Static
inner classes are way less magic.