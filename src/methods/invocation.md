# Invocation

Once you've declared a method you can run the code inside of it by writing the
name of the method followed by `()` in a statement.

```java
void doThing() {
    System.out.println("Hello from inside a method!");
}

void main() {
    doThing();
}
```

Running the code in a method can be called a few things. "Running a method", "Calling a method", or "Invoking a method."[^wizard]

You can call a method multiple times. If you do, then the code inside of it will be run multiple times.

```java
void doThing() {
    System.out.println("Hello from inside a method!");
}

void main() {
    doThing();
    doThing();
}
```


[^wizard]: I like that last one because "invoking" makes me sound like a Wizard.