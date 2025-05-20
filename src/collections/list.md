# List

A `List` is an ordered collection of elements that generally allows duplicates.
Lists that come with Java implement the `java.util.List` interface
which provides myriad methods for working with such a collection.

```java,no_run
interface List<E> {
    int size();
    boolean isEmpty();
    E get(int index);
    // and more
}
```

`ArrayList` implements `List` and is likely the named class you will see
most often, but there are other implementations you will encounter as time goes on.

```java
import java.util.List;
import java.util.ArrayList;

class Main {
    void main() {
        List<String> names = new ArrayList<>();
        names.add("Andor");
        names.add("Bix");
        names.add("Luthen");

        IO.println(names);
    }
}
```

Every method and capability that `ArrayList` has is available from the `List` interface.[^saveafew]
This includes being able to be used in for-each loops.

```java
import java.util.List;
import java.util.ArrayList;

class Main {
    void main() {
        List<String> names = new ArrayList<>();
        names.add("Andor");
        names.add("Bix");
        names.add("Luthen");

        for (var name : names) {
            IO.println(name);
        }
    }
}
```

[^saveafew]: Save a really niche one

