# main

The `main` method can be declared to throw any kind of checked exception.

It is assumed that if an exception makes it all the way there that the way to handle it is crash
the program.

```java,panics
void main() throws Exception {
    throw new Exception("crash");
}
```