# Check for Equality

To check if the components of a record match with another, you can use the `equals`
method.

```java
record Elf(boolean pretentious) {}
```
```java
~record Elf(boolean pretentious) {}
class Main {
    void main() {
        var elfOne = new Elf(true);
        var elfTwo = new Elf(true);
        
        System.out.println(elfOne.equals(elfTwo));
    }
}
```

This is similar to how you check whether `String`s are equal.