# A Second file

In files that are not `Main.java` you can put other code, but
only in the form of a class.

By this I mean, while in `Main.java` you are able to write something like this.

```java
void sayHello() {
    System.out.println("Hello");
}

void main() {
    sayHello();
}
```

In a file named `Ball.java` you need to put all code inside a `Ball` class.

```java
class Ball {
    // You can write constructors, methods, fields, etc.
    final int size;

    Ball(int size) {
        this.size = size;
    }
}

// But you cannot have any "top level" methods or things outside
// of the Ball class
```

Then from `Main.java` you can make an instance of `Ball`

```java
void main() {
    var ball = new Ball(10);
    System.out.println("The ball is " + ball.size + "cm across");
}
```

When you run `java src/Main.java` it will find `src/Ball.java` and use the code in there.