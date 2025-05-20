# Set

A `Set` is a collection of elements that does not allow duplicates.
Sets that come with Java implement the `java.util.Set` interface.

```java,no_run
interface Set<E> {
    boolean contains(Object o);
    boolean add(E e);
    boolean remove(Object o);
    // and more
}
```

`HashSet` provides an implementation of `Set` that works via the same mechanics - `.hashCode` and `.equals` - as a `HashMap`.

```java
import java.util.Set;
import java.util.HashSet;

class Main {
    void main() {
        Set<String> agents = new HashSet<>();
        agents.add("Syril");
        agents.add("Dedra");

        IO.println(agents);

        // If you try to add a duplicate to a set it won't
        // crash, but there won't be two in the collection
        agents.add("Syril");

        IO.println(agents);
    }
}
```

Checking membership in a large set is generally fast for the same reasons adding a new element
to a large map is fast.