# Remove an item

You can use `.remove` to remove an item
from an `ArrayList`.

To do this you need to provide it the value you want to remove.
It will do all the array resizing required internally, even
if the item is in the middle of a list.

```java
import java.util.ArrayList;

void main() {
    ArrayList<String> names = new ArrayList<>();
    names.add("The Bowry King");
    names.add("The Elder");
    names.add("The Harbinger");

    IO.println(names);

    names.remove("The Elder");

    IO.println(names);
}
```

Alternatively you can remove an item by its index.

```java
import java.util.ArrayList;

void main() {
    ArrayList<String> names = new ArrayList<>();
    names.add("The Bowry King");
    names.add("The Elder");
    names.add("The Harbinger");

    IO.println(names);

    names.remove(2);
    names.remove(0);

    IO.println(names);
}
```

You need to be careful about that though. If your `ArrayList` holds `Integer`s then
Java can get confused between the implementation of remove that removes using the item itself
and the one that removes by index.

```java,not_desired_behavior
import java.util.ArrayList;

void main() {
    ArrayList<Integer> numbers = new ArrayList<>();
    numbers.add(1);
    numbers.add(2);
    numbers.add(3);

    IO.println(numbers);

    // Notice that this removes "2" which is at index 1!
    numbers.remove(1);

    IO.println(numbers);
}
```

This comes down to `int` and `Integer` being slightly different. When Java
sees an integer literal it assumes it is an `int`. It is only when circumstances
are such that it cannot possibly be an `int` that it automatically boxes it 
into an `Integer`.

It is rare, but if you encounter this issue you can use `Integer.valueOf` to deal with it.

```java
import java.util.ArrayList;

void main() {
    ArrayList<Integer> numbers = new ArrayList<>();
    numbers.add(1);
    numbers.add(2);
    numbers.add(3);

    IO.println(numbers);

    numbers.remove(Integer.valueOf(1));

    IO.println(numbers);
}
```