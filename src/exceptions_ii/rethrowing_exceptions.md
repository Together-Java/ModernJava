# Rethrowing Exceptions

When you catch an exception you have the option of again throwing an exception.

This is useful if you want to have behavior that occurs when something goes wrong but still
ultimately throw an exception for the rest of the code to deal with.[^examples]

```java,no_run
void dream() throws Exception {
    throw new Exception("Oh no");
}

void sleep() throws Exception {
    try {
        dream();
    }
    catch (Exception e) {
        IO.println("Something went wrong while dreaming");
        throw e;
    }
}
```

It is also an opportunity to "wrap" checked exceptions into unchecked ones.

```java
void dream() throws Exception {
    throw new Exception("Oh no");
}

void sleep() {
    try {
        dream();
    }
    catch (Exception e) {
        throw new RuntimeException(e);
    }
}

void main() {
    sleep();
}
```

Which seems crazy, but remember that "the point" of a checked exception is to have the calling code make a choice about how to handle an error condition. If you are okay with just crashing, throwing an unchecked exception is a perfectly valid choice.

[^examples]: These examples are all silly, I know. Once we get to files the mechanics will become useful.