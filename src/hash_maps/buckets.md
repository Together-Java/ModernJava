# Buckets

Once you know the range of your hash function,
the next step is to divide that range into buckets.

A bucket is the name for the place where you will store
all the values that match that hash key.


```java,no_run
class Bucket {

}
```

One way to divide your range into buckets is to make an array
then pick an index into that array by the hash.

```java
record CarsCharacter(
    String firstName, 
    String lastName
) {}

// Like before, we define our hash function
// to be the first letter of the last name.
char hashFunction(
    CarsCharacter carsCharacter
) {
    return carsCharacter.lastName().charAt(0);
}

class Bucket {

}

// Then, assuming we have some array of buckets
Bucket[] buckets = new Bucket[] {
    new Bucket(),
    new Bucket(),
    new Bucket()
};

// We can make logic that takes the result of the hash
// and gives an index for a bucket.
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


void main() {
    // These two have different hashes but end up in the
    // same bucket
    var sally = new CarsCharacter("Sally", "Carrera");
    System.out.println(hashFunction(sally));
    System.out.println(indexFor(hashFunction(sally)));

    var doc = new CarsCharacter("Doc", "Hudson");
    System.out.println(hashFunction(doc));
    System.out.println(indexFor(hashFunction(doc)));

    var lightning = new CarsCharacter("Lightning", "McQueen");
    System.out.println(hashFunction(lightning));
    System.out.println(indexFor(hashFunction(lightning)));


}
```

These are the drawers in our filing cabinet analogy.

