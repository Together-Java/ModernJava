# Extend a Class

For a class to extend another one you need to write `extends` and then the name of the class
which is being extended.

```java
class BodyOfWater {}

class Ocean extends BodyOfWater {}
```

If the class being extended has non-zero argument constructors,
the subclass must pass arguments to those constructors in it's constructor
using `super()`.

```java
class BodyOfWater {
    long depth;

    BodyOfWater(long depth) {
        if (this.depth < 0) {
            throw new IllegalArgumentException();
        }
        this.depth = depth;
    }
}

class Ocean extends BodyOfWater {
    String name;

    Ocean(String name, long depth) {
        this.name = name;
        // Before you exit, you must pass 
        // arguments to the super-class constructor.
        super(depth);
    }
}

void main() {
    Ocean pacific = new Ocean("Pacific", 36201L);
    IO.println(
        "The " + pacific.name + 
        " ocean is " + pacific.depth + 
        "' deep."
    );
}
```