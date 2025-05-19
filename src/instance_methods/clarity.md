# Clarity

Another reason you might want to use `this` is for code clarity.

It is a lot easier to know that a particular line refers to a field
or method on the same class if there is an explicit `this.` before
the reference.[^preference]

```java
class Elmo {
    int age;

    void sayHello() {
        IO.println("Hi, I'm Elmo");
        System.out.print("I am ");
        System.out.print(this.age);
        IO.println(" years old.");
    }
}

void main() {
    Elmo elmo = new Elmo();
    elmo.age = 3;

    elmo.sayHello();
}
```

[^preference]: This is very much a personal preference thing. I generally choose to write
`this.` whenever I am able to for this reason.