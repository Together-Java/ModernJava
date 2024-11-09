# Subtypes

Just as everything is a subtype of `Object`, anything which
implements an interface is a subtype of that interface.

For the following code this means that any field or variable
which holds a `Dog` can be assigned to an instance of `Mutt`.

```java
interface Dog {
    void bark();

    String fetch(String ball);
}

class Mutt implements Dog {
    @Override
    public void bark() {
        System.out.println("Bark");
    }

    @Override
    public String fetch(String ball) {
        return ball + " (with drool)";
    }
}

void main() {
    Dog dog = new Mutt();
}
```

Through a `Dog` variable you will be able to call any methods defined on the interface.
These will use the actual underlying implementation - in this case from `Mutt`.

```java
interface Dog {
    void bark();

    String fetch(String ball);
}

class Mutt implements Dog {
    @Override
    public void bark() {
        System.out.println("Bark");
    }

    @Override
    public String fetch(String ball) {
        return ball + " (with drool)";
    }
}

void main() {
    Dog dog = new Mutt();

    dog.bark();

    System.out.println(dog.fetch("Ball"));
}
```

