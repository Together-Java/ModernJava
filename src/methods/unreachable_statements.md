# Unreachable Statements

If Java can figure out that some line of code is unreachable because it will always come after a
`return`, then it will not run your code.

```java
void doThing() {
    System.out.println("A");
    return;
    // unreachable statement
    System.out.println("B");
}

void main() {
    doThing();
}
```

Java is easy to trick though.[^trick]

```java
void doThing() {
    System.out.println("A");
    if (true) {
        return;
    }
    System.out.println("B");
}

void main() {
    doThing();
}
```

[^trick]: This _will_ always return before the `println`, but Java chooses to not figure that out. It can't be smart enough to see through every `if`, so it doesn't try for any of them.
