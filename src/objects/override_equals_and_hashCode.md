# Override equals and hashCode

If you want to customize the `equals` method of an object the
general pattern for doing so is the following.

First, declare an equals method that matches the one that comes from `Object`.
Don't forget `@Override`.

```java,no_run
class Position {
    int x;
    int y;

    @Override
    public boolean equals(Object o) {

    }
}
```

This definition of equals accepts any `Object` as an argument. Therefore we first
need to make sure that the class of that `Object` is the same as the class you are
comparing it to.

```java,no_run
class Position {
    int x;
    int y;

    @Override
    public boolean equals(Object o) {
        if (o instanceof Position otherPosition) {

        }
        else {
            return false;
        }
    }
}
```

Then you compare the all the fields to make sure they are equal to each other as well.

```java,no_run
class Position {
    int x;
    int y;

    @Override
    public boolean equals(Object o) {
        if (o instanceof Position otherPosition) {
            return this.x == otherPosition.x && this.y == otherPosition.y;
        }
        else {
            return false;
        }
    }
}
```

How you do those comparisons depends on what is in the fields. For `int` and such you can use `==`. For fields
like `String` you need to use `.equals`.

```java,no_run
class Tree {
    String barkDescription;

    @Override
    public boolean equals(Object o) {
        if (o instanceof Tree otherTree) {
            // 
            return this.barkDescription.equals(otherTree.barkDescription);
        }
        else {
            return false;
        }
    }
}
```

If you anticipate, or don't take actions to prevent, a field potentially being `null`
then instead of `a.equals(b)` use `java.util.Objects.equals`. All it does special is handle
`null` without crashing.

```java,no_run
import java.util.Objects;

class Tree {
    String barkDescription;

    @Override
    public boolean equals(Object o) {
        if (o instanceof Tree otherTree) {
            return Objects.equals(otherTree.barkDescription);
        }
        else {
            return false;
        }
    }
}
```

Whenever you override `equals` you are supposed to override `hashCode` as well.
This is because - by default - every `Object` is going to give a `hashCode` consistent
with the default `equals` method. If you change how `equals` works, then you could
violate the contract of "if hashCode gives a different value, they definitely aren't equal."

Some parts of Java will rely on that, so its worth addressing.

If you define your `equals` method as above - essentially "they are equal if all their fields are equal" - then you can use `java.util.Objects.hash` to define your `hashCode`.[^exotic]

```java,no_run
import java.util.Objects;

class Position {
    int x;
    int y;

    @Override
    public boolean equals(Object o) {
        if (o instanceof Position otherPosition) {
            return this.x == otherPosition.x && this.y == otherPosition.y;
        }
        else {
            return false;
        }
    }

    @Override
    public int hashCode() {
        // Just give it all the fields you have.
        return Objects.hash(this.x, this.y);
    }
}
```

[^exotic]: If you defined a more exotic form of `equals` then how to properly make a `hashCode` is an exercise for you, the reader. If you give up then `return 1;` will always be "correct," if not ideal for the code
that uses `hashCode` as a quick "might be equal" check.
