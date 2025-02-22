# Get Items

You can get the value associated with a key by using `.get`. If there is no
value associated with that key it will return `null`.

```java
import java.util.HashMap;

class Main {
    void main() {
        var wins = new HashMap<String, Integer>();
        wins.put("Lightning McQueen", 2);
        wins.put("Tow Mater", 0);
        
        System.out.println(wins.get("Tow Mater"));
        System.out.println(wins.get("Doc Hudson"));
    }
}
```
