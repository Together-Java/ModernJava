# Inheritance

When one class extends another we say that it is "inheriting"
from the superclass.

What this means is that all the fields and methods of the class being extended
carry over into the extending class.

```java
class BodyOfWater {
    long depth;

    BodyOfWater(long depth) {
        if (this.depth < 0) {
            throw new IllegalArgumentException();
        }
        this.depth = depth;
    }

    void swim() {
        if (depth > 50) {
            IO.println("You have drowned");
        }
        else {
            IO.println("You are fine");
        }
    }
}

class Ocean extends BodyOfWater {
    String name;

    Ocean(String name, long depth) {
        this.name = name;
        super(depth);
    }
}

void main() {
    BodyOfWater pacific = new Ocean("Pacific", 36201L);
    pacific.swim(); // The swim method is "inherited"
}
```