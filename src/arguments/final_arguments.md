# Final Arguments

Just like normal variable declarations, arguments can be marked
`final`. This makes it so that they cannot be reassigned.

```java
void eat(final String food) {
    System.out.println("I ate " + food);
}

void main() {
    eat("Welsh Rarebit");
}
```

If you try to reassign a final argument, Java will not accept your program.


```java
void eat(final String food) {
    System.out.println("I ate " + food);
    // Will not work
    food = "toast";
    System.out.println(food);
}

void main() {
    eat("Welsh Rarebit");
}
```

This has the same use as regular final variables. If there are lots of lines
of code where a variable might be reassigned, it can be useful to not have
to read all that code to know that it does happen.[^opinion]

[^opinion]: Adding `final` to all arguments can make it harder to read the code, simply
because of visual noise.