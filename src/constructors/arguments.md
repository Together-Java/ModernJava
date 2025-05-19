# Arguments


If you declare a constructor which takes arguments, you can use those arguments to give initial values
to fields.[^this]

You need to pass the arguments in the `()` in the `new` expression, just like any other method invocation.

```java
class Muppet {
    String name;

    Muppet(String name) {
        this.name = name;
    }
}

void main() {
    Muppet gonzo = new Muppet("Gonzo");

    // "Gonzo"
    IO.println(gonzo.name);
}
```

When you declare a constructor that takes arguments, the default constructor will no longer be available.

```java,does_not_compile
class Muppet {
    String name;

    Muppet(String name) {
        this.name = name;
    }
}

void main() {
    // Need to provide a name now
    Muppet gonzo = new Muppet();
}
```

[^this]: Using `this.` for disambiguation comes in handy here, since often the names of arguments
will be the same as the fields you want to populate with them.