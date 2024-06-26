# File names

When you make a file called `Ball.java` you should expect to find a class named `Ball` inside of it.

This is a general rule. When you split code into multiple files each file should be
a class and the name of the class should match the name of the file.

So if I want to write a `Position` class

```java
class Position {
    int x;
    int y;
}
```

That should go in its own file named `Position.java`.