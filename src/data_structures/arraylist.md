
### Arraylist

The Array list in the `java.util` package acts as a normal Array with the exception of being able to easily modify its values. In an `Array` you need to resize the data structure to add/remove an item. `ArrayList` does this for you automatically so you don't need to resize the Array manually. **Elements inside an Array list are Objects** Thus `Type` is a wrapper equivalent of a type. 

```java
import java.util.ArrayList;

ArrayList<Type> Name = new ArrayList<Type>(); 
```

***Functions***

```java
list.add(value); // Add item
list.set(indx, value); // Modify
list.get (indx); // Retrieve
list.remove(indx); // Delete
list.clear(); // Remove all items
list.size(); // Gives number of items in a list
```
