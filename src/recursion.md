# Recursion

In a method you can call another method.

```java
void doOtherThing() {
    System.out.println("B");
}

void doThing() {
    System.out.println("A");
}

void main() {
    doThing();
}
```

This is at the foundation of most code so should, at this point,
be a given.

What might not be obvious is that you can call the method currently running.

```java
void countDown(int value) {
    System.out.println(value);
    if (value > 0) {
        countDown(value - 1);
    }
}

void main() {
    countDown(10);
}
```

This is what we call "recursion."