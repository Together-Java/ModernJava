# Messages

You can attach a message to an exception to give context to
whoever sees the program crash as to why that happened.

You do this by putting a `String` in the parentheses when throwing
your exception.

```java,panics
void crashesOnFive(int x) {
    if (x == 5) {
        throw new RuntimeException("5 is an evil number");
    }
}

void main() {
    crashesOnFive(1);
    System.out.println("Made it to step 1");

    crashesOnFive(5);
    System.out.println("Will not make it to step 2");
}
```