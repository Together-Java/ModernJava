# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1.

Declare an interface named `DoubleArray` which requires
two methods of classes that implementing classes: `length` and `get`.

These methods should be specified to work the same as how `[]` and `.length`
work on a `double[]`.

```java,no_run
interface DoubleArray {
    // CODE HERE
}
```

## Challenge 2.

Make a class that implements your `DoubleArray` interface
using a `double[]` in a field to perform all the operations.

```java,editable
interface DoubleArray {
    // CODE FROM PREVIOUS CHALLENGE
}

class RealDoubleArray /* CODE HERE */ {
    // CODE HERE
}

class Main {
    void main() {
        DoubleArray arr = new RealDoubleArray(new double[] {
            1.0, 1.5, 2.0, 2.5, 3.0
        });

        for (int i = 0; i < arr.length(); i++) {
            IO.println("Got double value: " + arr.get(i));
        }
    }
}
```
## Challenge 3.

Make a second class that implements `DoubleArray` but have this one
be backed by an `int[]` and perform widening conversions when returning values.

```java,editable
interface DoubleArray {
    // CODE FROM PREVIOUS CHALLENGE
}

class FauxDoubleArray  /* CODE HERE */ {
    // CODE HERE
}

class Main {
    void main() {
        DoubleArray arr = new FauxDoubleArray(new int[] {
            1, 2, 3, 4, 5
        });

        for (int i = 0; i < arr.length(); i++) {
            IO.println("Got double value: " + arr.get(i));
        }
    }
}
```

## Challenge 4.

Make an implementation of the following `Tarot` interface for [each tarot card
featured in JoJo's Bizzare Adventure](https://jojowiki.com/Tarot_Cards).

```java
interface Tarot {
    String symbolism();

    String standUser();
}
```
