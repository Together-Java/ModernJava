# Hash Maps

If you want to find an element in an array you usually
need to check every element one by one.

```java
String[] carsCharacters = new String[] {
    "Tow Mater",
    "Lightning McQueen",
    "Doc Hudson"
};

boolean wasInCars(String name) {
    for (var characterName : carsCharacters) {
        if (characterName.equals(name)) {
            return true;
        }
    }
    return false;
}

void main() {
    System.out.println(wasInCars("Lightning McQueen"));
    System.out.println(wasInCars("Blade Ranger"));
}
```

For small arrays, this is no biggie. A computer can check over a few dozen things pretty quickly.

But for big arrays, this stinks.

What we want is some way to quickly look up something, regardless of how many things there are to
check over. This is what a Hash Map gives us.