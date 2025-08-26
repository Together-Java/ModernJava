# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1.

Convert this program which uses a switch without fallthrough
to instead use fallthrough for all the common cases.

```java,editable
enum Character {
    GOKU,
    PICCOLO,
    FRIEZA,
    VEGETA,
    PILAF,
    GOHAN,
    BEERUS
}

class Main {
    String isEvil(Character c) {
        switch (c) {
            case GOKU -> {
                // Man puts the multiverse in danger
                // on account of wanting to fight!
                return "debatable";
            }
            case PICCOLO -> {
                return "not_anymore";
            }
            case FRIEZA -> {
                return "yes";
            }
            case VEGETA -> {
                return "not_anymore";
            }
            case PILAF -> {
                return "not_anymore";
            }
            case GOHAN -> {
                return "no";
            }
            case BEERUS -> {
                // He's more a force of nature,
                // but its relative.
                return "debatable";
            }
            default -> {
                return "unknown";
            }
        }
    }

    void main() {
        IO.println("Goku: " + isEvil(Character.GOKU));
        IO.println("Piccolo: " + isEvil(Character.PICCOLO));
        IO.println("Frieza: " + isEvil(Character.FRIEZA));
        IO.println("Vegeta: " + isEvil(Character.VEGETA));
        IO.println("Pilaf: " + isEvil(Character.PILAF));
        IO.println("Gohan: " + isEvil(Character.GOHAN));
        IO.println("Beerus: " + isEvil(Character.BEERUS));
    }
}
```

## Challenge 2.

Convert the previous program using fallthrough to also
be directly returned as a switch expression using `yield`.

## Challenge 3.

Write a method named `aToZ` which, given a character
between `a` and `z`, will print all the letters
from that letter on until `z`.

Make use of a switch with fallthrough instead of loops or any other mechanism.

```java,editable
class Main {
    void aToZ(char c) {
        // CODE HERE
    }

    void main() {
        aToZ('z'); // z
        aToZ('x'); // x y z
        aToZ('a'); // a b c d ... x y z
    }
}
```
