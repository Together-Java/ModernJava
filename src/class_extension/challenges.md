# Challenges

Remember the rules for this are

- Try to use only the information given up to this point in this book.
- Try not to give up until you've given it a solid attempt

## Challenge 1.

Write a class called `Tree` which extends `ArrayList<Apple>`.

Add a `.grow()` method which adds two apples to itself
of arbitrary size.

```java,editable
record Apple(double size) {}

// CODE HERE

class Main {
    Tree tree = new Tree();
    tree.grow();
    tree.grow();

    // You should have inherited the toString
    // from ArrayList
    IO.println(tree);

    // As well as all the other methods
    tree.add(new Apple(100));
    IO.println(tree);

    for (var apple : tree) {
        IO.println(apple);
    }
}
```

## Challenge 2.

Rewrite your `Tree` class from above to instead extend `AbstractList<Apple>`.
You can find the documentation for `AbstractList` [here](https://docs.oracle.com/javase/8/docs/api/java/util/AbstractList.html).

## Challenge 3.

Make an `abstract` class called `Fish`. It should provide a method named
`swim` and a method named `howLongSwim` that returns how many times `swim`
was called.

This 
```java
// CODE HERE

class Dory extends Fish {
    void justKeepSwimming() {
        IO.println("Just keep swimming");
        this.swim();

        IO.println("Just keep swimming");
        this.swim();

        IO.println("Just keep swimming");
        this.swim();

        IO.println("swimming");
        this.swim();

        IO.println("swimming");
        this.swim();
    }
}

class Main {
    void main() {
        var dory = new Dory();
        dory.justKeepSwimming();

        IO.println(dory.howLongSwim());
    }
}
```

## Challenge 4.

Make the field you use to track how many times 
the fish swam `protected`. Also make the `swim`
method `protected` and `abstract`.

Write comments in your code such that the "contract"
between your class and classes implementing it
is that they must keep the `swam` field up to date.

This 
```java
// CODE HERE

class Dory extends Fish {


    @Override
    void swim() {
        IO.println("Just keep swimming");
        this.swam++;

        IO.println("Just keep swimming");
        this.swam++;

        IO.println("Just keep swimming");
        this.swam++;

        IO.println("swimming");
        this.swam++;

        IO.println("swimming");
        this.swam++;
    }
}

class Main {
    void main() {
        var dory = new Dory();
        dory.swim();

        IO.println(dory.howLongSwim());
    }
}
```

