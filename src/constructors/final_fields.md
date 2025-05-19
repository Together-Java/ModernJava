# Final Fields


If you declare a field as `final`, its value cannot be changed after an instance of a class is made.

You are required to explicitly initialize `final` fields in the constructor.

```java
class Muppet {
    final String name;

    Muppet(String name) {
        // Without this, it wouldn't work
        this.name = name;
    }
}

void main() {
    Muppet gonzo = new Muppet("Gonzo");
    IO.println(gonzo.name);

    // Cannot update the .name field later
    // gonzo.name = "Gonzo, the great";
}
```

You can also do this directly when declaring the field.[^constant]

```java
class Muppet {
    // Aren't they all though?
    final boolean talented = true;
}

void main() {
    Muppet gonzo = new Muppet();
    IO.println(gonzo.talented);
}
```

[^constant]: This is primarily useful for "constant" values. You will need these, but
having constants attached to instances is a bit unique and won't happen that often.