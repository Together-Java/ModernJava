# Implementation

All interfaces do[^fornow] is hold method declarations.

If you want to have a class which "implements"
the interface you can do so by writing `implements` followed by the interface
name.

```java
interface Dog {
    void bark();

    String fetch(String ball);
}

class Mutt implements Dog {

}
```

Then you all you need to do is declare methods which match up with the methods defined in the interface.
Keep in mind that while you didn't write `public` in the interface, you need to write `public`
when implementing a method from an interface.[^all]

```java
interface Dog {
    void bark();

    String fetch(String ball);
}

class Mutt implements Dog {
    public void bark() {
        System.out.println("Bark");
    }

    public String fetch(String ball) {
        return ball + " (with drool)";
    }
}
```

[^fornow]: For now*

[^all]: All methods that come from an interface must be `public`.