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
    location.latitude = 40.2085;
    location.longitude = -3.713;
    return location;
}

void main() {
    Location treasureIsland = findTreasureIsland();
    System.out.println(
        "Treasure island is located at " +
            location.latitude +
            " " +
            location.longitude +
            "."
    );
}
```

[^manymore]: There are many more reasons to make your own classes, but this one is
pretty quick to see even at this stage.