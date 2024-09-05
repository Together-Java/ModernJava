# Growable Buckets

As you may have reasoned, a hash map's buckets
will start out empty but later have elements added to them.

This means that they will need to grow over time.

One way to do this is with a growable array.

```java
class Bucket {
    private CarsCharacter[] data;
    private int size;

    Bucket() {
        this.data = new CarsCharacter[0];
        this.size = 0;
    }

    CarsCharacter get(int index) {
        if (index >= size) {
            throw new IndexOutOfBoundsException(index);
        }
        return this.data[index];
    }

    void set(int index, CarsCharacter value) {
        if (index >= size) {
            throw new IndexOutOfBoundsException(index);
        }
        this.data[index] = value;
    }

    int size() {
        return this.size;
    }

    void add(CarsCharacter value) {
        if (size >= this.data.length - 1) {
            int newLength = this.data.length * 2;
            if (newLength == 0) {
                newLength = 2;
            }

            CarsCharacter[] newArray = new CarsCharacter[newLength];
            for (int i = 0; i < this.data.length; i++) {
                newArray[i] = this.data[i];
            }
            this.data = newArray;
        }

        this.data[size] = value;
        this.size++;
    }
}
```

Every detail of this is the same as the `GrowableIntArray` we made earlier,
save the fact that it is called `Bucket` and instead of `int`s it holds
`CarsCharacter`s.[^makenote]

[^makenote]: Make note of this annoying similarity somewhere in your mind. It will come up later.