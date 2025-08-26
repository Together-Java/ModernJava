# Return Multiple Values

Methods can only ever return one type of thing. This
usually retricts you to only ever returning one `int` or
one `String`.

But if you make a class that has multiple fields
you can use that to return more than one piece of information.[^manymore]

```java
class Location {
    double latitude;
    double longitude;
}

Location findTreasureIsland() {
    Location location = new Location();
    location.latitude = 51.4075;
    location.longitude = 0.4636;
    return location;
}

void main() {
    Location treasureIsland = findTreasureIsland();
    IO.println(
        "Treasure island is located at " +
            treasureIsland.latitude +
            " " +
            treasureIsland.longitude +
            "."
    );
}
```

[^manymore]: There are many more reasons to make your own classes, but this one is
pretty quick to see even at this stage.