# Invoke Other Methods

Inside of an instance method you can invoke other instance methods
on the same class by writing their name and providing any needed arguments.

```java
class Elmo {
    int age;

    void sayHello() {
        System.out.println("Hi, I'm Elmo");
        System.out.print("I am ");
        System.out.print(age);
        System.out.println(" years old.");
    }

    void startTheShow(String showName) {
        sayHello();
        System.out.println("Welcome to " + showName);
    }
}

void main() {
    Elmo elmo = new Elmo();
    elmo.age = 3;

    elmo.startTheShow("Sesame Street");
}
```