# Invariants

Having private fields and methods is useful when you want
to maintain some invariants.

Say you wanted a class that holds an even number.

```java
class EvenNumberHolder {
    int value;

    EvenNumberHolder(int value) {
        if (value % 2 == 1) {
            throw new RuntimeException(value + " is not even");
        }

        this.value = value;
    }
}
```

You can always make the value `final` to prevent its value from being changed.

```java
class EvenNumberHolder {
    final int value;

    EvenNumberHolder(int value) {
        if (value % 2 == 1) {
            throw new RuntimeException(value + " is not even");
        }
        
        this.value = value;
    }
}
```

But if you actually wanted to change its value that isn't enough.

By making the field private you can know that other code has to call methods to access or
change the value. That gives you a clean place to "enforce" your invariants.

```java
class EvenNumberHolder {
    private int value;

    EvenNumberHolder(int value) {
        // The constructor explicitly rejects an odd value
        if (value % 2 == 1) {
            throw new RuntimeException(value + " is not even");
        }
        
        this.value = value;
    }

    // There is no way to get an odd value now - you can only
    // change it in steps of two.
    int value() {
        return this.value;
    }

    void addTwo() {
        this.value += 2;
    }

    void subtractTwo() {
        this.value -= 2;
    }
}
```