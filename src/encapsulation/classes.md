# Classes

One step above methods is classes.

When classes have private fields and all interactions with those fields
are mediated through methods

The `ArrayList` class that comes with Java looks something like this.[^liberties]

```java
public class ArrayList<E> extends AbstractList<E>
        implements List<E>, RandomAccess, Cloneable, java.io.Serializable
{
    Object[] elementData;

    private int size;

    public ArrayList() {
        this.elementData = DEFAULTCAPACITY_EMPTY_ELEMENTDATA;
    }

    private void add(E e, Object[] elementData, int s) {
        if (s == elementData.length)
            elementData = grow();
        elementData[s] = e;
        size = s + 1;
    }

    private Object[] grow(int minCapacity) {
        int oldCapacity = elementData.length;
        if (oldCapacity > 0 || elementData != DEFAULTCAPACITY_EMPTY_ELEMENTDATA) {
            int newCapacity = ArraysSupport.newLength(oldCapacity,
                    minCapacity - oldCapacity, /* minimum growth */
                    oldCapacity >> 1           /* preferred growth */);
            return elementData = Arrays.copyOf(elementData, newCapacity);
        } else {
            return elementData = new Object[Math.max(DEFAULT_CAPACITY, minCapacity)];
        }
    }

    private Object[] grow() {
        return grow(size + 1);
    }

    public boolean add(E e) {
        modCount++;
        add(e, elementData, size);
        return true;
    }

    // ...
}
```

People who write programs that depend on calling `.add` on an `ArrayList` do not need
to understand how or when the internal `elementData` and `size` fields are updated. Those also
need not be the only fields that exist. All that is required is "calling `.add` will add an element to the list."

It is in this way that classes provide encapsulation. They can hide the fields which
are needed and the way in which they are used - "implementation details" - in order
to provide some implicit interface.


[^liberties]: Creative liberties taken.