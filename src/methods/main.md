# main

The `main` method works the same as any other method. Java just treats it special by choosing to
call it in order to start your programs.

```java
void main() {
    IO.println("Java will start here");
}
```

This means you can do anything in your `main` method you can do in any other method, including returning early.

```java
void main() {
    int x = 5;

    if (x == 5) {
        return;
    }

    IO.println("WONT RUN");
}
```
