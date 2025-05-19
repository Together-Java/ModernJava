# Annotations

Comments are useful when reading code. Since they can contain any text,
you can use them to clarify your intent, make note of issues to address
later, etc.

```java
class Main {
    // TODO: Make this actually add one
    int addOne(int x) {
        return x + 2;
    }

    // The return value here will always be non-negative
    int absoluteValue(int x) {
        if (x < 0) {
            return -x;
        }
        else {
            return x;
        }
    }

    int main() {
        IO.println(addOne(5));
        IO.println(absoluteValue(-25));
    }
}
```

The problem with comments is that they are just text. It would be difficult to write a program
that acts upon or uses information in a comment.

Annotations, which you can think of as "structured comments", are useful for this purpose.

```java
class Main {
    @TODO("Make this actually add one")
    int addOne(int x) {
        return x + 2;
    }

    @NonNegative int absoluteValue(int x) {
        if (x < 0) {
            return -x;
        }
        else {
            return x;
        }
    }

    int main() {
        IO.println(addOne(5));
        IO.println(absoluteValue(-25));
    }
}
```