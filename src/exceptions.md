# Exceptions

When you do something that Java doesn't know how to handle, like
dividing a number by zero, your program will fail.

The way that this happens is that an "exception" is thrown.

Say that in "normal conditions" code will proceed top to bottom, line by line.
In "exceptional conditions" code will no longer be able to proceed.

```java,panics
void main() {
    int x = 5 / 0;
    IO.println("Won't get here, an exception will occur");
}
```


