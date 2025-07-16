# Abstract Classes

Abstract classes are classes which you cannot make an instance of directly.[^concrete]

```java,does_not_compile
abstract class Plant {}

void main() {
    // You cannot make an instance because 
    // it is an abstract class.
    var p = new Plant();
}
```

The use-case for these is making classes which are designed to be subclassed.
An example of this that comes with Java is `AbstractList`. 

`AbstractList` defines most of the methods required by the `List` interface and is intended to
lower the effort required to make a custom `List` implementation.

```java
import java.util.AbstractList;

// This subclass is a List containing the numbers 5 and 7
class FiveAndSeven 
    // Almost all of the implementation is inherited from AbstractList
    extends AbstractList<Integer> {

    @Override
    public Integer get(int index) {
        return switch (index) {
            case 0 -> 5;
            case 1 -> 7;
            default -> throw new IndexOutOfBoundsException();
        };
    }

    @Override
    public int size() {
        return 2;
    }
}

void main() {
    var l = new FiveAndSeven();
    IO.println(l);
}
```

[^concrete]: "Abstract" as a term here means something close to "not in reality." You will hear people refer to non-abstract classes as "concrete" classes.