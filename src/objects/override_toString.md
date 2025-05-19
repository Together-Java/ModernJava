# Override toString

To customize the behavior of `toString`
in your own classes you need to "override"
the `toString` method from `Object`.

What this means is that you need to define a method
which has the same name, arguments, return type, and visibility
as the one defined in `Object`.

That is, a `public` method named `toString` which takes no
arguments and returns a `String`.

```java
class Window {
    public String toString() {
        return "Window!";
    }
}

void main() {
    Object o = new Window();
    IO.println(o);
}
```

This is how you can customize the output of `IO.println`.

It is common practice for a class holding data to
include the values of its fields in its `toString` representation.
This can be very helpful for debugging.

```java
class Position {
    int x;
    int y;

    Position(int x, int y) {
        this.x = x;
        this.y = y;
    }

    public String toString() {
        return "Position[x=" + x + ", y=" + y + "]";
    }
}

void main() {
    Object o = new Position(9, 8);
    IO.println(o);
}
```