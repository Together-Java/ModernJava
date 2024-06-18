# Performance Problems

While the code as is _works_, it will not perform well.

Since we copy the underlying array every time someone adds a new element it can be expensive to add a lot of elements.

Pretend we were going to add a hundred elements to the growable array.

```java
~class GrowableIntArray {
~    // Store an int[] internally
~    private int[] data;
~
~    GrowableIntArray() {
~        // Make sure to initialize it correctly
~        this.data = new int[0];
~    }
~
~    // When someone wants to get an item, get it from the array
~    int get(int index) {
~        return this.data[index];
~    }
~
~    // Same deal when someone wants to set an item at an index.
~    void set(int index, int value) {
~        this.data[index] = value;
~    }
~
~    // And we need an accessor for the size so that someone
~    // can loop over the array.
~    int size() {
~        return this.data.length;
~    }
~
~    void add(int value) {
~        // Copy the old array to a new, bigger one
~        int[] newArray = new int[this.data.length + 1];
~        for (int i = 0; i < this.data.length; i++) {
~            newArray[i] = this.data[i];
~        }
~
~        // Then put the new element at the end
~        newArray[newArray.length - 1] = value;
~
~        // And swap the array
~        this.data = newArray; 
~    }
~}
~
~
class Main {
    void main() {
        var array = new GrowableIntArray();

        for (int i = 0; i < 100; i++) {
            array.add(i);
        }

        System.out.println(array.size());
    }
}
```

For the each element we need to make a copy of an array. So when we add the first element we need to make an array 1 element big. The second, copy that 1 element array and make a new
2 element one.

So if you do napkin math on the things that need to happen you get this

```
1 + 2 + 3 + 4 + 5 + 6 + 7 + 8 + 9 + 10 + 11 + 12 ...
```

Which is just a crazy number of copies. It means calling `.add` on an already big list will be slow and calling `.add` a lot of times to make a big list will be very slow.