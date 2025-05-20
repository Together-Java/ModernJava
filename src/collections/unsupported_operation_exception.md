# UnsupportedOperationException

`List`, `Map`, and `Set` are interfaces with a lot of methods.
There are circumstances - like a `List` directly wrapping an array -
where it isn't possible to provide an implementation
for all those methods.

In these situations, the specific exception that will be thrown is an `UnsupportedOperationException`.

```java
import java.util.List;
import java.util.Arrays;

class Main {
    void main() {
        String[] furniture = new String[] {
            "Ottoman",
            "Table",
            "Dresser"
        };

        List<String> furnitureList = Arrays.asList(furniture);

        try {
            furnitureList.add("Shelf");
        } catch (UnsupportedOperationException e) {
            IO.println("Tried to do an unsupported operation");
        }
    }
}
```

For each collection some operations are mandatory to implement - like `.size` on `List` -
while others are allowed to be unsupported and still be a "valid" implementation.