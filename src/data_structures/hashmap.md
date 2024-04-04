### Hashmaps

With arrays you have to store data in an ordered sequence identified with a indx. `Hashmaps` store data in a (key, pair) sequence that you can access by the index referring to another Object(indx is also an Object)

```java
import java.util.HashMap;
HashMap<Type, Type> Name = new HashMap<Type, Type>();
```

**Functions:**

```java
map.put(identifier, value);
map.get(identifier);
map.remove(identifier);
map.clear(); // Deletes the whole map
map.size();
```

Note: use `keyset()` to only get keys and `values()` to get specific Object values in loops
