# Multiple Instances

If you make multiple instances of a class with `new`
those classes will each have their own values for
fields.

```java
class Muppet {
    String name;
}

void main() {
    Muppet kermit = new Muppet();
    kermit.name = "Kermit The Frog";

    Muppet animal = new Muppet();
    animal.name = "animal";

    // kermit and animal are distinct muppets
    // and thus each have their own name.
    IO.println(kermit.name);
    IO.println(animal.name);
}
```

