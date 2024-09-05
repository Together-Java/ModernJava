# Get Items

Similarly to get an item from a map
you need to do the following

1. Compute the hash code of the item.
2. Find the bucket that item should go in.
3. Go through each item in the bucket to see if it matches.[^more]

```java
record CarsCharacter(
    String firstName, 
    String lastName
) {}

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



class CarsCharacterHashMap {
    Bucket[] buckets = new Bucket[] {
        new Bucket(),
        new Bucket(),
        new Bucket()
    };

    int indexFor(char hash) {
        if (hash >= 'A' && hash <= 'F') {
            return 0;
        }
        else if (hash >= 'G' && hash <= 'N') {
            return 1;
        }
        else {
            return 2;
        }
    }

    char hashFunction(
        CarsCharacter carsCharacter
    ) {
        return carsCharacter.lastName().charAt(0);
    }

    void put(CarsCharacter character) {
        // 1. Compute the hash code
        char hash = hashFunction(character);
        // 2. Find the bucket
        Bucket bucket = buckets[indexFor(hash)];
        // 3. Add to the bucket
        bucket.add(character);
    }

    ` get(CarsCharacter character) {
        // 1. Compute the hash code
        char hash = hashFunction(character);
        // 2. Find the bucket
        Bucket bucket = buckets[indexFor(hash)];
        // 3. Add to the bucket
        bucket.add(character);
    }
}

void main() {
    var map = new CarsCharacterHashMap();

    map.put(new CarsCharacter("Sally", "Carrera"));
    map.put(new CarsCharacter("Doc", "Hudson"));
    map.put(new CarsCharacter("Lightning", "McQueen"));

    System.out.println(map.buckets[0].size());
    System.out.println(map.buckets[1].size());
    System.out.println(map.buckets[2].size());
}
```

[^more]: There is more to say on how we determine if an item is a match, but
we will cover that later. For now just assume calling `.equals` will
make sense.
