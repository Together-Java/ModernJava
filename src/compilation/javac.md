# javac

The compiler used for compiling Java code is called `javac`.
This stands for "**Java** **C**ompiler".

Its job is to take a list of `.java` files and compile
them into `.class` files.

For a single file Java program you can do this by running
a command similar to the following.

```bash
javac -d output src/Main.java
```

The `-d output` in that example means "put the compiled class files in a folder called `output`."
After running the command above you would expect to see something like the following.

```text
src/
    Main.java
output/
    Main.class
```

You aren't guarenteed that any given `.java` file will produce only one `.class` file
as output. Inner classes are one reason for this, but there are others.

```text
src/
    Main.java
output/
    Main.class
    Main$1.class
    Main$Thing.class
```

To compile multiple files you need to list every `.java` file
one after another.

```