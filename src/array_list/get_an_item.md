# Get an item

To get an item at a given index in an `ArrayList`
you should use `.get`

```java
import java.util.ArrayList;

void main() {
    ArrayList<String> names = new ArrayList<>();
    names.add("Winston Scott");

    String name = names.get(0);
    System.out.println(name);
}
```

If the index you picked is greater than the number of elements in the `ArrayList`
it will throw an `IndexOutOfBoundsException`

```java,panics
import java.util.ArrayList;

void main() {
    ArrayList<String> names = new ArrayList<>();
    names.add("Killa Harkan");

    String name = names.get(10);
    System.out.println(name);
}
```