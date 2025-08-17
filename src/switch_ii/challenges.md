# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1

Complete the switch expression such that it yields 
the appropriate value for each case.

In the surfer case, make sure to print out "Radical!" before yielding
the value.

```java,editable
enum Profession {
    FIREFIGHTER,
    PLUMBER,
    SURFER
}

enum NaturalEnemy {
    FIRE,
    LEAKY_PIPES,
    BODACIOUS_WAVES
}

NaturalEnemy enemy(Profession p) {
    switch (p) {
        case FIREFIGHTER -> {
            // CODE HERE
        };
        case PLUMBER -> {
            // CODE HERE
        } 
        case SURFER -> {
            // CODE HERE
        }
    }
}

void main() {
    IO.println(enemy(Profession.FIREFIGHTER));
    IO.println(enemy(Profession.PLUMBER));
    IO.println(enemy(Profession.SURFER));
}
```

## Challenge 2

Update your program above to omit `yield` in the two cases where it is not needed.