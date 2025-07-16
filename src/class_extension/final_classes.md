# Final Classes

If a class is marked `final` it cannot be extended.

```java,does_not_compile
final class Apple {}

// Cannot extend a final class
class RedApple extends Apple {}
~void main() {}
```

Because thinking about what the implications are if someone extends a class is hard,
it is reasonable to always declare your classes as `final` unless you have some reason not to.

```java
// It's not that something bad would happen if someone
// extended this class. It's that not having to think
// about it is useful.
final class Saltine {
    int saltiness;

    Saltine(int saltiness) {
        this.saltiness = saltiness;
    }
}
```

Records and Enums are always implicitly final.

```java,does_not_compile
record Pos(int x, int y) {}

// Records are final
class Pos2 extends Pos {}

enum StopLight { RED, YELLOW, GREEN }

// Enums are final
class StopLight2 extends StopLight {}
~class Main {void main() {}}
```