# Invoke Other Methods

Inside of an instance method you can invoke other instance methods
on the same class by writing their name and providing any needed arguments.

```java
class Elmo {
    int age;

    void sayHello() {
        IO.println("Hi, I'm Elmo");
        IO.print("I am ");
        IO.print(age);
        IO.println(" years old.");
    }

    void startTheShow(String showName) {
        sayHello();
        IO.println("Welcome to " + showName);
    }
}

void main() {
    Elmo elmo = new Elmo();
    elmo.age = 3;

    elmo.startTheShow("Sesame Street");
}
```