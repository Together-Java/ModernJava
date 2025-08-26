# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1.

Create an interface named `TabbyCat`. It should 
extend the provided `Cat` interface and provide
a `lounge` method along with a default implementation of that
method.

```java
interface Cat {
    void purr();
}

// CODE HERE

class Garfield implements TabbyCat {
    @Override
    public void purr() {
        IO.println("mmmm lasagna");
    }
}

class Main {
    void main() {
        TabbyCat c = new Garfield();
        // Should come in via a default method.
        c.lounge();
    }
}
```

## Challenge 2.

Add a static field to the `Cat` interface
which indicates the healthy amount of lasagna for a cat to 
consume.[^zero]

```java
interface Cat {
    void purr();
}

class Main {
    void main() {
        // 0
        IO.println(Cat.HEALTHY_AMOUNT_OF_LASAGNA);
    }
}
```

## Challenge 3.

Put a static method on the `Cat` interface named `garfield"
which returns an instance of `TabbyCat`.

```java,no_run
public interface Cat {
    // CODE HERE
}
```

```java,no_run
public interface TabbyCat extends Cat {
    // CODE FROM PREVIOUS CHALLENGES
}
```

```java,no_run
class Garfield implements TabbyCat {
    @Override
    public void purr() {
        IO.println("mmmm lasagna");
    }
}
```

```java
public class Main {
    void main() {
        TabbyCat tc = Cat.garfield();
        tc.lounge();
    }
}
```

Note that this gives you a way to expose a `Garfield` instance
to other packages, even if the `Garfield` class itself
is `non-public`.[^unrunnable]

[^zero]: Zero, it can literally kill them.

[^unrunnable]: Apologies for the inconvenience. To make the point about
package visibility I had to make the code in browser non runnable
or editable. You should be able to manage at this point though.