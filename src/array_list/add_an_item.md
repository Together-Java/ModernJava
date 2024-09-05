# Add an item

To add an item to an `ArrayList` you use the `.add`
method.

```java
import java.util.ArrayList;

void main() {
    ArrayList<String> names = new ArrayList<>();
    names.add("The Bowery King");
    names.add("Caine");

    System.out.println(names);
}
```

The way this works is conceptually the 
same as the growable array that we went over earlier.

All you need to know though is that you can add 
as many items as you will and the container will grow
dynamically.
