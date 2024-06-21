# Printing a Record

When printing out a record, the output will include
each of the components of the record.

```java
record Goblin(String name, int hp) {}
```
```java
~record Goblin(String name, int hp) {}
class Main {
    void main() {
        var goblin = new Goblin("Gobbo", 11);

        System.out.println(goblin);
    }
}
```
```
Goblin[name=Gobbo, hp=11]
```

This is more intelligable than what you would get by default from a regular class.[^possible]

```
Goblin@609db43b
```

[^possible]: It is possible to make a regular class print differently, but we'll get to that later.