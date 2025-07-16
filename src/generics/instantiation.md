# Instantiation

When you make an instance of a class that takes generic parameters
you are expected to provide the actual concrete types you want to be used
in place of any type variables.

You do this by writing the name of the types inside a `<>` alongside the call to `new`.

```java
class Box<T> {
    T data;
}

void main() {
    var boxOfString = new Box<String>();

    boxOfString.data = "abc";

    String s = boxOfString.data;

    IO.println(s);
}
```