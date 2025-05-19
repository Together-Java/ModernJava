# Size

The you can access the number of elements in an
`ArrayList` with the `.size()` method.

```java
import java.util.ArrayList;

void main() {
    ArrayList<String> names = new ArrayList<>();

    IO.println(names.size());

    names.add("Vincent Bisset de Gramont");
    IO.println(names.size());

    names.add("Mr. Nobody");
    IO.println(names.size());
}
```

This will tell you the number of elements in the `ArrayList` but
not the amount of space allocated by the underlying array. 

This is fine because, if you aren't the one making a growable array,
it doesn't matter. All you need to concern yourself with is what is actually
there, not any book keeping.