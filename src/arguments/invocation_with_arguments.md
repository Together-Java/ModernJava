# Invocation with Arguments

To invoke a method which takes arguments you need to, instead of writing
`()` after the method name, write `(` followed by a comma separated list
of literals or variable names ending with `)`.

```java
void eat(String food) {
    System.out.println("I ate " + food);
}

void happyBirthday(String to, int age) {
    System.out.println(
        "Happy " + age + "th birthday " + to + "!"
    );
}

void main() {
    // This calls the 'eat' method with the String "cake"
    // as an argument.
    eat("Cake");

    // You can also call methods using values stored in
    // variables.
    String veggie = "carrot";
    eat(veggie);

    // For more than one argument, you separate them with commas
    happyBirthday("Charlotte", 24);
}
```
