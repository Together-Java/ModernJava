# HashMap


<img src="/hash_maps/header.png" height="200px"/>

Arrays and their growable cousin `ArrayList` store a sequence of elements.
This is often enough, but if you want to find an element in an array you usually
need to check every element one by one.

```java
record Character(
    String name, 
    boolean protaganist
) {}

Character findCharacter(
    Character[] cast, 
    String name
) {
    for (var character : cast) {
        if (character.name().equals(name)) {
            return character;
        }
    }
    return null;
}

void main() {
    Character[] carsCharacters = new Character[] {
        new Character("Tow Mater", false),
        new Character("Lightning McQueen", true),
        new Character("Doc Hudson", false)
    };

    IO.println(findCharacter(carsCharacters, "Lightning McQueen"));
    IO.println(findCharacter(carsCharacters, "Blade Ranger"));
}
```

For small arrays, this is no biggie. A computer can check over a few dozen things pretty quickly.

But for big arrays, this stinks.

What we want is some way to quickly look up something, regardless of how many things there are to
check over. This is what a HashMap gives us.

```java
import java.util.HashMap;

record Character(
    String name, 
    boolean protaganist
) {}

void main() {
    HashMap<String, Character> carsCharacters = new HashMap<>();
    
    carsCharacters.put(
        "Tow Mater",
        new Character("Tow Mater", false)
    );

    carsCharacters.put(
        "Lightning McQueen",
        new Character("Lightning McQueen", false)
    );
    
    carsCharacters.put(
        "Doc Hudson",
        new Character("Doc Hudson", false)
    );

    IO.println(carsCharacters.get("Lightning McQueen"));
    IO.println(carsCharacters.get("Blade Ranger"));
}
```