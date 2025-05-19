# Loop over Contents

Just like the `.length` and `[]` operations on arrays,
you can loop over all the elements in an `ArrayList`
with the combination of `.size()` and `.get(idx)`

```java
import java.util.ArrayList;

void main() {
    ArrayList<String> names = new ArrayList<>();
    names.add("Sofia Al-Azwar");
    names.add("Viggo Tarasov");
    names.add("Iosef Tarasov");

    for (int i = 0; i < names.size(); i++) {
        String name = names.get(i);

        IO.println("NAME: " + name);
    }
}
```

Its not a rule, but this is also a convenient use of for loops.
You can use all the same tricks you learned when looping over arrays here.