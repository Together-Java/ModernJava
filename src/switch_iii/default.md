# default

Just like with normal switches, C-style switches can have a `default` label
that matches when no other label does.

```java
class Main {
    boolean shouldBeMainCharacter(String name) {
        switch (name) {
            case "Gohan":
                return true;
            default:
                return false;
        }
    }

    void main() {
        IO.println(
                shouldBeMainCharacter("Goku")
        );
    }
}
```

If you have a C-style switch over an enum you need this `default` case for exhaustiveness. Java does not
otherwise accept that you have covered all the cases.

```java,does_not_compile
enum Technique {
    KAMEHAMEHA,
    INSTANT_TRANSMISSION,
    KAIOKEN,
    ULTRA_INSTINCT
}

class Main {
    boolean didGokuStealItFromSomeoneElse(Technique technique) {
        switch (technique) {
            case KAMEHAMEHA:
                IO.println("Master Roshi Taught it to him");
                return true;
            case INSTANT_TRANSMISSION:
                IO.println("Space aliens");
                return true;
            case KAIOKEN:
                IO.println("King Kai's name is in it!");
                return true;
            case ULTRA_INSTINCT:
                IO.println("I'd say not");
                return false;
            // Even though we covered every option, Java doesn't trust us.
            // You need a default label or to return later in the function
            //
            // default: 
            //    throw new IllegalStateException("Unexpected: " + technique);
        }
    }

    void main() {
        IO.println(
                didGokuStealItFromSomeoneElse(Technique.INSTANT_TRANSMISSION)
        );
    }
}
```