# Interface Extension

Interfaces can extend other interfaces. 

```java,no_run
interface Dog {
    void bark();
}

record Color(int r, int g, int b) {}

interface ColoredDog extends Dog {
    Color color();
}
```

This means a few things. First an implementing class
must specify all the methods from both.

```java,no_run
class Clifford implements ColoredDog {
    @Override
    public void bark() { // Must define the methods on Dog
        IO.println("BARK BARK");
    }

    @Override
    public Color color() { // As well as on ColoredDog
        return new Color(255, 0, 0); // Red
    }
}
```

Second, interface extension "establishes a subtyping relationship."
Something which implements a sub-interface can be used in a
place expecting the super-interface.

```java,no_run
void main() {
    Clifford clifford = new Clifford();
    clifford.bark();
    IO.println(clifford.color());

    IO.println("-------");
    // clifford is a "ColoredDog"
    ColoredDog coloredDog = clifford;
    // So all the methods on ColoredDog are available
    coloredDog.bark();
    IO.println(coloredDog.color());


    IO.println("-------");
    // all "ColoredDog"s are also "Dog"s
    Dog dog = coloredDog;
    // So you can use the methods from Dog, but not any
    // from ColoredDog
    dog.bark();
    // IO.println(dog.color()); - Won't work

    IO.println("-------");
    // and all "Dog"s are "Object"s
    Object o = dog;
    // So you only have access to the methods from Object unless you
    // use instanceof to recover the actual type of the object
    if (o instanceof ColoredDog c) {
        c.bark();
        IO.println(c.color());
    }
}
```
