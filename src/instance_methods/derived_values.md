# Derived Values

A common use for methods is to provide a value that is derived from
the values of other fields.

```java
class Elmo {
    int age;

    int nextAge() {
        return age + 1;
    }
}

void main() {
    Elmo elmo = new Elmo();
    elmo.age = 3;

    System.out.println("Elmo is " + elmo.age + " right now,");
    System.out.println("but next year Elmo will be " + elmo.nextAge());
}
```

Which is useful for situations like where you store someones first and last name