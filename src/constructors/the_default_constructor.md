# The Default Constructor

If you don't declare a constructor, it will be the same as declaring an "empty"
constructor. All fields will be initialized to their default values.

```java
class Muppet {
    String name;
    boolean talented;

    Muppet() {
    }
}

void main() {
    Muppet gonzo = new Muppet();

    // null
    IO.println(gonzo.name);
    // false
    IO.println(gonzo.talented);
}
```