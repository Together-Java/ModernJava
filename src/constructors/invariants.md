# Invariants


Just like any other method, constructors can throw exceptions.

You can use this fact to establish what we call an "invariant."

Say we have a `final` age field and that the constructor for a class throws an exception
if a given age is negative.

```java
class Muppet {
    final String name;
    final int age;

    Muppet(String name, int age) {
        this.name = name;

        if (age < 0) {
            throw new RuntimeException("Age cannot be negative");
        }
        this.age = age;
    }
}

void main() {
    Muppet bigBird = new Muppet("Big Bird", 6);
    System.out.println(
        bigBird.name + " is " + bigBird.age + " years old."
    );
}
```

In every other part of our program now we can rely on age being a non-negative number.
That is a property of instances that will not change.[^naming]

This is a lot more useful than it seems at first, stay tuned.

[^naming]: It will not change. It will not vary, it is in-variant. Get it?
