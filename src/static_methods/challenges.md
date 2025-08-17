# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1

Change this position class such that it doesn't only have an `x` and a `y`. It should
also have a `z`.

Then add the following static methods. `fromZ`, `fromXY`, `fromXZ`, and `fromYZ`.

```java,editable
class Position {
    int x;
    int y;

    Position(int x, int y) {
        this.x = x;
        this.y = y;
    }

    static Position fromX(int x) {
        return new Position(x, 0);
    }

    static Position fromY(int y) {
        return new Position(0, y);
    }
}

class Main {
    void main() {
        var p1 = Position.fromXY(1, 2);
        IO.println("(" + p1.x + ", " + p1.y + ", " + p1.z + ")");

        var p2 = Position.fromYZ(1, 2);
        IO.println("(" + p2.x + ", " + p2.y + ", " + p2.z + ")");

        var p3 = Position.fromXZ(1, 2);
        IO.println("(" + p3.x + ", " + p3.y + ", " + p3.z + ")");

        var p4 = Position.fromZ(4);
        IO.println("(" + p4.x + ", " + p4.y + ", " + p4.z + ")");
    }
}
```

## Challenge 2

Make a static method in the `Maths` class called `quadraticFormula`.
It should take in an `a`, `b`, and `c` and run the [quadradic formula](https://en.wikipedia.org/wiki/Quadratic_formula) on those values.

This formula will give you either one "real" solution, two real solutions,
or two imaginary solutions.

For now just throw an exception if the solutions are imaginary
and treat having one solution as having two solutions with the same value.

```java,editable
class Maths {
    // CODE HERE
}

class Main {
    void main() {
        var result = Maths.quadraticFormula(6, -17, 12);
        IO.println(result.solutionOne);
        IO.println(result.solutionTwo);
    }
}
```

## Challenge 3

Update your code above to also communicate if a solution is imaginary.
Use a boolean or an enum field on whatever class you wrote to hold both solutions
for this.[^other]

[^other]: You will learn other ways later.

## Challenge 4

Make the following code compile. Do so first by changing one of the fields to `static`
then by instead passing an extra argument to the `static` method.

```java,no_run
class Keychain {
    final String[] keys;

    Keychain(String[] keys) {
        this.keys = keys;
    }

    boolean hasKey(String key) {
        for (int i = 0; i < keys.length; i++) {
            if (keys[i].equals(key)) {
                return true;
            }
        }
        return false;
    }
}


class Main {
    Keychain keychain = new Keychain(new String[] {
        "house",
        "car",
        "shed"
    });

    static void unlock(String thing) {
        if (keychain.hasKey(thing)) {
            IO.println("You have unlocked my " + thing);
        }
        else {
            IO.println("You don't have a key for my " + thing);
        }
    }
    
    void main() {
        unlock("house");
        unlock("car");
        unlock("shed");
        unlock("heart");
    }
}
```