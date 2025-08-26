# Lambda Expressions

To make an implementation of a functional interface
you can use a "lambda expression."

If the method on the functional interface
takes no arguments, you write `() ->` followed
by the code to run when that method is called.

```java
@FunctionalInterface
interface Band {
    void playHitSong();
}

class Main {
    void main() {
        Band twrp = () -> {
            IO.println("Got no commitments today");
            IO.println("No work all play");
        }
    }
}
```

Just like with `switch` if there is only one line to run you may omit the `{}`s.

```java
@FunctionalInterface
interface Band {
    void playHitSong();
}

class Main {
    void main() {
        Band theProtomen = () -> IO.println("Light up the Night!");
    }
}
```