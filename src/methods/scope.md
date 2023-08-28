# Scope

Methods can contain any code, including variable declarations.

```java
void sayMathStuff() {
    int x = 1;
    int y = 2;
    System.out.println("x is " + x);
    System.out.println("y is " + y);
    System.out.println("x + y is " + (x + y));
}

void main() {
    sayMathStuff();
}
```

When a method declares a variable inside of its body, that declaration is "scoped" to that method.
Other code cannot see that variable.

```java
void sayMathStuff() {
    int x = 1;
    int y = 2;
    System.out.println("x is " + x);
    System.out.println("y is " + y);
    System.out.println("x + y is " + (x + y));
}

void main() {
    sayMathStuff();
    // Error, x doesn't exist here
    System.out.println(x);
}
```

This is why we have called variables "local variables." They are local to the "scope" of the
method they are declared in.
