# Field Initialization

You can set an initial value for a field in a few ways.

One is to access to assign the field directly on the instance created.

```java
class Muppet {
    String name;
}

void main() {
    Muppet kermit = new Muppet();
    kermit.name = "Kermit The Frog";
}
```

Another is to set a default value directly in the field declaration. This makes the most sense
if its a value that most instances will share.

```java
class Muppet {
    // Most are!
    boolean talented = true;
}

void main() {
    Muppet kermit = new Muppet();
}
```
