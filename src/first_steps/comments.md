# Comments

At various points, I am going to leave "comments" in the code. Comments are parts of the code that
are solely there for a human to be able to read as an explanation and can be written in regular
words.

## Single-line Comments

```java
void main() {
    // This prints hello world!
    IO.println("Hello, World!");
}
```

The rules for this are that if you see a `//`, everything after that in the same line
is ignored.

If you put `//` in front of something that is "code" and not an English explanation we colloquially call that "commenting out" the line.

```java
void main() {
    IO.println("Hello, World!");
    // The line that prints out goodbye is "commented out"
    // IO.println("Goodbye!");
}
```

You might want to do that at various points where you want to see what happens if you "turn off" parts of
the code.

## Multi-line comments

If you put `/*` in the code then everything up until the next `*/` will be treated as a comment. The distinction
here is that this style of comment can span multiple lines.

```java
void main() {
    /*
        I have eaten
        the plums
        that were in
        the icebox
        and which
        you were probably
        saving
        for breakfast
        Forgive me
        they were delicious
        so sweet
        and so cold
    */
    IO.println("Hello, World!");
}
```

So that's a mechanism you will see me use and you can use yourself however you see fit.
