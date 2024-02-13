# Disambiguation

One reason you might need to use `this` is if the name
of an argument to a method is the same as the name of a field.

```java
class Elmo {
    int age;

    boolean isOlderThan(int age) {
        return this.age > age;
    }
}

void main() {
    Elmo elmo = new Elmo();
    elmo.age = 3;

    // true
    System.out.println(elmo.isOlderThan(2));
}
```

If you didn't do this, it would be ambiguous whether you were referring to the field
or the argument. This removes the ambiguity.[^javanotconfused]

[^javanotconfused]: Really it isn't ambiguous for Java. It will just think you are referring to the argument.
It is ambiguous from the perspective of a human being reading the code though.