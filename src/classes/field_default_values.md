# Field Default Values

Before a field in a class is given a value it will have the same default value as it would
if you made an array of the field's type.

That is: `0` for `int`, `0.0` for `double`, `false` for `boolean`, and `null` for most all else.

```java
class Muppet {
    int age;
    double salary;
    boolean talented;
    String name;
}

void main() {
    Muppet kermit = new Muppet();

    // 0
    System.out.println(kermit.age);
    // 0.0
    System.out.println(kermit.salary);
    // false
    System.out.println(kermit.talented);
    // null
    System.out.println(kermit.name);
}
```