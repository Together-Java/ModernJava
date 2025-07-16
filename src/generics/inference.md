# Inference

Sometimes Java has enough information to know
what the right values for type variables would be without you
specifying them.

In these cases you can rely on the compiler to infer them by writing `<>` with no type variables
in between.

```java
class Box<T> {
    T data;
}

void main() {
    // It is being assigned to a Box<String> on the left
    // so Java can figure out what should be on the right.
    Box<String> boxOfString = new Box<>();

    boxOfString.data = "abc";

    String s = boxOfString.data;

    IO.println(s);
}
```

This inference does not work on the left-hand side of an `=`.

```java,does_not_compile
class Box<T> {
    T data;
}

void main() {
    // Use var if you want inference for local variables.
    Box<> boxOfString = new Box<String>();

    boxOfString.data = "abc";

    String s = boxOfString.data;

    IO.println(s);
}
```