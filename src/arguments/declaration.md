# Declaration

To declare a method take an argument, instead of putting `()` after the method name
you need to put a comma separated list of argument declarations.

Each argument declaration looks the same as a variable declaration and has both a type and a name.

```java
// This declares a single argument named "food" that
// has a type of "String".
void eat(String food) {
    System.out.println("I ate " + food);
}