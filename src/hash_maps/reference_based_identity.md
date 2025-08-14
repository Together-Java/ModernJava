# Reference Based Identity

The hash function that `HashMap` uses is `.hashCode()`. It uses the number
returned from this method to decide which of the buckets it maintains
to put an item into.

Instead of making buckets like `A-G` and `H-Z`, it will use ranges of numbers. The concept is the
same though

For classes you make yourself, their `hashCode` will be based on what we call an object's
"identity." This means that while different instances of a class might give the same (incomplete sentence)


```java
~void main() {
~    new Main().main();    
~}
~
class LivingRaceCar {
    int cursedness;

    // God, could you imagine being judged by a Honda?
    LivingRaceCar(int cursedness) {
        this.cursedness = cursedness;
    }
}

class Main {
    void main() {
        var carA = new LivingRaceCar(10);
        // Car B is a reference to Car A
        var carB = carA;
        // Car C is a distinct object with its own identity
        var carC = new LivingRaceCar(10);
        
        // Accordingly, Car C will probably have a different
        // hashCode. This is despite it having the same
        // values in its fields. It is a "distinct" object.
        IO.println("A: " + carA.hashCode());
        IO.println("B: " + carB.hashCode());
        IO.println("C: " + carC.hashCode());
    }
}
```

Identity is also what the default `.equals` implementation is based off of. 
If two variables reference the same object then `.equals` will return `true`.

```java
~void main() {
~    new Main().main();    
~}
~
class LivingRaceCar {
    int cursedness;

    LivingRaceCar(int cursedness) {
        this.cursedness = cursedness;
    }
}

class Main {
    void main() {
        var carA = new LivingRaceCar(10);
        // Car B is a reference to Car A
        var carB = carA;
        // Car C is a distinct object with its own identity
        var carC = new LivingRaceCar(10);
        
        // Car C therefore will only equal itself
        // Car A and B will equal each other
        IO.println("A.equals(A): " + carA.equals(carA));
        IO.println("A.equals(B): " + carA.equals(carB));
        IO.println("A.equals(C): " + carA.equals(carC));
        IO.println("B.equals(A): " + carB.equals(carA));
        IO.println("B.equals(B): " + carB.equals(carB));
        IO.println("B.equals(C): " + carB.equals(carC));
        IO.println("C.equals(A): " + carC.equals(carA));
        IO.println("C.equals(B): " + carC.equals(carB));
        IO.println("C.equals(C): " + carC.equals(carC));
    }
}
```