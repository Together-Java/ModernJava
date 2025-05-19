# Reassignment

Inside of a method, arguments work the same as normal variable declarations.
This means that their value can be reassigned
within the method body;

```java
void eat(String food) {
    IO.println("I ate " + food);
    food = "nothing";
    IO.println("Now I have " + food);
}

void main() {
    eat("Cake");
}
```

Reassigning an argument's value will not affect the value assigned to
any variables passed to the method by the caller.

```java
void eat(String food) {
    IO.println("I ate " + food);
    food = "nothing";
    IO.println("Now I have " + food);
}

void main() {
    String fruit = "apple";
    eat(fruit);
    IO.println(
        "But in the caller I still have an " + fruit
    );
}
```
