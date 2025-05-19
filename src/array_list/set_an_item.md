# Set an item

You can set an item at an index with `.set`

```java
import java.util.ArrayList;

void main() {
    ArrayList<String> names = new ArrayList<>();
    names.add("John Wick");

    names.set(0, "Baba Yaga");

    IO.println(names);
    IO.println(names.get(0));
}
```

If the index you provide is out of bounds, you will get an `IndexOutOfBoundsException`.

```java,panics
import java.util.ArrayList;

void main() {
    ArrayList<String> names = new ArrayList<>();
    names.add("John Wick");

    names.set(15, "Baba Yaga");
}
```