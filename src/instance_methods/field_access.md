# Field Access

Within an instance method's definition, you can access the values
of any fields declared in the class by just writing their name.

```java
class Elmo {
    int age;

    void sayHello() {
        IO.println("Hi, I'm Elmo");
        System.out.print("I am ");

        // You can use elmo's age by just writing "age"
        System.out.print(age);
        IO.println(" years old.");
    }
}

void main() {
    Elmo elmo = new Elmo();
    elmo.age = 3;

    elmo.sayHello();
}
```