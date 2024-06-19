# The anonymous main class

If you remember when I first showed you classes, you were working inside
the anonymous main class.

```java,no_run
class Muppet {
    String name;
}

void main() {
    Muppet kermit = new Muppet();
    kermit.name = "Kermit The Frog";
}
```

This means that all the classes you made were, in reality, inner classes.

```java,no_run
class Main {
    class Muppet {
        String name;
    }

    void main() {
        Muppet kermit = new Muppet();
        kermit.name = "Kermit The Frog";
    }
}
```

Which is how they would have access to any "global fields" you declared
and why static factory methods would not work.

```java,no_run,does_not_compile
class Main {
    class Muppet {
        String name;

        static Muppet fromName(String name) {
            // You cannot make an instance of an inner class
            // from within a static method, so this wouldn't work.
            Muppet muppet = new Muppet();
            muppet.name = name;
            return muppet;
        }
    }

    void main() {
        Muppet kermit = Muppet.fromName("Kermit The Frog");
    }
}
```