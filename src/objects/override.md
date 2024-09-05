# @Override

If you intend to override a method you should put
`@Override` above that method.

```java
class Position {
    int x;
    int y;

    Position(int x, int y) {
        this.x = x;
        this.y = y;
    }

    @Override
    public String toString() {
        return "Position[x=" + x + ", y=" + y + "]";
    }
}

void main() {
    Object o = new Position(9, 8);
    System.out.println(o);
}
```

This doesn't change anything about how the program works,
but it is a signal to Java that you intended to be overriding a method.
If you get something wrong with the name, visibility, return type,
or argument types of the method then putting `@Override` 
means Java will warn you about those sorts of issues.

```java,panics
class Position {
    int x;
    int y;

    Position(int x, int y) {
        this.x = x;
        this.y = y;
    }

    // toString on Object doesn't take in an int
    // but this would otherwise be allowed 
    // since its technically a distinct method
    @Override
    public String toString(int value) {
        return "Position[x=" + x + ", y=" + y + "]";
    }
}

void main() {
    Object o = new Position(9, 8);
    System.out.println(o);
}
```