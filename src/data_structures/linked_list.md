### Linked list

Almost identical to the Array list . They share the same functions due to them both sharing the `List` interface. Unlike ArrayList it doesn't Have an Array fundamentally though. it's a series of private nested classes of type `Entry` it references a `next` and `previous` item. Its like containers linked to each other.

**Usecase: Arraylist to store data as a better alternative to Arrays and LinkedList to manipulate data**

```java
import java.util.LinkedList;
LinkedList<Type> Name = new LinkedList<Type>();
```

**Functions:**

*Listed above will also work*

```java
list.addFirst();
list.getFirst();
list.removeFirst();

list.addLast();
list.getLast();
list.removeLast();

```
