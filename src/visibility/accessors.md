# Accessors

When a field is hidden that is usually because you want to control
how it might be changed.

To access the current value of a private field you need to go through a non-private method.
If a method just provides access to a field we call that an "accessor."

```java,no_run
class Dog {
    private String name;

    Dog(String name) {
        this.name = name;
    }

    // The name field is private, but
    // you can access it by calling the name method.
    String name() {
        return this.name;
    }
}
```
```java
class Main {
    void main() {
        var dog = new Dog("Daisy");

        // dog.name won't work because the name field is private
        // dog.name() will work because the name method is not
        System.out.println(dog.name());
    }
}
~class Dog {
~   private String name;
~
~   Dog(String name) {
~       this.name = name;
~   }
~
~    String name() {
~        return this.name;
~    }
~}
```

We would also consider things like the `length` method on `String`s to be "accessors."[^notthat]

```java
void main() {
    String s = "abc";
    System.out.println(
        // We can't see what fields underly this,
        // but we can access the length
        s.length()
    );
}
```

[^notthat]: Not that the categorization matters much, but socially we expect "accessor"-looking methods to only give you a value and not "do stuff" like
increment a number or mess with a file.