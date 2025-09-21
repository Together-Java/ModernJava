# Method References

Often it will make sense to separate the code
for a lambda into its own method.

```java
interface Drummer {
    void drum();
}

class Main {
    void doDrum() {
        IO.println("ratatatatat");
        IO.println("crash!");
        IO.println("crash!");
        IO.println("ratatatatat");
    }

    void main() {
        Drummer drummer = () -> doDrum();
        drummer.drum();
    }
}
```

When you have a method that matches[^exactly] the method required by a functional interface
you can use a "method reference."

For instance methods this will look like `instance::methodName`. So inside a method
this can be `this::methodName` but you can also have a `variableName::methodName`

```java
interface Drummer {
    void drum();
}

interface Musician {
    void play();
}

class Main {
    void doDrum() {
        IO.println("ratatatatat");
        IO.println("crash!");
        IO.println("crash!");
        IO.println("ratatatatat");
    }

    void main() {
        Drummer drummer = this::doDrum;
        drummer.drum();

        Musician musician = drummer::drum;
        musician.play();
    }
}
```

For static methods it will look like `ClassName::doDrum`.

```java
interface Drummer {
    void drum();
}

class Main {
    static void doDrum() {
        IO.println("ratatatatat");
        IO.println("crash!");
        IO.println("crash!");
        IO.println("ratatatatat");
    }

    void main() {
        Drummer drummer = Drummer::doDrum;
        drummer.drum();
    }
}
```

And finally for instance methods where the the functional interface's method takes the instance
explicitly as an argument it will look the same as a static method reference.

```java
interface StringTransformer {
    String transform(String s);
}

class Main {
    void main() {
        // Instance method, but looks like a reference
        // to a static method that just so happens to
        // take a String as a first argument
        StringTransformer t = String::toUpperCase;
        IO.println(t.transform("ratatatatat"));
    }
}
```


[^exactly]: It doesn't have to match _exactly_ but describing the exact matching mechanism isn't that important. Play it by ear.