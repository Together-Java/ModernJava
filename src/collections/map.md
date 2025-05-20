# Map

A `Map` is a collection that maps keys to values. Maps that come with
Java implement the `java.util.Map` interface.

```java
interface Map<K, V> {
    V get(Object key);
    V put(K key, V value);
    // and more
}
```

`HashMap` is one implementation of `Map` you are likely to see and use.

```java
import java.util.Map;
import java.util.HashMap;

class Main {
    void main() {
        Map<String, Integer> ages = new HashMap<>();
        ages.put("Andor", 26);
        ages.put("Bix", 27);
        ages.put("Luthen", 59);

        IO.println(ages);
    }
}
```

Just like `ArrayList` and `List`, all the useful capabilities of `HashMap` are available
via the `Map` interface.