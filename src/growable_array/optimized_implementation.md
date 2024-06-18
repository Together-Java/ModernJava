# Optimized Implementation

So with that context we can update the simple implementation as follows.

Note the use of `IndexOutOfBoundsException`. It is an unchecked exception that
comes with Java specifically for when an index is out of bounds.[^obvious]

```java
class GrowableIntArray {
    private int[] data;
    // We need a different variable to store the size
    // since the array's size will different than we want.
    private int size;

    GrowableIntArray() {
        this.data = new int[0];
        this.size = 0;
    }

    int get(int index) {
        // Now that we manage the size, we need to do
        // "bounds checks" ourselves
        if (index >= size) {
            throw new IndexOutOfBoundsException(index);
        }
        return this.data[index];
    }

    void set(int index, int value) {
        // For setting as well
        if (index >= size) {
            throw new IndexOutOfBoundsException(index);
        }
        this.data[index] = value;
    }

    int size() {
        // We use the size we store rather than the length of the array
        return this.size;
    }

    void add(int value) {
        // if we won't have enough room in the array, make a new one.
        if (size >= this.data.length - 1) {
            // Overallocate by 2x
            int newLength = this.data.length * 2;
            if (newLength == 0) {
                newLength = 2; // Unfortunately 0 * 2 is 0, so account for that
            }

            int[] newArray = new int[newLength];
            for (int i = 0; i < this.data.length; i++) {
                newArray[i] = this.data[i];
            }
            this.data = newArray; 
        }

        // And at this point we know the array is big enough
        this.data[size] = value;
        this.size++;
    }
}
```

[^obvious]: I love obvious and circular statements like this, if you haven't noticed.