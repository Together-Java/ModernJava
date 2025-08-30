# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1.

The `Witch` class has a method named `pullFromHat`
that returns an `Object` that is sometimes a `Spell` and sometimes a `Broom`.

If it is a `Broom` call the `.fly()` method on it. If it is a `Spell` call `.cast`.

```java
class Spell {
    private final String name;

    Spell(String name) {
        this.name = name;
    }

    void cast() {
        IO.println("Casting " + name + "...");
    }
}

class Broom {
    void fly() {
        IO.println("Flying!");
    }
}

class Witch {
    Object pullFromHat() {
        double r = Math.random();
        if (r < 0.25) {
            return new Spell("Ensmallen");
        }
        else if (r < 0.5) {
            return new Spell("Embiggen");
        }
        else if (r < 0.75) {
            return new Spell("Enlongen");
        }
        else {
            return new Broom();
        }
    }
}

class Main {
    void main() {
        var witch = new Witch();

        Object item = witch.pullFromHat();

        // CODE HERE
    }
}
```

## Challenge 2.

Will the following code work? Why or why not?

```java,editable
class Main {
    void main() {
        String s = "abc";
        Object o = s;

        IO.println(o.length());
    }
}
```

## Challenge 3.

Will the following code work? Why or why not?

```java,editable
class Main {
    void main() {
        Object o = "abc";
        String s = o;

        IO.println(s.length());
    }
}
```

## Challenge 4.

Implement `toString`, `equals`, and `hashCode` 
on the following `Ogre` class such that it behaves
the same as an `Ogre` record.

```java
record Ogre(String name, double strength) {}
```

```java,editable
class Ogre {
    final String name;
    final double strength;

    Ogre(String name, double strength) {
        this.name = name;
        this.strength = strength;
    }

    // CODE HERE
}

class Main {
    void main() {
        Ogre o1 = new Ogre("Morihito", 100);
        Ogre o2 = new Ogre("Morihito", 100);

        IO.println(o1); // Ogre[name=Morihito, strength=100]
        IO.println(o1.equals(o2)); // True
        IO.println(o1.hashCode() == o2.hashCode()); // True
        IO.println(o1.equals(new Ogre("Reiji", 5))); // False
        IO.println(o1.hashCode() == new Ogre("Reiji", 5).hashCode()); // False
    }
}
```

