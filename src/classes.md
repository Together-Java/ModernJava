# Classes

Up until now all the data types you have used - `int`, `String`, etc. -
came with Java. This works for awhile, but eventually you will want or need to define your own types.

The way to do this is with a "class."

```java
class Person {

}
```

Every
A class can be thought of as a "blueprint" for making an
to represent things in your programs.

Methods can only have one return value. This means that if you wanted to make a method
that returned two values, such as the location of buried treasure, you would have trouble.

```java
// Can only declare one "thing" that will be returned
double getTreasureLocation() {
    // Can't return two values.
    return 43.8803, 103.4538
}
```

This is the first[^many] use of classes. You can declare your own class which can hold multiple
values and use that to smuggle them across a method return.

```java
class Location {
    double latitude;
    double longitude;
}

Location getTreasureLocation() {
    Location treasure = new Location();
    treasure.latitude = 43.8803;
    treasure.longitude = 103.4538;
    return treasure;
}

void main() {
    Location treasure = getTreasureLocation();

    System.out.println(
        "The treasure is at " +
        treasure.latitude +
        "N, " +
        treasure.longitude +
        "W."
    );
}
```

[^many]: of many
