# Field Updates

You can also update the value of any field from within an instance
method the same as if it were a local variable.

```java
class Elmo {
    int age;

    void sayHello() {
        System.out.println("Hi, I'm Elmo");
        System.out.print("I am ");
        System.out.print(age);
        System.out.println(" years old.");
    }

    void haveBirthday() {
        age = age + 1;
    }
}

void main() {
    Elmo elmo = new Elmo();
    elmo.age = 3;

    elmo.sayHello();
    elmo.haveBirthday();
    elmo.sayHello();
}
```