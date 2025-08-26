# Return Multiple Values

One of the initial reasons I gave for wanting to use a class
was returning multiple values from a method.

A record is likely better for that purpose than a regular class.

```java
record Location(double latitude, double longitude) {}

Location findTreasureIsland() {
    return new Location(51.4075, 0.4636);
}

void main() {
    Location treasureIsland = findTreasureIsland();
    IO.println(
        "Treasure island is located at " +
            treasureIsland.latitude() +
            " " +
            treasureIsland.longitude() +
            "."
    );
}
```

Regular classes are, of course, still useful. Its just for classes which only
hold some data together (and nothing else interesting) getting a constructor and accessors automatically is very convenient.
