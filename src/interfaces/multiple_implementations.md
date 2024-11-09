# Multiple Implementations

Interfaces can be implemented any number of times. This means
that code which accepts an interface can't truly know the specifics
of how methods will work.

This is a problem if you want maximum predictability but its
also the whole point of using an interface over a regular class.
You can write code that depends on a few key methods being defined
and be flexible to different ways of defining those methods.

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

class Cat implements Dog {
    @Override
    public void bark() {
        System.out.println("Meow");
    }

    @Override
    public String fetch(String ball) {
        return "no.";
    }
}

void barkAndFetch(Dog dog) {
    dog.bark();
    System.out.println(dog.fetch("Ball"));
}

void main() {
    barkAndFetch(new Mutt());
    barkAndFetch(new Cat());
}
```
