# Static Methods

Interfaces may specify `static` methods. These work similarly to static methods
on classes in that they can be used without an actual instance of a class.

```java
interface Animal {
    static boolean allowedLooseInHouse(String species) {
        if ("dog".equals(species) || "cat".equals(species)) {
            return true;
        }
        else {
            // My cousin has a Pig that we were all afraid
            // was going to straight up eat her child.
            //
            // The child got old enough that it's not a concern,
            // but good God.
            return false;
        }
    }
}

void main() {
    IO.println(Animal.allowedLooseInHouse("dog"));
    IO.println(Animal.allowedLooseInHouse("cat"));
    IO.println(Animal.allowedLooseInHouse("pig"));
}
```

You may use this mechanic for any reason, but often it is most convenient
for "factory methods" - methods which make it easy to construct objects
related to the interface hierarchy.

A prime example of this is `List.of`. `of` is a static method defined on the `List`
interface.

```java
void main() {
    // of will return a List<String>, but code using this
    // factory doesn't see the actual implementing class
    List<String> critters = List.of("dog", "cat", "bat");
    IO.println(critters);
}
```

If the logic in a static interface method gets complex enough, it is also allowed
to define a private static method. 

This is unique for interfaces, as usually
everything in them is considered `public`. 
Even without writing `public`, a `static` interface method is by default a public method.

```java,no_run
interface Animal {
    private static void eat() {
    }

    private static void sleep() {
    }

    static void live() {
        eat();
        sleep();
    }
}
```

