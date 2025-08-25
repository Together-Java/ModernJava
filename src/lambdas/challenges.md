# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1.

Replace the `Sunflower` class with a lambda expression.

```java,editable
@FunctionalInterface
interface Flower {
    void bloom();
}

class Sunflower implements Flower {
    @Override
    public void bloom() {
        IO.println("bright yellow flower.");
    }
}

class Main {
    void bloomField(Flower flower) {
        for (int i = 0; i < 15; i++) {
            flower.bloom();
        }
    }

    void main() {
        Flower sunflower = new Sunflower();
        bloomField(sunflower);
    }
}
```

## Challenge 2.

Add a new method to the `Flower` interface above while
keeping the `@FunctionalInterface` annotation. What error does Java
give you?

What errors do you see if you remove the annotation but still have
lambdas in your code?

## Challenge 3.

Change the lambda expression you used for the `Flower` interface
to a method reference.

## Challenge 4.

One of these snippets of code will throw a `NullPointerException`. The other
will not. Which do you think will do which? Why do you think that is?

```java
@FunctionalInterface
interface Screamer {
    void scream();
}

class Lemon {
    void grab() {
        IO.println("UNACCEPTABLE!");
    }
}

class Main {
    void main() {
        Lemon lemon = null;
        Screamer s = lemon::grab;
    }
}
```

```java
@FunctionalInterface
interface Screamer {
    void scream();
}

class Lemon {
    void grab() {
        IO.println("UNACCEPTABLE!");
    }
}

class Main {
    void main() {
        Lemon lemon = null;
        Screamer s = () -> lemon.grab();
    }
}
```
## Challenge 4.

You should have done this challenge before:

> Make a method named `promptGeneric` which can prompt the user for information
> but, based on if what they typed is properly interpretable, can reprompt them.
> 
> As part of this make a `Parser` interface and at least two implementations: `IntParser`
> and `DoubleParser`.

If not, do so now. Then in either case replace the usages of `IntParser` and `DoubleParser`
with method references.

```java
// CODE HERE

class Main {
    // CODE HERE

    void main() {
        int x = promptGeneric(
            "Give me an x: ", new IntParser()
        );
        double y = promptGeneric(
            "Give me a floating point y: ", new DoubleParser()
        );
    }
}
```