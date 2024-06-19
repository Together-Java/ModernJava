# Unchecked Exceptions

When a part of your code might throw a "unchecked" exception, other
parts of your code do not need to account for that possibility.

```java
int divide(int x, int y) {
    if (y == 0) {
        // Will work because you are not forced to handle
        // an unchecked exception
        throw new RuntimeException();
    }

    return x / y;
}
~void main() {
~    
~}
```

We call them unchecked because you don't need to check for them.