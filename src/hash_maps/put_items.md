# Put Items

You can associate a key with a value by calling the `.put` method.[^watchcars]

```java
import java.util.HashMap;

class Main {
    void main() {
        var wins = new HashMap<String, Integer>();
        wins.put("Lightning McQueen", 2);
        wins.put("Tow Mater", 0);
        
        IO.println(wins);
    }
}
```

[^watchcars]: Cars was a delightful movie. Go to your local second hand store, get
a copy on DVD, and make a night of it.