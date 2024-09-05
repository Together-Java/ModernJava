# Hash Functions

A hash function is something that takes a piece of data
and extracts a smaller, but predictable, piece of data from it.

```java
record CarsCharacter(
    String firstName, 
    String lastName
) {}

char hashFunction(
    CarsCharacter carsCharacter
) {
    return carsCharacter.lastName().charAt(0);
}

void main() {
    var lightning = new CarsCharacter("Lightning", "McQueen");

    char firstOfLast = hashFunction(lightning);
    System.out.println(firstOfLast);
}
```

Taking the first letter of a last name is an example of this. You can't
reverse `M` into `McQueen`, but you can take `McQueen` and know to look
in the bucket labeled `M`.

We need hash functions to decide what "filing cabinet"
a thing should go in.