# ArrayList

Java comes with a generic growable array. It is called
an `ArrayList`.

```java
import java.util.ArrayList;

void main() {
    ArrayList<String> names = new ArrayList<>();
    names.add("John Wick");

    IO.println(names);
}
```