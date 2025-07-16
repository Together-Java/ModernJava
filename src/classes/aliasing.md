# Aliasing


When two variables point to the same instance of a class, those variables will be
aliases for the same data.

This means that, just like arrays, if you change the value of a field on one that change
will be visible on the other.

```java
class Muppet {
    String name;
}

void main() {
    Muppet kermit = new Muppet();
    Muppet darkKermit = kermit;

    kermit.name = "Kermit The Frog";

    // Kermit The Frog
    IO.println(kermit.name);
    // Kermit The Frog
    IO.println(darkKermit.name);
}
```