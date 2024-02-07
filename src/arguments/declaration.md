# Declaration

To declare a method which takes arguments, instead of putting `()` after the method name
you need to put a comma separated list of argument declarations.

Each argument declaration looks the same as a variable declaration and has both a type and a name.

```java,no_run
// This declares a single argument named "food" that
// has a type of "String".
void eat(String food) {
    System.out.println("I ate " + food);
}

// This declares two arguments
// "to", which is a String and
// "age", which is an int.
void happyBirthday(String to, int age) {
    System.out.println(
        "Happy " + age + "th birthday " + to + "!"
    );
}
```
