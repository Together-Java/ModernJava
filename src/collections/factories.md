# Factories

There are methods on `List`, `Set`, and `Map`[^interface_static_methods] which can give
you instances of their corresponding collection.

```java
import java.util.List;
import java.util.Set;
import java.util.Map;

class Main {
    void main() {
        List<String> weapons = List.of("Lightsaber", "Blaster");
        Set<String> ships = Set.of("Tie Fighter", "X-Wing");
        Map<String, Integer> midichlorians = Map.of(
            "Anakin", 27000,
            "Jar-Jar Binks", 0
        );

        IO.println(weapons);
        IO.println(ships);
        IO.println(midichlorians);
    }
}
```

The collections returned by these `of` methods are immutable. This means methods
which would change the underlying collection will throw an `UnsupportedOperationException`.[^fine]

```java,panics
import java.util.List;

class Main {
    void main() {
        List<String> weapons = List.of("Lightsaber", "Blaster");
        
        // Unsupported
        weapons.add("A winning smile?")

        IO.println(weapons);
    }
}
```

If you want the convenience of the factory methods but actually want an `ArrayList`, `HashMap`, or
a similar collection which supports `.add`, `.remove`, etc. you are in luck. Those classes generally
have a constructor which will copy another `List`, `Map`, or `Set`.

```java
import java.util.List;

class Main {
    void main() {
        // Reads better than a bunch of .add calls
        List<String> weapons = new ArrayList<>(List.of("Lightsaber", "Blaster"));
        
        // Will work!
        weapons.add("A winning smile?")

        IO.println(weapons);
    }
}
```


If you want the opposite - if you want to make a copy of something like an `ArrayList`
which does not support `.add`, `.remove`, etc. - you can use `copyOf`.

```java
import java.util.List;

class Main {
    void main() {
        List<String> weapons = new ArrayList<>(List.of("Lightsaber", "Blaster"));
        weapons.add("A winning smile?")
        IO.println(weapons);

        // Similar methods exist for Map and Set
        List<String> unchangable = List.copyOf(weapons);
        IO.println(unchangable);
    }
}
```

[^interface_static_methods]: Interfaces can have static methods. We'll cover it in a bit. For now all you need to know is that these methods exist, not how to define similar ones yourself.

[^fine]: This is often fine. When something doesn't change after construction its one less thing to 
have to think about when reading code. If you pass an `ArrayList` to a method you do need to wonder
if it is only going to be read or if something that you forgot about will call `.add`, `.remove`, etc.