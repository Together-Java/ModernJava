# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1.

Write two static methods in the following `Bytes` class.

The first should take an `int` and return an array of 4
bytes.

The second should take that array of 4 bytes and give back the original int.

There are a few ways to do this, but you only pass the test if
you can do a "full round trip."

```java,editable
class Bytes {
    static int toInt(byte[] bytes) {
        // CODE HERE
    }
    static byte[] toBytes(int value) {
        // CODE HERE
    }
}

class Main {
    void main() {
        int i = 172089379;

        byte[] bs = Bytes.toBytes(i);

        // 172089379
        IO.println(Bytes.fromInt(bs));
    }
}
```

## Challenge 2.

Turn the `String` `"hello world"` into a `short[]`. Print the contents
of this `short[]` and then turn it back into a `String`.

```java
class Main {
    void main() {
        String s = "hello world";

        short[] shorts;

        // CODE HERE

        String roundTripped;

        // CODE HERE
    }
}
```

## Challenge 3.

Make a class named `UnsignedInteger`. It should wrap up an `int` such that
all operations on it are performed using the appropriate unsigned specific methods
when needed.

At a minimum:

- Implement `toString` so that the unsigned representation is used
- Implement `equals` and `hashCode`
- Implement `plus` and `minus`
- Implement the `Comparable<UnsignedInteger>` interface.

```java
// CODE HERE

class Main {
    void main() {
        var i = new UnsignedInteger(0);
        IO.println(i.minus(new UnsignedInteger(1)));
    }
}
```

## Challenge 4.

Convert this program to use `float` instead of `double`.

```java
class Main {
    void main() {
        double radius = Double.parseDouble(
            IO.readln("What is the radius of the circle? ")
        );
        double pi = 3.14;
        double circumference = 2 * pi * radius;

        IO.println("Circumference: " + circumference);
    }
}
```