# Factories

Another interesting use of static methods is what we would call a "factory"
method.

Say you have a class like the following.

```java
class Position {
    int x;
    int y;

    Position(int x, int y) {
        this.x = x;
        this.y = y;
    }
}
~void main() {}
```

It would be reasonable want to add an overloaded constructor for when `y` is `0`.

```java
class Position {
    int x;
    int y;

    Position(int x, int y) {
        this.x = x;
        this.y = y;
    }

    Position(int x) {
        this.x = x;
        this.y = 0;
    }
}
~void main() {}
```

But now it is impossible to add a constructor that works for when `x` is `0`.

```java,does_not_compile
class Position {
    int x;
    int y;

    Position(int x, int y) {
        this.x = x;
        this.y = y;
    }

    Position(int x) {
        this.x = x;
        this.y = 0;
    }

    Position(int y) {
        this.x = 0;
        this.y = y;
    }
}
~void main() {}
```

Using a static method to create a `Position` - i.e. as a "factory" - is a way around the issue.[^note]

```java
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
```
```java
~class Position {
~    int x;
~    int y;
~
~    Position(int x, int y) {
~        this.x = x;
~        this.y = y;
~    }
~
~    static Position fromX(int x) {
~        return new Position(x, 0);
~    }
~
~    static Position fromY(int y) {
~        return new Position(0, y);
~    }
~}
~
class Main {
    void main() {
        var p1 = new Position(1, 2);
        var p2 = Position.fromX(4);
        var p3 = Position.fromY(5);

        System.out.println(p1.x + ", " + p1.y);
        System.out.println(p2.x + ", " + p2.y);
        System.out.println(p3.x + ", " + p3.y);
    }
}
```

[^note]: This won't work if you defined `Position` inside the anonymous main class. I'll tell you why later.