# The Anonymous Main Class

Surprise! Everything in Java is actually in a class.

This includes the code in `Main.java`.

```java
void main() {
    System.out.println("What, really?");
}
```

Everything we've written so far has been in what is called "the anonymous main class."
We call it anonymous because we never gave it a name. 

We call it the main class because you are only allowed to skip naming a class if it is the one you use to start your program, and that requires a `void main()` method.

If you take any code we've produced up until now and wrap it with `class Main {}` it will continue to work as-is.

```java
class Main {
    void main() {
        System.out.println("yep.");
    }
}
```

What Java will do is run `new Main().main();` to start your program.


