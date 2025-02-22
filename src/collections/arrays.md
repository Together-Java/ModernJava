# Arrays

Arrays are the odd duck out in the world of collections. They are basically a `List` but aren't `List`s.

You can make a `List` which is a view over an array with `Arrays.asList`.

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

        System.out.println(furnitureList);
    }
}
```

Changes made to the `List` returned from `Arrays.asList` will be reflected in the underlying array.

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

        furnitureList.set(0, "Recliner");

        System.out.println(Arrays.toString(furniture));
    }
}
```

Accordingly, any methods on `List` which try to perform operations that an array cannot support (such as `.add`) will throw exceptions.

```java,panics
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

        // Cannot add to an array!
        furnitureList.add("Shelf");
    }
}
```