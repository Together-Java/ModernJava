# this

Within an instance method, you have access to a magic variable called `this`.

`this` is a variable that contains the current instance of the class.

You can use `this` to access fields or invoke any method.

```java
class Elmo {
    int age;

    void sayHello() {
        System.out.println("Hi, I'm Elmo");
        System.out.print("I am ");
        System.out.print(this.age);
        System.out.println(" years old.");
    }

    void startTheShow(String showName) {
        this.sayHello();
        System.out.println("Welcome to " + showName);
    }
}

void main() {
    Elmo elmo = new Elmo();
    elmo.age = 3;

    elmo.startTheShow("Sesame Street");
}
```