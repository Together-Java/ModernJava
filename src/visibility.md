# Visibility

When code is all in one file, everything is "visible." This means that
if there is a method you are always allowed to call it.

```java
class Main {
    void canCallThis() {
        System.out.println("of course!")
    }

    void main() {
        canCallThis();
    }
}
```

And if there is a field you can read it, if there is a class you can make an instance of it, etc.

Once we split into multiple files, you are allowed to make things less visible.
