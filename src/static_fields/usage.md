# Usage

To use a static field within the class it is declared you just need to write the name of the field.

```java
class Main {
    static int count = 0;

    void main() {
        IO.println(count);
    }
}
```

To use it from another class or to disambiguate it from a regular field with the same
name, you should prefix it with the name of the class it is declared in plus a `.`.


```java
class Main {
    static int count = 0;

    void main() {
        IO.println(Main.count);
    }
}
```