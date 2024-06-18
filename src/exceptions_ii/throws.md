# throws

One way to handle a checked exception is to add a `throws` to the end
of your method declaration.

```java
int divide(int x, int y) throws Exception {
    if (y == 0) {
        throw new Exception();
    }

    return x / y;
}

~void main() {
~    
~}
```

This will make it so that calling code needs to check for the possibility of that 
exception being thrown.

```java,does_not_compile
int divide(int x, int y) throws Exception {
    if (y == 0) {
        throw new Exception();
    }

    return x / y;
}

void doStuff() {
    divide(1, 0);
}

~void main() {
~    
~}
```

You can also declare unchecked exceptions using `throws` but you are never required to.[^doc]
 
```java
int divide(int x, int y) throws RuntimeException {
    if (y == 0) {
        throw new RuntimeException();
    }

    return x / y;
}

~void main() {
~    
~}
```

[^doc]: This is one of many things that you might choose to do for the benefit of a human reader that isn't strictly needed for correct Java.